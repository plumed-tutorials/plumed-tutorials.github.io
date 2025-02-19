# Masterclass 22.15: Mechanical pulling + FISST module

This lesson was given as part of the PLUMED masterclass series in 2022.  It includes:

* Two videos that describe the theory. 
* A series of exercises for you to complete.

The flow chart shown below indicates the order in which you should consult the resources.  You can click on the nodes to access the various resources.  Follow the thick black lines for the best results.  The resources that are connected by dashed lines are supplmentary resources that you may find useful when completing the exercise.

This lesson was the fifteenth masterclass in the 2022 series.

Solutions are available from [This page](https://github.com/hockyg/masterclass-22-15)

Some relevant perspective articles to consider are [this one](https://doi.org/10.1021/acs.jpcb.1c06330) from Hocky and [this one](https://doi.org/10.1021/acs.jpcb.1c10715) from Stirnemann.

```mermaid
flowchart TB;
  A[syntax] -.-> C[Lecture I];
  B[paper1] -.-> C;
  C ==> D[instructions];
  D ==> E[Lecture II];
  E ==> F[paper2];
  click A "../../../21/001/data/NAVIGATION.html" "A previous tutorial that introduces the basics of PLUMED syntax"
  click B "https://dx.doi.org/10.1063/5.0009280" "A paper describing the FISST method that is used in this tutorial"
  click C "video1.html" "A lecture that was given on October 17th 2022 as part of the plumed masterclass series that introduces you to the exercises in this lesson"
  click D "INSTRUCTIONS.html" "Instructions for the exercises that you are supposed to complete"
  click E "video2.html" "A lecture that was given on October 24th 2022 as part of the plumed masterclass series that gives background on modelling mechanobiological processes, and then goes through the solutions to the exercises in the lesson"
  click F "https://doi.org/10.1021/acs.jpcb.3c07081" "A follow up paper combining FISST with replica exchange"
```
