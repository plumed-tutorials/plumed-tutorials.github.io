# Masterclass 22.01: Funnel Metadynamics (FM): predicting ligand binding models, binding free energies and kinetics

This lesson was given as part of the PLUMED masterclass series in 2022.  It included:

* A two video set covering the theory behind the technique and practical information to set up and analyse the results.
* A set of inputs to try the code and rerun FM on a paradigmatic system.
* Some supplementary python notebooks that provide further background information on the exercise.

The flow chart shown below indicates the order in which you should consult the resources.  You can click on the nodes to access the various resources.  Follow the thick black lines for the best results.  The resources that are connected by dashed lines are supplmentary resources that you may find useful when completing the exercise.

This data was presented among the masterclasses in the 2022 series.

```mermaid
flowchart TB;
  A[Install] ==> B[Lecture I];
  B ==> C[Slides];
  B ==> D[Instructions];
  D ==> E[web server];
  E ==> H[Showcase]
  D ==> F[Lecture II];
  E ==> F;
  F ==> G[Solution];
  click A "INSTALL.html" "Instructions for how to install the version of PLUMED that you will need for this exercise"
  click B "video1.html" "This lesson explains the basics about ligand/target binding and the scope of FM."
  click C "plumed_masterclass_22-1.html" "The slides for the theory explained in Lecture I."
  click D "INSTRUCTIONS.html" "A step-by-step procedure that will wlk you through the FM procedure."
  click E "https://mbuto.si.usi.ch/" "Web server to set up a FM simulation. Can be used in substitution of the tcl plug-in funnel.tcl."
  click F "video2.html" "A lecture that goes a little more in deep in the practical phases of preparing and analysing a FM simulation"
  click G "Solution.html" "A python notebook that contains results and analyses of the simulation that is discussed in the masterclass."
  click H "video3.html" "A video showcasing Funnel Metadynamics Pre-Processing Tool functionalities"
```
{% raw %}
<b><a href="https://www.plumed.org/doc-master/user-doc/html/actionlist/?actions=" target="_blank">Click here</a> to open manual pages for actions discussed in this tutorial.</b>
{% endraw %}
