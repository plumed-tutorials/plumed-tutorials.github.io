# Masterclass 22.08: Modelling Concentration-Driven processes with PLUMED

This lesson was given as part of the PLUMED masterclass series in 2022.  It includes:

* Two videos that describe the theory. 
* A series of exercises for you to complete.
* A python notebook that contains a full solution to the exercises.

The flow chart shown below indicates the order in which you should consult the resources.  You can click on the nodes to access the various resources.  Follow the thick black lines for the best results.  The resources that are connected by dashed lines are supplmentary resources that you may find useful when completing the exercise.

This lesson was the seventh masterclass in the 2022 series.

```mermaid
flowchart TB;
  A[ref1] -.-> B[Lecture I];
  B ==> C[Instructions];
  C ==> D[Lecture III];
  D ==> E[Solutions];
  click A "../../../21/001/data/NAVIGATION.html" "A previous tutorial that introduces the basics of PLUMED syntax"
  click B "video1.html" "A lecture that was given on May 23rd 2022 as part of the plumed masterclass series that introduces you to the exercises in this lesson"
  click C "INSTRUCTIONS.html" "Instructions for the exercise that you are supposed to complete"
  click D "video2.html" "A lecture that was given on June 1st 2022 as part of the plumed masterclass series that goes through the solutions to the exercises in the lesson"
  click E "Solution/Solution.html" "A python notebook where the answers to the exericses are discussed"
```
{% raw %}
<b><a href="https://www.plumed.org/doc-master/user-doc/html/actionlist/?actions=PRINT,DFSCLUSTERING,GROUP,RESTRAINT,MATRIX_VECTOR_PRODUCT,SUM,CLUSTER_DISTRIBUTION,FLUSH,ONES,CLUSTER_NATOMS,CONTACT_MATRIX,MORE_THAN,COORDINATIONNUMBER" target="_blank">Click here</a> to open manual pages for actions discussed in this tutorial.</b>
{% endraw %}
