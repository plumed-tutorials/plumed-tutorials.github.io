# Masterclass 22.13: SASA module - The solvent accessible surface area of proteins as a collective variable, and the application of PLUMED for implicit solvent simulations

This lesson was given as part of the PLUMED masterclass series in 2022.  It includes:

* Two videos that describe the theory. 
* A series of exercises for you to complete.

The flow chart shown below indicates the order in which you should consult the resources.  You can click on the nodes to access the various resources.  Follow the thick black lines for the best results.  The resources that are connected by dashed lines are supplementary resources that you may find useful when completing the exercise.

This lesson was the thirteenth masterclass in the 2022 series.

```mermaid
flowchart TB;
  A[syntax] -.-> H[Lecture I];
  B[metadynamics] -.-> H;
  C[Hasel algorithm] -.-> H;
  D[LCPO algorithm] -.-> H;
  E[SASA temperature] -.-> H;
  F[SASA pressure] -.-> H;
  G[SASA osmolytes] -.-> H;
  H ==> I[Instructions];
  I ==> J[Lecture II];
  click A "../../../21/001/data/NAVIGATION.html" "A previous tutorial that introduces the basics of PLUMED syntax"
  click B "../../../21/004/data/NAVIGATION.html" "A previous tutorial on metadynamics, which is the method that is used in this tutorial"
  click C "https://www.sciencedirect.com/science/article/abs/pii/0898552988900152" "A paper describing one of the algorithms that is used to calculate the ASA in the tutorial"
  click D "https://onlinelibrary.wiley.com/doi/10.1002/%28SICI%291096-987X%2819990130%2920%3A2%3C217%3A%3AAID-JCC4%3E3.0.CO%3B2-A" "A paper describing the other algorithm that is used to calculate the ASA in the tutorial"
  click E "https://pubs.acs.org/doi/abs/10.1021/acs.jpcb.1c01694" "A paper describing how the transfer free energy change upon a change in temperature is calculated"
  click F "https://pubs.acs.org/doi/abs/10.1021/acs.jpcb.1c04398" "A paper describing how the transfer free energy change upon a change in pressure is calculated"
  click G "https://pubs.acs.org/doi/abs/10.1021/acs.jpcb.2c00889" "A paper describing how the transfer free energy change upon a change in osmolyte solution is calculated"
  click H "video1.html" "A lecture that was given on September 19st 2022 as part of the plumed masterclass series that introduces you to the exercises in this lesson"
  click I "INSTRUCTIONS.html" "Instructions for the exercises that you are supposed to complete"
  click J "video2.html" "A lecture that was given on September 26th 2022 as part of the plumed masterclass series that goes through the solutions to the exercises in the lesson"
```
