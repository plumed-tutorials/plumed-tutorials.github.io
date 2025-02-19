<h3>Overview</h3>

A tutorial to run simple surface binding calculations using Metadynamics through PLUMED. The procedure described herein is an extension of the [earlier work of Doudou <em>et al.</em>](https://pubmed.ncbi.nlm.nih.gov/26609600/) (1) where the binding free energy of a model binding system (and a benzamidine−trypsin system) are calculated from a one-dimensional PMF and standardised to a reference state of a 1 M solution. This procedure has been used extensively by our group for binding processes on surfaces of [halite](https://pubs.acs.org/doi/full/10.1021/acs.jctc.2c00787) (2) and [calcite](https://pubs.acs.org/doi/full/10.1021/acs.jpcc.3c02864) (3).

A harmonic restraint is applied to the binding atom orthogonal to the collective variable used to describe the binding process. This has the effect of constraining the binding atom to a cylindrical volume orthogonal to the surface of interest. Equations 8 and 9 from the original paper of Doudou <em>et al.</em> demonstrate that the volume explored in the unbound region by the restrained binding atom can be analytically calculated and referenced to the standard-state volume, producing a volumed-based free energy correction to be applied to the total binding energy. 

While the original paper allows for the correction of a harmonic restraint with any spring constant, this method will only ever produce an upper limit for any free energy barriers separating the bound and unbound regions due to being forced to follow a straight path during separation. Here we describe how to apply and account for a flat-bottomed cylindrical restraint with harmonic walls starting at a specified radius instead of the harmonic restraint used in the original paper, which represents the limiting case of the general approach as the cylinder radius tends to zero. The flat-bottomed restraint provides a region unperturbed by any harmonic potential, allowing for the possibility of producing the actual free energy profile with accurate barrier heights, for a sufficiently large radius value, which could then be used for kinetic studies. Described [here](markdown/theory.md) are the integrals for the flat-bottomed potentials and a brief overview on how to turn the one-dimensional PMF into a standard binding free energy.

<h3>System creation</h3>

For this tutorial, we have constructed a simple model system that will run and converge quickly on any machine while still mimicking the important aspects of an actual binding profile. The details on how this has been done are presented [here](markdown/system.md).

<h3>Input files & running simulation</h3>

[OpenMM](https://github.com/openmm/openmm) (4) has been chosen as the molecular dynamics engine for this tutorial, utilising PLUMED through the [openmm-plumed plugin](https://github.com/openmm/openmm-plumed). Details on the input files provided, their meaning, and how to use them are discussed [here](markdown/inputs.md).

<h3>Analysing simulation</h3>

Using the PLUMED command line tool and a series of Python and bash scripts, we demonstrate how to analyse the raw HILLS file produced by these simulations and generate the final standard binding free energies. All details can be found [here](markdown/analysis.md).

<h3>References</h3>

1. Doudou S, Burton NA, Henchman RH. Standard free energy of binding from a one-dimensional potential of mean force. Journal of Chemical Theory and Computation. 2009 Apr 14;5(4):909-18.
2. Silvestri A, Raiteri P, Gale JD. Obtaining consistent free energies for ion binding at surfaces from solution: pathways versus alchemy for determining kink site stability. Journal of Chemical Theory and Computation. 2022 Sep 8;18(10):5901-19.
3. Armstrong BI, Silvestri A, De La Pierre M, Raiteri P, Gale JD. Determining the complete stability of calcite kink sites: Real vs ideal. The Journal of Physical Chemistry C. 2023 Jul 5;127(28):13958-68.
4. Eastman P, Galvelis R, Peláez RP, Abreu CR, Farr SE, Gallicchio E, Gorenko A, Henry MM, Hu F, Huang J, Krämer A. OpenMM 8: molecular dynamics simulation with machine learning potentials. The Journal of Physical Chemistry B. 2023 Dec 28;128(1):109-16.

```mermaid
flowchart TB
  F[Metadynamics] --> A[Original Work]
  A --> B[Theory]
  B --> C[Model system]
  C --> D[Inputs]
  D --> E[Analysis]

  click F "../../../21/004/data/NAVIGATION.html" "A tutorial that introduces the basics of metadynanics"
  click A "https://pubmed.ncbi.nlm.nih.gov/26609600/" "Theory behind computing standard binding free energies."
  click B "markdown/theory.html" "Extension to the theory for a cylindrical volume."
  click C "markdown/system.html" "Model system for surface binding calculations."
  click D "markdown/inputs.html" "Input file preparation and explanation."
  click E "markdown/analysis.html" "HILLS processing, free energy calculation and standardisation."
```
