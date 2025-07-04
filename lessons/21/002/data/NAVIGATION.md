#  PLUMED Masterclass 21.2: Statistical errors in MD 

This lesson was given as part of the PLUMED masterclass series in 2021.  It includes:

* A video that explain the theory covered and a second video which shows you how the exercises should be completed.
* A series of exercises that you should try to complete yourself.
* Some supplementary python notebooks that provide further background information on the exercise.

The flow chart shown below indicates the order in which you should consult the resources.  You can click on the nodes to access the various resources.  Follow the thick black lines for the best results.  The resources that are connected by dashed lines are supplmentary resources that you may find useful when completing the exercise. 

This lesson was the second masterclass in the 2021 series.  You will likely be able to complete the exercise without completing all the exercises in the first masterclass in the series.  However, the earlier masterclass contains instructions for installing PLUMED using conda that you may need to consult if you have not installed it already.

```mermaid
flowchart TB;
  H[PLUMED intro] -.-> A[Lecture I] 
  A ==> B[Instructions];
  A -.-> G[how data was generated];
  A -.-> C[template notebook];
  B ==> D[Lecture II];
  C -.-> D;
  G -.-> D;
  D --> E[solution];
  D --> F[alternative solution];
  click H "../../../21/001/data/NAVIGATION.html" "This elementary lesson shows you how to install PLUMED and some basic and more advanced syntax. You will only need to complete up to exercise 1 of this earlier lesson to complete these exercises on statistical errors."
  click A "video1.html" "A lecture that was given on February 1st 2021 as part of the plumed masterclass series that introduces you to the exercises in this lesson"
  click B "GAT_SAFE_README.html" "The instructions for the exercises"
  click G "notebooks/gendata.html" "A python notebook that shows how the data sets in the files uncorrelated_data, correlated_data and weighted data that are all used in the exericses was generated"
  click C "notebooks/template.html" "A python notebook file that explains how you can work on the exercises from a python notebook.  Advice on running PLUMED from a notebook and on plotting the data that is generated is given."
  click D "video2.html" "A lecture that was given on February 8th 2021 as part of the plumed masterclass series that goes through the solutions to the exercises in the lesson"
  click E "notebooks/solution.html" "A python notebook file that provides a complete set of solutions to the exercises"
  click F "notebooks/answers_notebook.html" "A second python notebook file that contains solutions to the exercises.  In this notebook a different method has been used to generate the figures showing the final free energy surfaces."
```
{% raw %}
<b><a href="https://www.plumed.org/doc-master/user-doc/html/actionlist/?actions=AVERAGE,HISTOGRAM,READ,CONVERT_TO_FES,CUSTOM,REWEIGHT_BIAS,COORDINATIONNUMBER,PRINT,METAD,DISTANCE,UPPER_WALLS,UNITS,COM,DUMPGRID,RESTRAINT,CONSTANT" target="_blank">Click here</a> to open manual pages for actions discussed in this tutorial.</b>
{% endraw %}
