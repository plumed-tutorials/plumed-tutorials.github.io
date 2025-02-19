# hybrid Small Angle Scattering — hands-on guide

This guide is designed to provide users with practical advice on using the hySAS module. For theoretical information about the method, please refer to the related [manuscript](https://pubs.acs.org/doi/full/10.1021/acs.jctc.3c00864). The guide is divided into several sections:

#### [hySAS Intro & Overview](intro.md)
A brief introduction to the method, basic concepts, and an overview of the analyses that can be performed.

#### [Determining the Scattering Profile with hySAS](01.md)
From coordinates to a SAS curve: steps and examples to analyse a PDB file or a trajectory.

#### [Generating a Conformational Ensemble with GMX and hySAS](02.md)
Combining GROMACS and PLUMED to generate conformational ensembles restrained by SAS data using different coupling methods.

#### [Preparing the Input Files](input.md)
Guidelines and tips for preparing the input files.

#### [Compiling PLUMED with ARRAYFIRE Support](arrayfire.md)
Technical suggestions and a real-case example for installing PLUMED with ARRAYFIRE support on a SLURM-based HPC.

```mermaid
flowchart TB
  A[hySAS intro & overview]
  A --> B[Tutorial-1: <br> Determining the scattering profile with hySAS]
  B --> C[Tutorial-2: <br> Generating a conformational ensemble with GMX and hySAS]

  D[Technical Support: <br> Preparing the input files]
  D --> E[Technical Support: <br> Compiling PLUMED with ARRAYFIRE support]
  
  click A "intro.html" "hySAS intro & overview"
  click B "01.html" "Tutorial-1: Determining the scattering profile with hySAS"
  click C "02.html" "Tutorial-2: Generating a conformational ensemble with GMX and hySAS"
  click D "input.html" "Preparing the input files"
  click E "arrayfire.html" "Compiling PLUMED with ARRAYFIRE support"
```
