# Revising PLUMED 

After the Trieste meeting in 2017, I (Gareth Tribello) started revising some of the code in PLUMED in a separate branch called hack-the-tree.
The code in this new branch quickly diverged from the code in the master branch. This divergence, I now realise, was a good thing. The extensive
code base for a piece of scientific software places innumerable constraints on its development. Sometimes it helps to free yourself of these
constraints and to allow yourself to "break" some things. I think this process has allowed me to improve how some of the CVs
and methods I have written for PLUMED are implemented.

I think it is now time to merge some of these features from the hack-the-tree branch back into the master branch of PLUMED. I decided to write these pages as
I made the code from hack-the-tree amenable to the rest of the code. I hope they explain my thinking and help others use the
new features I have implemented. I also hope they inspire discussions about how we approach code development for a particular research community.
When I started this process I identified the following three themes that have driven a lot of my thinking over the last three years:

* [Passing data between actions](Passing.md) 
* [Reproducibility and extensibility](Reproducibility.md)
* [Hierachy and community](Community.md)

A lot of the posts in the pages that follow expand on these three ideas.


```mermaid
flowchart TB;
  A[Passing data] -.-> B[Reproducibility];
  B -.-> C[Hierachy];
  C -.-> D[Passing data to and from PLUMED I];
  D --> E[Passing data to and from PLUMED II];
  A --> D;
  E --> F[Passing the energy];
  A --> G[Virtual atoms]
  B --> H[Graphs]
  A --> I[multi colvar]
  H --> I
  I --> J[multi colvar shortcuts]
  B --> J
  C --> J
  J --> K[contact matrices]
  I --> K
  K --> L[the task list]
  I --> L
  B --> M[Sprint]
  K --> M
  K --> T[Clusters]
  L --> Q[Symmetry functions]
  Q --> N[Steinhardt parameters]
  Q --> O[Behler Symmetry functions]
  Q --> P[Volumes]
  B --> R[Averaging]
  R --> S[Histograms]
  D --> U[RMSD]
  U --> V[Paths]
  K --> V
  click A "Passing.html" "8th May 2023: General thoughts about how data is passed between PLUMED actions"
  click B "Reproducibility.html" "8th May 2023: General thoughts about why we want to do calculations that are reproducibile"
  click C "Community.html" "8th May 2023: General thoughts about how we support communities of scholars"
  click D "MDInterfaceI.html" "8th May 2023: A description of how data is passed to and from PLUMED"
  click E "MDInterfaceII.html" "21st May 2023: A description of how atomic properties are passed to and from PLUMED"
  click F "PassingEnergy.html" "21st May 2023: A description of how potential energy is passed to PLUMED"
  click G "VirtualAtoms.html" "22nd May 2023: A description of how virtual atom positions are passed between Actions in PLUMED"
  click H "Graphs.html" "1st June 2023: A description of the way we can use graphs to illustrate PLUMED input files"
  click I "MultiColvar.html" "1st June 2023: An explaination of how multicolvar is implemented"
  click J "MultiColvarShortcut.html" "9th June 2023: An explanation of how backwards compatibility for MultiColvar has been ensured and an introduction to ActionShortcut"
  click K "contactMatrix.html" "12th June 2023: An explanation of how coordination numbers and contact maps can be used to construct CVs"
  click L "Tasks.html" "13th June 2023: More details on how the task list are used in the calculation of MultiColvars and contact matrix based CVs"
  click M "Sprint.html" "3rd July 2023: Details on how SPRINT collective variables are implemented using shortcuts"
  click N "Steinhardt.html" "13th September 2023: An explanation of how Steinhardt parameters are implemented in PLUMED"
  click O "Behler.html" "14th September 2023: An explanation of how Behler-Parinello symmetry functions are implemented in PLUMED"
  click P "Volumes.html" "15th September 2023: Information on how you can use PLUMED to calculate the number of atoms and average for a symmetry function in a region"
  click Q "SymmetryFunction.html" "15th September 2023: Information on how you can use PLUMED to calculate symmetry functions"
  click R "averaging.html" "11th December 2023: Averages in the new version of PLUMED and thoughts about indistinguisability"
  click S "histograms.html" "11th December 2023: Histograms in the new version of PLUMED"
  click T "Clusters.html" "28th Feburary 2024: DFS clustering in the new version of PLUMED"
  click U "RMSD.html" "29th February 2024: Some thoughts on RMSD and ways of getting simplifying the code by getting rid of the reference class"
  click V "Path.html" "29th February 2024: Implementing PATH and GPROPERTYMAP using the new functionality"
```
