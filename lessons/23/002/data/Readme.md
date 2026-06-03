# Plumed Flagship meeting: Lecture: Parallel and GPUs programming in PLUMED

We have some simple examples for using parallelism in plumed:

- `SerialCoordination.cpp` is a ~~vandalized~~ simplified version of the cv `Coordination`
- `OMPCoordination.cpp` is an example on how openMP can be used in Plumed
- `MPICoordination.cpp` is an example on how MPI can be used in Plumed
- `CUDACoordination.cpp` is an example on trying to user Cuda for solving this problem (it needs an ad hoc compiler queue and the kernel `CUDACoordinationkernel.cu` )

(The original `Coordination` combines the use of both openMP and MPI)

Plumed helps the developer with some tools for parallelism:
- `tools/OpenMP.h` contains some function that are useful in working with openMP.
In the example we are using `OpenMP::getNumThreads()` to get the number of threads from the environmental variable `PLUMED_NUM_THREADS`

- `tools/Communicator.h` is present as the variable `comm` that is inherited through `PLMD::Action`.
`PLMD::Communicator` is an interface to some of the functionalities of the C API of `mpi.h`.
In the example we are using `PLMD::Communicator::Get_size()` to get the number of the processes spawned by mpirun, 
`PLMD::Communicator::Get_rank()` to get the id of the process, and 
`PLMD::Communicator::Sum()` to sum the result of the coordination and make the correct value avayable for further calculations.

## Intro

The exercise uses `Base.hpp` to give a very base version of the COORDINATION CV, in this case it is returning the sum of the number of atoms that are within R_0 from each atom. For simplicity it the pbcs will be ignored throught all of the examples.
`MyCoordinationBase` in `Base.hpp` do not have the calculate method and so the example will have more or less the following structure:

```c++
#include "Base.hpp"
namespace PLMD {
class MyCoordination : public MyCoordinationBase {
public:
  explicit MyCoordination(const ActionOptions &ao)
      : Action(ao), MyCoordinationBase(ao) {}
  ~MyCoordination() = default;
  // active methods:
  void calculate() override;
};
PLUMED_REGISTER_ACTION(MyCoordination, "MYCOORDINATION")
void MyCoordination::calculate() {
...code goes here...
}
} // namespace PLMD

```
For automation purposes (see the `Makefile`) we are using the same key `PLUMED_REGISTER_ACTION(MyCoordination, "MYCOORDINATION")` for all of the examples.
### Prerequisites
- Plumed 2.9.0 configured and installed with `--enable-modules=all` and MPI
  - in my workstation I am using gcc 9.4.0 and openmpi 4.1.1
- For the GPU offloading the example is written with Nvdia's Cuda
  - In my workstation I am using cuda 11.7 with a T1000 card


## [The serial code](Readme_Serial.md)

## [Threading: openMP](Readme_OMP.md)

## [Processes: MPI](Readme_MPI.md)

## [EXTRA: GPU offloading with Cuda](Readme_CUDA.md)

## Closing information

The file in the `Solution` directory give the correct results
