#  PLUMED Installation: An interactive guide

There are a variety of different ways of getting your hands on PLUMED.  For example you can:

* Install it from [Conda](conda.md).  See [here](https://docs.conda.io/en/latest/miniconda.html) for more info on Conda.
* Install it from [MacPorts](macports.md).  See [here](https://www.macports.org) for more information on macports.
* Compile it yourself

If you just want to run the code on your local machine to do the exercises for the tutorials here we would recommend installing 
PLUMED from Conda. However, if you want to use PLUMED to do production calculations we would recommend compiling 
it yourself. 

If you are impatient the short version of the installation process is to use the following three commands:

```bash
./configure --enable-modules=all
make -j 4
make install
```

Notice that you can set the location to install plumed using the `--prefix` option when you call configure and that further details 
on these three commands is available on [this page](installation_old.md). Alternatively, [this page](Installation.md) presents the same information 
in a way that some people find easier to navigate. 

You will most likely want to use PLUMED in tandem with an MD code. For some MD codes we regularly test the interfaces between them and 
PLUMED.  We display the results obtained from these tests and the installation scripts that we use for thse tests 
[here](http://plumed-testcenter.github.io).  If you are using an MD code that doesn't appear on that website you can find the information
we have on using it in tandem with PLUMED from the following chart. 

```mermaid
flowchart TB;
  A[MD codes] ~~~ C1[Using with ABIN]
  A ~~~ C2[Using with AceMD]
  A ~~~ C3[Using with AmberTools]
  C1 ~~~ C4[Using with CP2K]
  C2 ~~~ C5[Using with DL_POLY4]
  C3 ~~~ C6[Using with ESPResSo]
  C4 ~~~ C7[Using with IPHIGENIE]
  C5 ~~~ C8[Using with LAMMPS]
  C6 ~~~ C9[Using with OpenMM]
  C7 ~~~ C10[Using with PINYMD]
  C8 ~~~ C11[Using with VNLATK]
  C9 ~~~ C12[Using with Yaff]
  C10 ~~~ C13[Using with ipi]
  C11 ~~~ C14[Using with gromacs]
  C12 ~~~ C15[Using with namd]
  C13 ~~~ C16[Using with qespresso]
  C14 ~~~ C17[Using with other]
  click C1 "https://github.com/PHOTOX/ABIN" "You can find the interface to PLUMED for this code <a href="
  click C2 "https://github.com/tonigi/ACEMD-PLUMED" "AceMD is a code authored by Toni Giorgino"
  click C3 "http://ambermd.org/" "PLUMED can be used with the sander module from version 15 onwards"
  click C4 "https://www.cp2k.org/howto:install_with_plumed" "PLUMED has been available in CP2K since Feb 2015"
  click C5 "ftp://ftp.dl.ac.uk/ccp5/DL_POLY/DL_POLY_4.0/DOCUMENTS/USRMAN4.pdf" "Information on how to use and install PLUMED with DLPOLY can be found in the manual."
  click C6 "http://davidebr.github.io/espresso/" "Plumed was inserted into ESPResSo by Davide Branduardi"
  click C7 "https://sourceforge.net/p/iphigenie/wiki/Compilation/" "IPhigenie is a fast and versatile MD program"
  click C8 "https://lammps.sandia.gov/doc/Build_extras.html#user-plumed-package" "There has been a native implementation of PLUMED in LAMMPS since Nov 2018.  Details on how to use PLUMED with LAMMPS is available <a href="
  click C9 "http://github.com/peastman/openmm-plumed" "To use openMM and PLUMED you need to download the openmp-plumed plugin."
  click C10 "https://github.com/TuckermanGroup/PINY/tree/plumed" "PINY is a code from the Tuckerman group.  You can use PLUMED with PINY if you download the plumed branch."
  click C11 "https://docs.quantumwise.com/tutorials/metadynamics_with_plumed/metadynamics_with_plumed.html" "VNL-ATK is an MD code from quantumwise"
  click C12 "https://github.com/molmod/yaff/blob/master/doc/ug_sampling.rst" "An interface to PLUMED has been available in Yaff since Jul 2019"
  click C13 "http://ipi-code.org/assets/pdf/manual.pdf" "IPi is a ring polymer molecular dynamics code (and more) from the group of Michele Ceriotti."
  click C14 "gromacs.html" "To use PLUMED with gromacs you need to patch the gromacs source code as described here"
  click C15 "namd.html" "To use PLUMED with namd you need to patch the namd source code as described here"
  click C16 "qespresso.html" "To use PLUMED with qespresso you need to patch the qespresso source code as described here"
  click C17 "https://www.plumed.org/doc-master/developer-doc/html/_how_to_plumed_your_m_d.html" "Instructions for linking your own code with PLUMED"
```

No actions were used in this tutorial so if you click on the link below (which is generated automatically) you will be taken to an empty 
version of the action list page of the PLUMED manual.
{% raw %}
<b><a href="https://www.plumed.org/doc-master/user-doc/html/actionlist/?actions=" target="_blank">Click here</a> to open manual pages for actions discussed in this tutorial.</b>
{% endraw %}
