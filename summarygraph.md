
Browse the lessons
------------------------

The graph below shows a subset of the lessons that have been submitted to the PLUMED-TUTORIALS website and suggests an order for working through them. PLUMED-TUTORIAL monitors whether PLUMED input files in these lessons are compatible with the current and development versions of the code and integrates links from these files to the PLUMED manual.  Inputs in the tutorials listed below were last tested on {{ site.data.date.date }}.
   
You can return to a complete list of the tutorials by clicking [here](browse.md).

```mermaid
%%{init: {"flowchart": {"defaultRenderer": "elk"}} }%%
   
flowchart TD
0("VisMetaDynamics")
1("Metadynamics")
2("An introduction to CpH-
Metadynamics simulations")
3("Parameterization of Path CVs
for drug-target binding")
4("PLUMED syntax and analysis")
5("Multiple Walkers Metadynamics
Simulations with a Reactive
Machine Learning Interatomic
Potential")
6("Statistical errors in MD")
7("Transition-Tempered
Metadynamics")
8("Standard binding free energies
from cylindrical restraints")
9("Volume-based Metadynamics")
10("A Bayesian approach to
integrate cryo-EM data into MD
simulations with PLUMED")
11("Mechanical pulling + FISST
module")
12("Free energy calculations in
crystalline solids")
13("Rethinking Metadynamics using
the OPES method")
14("Modelling Concentration-driven
processes with PLUMED")
15("Permutationally Invariant
Networks for Enhanced Sampling
(PINES)")
16("Using the maze module")
17("Replica exchange methods")
18("Umbrella Sampling")
19("Defining custom machine
learning CV with metatomic")
20("Alpha-Fold Metainference for
structural ensemble prediction
of a partially disordered
protein")
21("Path integral metadynamics")
22("SASA module - The solvent
accessible surface area of
proteins as a collective
variable, and the application
of PLUMED for implicit solvent
simulations")
23("Hamiltonian replica exchange
with PLUMED and GROMACS")
24("Using path collective
variables to find reaction
mechanisms in complex free
energy landscapes")
25("Analysis of PLUMED output by
Metadynminer")
26("Dimensionality reduction")
27("Refining AlphaFold models for
virtual screening")
28("Setting Up and Analyzing Bias-
Exchange Metadynamics
Simulations")
29("ASE-PLUMED interface")
30("Enhanced sampling for
magnesium-RNA binding dynamics")
31("Exploring Free Energy Surfaces
with MACE-PLUMED Metadynamics")
32("Modelling mechanobiological
processes")
33("EDS module and Coarse-Grained
directed simulations")
34("Machine learning collective
variables with PyTorch")
35("Optimizing PLUMED performances")
36("Installing PLUMED")
subgraph g0 [ ]
0("VisMetaDynamics")
2("An introduction to CpH-
Metadynamics simulations")
3("Parameterization of Path CVs
for drug-target binding")
5("Multiple Walkers Metadynamics
Simulations with a Reactive
Machine Learning Interatomic
Potential")
7("Transition-Tempered
Metadynamics")
8("Standard binding free energies
from cylindrical restraints")
0~~~8;
9("Volume-based Metadynamics")
2~~~9;
13("Rethinking Metadynamics using
the OPES method")
3~~~13;
15("Permutationally Invariant
Networks for Enhanced Sampling
(PINES)")
5~~~15;
17("Replica exchange methods")
7~~~17;
19("Defining custom machine
learning CV with metatomic")
8~~~19;
21("Path integral metadynamics")
9~~~21;
22("SASA module - The solvent
accessible surface area of
proteins as a collective
variable, and the application
of PLUMED for implicit solvent
simulations")
13~~~22;
25("Analysis of PLUMED output by
Metadynminer")
15~~~25;
30("Enhanced sampling for
magnesium-RNA binding dynamics")
17~~~30;
31("Exploring Free Energy Surfaces
with MACE-PLUMED Metadynamics")
19~~~31;
end
1("Metadynamics")
1--> g0;
subgraph g6 [ ]
33("EDS module and Coarse-Grained
directed simulations")
6("Statistical errors in MD")
10("A Bayesian approach to
integrate cryo-EM data into MD
simulations with PLUMED")
11("Mechanical pulling + FISST
module")
14("Modelling Concentration-driven
processes with PLUMED")
16("Using the maze module")
33~~~16;
20("Alpha-Fold Metainference for
structural ensemble prediction
of a partially disordered
protein")
6~~~20;
24("Using path collective
variables to find reaction
mechanisms in complex free
energy landscapes")
10~~~24;
26("Dimensionality reduction")
11~~~26;
27("Refining AlphaFold models for
virtual screening")
14~~~27;
28("Setting Up and Analyzing Bias-
Exchange Metadynamics
Simulations")
16~~~28;
29("ASE-PLUMED interface")
20~~~29;
end
4("PLUMED syntax and analysis")
4--> g6;
6-->18;
11-->32;
12("Free energy calculations in
crystalline solids")
13-->12;
13-->34;
17-->23;
17-->35;
18("Umbrella Sampling")
18-->1;
23("Hamiltonian replica exchange
with PLUMED and GROMACS")
32("Modelling mechanobiological
processes")
34("Machine learning collective
variables with PyTorch")
35("Optimizing PLUMED performances")
36("Installing PLUMED")
36-->4;
click 0 "lessons/25/001/data/NAVIGATION.html" "A graphical tool that allows you to visually inspect how the free energy surface for a metadynamics simulation is affected by the choice of hyperparameters [Authors: Christian Phillips]"
click 1 "lessons/21/004/data/NAVIGATION.html" "How to calculate statistical averages and free energy surfaces using metadynamics [Authors: Max Bonomi]"
click 2 "lessons/24/020/data/NAVIGATION.html" "This tutorial aims to train users to perform CpH-Metadynamics simulations using the stochastic titration constant-pH Molecular Dynamics method and PLUMED. [Authors: Tomas Silva]"
click 3 "lessons/24/011/data/NAVIGATION.html" "Using path CVs to study drug target binding with metadynamics [Authors: Mattia Bernetti and Matteo Masetti]"
click 4 "lessons/21/001/data/NAVIGATION.html" "Basic features of the PLUMED input syntax with a particular focus on PBCs and selection tools [Authors: Max Bonomi]"
click 5 "lessons/24/009/data/NAVIGATION.html" "Running metadynamics with a reactive, machine-learning interaction potential [Authors: Kam-Tung Chan and Davide Donadio]"
click 6 "lessons/21/002/data/NAVIGATION.html" "How to calculate errors on averages calculated from unbiased and biased MD simulations using the method of block averages. [Authors: Gareth Tribello]"
click 7 "lessons/24/007/data/NAVIGATION.html" "An introduction to the transition tempered metadynamics method [Authors: Jiangbo Wu and Gregory A. Voth]"
click 8 "lessons/24/006/data/NAVIGATION.html" "Calculating standard binding free energies with metadynamics, PLUMED and OpenMM [Authors: Blake I Armstrong, Paolo Raiteri and Julian D Gale]"
click 9 "lessons/24/004/data/NAVIGATION.html" "This tutorial teaches you how to run free energy calculations to investigate protein-ligand binding [Authors: Riccardo Capelli]"
click 10 "lessons/22/017/data/NAVIGATION.html" "How to use PLUMED to perform single-structure and ensemble refinement using cryo-EM maps and EMMIVox. [Authors: Samuel Hoff and Max Bonomi]"
click 11 "lessons/22/015/data/NAVIGATION.html" "This tutorial explains how mechanical forces can be modeled using PLUMED and the FISST module [Authors: Guillaume Stirnemann and Glen Hocky]"
click 12 "lessons/22/012/data/NAVIGATION.html" "An introduction to the Environmental similarity CV and the calculation of chemical potentials of liquids and solids [Authors: Pablo Piaggi]"
click 13 "lessons/22/003/data/NAVIGATION.html" "An introduction to the On-the-fly Probability Enhanced Sampling method [Authors: Michele Invernizzi]"
click 14 "lessons/22/008/data/NAVIGATION.html" "An introduction to the tools that are available in PLUMED for simulating concentration-driven processes such as nucleation, growth and diffusion. [Authors: Matteo Salvalaglio]"
click 15 "lessons/24/013/data/NAVIGATION.html" "An introduction to using permutationally invariant networks for enhanced sampling [Authors: Nicholas S.M. Herringer, Aniruddha Seal, Armin Shayesteh Zadeh, Siva Dasetty, Andrew L. Ferguson]"
click 16 "lessons/24/008/data/NAVIGATION.html" "Sampling ligand-protein dissociation using the maze module [Authors: Jakub Rydzewski]"
click 17 "lessons/21/005/data/NAVIGATION.html" "Running umbrella sampling with replica exchange, bias exchange metadynamics and parallel tempering metadynamics [Authors: Giovanni Bussi]"
click 18 "lessons/21/003/data/NAVIGATION.html" "How to calculate statistical averages and free energy surfaces using umbrella sampling [Authors: Giovanni Bussi]"
click 19 "lessons/25/003/data/NAVIGATION.html" "An introduction to the use of interface between plumed and the metatomic library [Authors: Guillaume Fraux, Rohit Goswami and Michele Ceriotti]"
click 20 "lessons/24/014/data/NAVIGATION.html" "A tutorial about how metainference can be used in tandem with Alpha-fold to predict the ensemble of structures for a partially disordered protein. [Authors: Faidon Brotzakis, Hussein Murtada and Michele Vendruscolo]"
click 21 "lessons/24/005/data/NAVIGATION.html" "Incorporating nuclear quantum effects in metadynamics simulations using path integrals [Authors: Guillaume Fraux and Michele Ceriotti]"
click 22 "lessons/22/013/data/NAVIGATION.html" "An introduction to the SASA module and a description of how PLUMED can be used for implicit solvent simulations. [Authors: Andrea Arsiccio]"
click 23 "lessons/22/010/data/NAVIGATION.html" "An introduction to running Hamiltonian replica exchange calculations using PLUMED and GROMACS. [Authors: Giovanni Bussi]"
click 24 "lessons/22/009/data/NAVIGATION.html" "An introduction to using path collective variables for describing and simulating activated molecular processes [Authors: Bernd Ensing]"
click 25 "lessons/22/002/data/NAVIGATION.html" "An introduction to the R package Metadynminer which can be used to analyse the output from metadynamics simulations [Authors: Vojtech Spiwok]"
click 26 "lessons/21/006/data/NAVIGATION.html" "An introduction to techniques such as dimensionality reduction, path collective variables, and indistinguishability that you may need to use in your own research projects. [Authors: Gareth Tribello]"
click 27 "lessons/25/002/data/NAVIGATION.html" "A tutorial to use bAIes to refine AlphaFold models for small-molecule virtual screening [Authors: Samiran Sen]"
click 28 "lessons/24/021/data/NAVIGATION.html" "This tutorial offers a comprehensive protocol, complemented by practical examples, for setting up and performing free energy analysis of bias-exchange metadynamics simulations of cis-trans isomerization in a proline-containing peptide. [Authors: Fabrizio Marinelli and Vanessa Ariadna Leone Alvarez]"
click 29 "lessons/24/019/data/NAVIGATION.html" "Using PLUMED from ASE [Authors: Daniel Sucerquia, Pilar Cossio, Olga Lopez-Acevedo]"
click 30 "lessons/24/017/data/NAVIGATION.html" "This tutorial will teach you how to use PLUMED, GROMACS and Python notebooks to implement an enhanced sampling strategy for magnesium-RNA binding dynamics. [Authors: Olivier Languin Cattoen]"
click 31 "lessons/24/012/data/NAVIGATION.html" "Performing metadynamics simulations with LAMMPS, MACE and PLUMED [Authors: S.G.H. Brookes, C. Schran, A. Michaelides]"
click 32 "lessons/24/010/data/NAVIGATION.html" "A tutorial on modelling mechanobiological processes [Authors: Claire Pritchard, Guillaume Stirnemann and Glen Hocky]"
click 33 "lessons/22/006/data/NAVIGATION.html" "This tutorials describes how to bias simulations to agree with experimental data using experiment directed simulation. [Authors: Glen Hocky and Andrew White]"
click 34 "lessons/22/005/data/NAVIGATION.html" "An introduction to designing data-driven CVs using two methods (DeepLDA and DeepTICA). [Authors: Luigi Bonati]"
click 35 "lessons/21/007/data/NAVIGATION.html" "Some lessons on monitoring and improving the performance of PLUMED and gromacs [Authors: Max Bonomi]"
click 36 "lessons/20/001/data/NAVIGATION.html" "An interactive tutorial resource on compiling PLUMED and linking it with MD codes. [Authors: Gareth Tribello]"
```
