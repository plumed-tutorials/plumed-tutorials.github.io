# Unbiased

This folder contains the seeding simulations needed for training the autoencoder and tuning the switching function.

## Contents

- **1_solvate**: Creating the simulation box with 1 NaCl ion solvated in TIP3P water.
- **2_em**: Minimizing the simulation box to relax non-physical structures followed by a short NVT simulation for equilibration.
- **3_md**: An unbiased MD run to seed the autoencoder training.
- **4_calcPIV**: Computing PIV vector of the unbiased MD trajectory
