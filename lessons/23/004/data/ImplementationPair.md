## Implement the pair coordination

See the main [coordination implementation](Implementation.md), the code there is uses as a starting point for this  variant.

This should be the easiest implementation: 
If each kernel will run only on a couple it could be written like this:

```c++
template <bool usePBC, typename calculateFloat>
__global__ void
getCoord (const unsigned couples,
          const PLMD::GPU::rationalSwitchParameters<calculateFloat>
              switchingParameters,
          const calculateFloat *coordinates,
          const unsigned *trueIndexes,
          calculateFloat *ncoordOut,
          calculateFloat *devOut,
          calculateFloat *virialOut) {
  // blockDIm are the number of threads in your block
  const unsigned i = threadIdx.x + blockIdx.x * blockDim.x;
  const unsigned j = i + couples;
  
  // blocks are initializated with 'ceil (couples/threads)'
  if (i >= couples) { 
    return;
  }
  
  const unsigned idx = trueIndexes[i];
  const unsigned jdx = trueIndexes[j];
  if (idx == jdx) {
    return; 
  }

  // local calculation aid
  calculateFloat d_0, d_1, d_2;
  calculateFloat dfunc;

  d_0 = coordinates[X (j)] - coordinates[X (i)];
  d_1 = coordinates[Y (j)] - coordinates[Y (i)];
  d_2 = coordinates[Z (j)] - coordinates[Z (i)];

  dfunc = 0.;
  ncoordOut[i] = calculateSqr (
      d_0 * d_0 + d_1 * d_1 + d_2 * d_2, switchingParameters, dfunc);

  mydevX = dfunc * d_0;
  mydevY = dfunc * d_1;
  mydevZ = dfunc * d_2;

  devOut[X (i)] = -mydevX;
  devOut[Y (i)] = -mydevY;
  devOut[Z (i)] = -mydevZ;
  devOut[X (j)] = mydevX;
  devOut[Y (j)] = mydevY;
  devOut[Z (j)] = mydevZ;
  
  virialOut[couples * 0 + i] = -dfunc * d[0] * d[0];
  virialOut[couples * 1 + i] = -dfunc * d[0] * d[1];
  virialOut[couples * 2 + i] = -dfunc * d[0] * d[2];
  virialOut[couples * 3 + i] = -dfunc * d[1] * d[0];
  virialOut[couples * 4 + i] = -dfunc * d[1] * d[1];
  virialOut[couples * 5 + i] = -dfunc * d[1] * d[2];
  virialOut[couples * 6 + i] = -dfunc * d[2] * d[0];
  virialOut[couples * 7 + i] = -dfunc * d[2] * d[1];
  virialOut[couples * 8 + i] = -dfunc * d[2] * d[2];
}
```

The efficiency of this approach is not high, because we lose time in spinning up `ncouples` of threads, each one that does a single small task, the coordination of a single pair.

An attempt to make it quicker could be to slightly change the kernel with a for loop on some pairs.

```c++
template <bool usePBC, typename calculateFloat>
__global__ void
getCoord (const unsigned couples,
          const unsigned couplesPerThread,
          const PLMD::GPU::rationalSwitchParameters<calculateFloat>
              switchingParameters,
          const calculateFloat *coordinates,
          const unsigned *trueIndexes,
          calculateFloat *ncoordOut,
          calculateFloat *devOut,
          calculateFloat *virialOut) {
  // blockDIm are the number of threads in your block
  const unsigned tid = threadIdx.x + blockIdx.x * blockDim.x;
  
  for(unsigned k=0;k<couplesPerThread;++k){
    const unsigned i = couplesPerThread*tid + k;
    const unsigned j = i + couples;
    const unsigned idx = trueIndexes[i];
    const unsigned jdx = trueIndexes[j];
    if (i >= couples) { 
      break;
    }
    if (idx == jdx) {
      continue; 
    }

    // local calculation aid
    calculateFloat d_0, d_1, d_2;
    calculateFloat dfunc;

    d_0 = coordinates[X (j)] - coordinates[X (i)];
    d_1 = coordinates[Y (j)] - coordinates[Y (i)];
    d_2 = coordinates[Z (j)] - coordinates[Z (i)];

    dfunc = 0.;
    ncoordOut[i] += calculateSqr (
        d_0 * d_0 + d_1 * d_1 + d_2 * d_2, switchingParameters, dfunc);

    mydevX = dfunc * d_0;
    mydevY = dfunc * d_1;
    mydevZ = dfunc * d_2;

    devOut[X (i)] = -mydevX;
    devOut[Y (i)] = -mydevY;
    devOut[Z (i)] = -mydevZ;
    devOut[X (j)] = mydevX;
    devOut[Y (j)] = mydevY;
    devOut[Z (j)] = mydevZ;
  }
  virialOut[couples * 0 + tid] = -dfunc * d[0] * d[0];
  virialOut[couples * 1 + tid] = -dfunc * d[0] * d[1];
  virialOut[couples * 2 + tid] = -dfunc * d[0] * d[2];
  virialOut[couples * 3 + tid] = -dfunc * d[1] * d[0];
  virialOut[couples * 4 + tid] = -dfunc * d[1] * d[1];
  virialOut[couples * 5 + tid] = -dfunc * d[1] * d[2];
  virialOut[couples * 6 + tid] = -dfunc * d[2] * d[0];
  virialOut[couples * 7 + tid] = -dfunc * d[2] * d[1];
  virialOut[couples * 8 + tid] = -dfunc * d[2] * d[2];
}
```
This kernel works on `couplesPerThread` per thread. The problem with this prototype is that nearly all the operations are done in the global memory.
