# Parallelism in Plumed2

This lesson is a pratical introduction (with some exercises with code to modify) to the parallel functionality of PLUMED for the developers.

The code is hosted [here](https://github.com/Iximiel/PlumedFlagship_parallelism). You can start from the [introduction](Readme.md), and then read the [serial example](Readme_Serial.md) that contains the base idea of the CV.

You can then navigate the three cases ([openMP](Readme_OMP.md), [MPI](Readme_MPI.md), [Cuda](Readme_CUDA.md)) in any order

NB: For this lesson the CV is presented with no explicit derivatives calculated.



```mermaid
flowchart LR

Intro[Introduction]
Serial[Serial example]
OMP[OMP example]
MPI[MPI example]
CUDA[CUDA example]

Intro<==>Serial

Serial<==>OMP
Serial<==>MPI
Serial<==>CUDA

click Intro "Readme.html" "The introduction to the lessons"
click Serial "Readme_Serial.html" "The presentation of the base example"
click OMP "Readme_OMP.html" "The presentation of the openMP example"
click MPI "Readme_MPI.html" "The presentation of the MPI example"
click CUDA "Readme_CUDA.html" "A prototype for a Cuda implementation"
```
