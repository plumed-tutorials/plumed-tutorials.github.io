## Processes: MPI
```c++
void MyCoordination::calculate() {
  double ncoord = 0.;
  auto pos = getPositions();
  const unsigned nn = pos.size();
  unsigned stride = comm.Get_size();
  unsigned rank = comm.Get_rank();
  Vector distance;
  for (unsigned int i0 = rank; i0 < nn; i0 += stride) {
    for (unsigned int i1 = 0; i1 < nn; ++i1) {
      if (i0 == i1){continue;}
      distance = delta(getPosition(i0), getPosition(i1));
      ncoord += (distance.modulo() < R_0) ? 1 : 0;
    }
  }
  if (stride > 1) {
    comm.Sum(ncoord);
  }
  setValue(ncoord);
}
```

In this case the parallelization strategy passes through parallel processes:
with `unsigned rank = comm.Get_rank()` we inform the function wich is the this process, with `unsigned stride = comm.Get_size()` we want to know the number of processes that partecipate to the calculation.

The strategy here is to split the outer for cycle between the processes, so that each process will do only part of the loop. We are doing by hand what the `#pragma for` does behind the curtains in the threaded example.
The original cycle `for (unsigned int i0 = 0; i0 < nn; ++i0)` became `for (unsigned int i0 = rank; i0 < nn; i0 += stride)`: `stride` ensures that the calculation won't overlap.

We have less risk of having a data race because all the variable are instantiated for each different processor, meaning that non only the for loop is executed in parallel but that the change in data in a process won't affect other processes!

We have then the problem of obtaining the correct result: we have to set `ncoord` to the sum of all the `ncoord` in the various processes.
To do this sum we use the Plumed mpi inteface: `comm.Sum(ncoord)` this will call the reduction sum algorithm of the MPI library with no complications.
Plumed tools used:

- `tools/Communicator.h` is present as the variable `comm` that is inherited through `PLMD::Action`.
`PLMD::Communicator` is an interface to some of the functionalities of the C API of mpi.h
  - `PLMD::Communicator::Get_size()` to get the number of the processes spawned by mpirun
  - `PLMD::Communicator::Get_rank()` to get the id of the process
  - `PLMD::Communicator::Sum()` to obtain the correct sum of `ncoord` from all the processes

[back](Readme.md)

See also:
[serial](Readme_Serial.md) [openMP](Readme_OMP.md) [MPI](Readme_MPI.md) [Cuda](Readme_CUDA.md)
