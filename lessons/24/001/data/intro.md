# hySAS intro & overview

The combination of Small-Angle X-ray and Neutron Scattering (SAXS/SANS or SAS) experiments with molecular dynamics (MD) simulations is an effective strategy for the characterisation of biomolecules in solution. On the one hand, the limited resolution of SAS can benefit from the MD contribution, and on the other hand, the inaccuracy of MD can be mitigated by using the experimental data to drive the simulations and generate conformational ensembles in agreement with the SAS data.

To achieve this result, an energy penalty is introduced to the system potential. This bias depends on the difference between the SAS experimental data and the SAS profile calculated in real-time from the system coordinates retrieved from the ongoing simulation. In this way, all the conformations that are not in agreement with the experimental data are discouraged.

The predictor used to calculate the SAS intensity from the coordinates of the molecule is called the "forward model".

Although very promising, this approach is hampered by its high computational cost. One way to overcome this limitation is to calculate the intensity of the system of interest using a coarse-grained model, thus aggregating the scattering behaviour of groups of atoms into single particles. This does not mean that the simulation is also performed with a coarse-grained model, but that the SAS signal is calculated at a lower resolution: the simulation retains all the atomistic details!

Previously, we presented a hybrid resolution method that combines atomistic MD simulations with a Martini coarse-grained SAXS forward model.

We further enhance this technique by developing a novel hybrid-SAS method that is faster, more accurate, extended to the SANS intensity calculation and that is compatible with both proteins and nucleic acids. In the new hySAS forward model, an amino acid is represented by a single bead, while a nucleic acid is represented by three beads: one for the base, one for the sugar and one for the phosphate group. The centre of each particle is placed at the centre of mass of the atoms belonging to the bead itself. Protein-nucleic acid complexes are also compatible with the method.

In addition, an implicit and user-definable solvation layer contribution is included in the calculation to allow the reconstruction of a more realistic scattering behaviour in solution. This layer depends on solvent-solute interactions and, being typically more electron/neutron dense than the bulk solvent, actively contributes to the scattering signal. To account for this phenomenon, just for the beads that are exposed to the solvent is applyied an electron density correction. For this reason, the solvent-accessible surface area of a bead is calculated from the coordinates of the heavy atoms belonging to that bead using the LCPO algorithm.

Some additional features are introduced specifically for SANS. It is possible to handle the percentage of deuterium in solution and implicitly account for hydrogen-deuterium exchange for the bead that are exposed to the solvent.

As well as generating a conformational ensemble or refining a structure, it is possible to use the forward model to calculate the SAS profile from a PDB or a trajectory using the PLUMED driver.

For additional information, please refer to the related [manuscript](https://pubs.acs.org/doi/full/10.1021/acs.jctc.3c00864).

##### [Back to hySAS home](NAVIGATION.md)
