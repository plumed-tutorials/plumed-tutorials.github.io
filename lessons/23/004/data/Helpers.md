# The CUDAHELPERS library

This helper library contains an implementation of the reduction algorithm 
using the [cub](https://nvidia.github.io/cccl/cub/) building blocks and the
 interface between the [thrust](https://nvidia.github.io/cccl/thrust/) vectors
 and the PLMD::Vector and PLMD::Tensor classes.

The helper library is a header-only library `cudaHelpers.cuh`.

See the [coordination implementation](Implementation.md) for an example of how to use the code described here.

## The reduction interface

The original version used a plain CUDA C++ reduction and was implemented following 
[this guide](https://developer.download.nvidia.com/assets/cuda/files/reduction.pdf).
I recommend trying to implement the reduction algorithm by hand before using cub,
to have a better picture of the concept and of the algorithm.

The call to the reduction kernels is mediated by templated interface functions.

```c++
template <unsigned DATAPERTHREAD, typename T>
void doReduction1D(
  T *inputArray,         //the GPU-pointer to the input data
  T *outputArray,        //the GPU-pointer to the output data
  const size_t len,      //the lenght of the input array
  const unsigned blocks, //the number of block to use
  const size_t nthreads, //the number of thread to use
  cudaStream_t stream    //the stream to use for concurrent operations
  )
```
```c++
template <unsigned DATAPERTHREAD, typename T>
void doReductionND(
  T *inputArray,         //the GPU-pointer to the input data
  T *outputArray,        //the GPU-pointer to the output data
  const size_t len,      //the lenght of the input array
  const dim3 blocks,     //the number of block to use (in format blocks, nd)
  const size_t nthreads, //the number of thread to use
  cudaStream_t stream    //the stream to use for concurrent operations
  )
```

These interfaces ask for a `T*` instead of a `thrust::device_vector<T>` 
for flexibility, remember to pass a device pointer, not a CPU pointer.

The `dim3` type is a triplet of integers defined in the cuda headers.
Here we declare it as a couple of numbers to spawn a 2D (in this case) grid of
kernels: the first number is the number of groups that will be used, in case 
there are more data than threads available this will be >1 and then the reduction
 will need to be applied on the result of the calculation.
The second number is the number of data arrays that we are processing together, 
for example, the virial is saved in a format of 9  blocks of consecutive numbers
 and in that case we will use `dim3{N,9}`.
In the case of a single array, the 1D version will enqueue a specialized 1D kernel 

These functions should be called in a driver that loops on them, for example:
```C++
template<int datperthread,typename T>
T drive(const int threads, thrust::host_vector<T> &data){
  const int len = data.size();
  //this loads the data on the GPU, I'm using an host_vector to simplify the syntax
  thrust::device_vector<T> gpudata=data;
  thrust::device_vector<T> returnData;
  auto N= len;
  while (N>1){
    // scale the number of threads depending on N, each thread will process
    // datperthread numbers before doing the collective reduction
    size_t runningThreads = threadsPerBlock(ceil(double(N) / dataperthread));
    // decide the number of groups to be used
    unsigned groups = ceil(double(N) / (runningThreads * dataperthread));
    returnData.resize(groups);
    doReduction1D<dataperthread>(
        thrust::raw_pointer_cast(gpudata.data()),
        thrust::raw_pointer_cast(returnData.data()), N, groups,
        runningThreads);
    if (nGroups > 1) {
      //swap the data to use the output as input of the next iteration
      gpudata.swap(returnData);
    }
  }
  //the data can be transferred this easy (with thrust)!
  T toret = returnData[0];
  return toret;
}

```
this driver 'throws away' the input data (on the GPU) at each iteration, using
the containing array as a container for the output of the next iteration, 
and using the output.


These interfaces can be called without the stream and the kernels will be serially executed.


## The reduction kernel

Here I am showing only the ND kernel, the 1D one is like this one, but with 
the `blockIdx.y * something` parts removed.

The reduction kernels are assembled with _cub_ building blocks

```c++
template <typename T, int BLOCK_THREADS, int ITEMS_PER_THREAD>
__global__ void
reductionNDKernel(int num_valid,        // number if elements to be reduced
                  calculateFloat *d_in, // Tile of input
                  calculateFloat *d_out // Tile aggregate
) {
  // Specialize BlockReduce type for our thread block
  using BlockReduceT = cub::BlockReduce<calculateFloat, BLOCK_THREADS>;
  // Shared memory across all the threads of THIS block
  __shared__ typename BlockReduceT::TempStorage temp_storage;
  const int data_id = threadIdx.x + blockIdx.x * blockDim.x;
  //the explicit ITEMS_PER_THREAD here is used for the template parameter deduction of cub::LoadDirectBlocked
  T data[ITEMS_PER_THREAD];
  //this function loads the num_valid elements of data into the data array
  //is more or less equivalent to an unrolled version of
  // for(auto i=0;i<ITEMS_PER_THREAD;++i){
  //   if (data_id+i < num_valid){
  //     data[i] = d_in[ blockIdx.y * num_valid+ data_id+i];
  //   } else {
  //     data[i]= T(0)
  //   }
  // }
  cub::LoadDirectBlocked(data_id, d_in + blockIdx.y * num_valid, data,
                         num_valid, T(0.0));
  //Each thread sums its data elements into temp_storage[threadIdx.x]
  //then proceed with the reduction on the shared memory (see the link before)
  calculateFloat aggregate = BlockReduceT(temp_storage).Sum(data);
  if (threadIdx.x == 0) {
    d_out[blockIdx.x + blockIdx.y * gridDim.x] = aggregate;
  }
}
```

The last two arguments of `cub::LoadDirectBlocked` make sure that we are calling
the overload that assigns 0 to data when we are trying to load out-of-bound elements. 
We need to use this because we usually do not have powers of 2 data elements to be reduced.

## The PLMD-thrust interface

_cudaHelpers.cuh_ contains an interface between `thrust`, `cuda` and the `Tensor`
and `Vector` class from `PLMD`.

Both the `DataFrom` and the `DataTo` have an async and a non-async overload,
depending on the presence of the `stream` variable on call.

```c++
template <typename T, typename Y>
inline void plmdDataToGPU(thrust::device_vector<T> &dvmem, Y &data,
                          cudaStream_t stream);
```

```c++
template <typename T, typename Y>
inline void plmdDataFromGPU(thrust::device_vector<T> &dvmem, Y &data,
                            cudaStream_t stream);
```

`PLMD` data types store double precision numbers, when these functions are called
with a `thrust::device_vector<float>` as argument, they create a temporary 
`std::vector` to convert and pass the data from/to the GPU.
In this case, the `DataFrom` function ignores the stream parameter to avoid
starting to convert an array that has not been completely transferred from the GPU
