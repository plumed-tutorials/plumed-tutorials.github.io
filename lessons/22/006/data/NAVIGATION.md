# Masterclass 22.6: EDS module + Coarse-Grained directed simulations

This lesson was given as part of the PLUMED masterclass series in 2022.  It includes:

* Two videos that describe the theory. 
* A series of exercises for you to complete.
* A python notebook that contains a full solution to the exercises.

The flow chart shown below indicates the order in which you should consult the resources.  You can click on the nodes to access the various resources.  Follow the thick black lines for the best results.  The resources that are connected by dashed lines are supplmentary resources that you may find useful when completing the exercise.

This lesson was the sixth masterclass in the 2022 series.

```mermaid
flowchart TB;
  A[ref1] -.-> E[Lecture I];
  B[ref2] -.-> E;
  C[ref3] -.-> E;
  D[ref4] -.-> E;
  E ==> F[instructions];
  F ==> G[Lecture II];
  G --> H[pesmd solutions];
  G --> I[ala2 solutions];
  click A "../../../21/001/data/NAVIGATION.html" "A previous tutorial that introduces the basics of PLUMED syntax"
  click B "https://doi.org/10.1021/ct500320c" "The original paper describing the Experiment Directed Simulation (EDS) Method"
  click C "https://doi.org/10.1063/1.4974837" "A paper applying EDS to DFT water, where the EDS module was implemented"
  click D "https://doi.org/10.1021/acs.jctc.7b00690" "A paper describing the Coarse-Grained Directed Simulation Method (CGDS), which enhanced the EDS software"
  click E "video1.html" "A lecture that was given on April 26th 2022 as part of the plumed masterclass series that introduces you to the exercises in this lesson"
  click F "INSTRUCTIONS.html" "Instructions for the exercise that you are supposed to complete"
  click G "video2.html" "A lecture that was given on May 2nd 2022 as part of the plumed masterclass series that goes through the solutions to the exercises in the lesson"
  click H "pes_md/pesmd_analysis.html" "A python notebook that contains solutions to the first set of exercises that use pesmd"
  click I "plain_md/ala2_analysis.html" "A python notebook where that contains solutions to the second set of exercises that involve alanine dipeptide"
```
