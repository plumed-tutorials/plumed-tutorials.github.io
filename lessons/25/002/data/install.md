## Hardware requirements

To complete this tutorial you need:

 * A workstation with a multi-core CPU (6-8 cores should be enough);
 * For molecular dynamics (MD) runs, access to a Linux cluster is preferable;
 * a GPU to accelerate both the MD simulation and the calculation of the cryo-EM restraint.

## Software requirements

 Make sure you have installed:

 * A modern C++ compiler that supports OpenMP parallelization and C++17.
 * MPI library/compilers for multi-replica ensemble simulations.
 * Cuda, needed by both GROMACS and PLUMED. The exact version depends a bit on how old your GPUs are.
 * [LibTorch](https://pytorch.org/get-started/locally/). Make sure you download the C++ version (LibTorch, not pytorch) that is supported by the Cuda version you installed; 
 * [Phenix](https://phenix-online.org/documentation/index.html) (any recent version), if you want to validate single-structure refinement. Not really needed for ensemble modelling.
 * [Conda](https://www.anaconda.com) to install the python libraries needed by the pre- and post-processing scripts: see installation instructions below.
 * [GROMACS](https://www.gromacs.org) and [PLUMED](https://www.plumed.org): see installation instructions below.
 * UCSF [Chimera](https://www.cgl.ucsf.edu/chimera/download.html) or [ChimeraX](https://www.cgl.ucsf.edu/chimerax/) to visualize structural models.

## Setting up the Conda environment for pre/post-processing scripts

You can create a conda environment to install all the python libraries needed to run pre- and post-processing tools.

* `conda create --name baies`

* `conda activate baies`

* `conda install -c conda-forge mrcfile mdanalysis biopython`

   Make sure you are installing MDAnalysis version >= 2.0.0.

* In this environment, you also need to install `pytorch` using the instructions available [here](https://pytorch.org).
  Make sure you select a version compatible with the Cuda version installed on your machine or alternatively the CPU version.
  These instructions are for pytorch version 1.13.0 with Cuda 11.6:

  `conda install pytorch torchvision torchaudio pytorch-cuda=11.6 -c pytorch -c nvidia`


## PLUMED installation

### 1. Getting PLUMED

bAIes is currently implemented in the GitHub master branch of PLUMED, which you can obtain with:

`git clone https://github.com/plumed/plumed2.git`

or downloading the following zip archive:

`wget https://github.com/plumed/plumed2/archive/refs/heads/master.zip`

### 2. Configuring and compiling PLUMED
 
Please have a look [here](https://www.plumed.org/doc-master/user-doc/html/_i_s_d_b.html) for detailed instructions about compiling PLUMED with Libtorch support.
The main point is to enable Libtorch with:

`./configure --enable-libtorch`

## GROMACS installation

Detailed instructions about patching GROMACS with PLUMED, configuration and installation are available [here](https://www.plumed.org/doc-master/user-doc/html/_installation.html).

##### [Back to bAIes-SM home](NAVIGATION.md)
