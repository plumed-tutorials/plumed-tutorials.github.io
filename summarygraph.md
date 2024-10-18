
Browse the lessons
------------------------

The graph below shows a subset of the lessons that have been submitted to the PLUMED-TUTORIALS website and suggests an order for working through them. PLUMED-TUTORIAL monitors whether PLUMED input files in these lessons are compatible with the current and development versions of the code and integrates links from these files to the PLUMED manual.  Inputs in the tutorials listed below were last tested on {{ site.data.date.date }}.
   
You can return to a complete list of the tutorials by clicking [here](browse.md).

```mermaid
   
flowchart TD
0("Modelling mechanobiological
processes")
1("Mechanical pulling + FISST
module")
2("A Bayesian approach to
integrate cryo-EM data into MD
simulations with PLUMED")
3("PLUMED syntax and analysis")
4("Machine learning collective
variables with PyTorch")
5("Rethinking Metadynamics using
the OPES method")
6("Analysis of PLUMED output by
Metadynminer")
7("Metadynamics")
8("Umbrella Sampling")
9("Statistical errors in MD")
10("Installing PLUMED")
11("Using the maze module")
12("Transition-Tempered
Metadynamics")
13("Path integral metadynamics")
14("Free energy calculations in
crystalline solids")
15("Modelling Concentration-driven
processes with PLUMED")
16("Dimensionality reduction")
17("Replica exchange methods")
18("Multiple Walkers Metadynamics
Simulations with a Reactive
Machine Learning Interatomic
Potential")
19("Standard binding free energies
from cylindrical restraints")
20("Volume-based Metadynamics")
21("SASA module - The solvent
accessible surface area of
proteins as a collective
variable, and the application
of PLUMED for implicit solvent
simulations")
22("Hamiltonian replica exchange
with PLUMED and GROMACS")
23("EDS module and Coarse-Grained
directed simulations")
24("Optimizing PLUMED performances")
1-->0;
3-->1;
3-->2;
3-->9;
3-->11;
3-->15;
3-->16;
3-->23;
10-->3;
5-->4;
5-->14;
8-->7;
7-->5;
7-->6;
7-->12;
7-->13;
7-->17;
7-->18;
7-->19;
7-->20;
7-->21;
9-->8;
17-->24;
17-->22;
click 0 "lessons/24/010/data/NAVIGATION.html" "A tutorial on modelling mechanobiological processes [Authors: Claire Pritchard, Guillaume Stirnemann and Glen Hocky]"
click 1 "lessons/22/015/data/NAVIGATION.html" "This tutorial explains how mechanical forces can be modeled using PLUMED and the FISST module [Authors: Guillaume Stirnemann and Glen Hocky]"
click 2 "lessons/22/017/data/NAVIGATION.html" "How to use PLUMED to perform single-structure and ensemble refinement using cryo-EM maps and EMMIVox. [Authors: Samuel Hoff and Max Bonomi]"
click 3 "lessons/21/001/data/NAVIGATION.html" "Basic features of the PLUMED input syntax with a particular focus on PBCs and selection tools [Authors: Max Bonomi]"
click 4 "lessons/22/005/data/NAVIGATION.html" "An introduction to designing data-driven CVs using two methods (DeepLDA and DeepTICA). [Authors: Luigi Bonati]"
click 5 "lessons/22/003/data/NAVIGATION.html" "An introduction to the On-the-fly Probability Enhanced Sampling method [Authors: Michele Invernizzi]"
click 6 "lessons/22/002/data/NAVIGATION.html" "An introduction to the R package Metadynminer which can be used to analyse the output from metadynamics simulations [Authors: Vojtech Spiwok]"
click 7 "lessons/21/004/data/NAVIGATION.html" "How to calculate statistical averages and free energy surfaces using metadynamics [Authors: Max Bonomi]"
click 8 "lessons/21/003/data/NAVIGATION.html" "How to calculate statistical averages and free energy surfaces using umbrella sampling [Authors: Giovanni Bussi]"
click 9 "lessons/21/002/data/NAVIGATION.html" "How to calculate errors on averages calculated from unbiased and biased MD simulations using the method of block averages. [Authors: Gareth Tribello]"
click 10 "lessons/20/001/data/NAVIGATION.html" "An interactive tutorial resource on compiling PLUMED and linking it with MD codes. [Authors: Gareth Tribello]"
click 11 "lessons/24/008/data/NAVIGATION.html" "Sampling ligand-protein dissociation using the maze module [Authors: Jakub Rydzewski]"
click 12 "lessons/24/007/data/NAVIGATION.html" "An introduction to the transition tempered metadynamics method [Authors: Jiangbo Wu and Gregory A. Voth]"
click 13 "lessons/24/005/data/NAVIGATION.html" "Incorporating nuclear quantum effects in metadynamics simulations using path integrals [Authors: Michele Ceriotti]"
click 14 "lessons/22/012/data/NAVIGATION.html" "An introduction to the Environmental similarity CV and the calculation of chemical potentials of liquids and solids [Authors: Pablo Piaggi]"
click 15 "lessons/22/008/data/NAVIGATION.html" "An introduction to the tools that are available in PLUMED for simulating concentration-driven processes such as nucleation, growth and diffusion. [Authors: Matteo Salvalaglio]"
click 16 "lessons/21/006/data/NAVIGATION.html" "An introduction to techniques such as dimensionality reduction, path collective variables, and indistinguishability that you may need to use in your own research projects. [Authors: Gareth Tribello]"
click 17 "lessons/21/005/data/NAVIGATION.html" "Running umbrella sampling with replica exchange, bias exchange metadynamics and parallel tempering metadynamics [Authors: Giovanni Bussi]"
click 18 "lessons/24/009/data/NAVIGATION.html" "Running metadynamics with a reactive, machine-learning interaction potential [Authors: Kam-Tung Chan and Davide Donadio]"
click 19 "lessons/24/006/data/NAVIGATION.html" "Calculating standard binding free energies with metadynamics, PLUMED and OpenMM [Authors: Blake I Armstrong, Paolo Raiteri and Julian D Gale]"
click 20 "lessons/24/004/data/NAVIGATION.html" "This tutorial teaches you how to run free energy calculations to investigate protein-ligand binding [Authors: Riccardo Capelli]"
click 21 "lessons/22/013/data/NAVIGATION.html" "An introduction to the SASA module and a description of how PLUMED can be used for implicit solvent simulations. [Authors: Andrea Arsiccio]"
click 22 "lessons/22/010/data/NAVIGATION.html" "An introduction to running Hamiltonian replica exchange calculations using PLUMED and GROMACS. [Authors: Giovanni Bussi]"
click 23 "lessons/22/006/data/NAVIGATION.html" "This tutorials describes how to bias simulations to agree with experimental data using experiment directed simulation. [Authors: Glen Hocky and Andrew White]"
click 24 "lessons/21/007/data/NAVIGATION.html" "Some lessons on monitoring and improving the performance of PLUMED and gromacs [Authors: Max Bonomi]"
```
