## Premise

We now try to change what we made in the [self-coordination](Implementation.md) and determine the coordination between two groups.

I am assuming that you have already read the details about how the coordination is implemented in the [other chapter](Implementation.md).
So here you will see some more abstract pseudo code. Always refer to my (evolving) [repository](https://github.com/Iximiel/cudaOnPlumed) and on the main [plumed repository](https://github.com/plumed/plumed2) for a more accurate and performant code.

## Wait, and the derivatives?
First of all let's hastily rewrite the core kernel, stripped of the declarations 

```c++
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
  const float x = coordinates[X (i)];
  const float y = coordinates[Y (i)];
  const float z = coordinates[Z (i)];
  /* declaring calculation and output variables
  ...
  */
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
/* setting the data to the output
  ...
  */
}
```
We want the coordination between all of the atoms of 'GROUPA' and all of the atoms of 'GROUPB'.
But this kernel solves a different problem: it loops on ALL the atoms and calculates the coordination between ALL of them.

How can we work around this?

Let's start to acknowledge that we will need to have different specialized kernels (since branching within a kernel will generate a loss of performance).

Then we change the signature of the new kernel:
```c++
__global__ void getCoordDual(
    const unsigned natA,
    const unsigned natB,
    const rationalSwitchParameters switchingParameters,
    const float *coordinatesA,
    const float *coordinatesB,
    const unsigned *trueIndexes, float *ncoordOut,
    float *devOut, float *virialOut)
```
So that we pass the parameters of the two groups separately.

we then make the first part of the kernel around this change ()
```c++
  // i is the index of the atoms that will be confronted with all the others
  const unsigned i = threadIdx.x + blockIdx.x * blockDim.x;

  // blocks are initializated with 'ceil (nat/threads)'
  if (i >= nat) 
    return;
  const unsigned idx = trueIndexes[i];
  const float x = coordinatesA[X (i)];
  const float y = coordinatesA[Y (i)];
  const float z = coordinatesA[Z (i)];
  /* declaring calculation and output variables
  ...
  */
  for (unsigned j = 0; j < natB; ++j) {
    /*calculations*/
  }
```
So now each atom of group A will ONLY interact with the atoms in group B, then we rewrote the core of the loop, discarding the "triangular things" of before:
```c++
  for (unsigned j = 0; j < natB; ++j) {
    // Safeguard against self interaction
    if (idx == trueIndexes[j])
      continue;
    
    d[0] = coordinatesB[3*j] - x;
    d[1] = coordinatesB[3*j+1] - y;
    d[2] = coordinatesB[3*j+2] - z;
    

    dfunc = 0.;
    coord = calculateSqr(d[0] * d[0] + d[1] * d[1] + d[2] * d[2],
     switchingParameters, dfunc);
    mydevX -= dfunc * d[0];
    mydevY -= dfunc * d[1];
    mydevZ -= dfunc * d[2];
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

``` 
And we end the kernel exactly like in the single group case:

```c++
  devOut[X(i)] = mydevX;
  devOut[Y(i)] = mydevY;
  devOut[Z(i)] = mydevZ;
  ncoordOut[i] = mycoord;
  virialOut[natA * 0 + i] = myVirial[0];
  virialOut[natA * 1 + i] = myVirial[1];
  virialOut[natA * 2 + i] = myVirial[2];
  virialOut[natA * 3 + i] = myVirial[3];
  virialOut[natA * 4 + i] = myVirial[4];
  virialOut[natA * 5 + i] = myVirial[5];
  virialOut[natA * 6 + i] = myVirial[6];
  virialOut[natA * 7 + i] = myVirial[7];
  virialOut[natA * 8 + i] = myVirial[8];
```

But now we still miss a piece: atoms indexed `i` are in GROUPA: it looks like we are storing the derivatives the coordination and the virial only relative to one of the two groups.
This affirmation is true only about the derivatives since coordination and virial are "couple" properties.

So, how do we solve this new problem of getting the derivatives of GROUPB?

## Calculationg the derivatives of the atoms B

We might calculate the derivative for group B along the ones of group A,
but we will end up needing `size`(groupA) * size(groupB)` extra triplette of floats
to be stored during the execution of the first kernel because we can't sum on the same
piece of data unless we stop the parallel calculation to avoid a data race.
Ad with this solution we would need to store these values since we are traversing the "matrix of couples" along the "group A axis".

But in that case, we will need `size(groupA) * size(groupB) * 8` bytes of memory for each dimension (3 in our case).
That means, for example, that for a system of 10000 atoms, in two groups of 5000 will be 200000000 bytes, 
that are roughly 200 MB, but since the relationship is quadratic and the memory on a GPU is usually scarce,
is not a scalable option (with a group of 100000 atoms divide d in two would be 20GB).

The easiest solution that I found is to redo the same loop, but with inverted groups, but keeping ONLY
calculating only the derivatives.
This does not make the algorithm scale differently (summing two algorithms with the same time complexity is an algorithm with the same time complexity) and does not use extra space.


```c++
//We use a similar signature without coordination and virial
__global__ void getABdevB(
    const unsigned natA,
    const unsigned natB,
    const rationalSwitchParameters switchingParameters,
    const float *coordinatesA,
    const float *coordinatesB,
    float *devOut) {
  // i is the index of the atoms that will be confronted with all the others
  const unsigned i = threadIdx.x + blockIdx.x * blockDim.x;
  // blocks are initializated with 'ceil (nat/threads)'
  if (i >= natB) 
    return;
  // we try working with less global memory possible
  // so we set up some temporary variables private to this kernel
  const unsigned idx = trueIndexes[i];
  //local results
  float mydevX = 0.0;
  float mydevY = 0.0;
  float mydevZ = 0.0;
  //local calculation aid
  float x = coordinatesB[3*i];
  float y = coordinatesB[3*i+1];
  float z = coordinatesB[3*i+2];
  float d[3];
  float dfunc;
  float coord;
  for (unsigned j = 0; j < natA; ++j) {
    // Safeguard against self interaction
    if (idx == trueIndexes[j])
      continue;
    
    d[0] = coordinatesA[3*j] - x;
    d[1] = coordinatesA[3*j+1] - y;
    d[2] = coordinatesA[3*j+2] - z;
    

    dfunc = 0.;
    coord = calculateSqr(d[0] * d[0] + d[1] * d[1] + d[2] * d[2],
     switchingParameters, dfunc);
    mydevX -= dfunc * d[0];
    mydevY -= dfunc * d[1];
    mydevZ -= dfunc * d[2];
  }
  // updating global memory ONLY at the end, to access to global memory fewer times per kernel
  devOut[X(i)] = mydevX;
  devOut[Y(i)] = mydevY;
  devOut[Z(i)] = mydevZ;
}
```

### Remarks
The problem of this approach is that if there is a great imbalance in numbers between 
the two groups, written as is does not scale efficiently.

For example, if you have group A with 1000 atoms and b with only one, you will get the first kernel doing a single iteration in 1000 threads for the first atoms, and the second kernel occupying a single thread for 1000 iterations.
But this may be solved by trying to balance how much work each thread will need to do.

