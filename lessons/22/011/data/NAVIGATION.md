# Masterclass 22.11: Variationally Enhanced Sampling

This Masterclass will discuss how to run variationally enhanced sampling simulations with PLUMED. This lesson was given as part of the PLUMED masterclass series in 2022. 

It includes:

* A video lecture that explains the background and theory behind Variationally Enhanced Sampling (Lecture 1).
* The lecture slides covered in Lecture 1. 
* A series of exercises that you should try to complete yourself.
* A Video lecture going over how the exercises should be completed (Lecture 2).
* A python notebook with the solution that was used in Lecture 2.

The flow chart shown below indicates the order in which you should consult the resources.  You can click on the nodes to access the various resources.  Follow the thick black lines for the best results.  The resources that are connected by dashed lines are supplementary resources that you may find useful when completing the exercise.


```mermaid
flowchart TB;
  A[ref1] ==> B[Lecture I];
  A ==> C[Slides];
  B ==> D[Instructions];
  C ==> D[Instructions];
  D ==> E[Lecture II];
  D ==> F[Solution];
  click A "https://github.com/plumed/masterclass-2022" "Instructions for how to install the version of PLUMED that you will need for this exercise"
  click B "video1.html" "A video lecture that was given on July 4st 2022 to cover the background behind Variationally Enhanced Sampling"
  click C "Slides/PLUMED-Masterclass-22-11-July4-2022.html" "The slides from the first video lecture"
  click D "INSTRUCTIONS.html" "The instructions for the exercises"
  click E "video2.html" "A lecture that was given on July 11th 2022 as part of the plumed masterclass series that goes through the solutions to the exercises in the lesson"
  click F "Solutions-July11-2022/Analysis_Solutions-July11-2022.html" "A python notebook that contains a full set of solutions to the exercises that are discussed in the masterclass.  This notebook is the one that was edited during the second video lecture of the masterclass"
```
{% raw %}
<b><a href="https://www.plumed.org/doc-master/user-doc/html/actionlist/?actions=CONVERT_TO_FES,TD_WELLTEMPERED,UPPER_WALLS,PRINT,READ,DUMPGRID,BF_WAVELETS,DISTANCE,COORDINATION,TD_UNIFORM,OPT_AVERAGED_SGD,VES_LINEAR_EXPANSION,REWEIGHT_BIAS,BF_LEGENDRE,HISTOGRAM" target="_blank">Click here</a> to open manual pages for actions discussed in this tutorial.</b>
{% endraw %}
