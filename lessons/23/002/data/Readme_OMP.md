## Threading: openMP
```c++
void MyCoordination::calculate() {
  double ncoord = 0.;
  auto pos = getPositions();
  const unsigned nn = pos.size();
  unsigned nt = OpenMP::getNumThreads();
  Vector distance;
#pragma omp parallel num_threads(nt)
  {//start parallel scope
#pragma omp for 
    for (unsigned int i0 = 0; i0 < nn; ++i0) {
      for (unsigned int i1 = 0; i1 < nn; ++i1) {
        if (i0 == i1) {continue;}
        distance = delta(getPosition(i0), getPosition(i1));
        ncoord += (distance.modulo() < R_0) ? 1 : 0;
      }
    }
  }//end parallel scope
  setValue(ncoord);
}
```

This is nearly identical to the serial version. With few differences:
We are asking the system if we want to run with more threads with `unsigned nt = OpenMP::getNumThreads()`, (if is the first time that it is called stores and return the number in the environmental variable `PLUMED_NUM_THREADS`, otherwise it will return the stored number).

Then with that information we open a parallel environment with `#pragma omp parallel num_threads(nt)` in which we explicilty specify the number of threads (otherwise il will use the number in the environmntal variable `OMP_NUM_THREADS`).
Note that the pragma is prepended to a scope delimited by curly braces: the code within them will be distribuited between the threads.

Then we have the next pragma instruction: `#pragma omp for`: this pragma will tranform the `for` in order to make it work in the multithreaded environment.

<details>
  <summary>SPOILER</summary>

 There is at least a race condition here: can you spot it?

<details>
    <summary>ANSWER</summary>

`ncoord` is the race condition: each time two threads or more threads execute the `+=` simultaneusly they will increment the `ncoord` from the same value, meaning the the number saved in memory has been incremented only once instead of twice or more.

The solution is to append `reduction(+:)` to for pragma: `#pragma for reduction(+:)`
  </details>
</details>

Plumed tools used:
- `tools/OpenMP.h` contains some function that are useful in working with openMP.
  - `OpenMP::getNumThreads()` to get the number of threads from the environmental variable `PLUMED_NUM_THREADS

[back](Readme.md)

See also:
[serial](Readme_Serial.md) [openMP](Readme_OMP.md) [MPI](Readme_MPI.md) [Cuda](Readme_CUDA.md)
