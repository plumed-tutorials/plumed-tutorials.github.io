# Introduction

This tutorial will teach you how to use PLUMED, GROMACS and Python notebooks to implement an enhanced sampling strategy for magnesium-RNA binding dynamics.

## Prerequisites

- [GROMACS basic usage](http://www.mdtutorials.com/gmx/)
- [PLUMED basic syntax and analysis](https://www.plumed-tutorials.org/lessons/21/001/data/NAVIGATION.html)
- Python notebooks

## Scientific context

Magnesium(II) ions are abundant in living cells and they interact with RNA molecules, modulating their folding, catalytic properties and structural dynamics. Mg<sup>2+</sup> are found to coordinate in the inner sphere of several RNA moieties, non-bridging phosphate oxygen atoms (OP1, OP2) being by and large the most frequent in PDB structures and having the strongest binding affinity [[1, 2]](#references). 

Due to its high charge density, Mg<sup>2+</sup> strongly interacts with innersphere ligands, resulting in slow (sub-microsecond) water-exchange kinetics compared to other biologically abundant cations, and even slower binding to phosphate groups [[3]](#references). This feature is amplified in most Molecular Dynamics force fields, which hinders satisfactiory sampling of the equilibrium properties of Mg-RNA interactions.

While force-field parameters can be designed in order to accelerate the slow dynamics of magnesium, it is unclear whether the limited flexibility of classical MD potentials allow for selective tuning of the kinetics without compromising other quantities of interest, such as thermodynamics and geometric properties. In this tutorial we will explore another approach, where we selectively bias the MD simulation to accelerate the process of interest, and that can be adapted in principle to any force field.

## Outline

In [Part 1](PART1.md) we will set up a model dinucleotide and use well-tempered metadynamics to characterize the binding free-energy landscape of Mg<sup>2+</sup> to non-bridging phosphate oxygens of the RNA backbone.

In [Part 2](PART2.md) we will use the previous simulation to design a biasing potential that selectively accelerates the binding kinetics.

In Part 3 we will see how to apply the method to a larger system using Hamiltonian replica exchange.

## References

[1] [Heping Zheng, Ivan G. Shabalin, Katarzyna B. Handing, Janusz M. Bujnicki and Wladek Minor. Magnesium-binding architectures in RNA crystal structures: validation, binding preferences, classification and motif detection. *Nucleic Acids Research* **2015** 43 (7), 3789–3801.](https://doi.org/10.1093/nar/gkv225)


[2] [Richard A. Cunha and Giovanni Bussi. Unraveling Mg<sup>2+</sup>-RNA binding with atomistic molecular dynamics. *RNA* **2017** 23 (5), 628-638.](https://doi.org/10.1261/rna.060079.116)

[3] [Olof Allnér, Lennart Nilsson, and Alessandra Villa. Magnesium Ion–Water Coordination and Exchange in Biomolecular Simulations. *Journal of Chemical Theory and Computation* **2012** 8 (4), 1493-1502.](https://doi.org/10.1021/ct3000734)
