# Implementation

Small disclaimer: the code I am presenting here is a simplified version of the
actual code that is available as an example implementation in this
[repository](https://github.com/Iximiel/cudaOnPlumed).
The actual implementation has type templates and supports pbcs.
These particulars are not useful in understanding the basis for a plumed
implementation of a  simple CV.

If this is not the first time you read this I have updated the code on the
repository to use the NVIDIA's [CCCL](https://github.com/NVIDIA/cccl) API.
You may find some changes in the code.
The code changes are not radical and I may have missed something while updating
the page, always refer to the repository for an up-to-date code.

## The switching function
In this case the coordination is calculated with
$\frac{1}{2} \sum_{i\lt{}nat}^{i} \sum_{j\lt{}nat,j\neq i}^{j} f(d_{ij})$, 
where $d_{ij}$ is the distances between atom $i$ and $j$, and $f(x)$ is a
function that usually has the form

$$
f(x)=\begin{cases}
1       & x \leq d_0\\
s(x)    & d_0<x\leq d_{max}\\
0       & x > d_{max} 
\end{cases}
$$

and $s(x)$ is a switching function that links smoothly 1 to 0 between $d_0$ and $d_{max}$

In this case, I used the RATIONAL function like in the default Plumed implementation:
$s(r)=\frac{ 1 - \left(\frac{ r - d_0 }{ r_0 }\right)^{n} }{ 1 - \left(\frac{ r - d_0 }{ r_0 }\right)^{m} }$.

But in this case, for simplicity, the implementation that I am showing will not
use the parameter
$d_0$, so $s(r)=\frac{ 1 - \left(\frac{ r }{ r_0 }\right)^{n} }{ 1 - \left(\frac{ r }{ r_0 }\right)^{m} }$.

Like in standard plumed implementation, the switching has a stretch parameter:
if $s(d_{max}) = shift $ and $stretch=\frac{1}{s(0)-s(d_{max})}$, $s(x)$ 
becomes $s^s(x)=s(x)*stretch+shift$

## The kernel and the  \_\_device\_\_ functions
### The coord kernel

In the following code snippets, the comments help read the flow of the code.
Here the code is presented in a simplified way, without templates for type and
without the pbc calculations.

The simplest kernel for calculating the coordination in a group of atoms is:
```c++
//global kernels can be called by the host, but are compiled for the GPU
__global__ void getSelfCoord(
    const unsigned nat,
    //you can pass structs directly to kernels
    const rationalSwitchParameters switchingParameters,
    const float *coordinates,
    const unsigned *trueIndexes, float *ncoordOut,
    float *devOut, float *virialOut) {
        
  // i is the index of the atoms that will be confronted with all the others
  const unsigned i = threadIdx.x + blockIdx.x * blockDim.x;

  // blocks are initializated with 'ceil (nat/threads)'
  if (i >= nat) 
    return;
  // we try working with less global memory possible
  // so we set up some temporary variables private to this kernel
  const unsigned idx = trueIndexes[i];
  //local results
  float mydevX = 0.0;
  float mydevY = 0.0;
  float mydevZ = 0.0;
  float mycoord = 0.0;
  float myVirial[9] = {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
  //local calculation aid
  float x = coordinates[3*i];
  float y = coordinates[3*i+1];
  float z = coordinates[3*i+2];
  float d[3];
  float dfunc;
  float coord;
  for (unsigned j = 0; j < nat; ++j) {
    // Safeguard against self interaction
    if (idx == trueIndexes[j])
      continue;
    
    d[0] = coordinates[3*j] - x;
    d[1] = coordinates[3*j+1] - y;
    d[2] = coordinates[3*j+2] - z;
    

    dfunc = 0.;
    coord = calculateSqr(d[0] * d[0] + d[1] * d[1] + d[2] * d[2],
     switchingParameters, dfunc);
    mydevX -= dfunc * d[0];
    mydevY -= dfunc * d[1];
    mydevZ -= dfunc * d[2];
    if (i < j) {
      mycoord += coord;
      myVirial[0] -= dfunc * d[0] * d[0];
      myVirial[1] -= dfunc * d[0] * d[1];
      myVirial[2] -= dfunc * d[0] * d[2];
      myVirial[3] -= dfunc * d[1] * d[0];
      myVirial[4] -= dfunc * d[1] * d[1];
      myVirial[5] -= dfunc * d[1] * d[2];
      myVirial[6] -= dfunc * d[2] * d[0];
      myVirial[7] -= dfunc * d[2] * d[1];
      myVirial[8] -= dfunc * d[2] * d[2];
    }
  }
  // updating global memory ONLY at the end, to access to global memory fewer times per kernel
  devOut[X(i)] = mydevX;
  devOut[Y(i)] = mydevY;
  devOut[Z(i)] = mydevZ;
  ncoordOut[i] = mycoord;
  virialOut[nat * 0 + i] = myVirial[0];
  virialOut[nat * 1 + i] = myVirial[1];
  virialOut[nat * 2 + i] = myVirial[2];
  virialOut[nat * 3 + i] = myVirial[3];
  virialOut[nat * 4 + i] = myVirial[4];
  virialOut[nat * 5 + i] = myVirial[5];
  virialOut[nat * 6 + i] = myVirial[6];
  virialOut[nat * 7 + i] = myVirial[7];
  virialOut[nat * 8 + i] = myVirial[8];
}
```

You can view this kernel as the inner body of the nested for loop that can be used
 to write the most naive serial implementation of the coordination 
 (the outer loop would run on the `i` variable).

The use of global memory should be limited in a kernel, because accessing global
memory is far slower than working on shared memory (that it is not used in this
case, shared memory is shared between kernels within a group) or the variables,
(the  "local memory") declared within each kernel.

Here within each kernel, I have accumulated the values in local variables and not
 on the global memory and then update the global memory only at the end of the 
 calculation. Using `mycoord += coord;` instead of `ncoordOut[i] += coord;` 
 within the loop will speed up the calculations.

In the actual implementation the `float myVirial[9];` and `float d[3];` are 
presented as a collection of 9 and 3 single declared values to use the registers
of the kernels, here are declared as an array for clarity.

### The switching function

The switching parameters are stored in a simple struct: when called, kernels
accept struct variables as inputs, making it simpler to pass parameters to functions:
```c++
struct rationalSwitchParameters {
  float dmaxSQ = std::numeric_limits<float>::max();
  float invr0_2 = 1.0;
  float stretch = 1.0;
  float shift = 0.0;
  int nn = 6;
  int mm = 12;
};
```

`calculateSqr` is a simple interface to the actual switching function and takes
the squared distance and prepares it for the actual rational function (by
precalculating $\left(\frac{ r }{ r_0 }\right)$). It is a rewriting of the 
`PLMD::SwitchingFunction::calculateSqr` method as a `__device__` function:
```c++
//device functions can called by other __device__ functions or kernel on the device, but not from the host
__device__ float
calculateSqr(const float distancesq,
             const rationalSwitchParameters switchingParameters,
             float &dfunc) {
  float result = 0.0;
  dfunc = 0.0;
  if (distancesq < switchingParameters.dmaxSQ) {
    const float rdist_2 = distancesq * switchingParameters.invr0_2;
    result = pcuda_Rational(rdist_2, switchingParameters.nn / 2,
                            switchingParameters.mm / 2, dfunc);
    // chain rule:
    dfunc *= 2 * switchingParameters.invr0_2;
    // cu_stretch:
    result = result * switchingParameters.stretch + switchingParameters.shift;
    dfunc *= switchingParameters.stretch;
  }
  return result;
}
``` 
Also `pcuda_Rational` is a rewrite to the method `PLMD::SwitchingFunction::do_rational` for the GPU:
```c++
__device__ float pcuda_Rational(const float rdist, const int NN,
                                         const int MM, float &dfunc) {
  float result;
  if (2 * NN == MM) {
    // if 2*N==M, then (1.0-rdist^N)/(1.0-rdist^M) = 1.0/(1.0+rdist^N)
    float rNdist = pcuda_fastpow(rdist, NN - 1);
    result = 1.0 / (1 + rNdist * rdist);
    dfunc = -NN * rNdist * result * result;
    
  } else {
    if (rdist > (1. - 100.0 * cu_epsilon) && rdist < (1 + 100.0 * cu_epsilon)) {
      result = NN / MM;
      dfunc = 0.5 * NN * (NN - MM) / MM;
    } else {
      float rNdist = pcuda_fastpow(rdist, NN - 1);
      float rMdist = pcuda_fastpow(rdist, MM - 1);
      float num = 1. - rNdist * rdist;
      float iden = 1.0 / (1.0 - rMdist * rdist);
      result = num * iden;
      dfunc = ((-NN * rNdist * iden) + (result * (iden * MM) * rMdist));
    }
  }
  return result;
}
```

From what I [understood](https://docs.nvidia.com/cuda/cuda-c-programming-guide/index.html#noinline-and-forceinline)
the compilers tend to inline `__device__` functions.
It is possible to enforce the behaviour with  `__forceinline__` or `__inline_hint__`


## Interfacing to cuda: invoking the kernel and the reductions
This section has changed heavily since the previous version
Go to the [helpers](Helpers.md) page for details on the reduction and on how the
 CCCL interface.

### Calling the kernel in the calculate() method

As in any other `PLMD::Action` we have a `calculate()` method.

We start with getting the positions of the atoms, and we immediately load them 
into the GPU:
```c++
//cudaPositions is a thrust::device_vector<float>
auto positions = getPositions();  
CUDAHELPERS::plmdDataToGPU(cudaPositions, positions, streamDerivatives);
```
during the construction of the action the number of atoms has already been
initialized, so no need to resize `cudaPositions` (for safety reasons
`plmdDataToGPU` will do it for you) or `cudaDerivatives`. Moreover, we are using
the async version of `plmdDataToGPU`, so we can set up other things on the CPU
while the data is copied.

Then we fetch the number of atoms and we prepare the memory and the number of
groups for calling the kernel:
```c++
auto nat = positions.size();
constexpr unsigned nthreads = 512;

//each thread work on a single atom,
//each group collects nthreads
unsigned ngroups = ceil(double(nat) / nthreads);

cudaCoordination.resize(nat);
cudaVirial.resize(nat * 9);
```
`cudaCoordination` and `cudaVirial` are the outputs of the kernel and will need
to be reduced after.

the kernel is called with the `<<<>>>` syntax, between the three brackets we
specify 2 to 4 information:
- the number of groups to use
- the number of threads per group
- the eventual quantity of shared memory
- the eventual stream to enqueue the kernel into

(specify the shared memory and the stream is optional):

```c++
getCoord<<<ngroups, nthreads, 0, streamDerivatives>>>(
    nat, switchingParameters,
    thrust::raw_pointer_cast(cudaPositions.data()),
    thrust::raw_pointer_cast(cudaTrueIndexes.data()),
    thrust::raw_pointer_cast(cudaCoordination.data()),
    thrust::raw_pointer_cast(cudaDerivatives.data()),
    thrust::raw_pointer_cast(cudaVirial.data()));
```
### Moving the derivatives to the host RAM

Before moving the data again on the CPU's RAM we want to be sure that the
[kernel](#the-coord-kernel) has finished its calculations by calling `cudaDeviceSynchronize();`.

Then we enqueue an async copy of the derivatives.

```c++
cudaDeviceSynchronize();
CUDAHELPERS::plmdDataFromGPU(cudaDerivatives, deriv, streamDerivatives);
```
### Calling the reductions in the calculate() method

After the [kernel](#the-coord-kernel) finishes we have the virial and the
coordination accumulated for each atom: we proceed to accumulate the results for
the whole system with the utilities in _cudaHelpers.cuh_, which are written using
the building blocks of CCCL/cub.
The reduction algorithm is recursively called by the following loop.

```c++
auto N = nat;
//at each consequent iteration the kernels will return nGroups elements
//so we repeat the loop until we have sum-reduced the data to only one (per component in the case of the virial)
while (N > 1) {
  size_t runningThreads = CUDAHELPERS::threadsPerBlock(N, maxNumThreads);
  //dataperthread is fixed and is the number of element each thread will work on
  unsigned nGroups = ceil(double(N) / (runningThreads * dataperthread));

  reductionMemoryCoord.resize(nGroups);
  reductionMemoryVirial.resize(9 * nGroups);
  
  //dim3 is a cuda struct that contains up to three integers
  //here we are reducing the 9 dimension of the virial
  dim3 ngroupsVirial(nGroups, 9);
  // doReductionND will need a 2D group size,
  //  - the first dimension is the number of group to use for each dimension,
  //  - the second dimension is the number of dimensions of the array
  CUDAHELPERS::doReductionND<dataperthread>(
        thrust::raw_pointer_cast(cudaVirial.data()),
        thrust::raw_pointer_cast(reductionMemoryVirial.data()), N,
        ngroupsVirial, runningThreads, streamVirial);

  CUDAHELPERS::doReduction1D<dataperthread>(
        thrust::raw_pointer_cast(cudaCoordination.data()),
        thrust::raw_pointer_cast(reductionMemoryCoord.data()), N, nGroups,
        runningThreads, streamCoordination);

  if (nGroups == 1) {
    CUDAHELPERS::plmdDataFromGPU(reductionMemoryVirial, virial, streamVirial);
    // here we are using the simplified thrust syntax
    coordination = reductionMemoryCoord[0];
  } else {
    // std::swap(reduceScalarIn,reduceSOut);
    reductionMemoryCoord.swap(cudaCoordination);
    reductionMemoryVirial.swap(cudaVirial);
  }

  N = nGroups;
}
```
The last iteration (where `nGroups == 1`) enqueue the async version of the GPU to CPU copies.

The swaps of the memory are there because the output of an iteration reduction
became the input of the next iteration and we want to use the already allocated
data as the next result recipient. These swap operations do not move the memory, but should exchange the addresses and the data between the two variables.


The ND-reduction expects the data to be organized as a series of concatenated
arrays (this is also known as a block arrangement, at least in the cub manual):
`[x0, x1, x2, ..., xn-2, xn-1, y0, y1, y2, ..., yn-2, yn-1, z0,... ]` and so on.

### Finalizing the results

After the reduction/accumulation, the data is then uploaded to Plumed with the
standard procedure, again we use `cudaDeviceSynchronize();` to be sure that all
the data have been moved to the CPU:
```c++
cudaDeviceSynchronize();
for (unsigned i = 0; i < deriv.size(); ++i)
  setAtomsDerivatives(i, deriv[i]);

setValue(coordination);
setBoxDerivatives(virial);
```
## Other implementations

I also set up the explanation for the implementation of the coordination for [two groups](ImplementationTwoGroups) and the [pair](ImplementationPair) version

