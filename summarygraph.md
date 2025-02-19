
Browse the lessons
------------------------

The graph below shows a subset of the lessons that have been submitted to the PLUMED-TUTORIALS website and suggests an order for working through them. PLUMED-TUTORIAL monitors whether PLUMED input files in these lessons are compatible with the current and development versions of the code and integrates links from these files to the PLUMED manual.  Inputs in the tutorials listed below were last tested on {{ site.data.date.date }}.
   
You can return to a complete list of the tutorials by clicking [here](browse.md).

```mermaid
%%{init: {"flowchart": {"defaultRenderer": "elk"}} }%%
   
flowchart TD
0("An introduction to CpH-
Metadynamics simulations")
1("Metadynamics")
2("ASE-PLUMED interface")
3("PLUMED syntax and analysis")
4("Enhanced sampling for
magnesium-RNA binding dynamics")
5("Permutationally Invariant
Networks for Enhanced Sampling
(PINES)")
6("Multiple Walkers Metadynamics
Simulations with a Reactive
Machine Learning Interatomic
Potential")
7("Statistical errors in MD")
8("Using the maze module")
9("Standard binding free energies
from cylindrical restraints")
10("Path integral metadynamics")
11("SASA module - The solvent
accessible surface area of
proteins as a collective
variable, and the application
of PLUMED for implicit solvent
simulations")
12("Hamiltonian replica exchange
with PLUMED and GROMACS")
13("Replica exchange methods")
14("EDS module and Coarse-Grained
directed simulations")
15("Rethinking Metadynamics using
the OPES method")
16("Umbrella Sampling")
17("Installing PLUMED")
18("VisMetaDynamics")
19("Alpha-Fold Metainference for
structural ensemble prediction
of a partially disordered
protein")
20("Exploring Free Energy Surfaces
with MACE-PLUMED Metadynamics")
21("Parameterization of Path CVs
for drug-target binding")
22("A Bayesian approach to
integrate cryo-EM data into MD
simulations with PLUMED")
23("Free energy calculations in
crystalline solids")
24("Using path collective
variables to find reaction
mechanisms in complex free
energy landscapes")
25("Machine learning collective
variables with PyTorch")
26("Analysis of PLUMED output by
Metadynminer")
27("Optimizing PLUMED performances")
28("Dimensionality reduction")
29("Setting Up and Analyzing Bias-
Exchange Metadynamics
Simulations")
30("Modelling mechanobiological
processes")
31("Mechanical pulling + FISST
module")
32("Transition-Tempered
Metadynamics")
33("Volume-based Metadynamics")
34("Modelling Concentration-driven
processes with PLUMED")
subgraph g0 [ ]
0("An introduction to CpH-
Metadynamics simulations")
32("Transition-Tempered
Metadynamics")
33("Volume-based Metadynamics")
4("Enhanced sampling for
magnesium-RNA binding dynamics")
5("Permutationally Invariant
Networks for Enhanced Sampling
(PINES)")
6("Multiple Walkers Metadynamics
Simulations with a Reactive
Machine Learning Interatomic
Potential")
0~~~6;
9("Standard binding free energies
from cylindrical restraints")
32~~~9;
10("Path integral metadynamics")
33~~~10;
11("SASA module - The solvent
accessible surface area of
proteins as a collective
variable, and the application
of PLUMED for implicit solvent
simulations")
4~~~11;
13("Replica exchange methods")
5~~~13;
15("Rethinking Metadynamics using
the OPES method")
6~~~15;
18("VisMetaDynamics")
9~~~18;
20("Exploring Free Energy Surfaces
with MACE-PLUMED Metadynamics")
10~~~20;
21("Parameterization of Path CVs
for drug-target binding")
11~~~21;
26("Analysis of PLUMED output by
Metadynminer")
13~~~26;
end
1("Metadynamics")
1--> g0;
subgraph g2 [ ]
2("ASE-PLUMED interface")
34("Modelling Concentration-driven
processes with PLUMED")
7("Statistical errors in MD")
8("Using the maze module")
14("EDS module and Coarse-Grained
directed simulations")
19("Alpha-Fold Metainference for
structural ensemble prediction
of a partially disordered
protein")
2~~~19;
22("A Bayesian approach to
integrate cryo-EM data into MD
simulations with PLUMED")
34~~~22;
24("Using path collective
variables to find reaction
mechanisms in complex free
energy landscapes")
7~~~24;
28("Dimensionality reduction")
8~~~28;
29("Setting Up and Analyzing Bias-
Exchange Metadynamics
Simulations")
14~~~29;
31("Mechanical pulling + FISST
module")
19~~~31;
end
3("PLUMED syntax and analysis")
3--> g2;
7-->16;
12("Hamiltonian replica exchange
with PLUMED and GROMACS")
13-->12;
13-->27;
15-->23;
15-->25;
16("Umbrella Sampling")
16-->1;
17("Installing PLUMED")
17-->3;
23("Free energy calculations in
crystalline solids")
25("Machine learning collective
variables with PyTorch")
27("Optimizing PLUMED performances")
30("Modelling mechanobiological
processes")
31-->30;
click 0 "lessons/24/020/data/NAVIGATION.html" "This tutorial aims to train users to perform CpH-Metadynamics simulations using the stochastic titration constant-pH Molecular Dynamics method and PLUMED. [Authors: Tomas Silva]"
click 1 "lessons/21/004/data/NAVIGATION.html" "How to calculate statistical averages and free energy surfaces using metadynamics [Authors: Max Bonomi]"
click 2 "lessons/24/019/data/NAVIGATION.html" "Using PLUMED from ASE [Authors: Daniel Sucerquia, Pilar Cossio, Olga Lopez-Acevedo]"
click 3 "lessons/21/001/data/NAVIGATION.html" "Basic features of the PLUMED input syntax with a particular focus on PBCs and selection tools [Authors: Max Bonomi]"
click 4 "lessons/24/017/data/NAVIGATION.html" "This tutorial will teach you how to use PLUMED, GROMACS and Python notebooks to implement an enhanced sampling strategy for magnesium-RNA binding dynamics. [Authors: Olivier Languin Cattoen]"
click 5 "lessons/24/013/data/NAVIGATION.html" "An introduction to using permutationally invariant networks for enhanced sampling [Authors: Nicholas S.M. Herringer, Aniruddha Seal, Armin Shayesteh Zadeh, Siva Dasetty, Andrew L. Ferguson]"
click 6 "lessons/24/009/data/NAVIGATION.html" "Running metadynamics with a reactive, machine-learning interaction potential [Authors: Kam-Tung Chan and Davide Donadio]"
click 7 "lessons/21/002/data/NAVIGATION.html" "How to calculate errors on averages calculated from unbiased and biased MD simulations using the method of block averages. [Authors: Gareth Tribello]"
click 8 "lessons/24/008/data/NAVIGATION.html" "Sampling ligand-protein dissociation using the maze module [Authors: Jakub Rydzewski]"
click 9 "lessons/24/006/data/NAVIGATION.html" "Calculating standard binding free energies with metadynamics, PLUMED and OpenMM [Authors: Blake I Armstrong, Paolo Raiteri and Julian D Gale]"
click 10 "lessons/24/005/data/NAVIGATION.html" "Incorporating nuclear quantum effects in metadynamics simulations using path integrals [Authors: Guillaume Fraux and Michele Ceriotti]"
click 11 "lessons/22/013/data/NAVIGATION.html" "An introduction to the SASA module and a description of how PLUMED can be used for implicit solvent simulations. [Authors: Andrea Arsiccio]"
click 12 "lessons/22/010/data/NAVIGATION.html" "An introduction to running Hamiltonian replica exchange calculations using PLUMED and GROMACS. [Authors: Giovanni Bussi]"
click 13 "lessons/21/005/data/NAVIGATION.html" "Running umbrella sampling with replica exchange, bias exchange metadynamics and parallel tempering metadynamics [Authors: Giovanni Bussi]"
click 14 "lessons/22/006/data/NAVIGATION.html" "This tutorials describes how to bias simulations to agree with experimental data using experiment directed simulation. [Authors: Glen Hocky and Andrew White]"
click 15 "lessons/22/003/data/NAVIGATION.html" "An introduction to the On-the-fly Probability Enhanced Sampling method [Authors: Michele Invernizzi]"
click 16 "lessons/21/003/data/NAVIGATION.html" "How to calculate statistical averages and free energy surfaces using umbrella sampling [Authors: Giovanni Bussi]"
click 17 "lessons/20/001/data/NAVIGATION.html" "An interactive tutorial resource on compiling PLUMED and linking it with MD codes. [Authors: Gareth Tribello]"
click 18 "lessons/25/001/data/NAVIGATION.html" "A graphical tool that allows you to visually inspect how the free energy surface for a metadynamics simulation is affected by the choice of hyperparameters [Authors: Christian Phillips]"
click 19 "lessons/24/014/data/NAVIGATION.html" "A tutorial about how metainference can be used in tandem with Alpha-fold to predict the ensemble of structures for a partially disordered protein. [Authors: Faidon Brotzakis, Hussein Murtada and Michele Vendruscolo]"
click 20 "lessons/24/012/data/NAVIGATION.html" "Performing metadynamics simulations with LAMMPS, MACE and PLUMED [Authors: S.G.H. Brookes, C. Schran, A. Michaelides]"
click 21 "lessons/24/011/data/NAVIGATION.html" "Using path CVs to study drug target binding with metadynamics [Authors: Mattia Bernetti and Matteo Masetti]"
click 22 "lessons/22/017/data/NAVIGATION.html" "How to use PLUMED to perform single-structure and ensemble refinement using cryo-EM maps and EMMIVox. [Authors: Samuel Hoff and Max Bonomi]"
click 23 "lessons/22/012/data/NAVIGATION.html" "An introduction to the Environmental similarity CV and the calculation of chemical potentials of liquids and solids [Authors: Pablo Piaggi]"
click 24 "lessons/22/009/data/NAVIGATION.html" "An introduction to using path collective variables for describing and simulating activated molecular processes [Authors: Bernd Ensing]"
click 25 "lessons/22/005/data/NAVIGATION.html" "An introduction to designing data-driven CVs using two methods (DeepLDA and DeepTICA). [Authors: Luigi Bonati]"
click 26 "lessons/22/002/data/NAVIGATION.html" "An introduction to the R package Metadynminer which can be used to analyse the output from metadynamics simulations [Authors: Vojtech Spiwok]"
click 27 "lessons/21/007/data/NAVIGATION.html" "Some lessons on monitoring and improving the performance of PLUMED and gromacs [Authors: Max Bonomi]"
click 28 "lessons/21/006/data/NAVIGATION.html" "An introduction to techniques such as dimensionality reduction, path collective variables, and indistinguishability that you may need to use in your own research projects. [Authors: Gareth Tribello]"
click 29 "lessons/24/021/data/NAVIGATION.html" "This tutorial offers a comprehensive protocol, complemented by practical examples, for setting up and performing free energy analysis of bias-exchange metadynamics simulations of cis-trans isomerization in a proline-containing peptide. [Authors: Fabrizio Marinelli and Vanessa Ariadna Leone Alvarez]"
click 30 "lessons/24/010/data/NAVIGATION.html" "A tutorial on modelling mechanobiological processes [Authors: Claire Pritchard, Guillaume Stirnemann and Glen Hocky]"
click 31 "lessons/22/015/data/NAVIGATION.html" "This tutorial explains how mechanical forces can be modeled using PLUMED and the FISST module [Authors: Guillaume Stirnemann and Glen Hocky]"
click 32 "lessons/24/007/data/NAVIGATION.html" "An introduction to the transition tempered metadynamics method [Authors: Jiangbo Wu and Gregory A. Voth]"
click 33 "lessons/24/004/data/NAVIGATION.html" "This tutorial teaches you how to run free energy calculations to investigate protein-ligand binding [Authors: Riccardo Capelli]"
click 34 "lessons/22/008/data/NAVIGATION.html" "An introduction to the tools that are available in PLUMED for simulating concentration-driven processes such as nucleation, growth and diffusion. [Authors: Matteo Salvalaglio]"
```
