# Computing the effect of mechanical force in PLUMED

### This repository contains files for the plumed masterclass presented on October 17, 2022.

It covers the effect of mechanical forces and the `fisst` module.

Masterclass videos were presented by Glen Hocky and Guillaume Stirnemann

FISST video (Hocky): https://www.youtube.com/live/1GSKhM57lo0?si=Fetb-LabeqlweNHU

Modeling of mechanobiological processes (Stirnemann) and solutions (Hocky): https://www.youtube.com/live/JjpKSzb9kJM?si=9zwW6_gW1siFZ9yJ

There are four systems:

- double_well/ - The effect of constant force is studied on a double well potential using `pesmd` and `metad`
- v-shape/ - The effect of force on a 2d potential is studied using `fisst`
  - This contains an example script showing how to reweight using FISST observable files
- helix/ - The effect of force on a model molecule is studied using `fisst` in LAMMPS
- ala10/ - The effect of force is studied on a solvated model peptide, decalanine, using GROMACS
