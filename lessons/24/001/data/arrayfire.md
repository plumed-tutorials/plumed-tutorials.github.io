# Installing PLUMED2 with ARRAYFIRE support
The purpose of this tutorial is to guide the user step-by-step through the process of compiling and installing PLUMED with ARRAYFIRE, an open-source library that supports a wide range of hardware accelerators for parallel computing.

In this specific scenario, the library is used to take advantage of CUDA-based GPUs to speed up the SAS calculation (ATOMISTIC / MARTINI / PARAMETERS / ONEBEAD representations). Furthermore, in order to show a real-life limit case, this installation example is performed on Leonardo, an HPC hosted by CINECA and managed by the SLURM scheduler.

To keep the working environment clean and compatible with other setups, in this guide the modules are not automatically loaded via .bashrc, .bash_aliases, or other configuration files, but are invoked during installation and then managed via the SLURM batch script used to submit jobs to the HPC.

## 1. Loading essential modules

To install ArrayFire, certain dependencies are required. Often, these dependencies are already available on HPC systems and can be loaded through modules. It is important to note that dependencies may also have their own dependencies, such as compilers or essential libraries. In general, to view the available modules on a SLURM-based HPC, you can use the command:
``` 
module avail
```
For a comprehensive list of requirements and additional installation suggestions, please visit the [official ARRAYFIRE GitHub page](https://github.com/arrayfire/arrayfire/wiki/Build-Instructions-for-Linux). Continuing with the Leonardo example, here is the list of basic modules that can be loaded directly from the shell:
``` 
module load profile/lifesc
module load gmp/6.2.1
module load mpfr/4.1.0
module load mpc/1.2.1
module load gcc/11.3.0
module load zlib/1.2.13--gcc--11.3.0
module load openmpi/4.1.4--gcc--11.3.0-cuda-11.8
module load openblas/0.3.21--gcc--11.3.0
module load cblas/2015-06-06--gcc--11.3.0
module load gsl/2.7.1--gcc--11.3.0
module load cuda/11.8
```
Other required modules are available from Leonardo, but for general purposes and to provide useful examples, the other dependencies will be installed manually in the next steps. It is assumed that the downloads are stored in the home folder.

## 2. Building dependencies from source
Let's start by creating a folder where all the codes will be installed:
``` 
mkdir $HOME/build
``` 
### FFTW
Download the "Fastest Fourier Transform in the West" package version 3.3.10:
``` 
wget https://www.fftw.org/fftw-3.3.10.tar.gz
``` 

Extract the archive:
``` 
tar -xzvf fftw-3.3.10.tar.gz
``` 
Copy the extracted folder to fftw-3.3.10_f and move into it:
```
cp -r fftw-3.3.10 fftw-3.3.10_f && cd fftw-3.3.10_f
```
The FFTW libraries must be built separately with single and double precision support. The next command configures the installation with 32-bit floating point support:
```
./configure --prefix=$HOME/build/fftw/ --enable-float --enable-shared CFLAGS="-march=native" --enable-avx2 --enable-sse2
```
Configuration details:
```
--prefix: Specifies the installation directory.
--enable-float: Enables single precision.
--enable-shared: Enables the compilation of shared libraries.
--enable-avx2 and --enable-sse2: Enable the use of AVX2 and SSE2 instructions respectively, which can improve the performance of operations on CPUs that support these instructions.
CFLAGS="-march=native": Sets compiler options to optimize the code for the specific architecture of the machine on which it is being compiled.
```
Compile and install the source code:
```
make && make install
```
In case of slowdowns, specify the number of processors to use, in this case 8:
```
make -j 8
```
Move to the fftw-3.3.10 folder and configure new instructions with the 64-bit floating point support:
```
cd ../fftw-3.3.10
./configure --prefix=$HOME/build/fftw/ --enable-shared CFLAGS="-march=native" --enable-avx2 --enable-sse2
```
Compile and install the source code:
```
make && make install
```
Set the LD_LIBRARY_PATH environment variable directly in the shell:
```
export LD_LIBRARY_PATH="$HOME/build/fftw/lib/:$LD_LIBRARY_PATH"
```
### Boost
Return to the download folder. Download the "Boost C++" libraries version 1.85.0:
``` 
wget https://boostorg.jfrog.io/artifactory/main/release/1.85.0/source/boost_1_85_0.tar.gz
```
Extract the archive:
```
tar -xzvf boost_1_85_0.tar.gz
```
Move into the boost folder:
```
cd boost_1_85_0
```
Initialise the Boost build system:
```
./bootstrap.sh
```
Install Boost libraries specifying the directory where Boost will be installed:
```
./b2 install --prefix=$HOME/build/boost
```
Add the Boost library path to the LD_LIBRARY_PATH and the include path to the PATH:
```
export PATH="$HOME/boost/include/:$PATH"
export LD_LIBRARY_PATH="$HOME/build/boost/lib/:$LD_LIBRARY_PATH"
```
### Spdlog
Return to the download folder. Clone and move into the spdlog repository:
```
git clone https://github.com/gabime/spdlog.git
cd spdlog
```
Checkout the specific version 1.9.2:
```
git checkout v1.9.2
```
Create build directory and navigate into it:
```
mkdir build && cd build
```
Run CMake to configure the build:
```
cmake .. -DCMAKE_INSTALL_PREFIX=$HOME/build/spdlog -DSPDLOG_BUILD_SHARED=ON
```
Compile and install the source code:
```
make && make install
```
Set the environment variables:
```
export PATH="$HOME/build/spdlog/include/:$PATH"
export LD_LIBRARY_PATH="$HOME/build/spdlog/lib64/:$LD_LIBRARY_PATH"
```
### Link to libcuda library
The next step can be tricky as it involves identifying a specific CUDA library on the cluster and linking it to your home directory. As the installation takes place on the login node, the CUDA drivers may not be directly available during code compilation. As an alternative, the stub library `libcuda.so` must be found on the HPC system. If the location is not clear, use the following command to find it:
```
find / -name libcuda.so 2>/dev/null
```
For Leonardo, the `libcuda.so` compatible with toolkit version 11.8 is located at:
```
/leonardo/prod/opt/compilers/cuda/11.8/none/lib64/stubs/libcuda.so
```
Create a folder in your home directory to link the library:
```
mkdir $HOME/libs && cd $HOME/libs
```
Link the library:
```
ln -s /leonardo/prod/opt/compilers/cuda/11.8/none/lib64/stubs/libcuda.so libcuda.so.1
```
Update the LD_LIBRARY_PATH environment variable:
```
export LD_LIBRARY_PATH="$HOME/libs/:$LD_LIBRARY_PATH"
```
## 3. Building and installing ArrayFire from source
Return to the download folder. Clone the ArrayFire repository:
```
git clone --recursive https://github.com/arrayfire/arrayfire.git
```
Move into the arrayfire directory and checkout the specific version (v3.9.0):
```
cd arrayfire
git checkout v3.9.0
```
Create a build directory and navigate into it:
```
mkdir build && cd build
```
Configure the build system with CMake:
```
cmake .. -DCMAKE_INSTALL_PREFIX=$HOME/build/arrayfire -DAF_BUILD_OPENCL=OFF -DAF_BUILD_CPU=OFF -DAF_BUILD_CUDA=ON -DAF_BUILD_FORGE=OFF -DFFTW_INCLUDE_DIR=$HOME/build/fftw/include -DFFTWF_LIBRARY=$HOME/build/fftw/lib/libfftw3f.so -DFFTW_LIBRARY=$HOME/build/fftw/lib/libfftw3.so -DBoost_DIR=$HOME/build/boost -DBoost_INCLUDE_DIR=$HOME/build/boost/include -DCUDA_TOOLKIT_ROOT_DIR=/leonardo/prod/opt/compilers/cuda/11.8/none -DNVPRUNE=/leonardo/prod/opt/compilers/cuda/11.8/none/bin/nvprune -Dspdlog_DIR=$HOME/build/spdlog/lib64/cmake/spdlog
```
Configuration details:
```
-DCMAKE_INSTALL_PREFIX=$HOME/build/arrayfire: Specifies the installation directory for ArrayFire.
-DAF_BUILD_OPENCL=OFF: Disables the OpenCL backend.
-DAF_BUILD_CPU=OFF: Disables the CPU backend.
-DAF_BUILD_CUDA=ON: Enables the CUDA backend.
-DAF_BUILD_FORGE=OFF: Disables the Forge library build.
-DFFTW_INCLUDE_DIR=$HOME/build/fftw/include: Specifies the directory containing the FFTW include files.
-DFFTWF_LIBRARY=$HOME/build/fftw/lib/libfftw3f.so: Specifies the single-precision FFTW library.
-DFFTW_LIBRARY=$HOME/build/fftw/lib/libfftw3.so: Specifies the double-precision FFTW library.
-DBoost_DIR=$HOME/build/boost: Specifies the directory containing Boost.
-DBoost_INCLUDE_DIR=$HOME/build/boost/include: Specifies the Boost include directory.
-DCUDA_TOOLKIT_ROOT_DIR=/leonardo/prod/opt/compilers/cuda/11.8/none: Specifies the CUDA toolkit root directory.
-DNVPRUNE=/leonardo/prod/opt/compilers/cuda/11.8/none/bin/nvprune: Specifies the path to the nvprune tool.
-Dspdlog_DIR=$HOME/build/spdlog/lib64/cmake/spdlog: Specifies the directory containing the spdlog CMake configuration files.
```
Build and install ArrayFire:
```
make && make install
```
Check that `libafcuda.so` is correctly built, all the required shared libraries must be resolved:
```
ldd $HOME/build/arrayfire/lib64/libafcuda.so
```
Update the LD_LIBRARY_PATH environment variable:
```
export LD_LIBRARY_PATH="$HOME/build/arrayfire/lib64/:$LD_LIBRARY_PATH"
```
## 4. Installing PLUMED2 with ArrayFire support
Clone the PLUMED repository:
```
git clone --recursive https://github.com/plumed/plumed2.git
```
Navigate to the PLUMED directory:
```
cd plumed2
```
Configure the build system:
```
./configure --prefix=$HOME/build/plumed CC=mpicc CXX=mpicxx --enable-modules=all --enable-asmjit --enable-fftw LDFLAGS="-L$HOME/build/arrayfire/lib64/ -Wl,-rpath,$HOME/build/arrayfire/lib64/ -L$HOME/build/fftw/lib/ -Wl,-rpath,$HOME/build/fftw/lib/" CPPFLAGS="-I$HOME/build/arrayfire/include -I$HOME/build/fftw/include" --enable-af_cuda --verbose
```
Configuration details:
```
CC=mpicc CXX=mpicxx: Specifies the MPI compilers to use.
--enable-modules=all: Enables all PLUMED modules.
--enable-asmjit: Enables the AsmJit library.
--enable-fftw: Enables FFTW support.
LDFLAGS: Specifies linker flags:
-L$HOME/build/arrayfire/lib64/: Adds the ArrayFire library directory to the linker search path.
-Wl,-rpath,$HOME/build/arrayfire/lib64/: Adds the ArrayFire library directory to the runtime library search path.
-L$HOME/build/fftw/lib/: Adds the FFTW library directory to the linker search path.
-Wl,-rpath,$HOME/build/fftw/lib/: Adds the FFTW library directory to the runtime library search path.
CPPFLAGS: Specifies preprocessor flags:
-I$HOME/build/arrayfire/include: Adds the ArrayFire include directory to the compiler search path.
-I$HOME/build/fftw/include: Adds the FFTW include directory to the compiler search path.
--enable-af_cuda: Enables ArrayFire CUDA support.
--verbose: Enables verbose output during the configuration process.
```
Build and install PLUMED:
```
make && make install
```
## 5. Logout & login
To prevent compatibility issues caused by exporting the stub library, completely logout of the HPC shell and perform a clean login. Avoiding this step could result in "CUDA device native identification" errors.

## 6. Write & run the SLURM batch script
Create a SLURM batch file, e.g. `RUN.sh`, using a text editor:
```
vim RUN.sh
```
Set the job configuration, the modules, the environment variables and run the PLUMED driver command:
```
#!/bin/bash

#SBATCH -A _PROJECT_
#SBATCH -p _PARTITION_
#SBATCH --time HH:MM:SS

#SBATCH --job-name=PLUMED_AF
#SBATCH -N 1                
#SBATCH --ntasks-per-node=1
#SBATCH --cpus-per-task=8  
#SBATCH --gres=gpu:1       
#SBATCH -o OUT.log

### MODULES ###
module load profile/lifesc
module load gmp/6.2.1
module load mpfr/4.1.0
module load mpc/1.2.1
module load gcc/11.3.0
module load zlib/1.2.13--gcc--11.3.0
module load openmpi/4.1.4--gcc--11.3.0-cuda-11.8
module load openblas/0.3.21--gcc--11.3.0
module load cblas/2015-06-06--gcc--11.3.0
module load gsl/2.7.1--gcc--11.3.0
module load cuda/11.8

### DEPENDENCIES ###
export LD_LIBRARY_PATH="$HOME/build/fftw/lib/:$LD_LIBRARY_PATH"
export PATH="$HOME/build/boost/include/:$PATH"
export LD_LIBRARY_PATH="$HOME/boost/lib/:$LD_LIBRARY_PATH"
export PATH="$HOME/build/spdlog/include/:$PATH"
export LD_LIBRARY_PATH="$HOME/build/spdlog/lib64/:$LD_LIBRARY_PATH"
export LD_LIBRARY_PATH="$HOME/build/arrayfire/lib64/:$LD_LIBRARY_PATH"

### PLUMED ###
export PATH="$HOME/build/plumed/bin:$PATH"
export LD_LIBRARY_PATH="$HOME/build/plumed/lib/:$LD_LIBRARY_PATH"
export PKG_CONFIG_PATH="$HOME/build/plumed/lib/pkgconfig/:$PKG_CONFIG_PATH"
export PLUMED_KERNEL="$HOME/build/plumed/lib/libplumedKernel.so"

export PLUMED_NUM_THREADS=$SLURM_CPUS_PER_TASK

### CMD ###
plumed driver --plumed plumed.dat --mf_xtc trj.xtc
```
In this example, the plumed command launches the driver to analyse the molecular dynamics trajectory `trj.xtc` according to the `plumed.dat` file. For the details regarding the `plumed.dat`instructions, refer to the Tutorial 1 of this guide.

Run the SLURM script file:
```
sbatch RUN.sh
```

## 7. Running GROMACS with PLUMED support
In addition to analysing a PDB or MD trajectory with the driver, it is possible to generate a conformational ensemble that agrees with SAS data using an MD engine. To enable this feature in GROMACS, it must be patched with the plumed-patch module and compiled with MPI support. Here is an example of a SLURM script that, after loading dependencies and environment variables, launches GROMACS with PLUMED support:

```
#!/bin/bash

#SBATCH -A _PROJECT_
#SBATCH -p _PARTITION_
#SBATCH --time HH:MM:SS

#SBATCH --job-name="hysas_metainference"
#SBATCH -o OUT.log

#SBATCH -N 1
#SBATCH --ntasks-per-node=4
#SBATCH --cpus-per-task=8
#SBATCH --gres=gpu:4
#SBATCH -o OUT.log

### MODULES ###
module load profile/lifesc
module load gmp/6.2.1
module load mpfr/4.1.0
module load mpc/1.2.1
module load gcc/11.3.0
module load zlib/1.2.13--gcc--11.3.0
module load openmpi/4.1.4--gcc--11.3.0-cuda-11.8
module load openblas/0.3.21--gcc--11.3.0
module load cblas/2015-06-06--gcc--11.3.0
module load gsl/2.7.1--gcc--11.3.0
module load cuda/11.8

### DEPENDENCIES ###
export LD_LIBRARY_PATH="$HOME/build/fftw/lib/:$LD_LIBRARY_PATH"
export PATH="$HOME/build/boost/include/:$PATH"
export LD_LIBRARY_PATH="$HOME/boost/lib/:$LD_LIBRARY_PATH"
export PATH="$HOME/build/spdlog/include/:$PATH"
export LD_LIBRARY_PATH="$HOME/build/spdlog/lib64/:$LD_LIBRARY_PATH"
export LD_LIBRARY_PATH="$HOME/build/arrayfire/lib64/:$LD_LIBRARY_PATH"

### PLUMED ###
export PATH="$HOME/build/plumed/bin:$PATH"
export LD_LIBRARY_PATH="$HOME/build/plumed/lib/:$LD_LIBRARY_PATH"
export PKG_CONFIG_PATH="$HOME/build/plumed/lib/pkgconfig/:$PKG_CONFIG_PATH"
export PLUMED_KERNEL="$HOME/build/plumed/lib/libplumedKernel.so"

### GROMACS ###
source $HOME/build/gmx24_mpi/bin/GMXRC

### EXPORT ###
export OMP_PROC_BIND=true
export OMP_NUM_THREADS=$SLURM_CPUS_PER_TASK

### CMD ###
MPIRUN=$(which mpirun)
MDRUN=$(which gmx_mpi)
NP=`expr $SLURM_JOB_NUM_NODES \* $SLURM_NTASKS_PER_NODE`

$MPIRUN -np $NP --map-by socket $MDRUN mdrun -v -deffnm replica -pin on -ntomp $SLURM_CPUS_PER_TASK -nsteps -1 -dlb yes -nb gpu -bonded gpu -pme gpu -plumed ../plumed.dat -multidir 0 1 2 3 -cpi replica.cpt -maxh 23.9
```

In this example a single node is dedicated to perform a multidir simulation of 4 replicas, one for each GPU.

## 8. Final notes
This guide was written and verified in June 2024, using the latest version of PLUMED available at that time. The names, paths, and versions of the modules can vary between HPC systems. Even for Leonardo, a software stack update might make this guide partially incompatible. However, all provided examples should offer a broad logic to customize and adapt the installation on local machines or other HPC systems.

##### [Back to hySAS home](NAVIGATION.md)
