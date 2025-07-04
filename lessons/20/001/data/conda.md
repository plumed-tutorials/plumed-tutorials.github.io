# Installing PLUMED with conda

If you use the conda package manager you can install a pre-compiled PLUMED binary using the following command:

```bash
conda install -c conda-forge plumed
```

Similarly, the python wrappers can be installed with

```bash
conda install -c conda-forge py-plumed
```

These packages are part of [conda-forge](https://anaconda.org/conda-forge) and as such should be binary compatible
with other codes from the same distribution. Notice that it should also be possible to combine the installed
plumed kernel with an MD code compiled outside of conda (or within a different conda environment)
if plumed is linked in runtime mode.
The only variable that you need to set in order to access to the installed plumed kernel is
`PLUMED_KERNEL` (e.g., `export PLUMED_KERNEL=/conda/prefix/lib/libplumedKernel.so`).

Notice that binaries are only available for Linux and MacOS and that they have a limited number of features.
In particular, they do not support MPI and do not include optional modules.
However, they can be used to quickly install a working PLUMED version without the need to have a compiler.

Notice that there are additional conda packages on the [plumed](https://anaconda.org/plumed/plumed) channel.
Those packages are for testing only.

## Masterclass 2022 

If you want to work through the tutorials on this site we recommend using conda. This section explains how you can insall
a version of PLUMED from conda that you can use to work through the tutorial exercises.
Unfortunately we can only provide precompiled conda packages for x64 architecture, Linux and MacOS.
This means that if you want to run the exercise on a different architecture (e.g., a new Mac with a ARM processor) you should install the software on your own.

First, make sure conda is installed by typing:
```
conda
```
If the command is not found, please refer to these [instructions to install conda on your machine](https://docs.conda.io/en/latest/miniconda.html).
Alternatively, if you use the [Homebrew package manager](https://brew.sh/), you can install conda with:
```
brew install --cask anaconda
# add this line to your .bashrc
export PATH="/usr/local/anaconda3/bin:$PATH"
```

Now we can create a conda environment for the PLUMED Masterclass:
```
conda create --name plumed-masterclass-2022
```

and activate it with:
```
conda activate plumed-masterclass-2022
```

Finally, we can proceed with the installation of the required software:
```
# install some basic analysis tool and the default plumed version
conda install -c conda-forge plumed py-plumed numpy pandas matplotlib notebook mdtraj mdanalysis git
```
If the Masterclass requires Gromacs, you can then run the following command:
```
# install plumed 2.8.0 and gromacs 2020.6 with MPI and all modules enabled
conda install --strict-channel-priority -c plumed/label/masterclass-2022 -c conda-forge plumed gromacs
```
If the Masterclass requires LAMMPS instead (for instance, Masterclass 22.12), the appropriate command is:
```
# install plumed 2.8.0 and lammps 23 Jun 2022 with MPI and all modules enabled
conda install --strict-channel-priority -c plumed/label/masterclass-2022 -c conda-forge plumed lammps
```
If the Masterclass requires AMBER (for instance, Masterclass 22.13), you should first create a separate AMBER environment:
```
# create a separate AMBER environment and install AMBER
conda create --name plumed-masterclass-2022-amber
conda activate plumed-masterclass-2022-amber
conda install -c conda-forge ambertools
```
And you should then stack the PLUMED and AMBER environments:
```
# stack the PLUMED and AMBER environments
conda activate plumed-masterclass-2022
conda activate --stack plumed-masterclass-2022-amber
export PLUMED_KERNEL=/your_path_here/plumed-masterclass-2022/lib/libplumedKernel.so
```

Conda will install a number of packages.
On MacOS, for instance, you should see something similar to this:
```
The following NEW packages will be INSTALLED:

  boost-cpp          conda-forge/osx-64::boost-cpp-1.79.0-h8b082ac_0
  gromacs            plumed/label/masterclass-2022/osx-64::gromacs-2020.6-h75233e6_1
  icu                conda-forge/osx-64::icu-70.1-h96cf925_0
  libhwloc           conda-forge/osx-64::libhwloc-1.11.13-hc10311c_0
  libxml2            conda-forge/osx-64::libxml2-2.9.14-h08a9926_0
  mpi                conda-forge/osx-64::mpi-1.0-openmpi
  openmpi            conda-forge/osx-64::openmpi-4.1.3-hd33e60e_103

The following packages will be SUPERSEDED by a higher-priority channel:

  plumed             conda-forge::plumed-2.8.0-nompi_h3651~ --> plumed/label/masterclass-2022::plumed-2.8.0-h75233e6_1
```
 Make sure that `gromacs` and `plumed` packages are installed from `plumed/label/masterclass-2022`.
 
 **Do not forget to activate the plumed-masterclass-2022 environment every time you open a new terminal/shell.**
 
 Notice that with some outdated conda version you might receive an error due to the fact that conda confuses python 3.1 with python 3.10.
 If you find an error like this one:
 ```
 PackagesNotFoundError: The following packages are not available from current channels:

  - python=3.1

 ```
 Make sure that you have at least conda 4.11.0 (or update conda with `conda update conda`).
 More at [this link](https://github.com/conda/conda/issues/11065)
