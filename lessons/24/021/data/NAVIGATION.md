```mermaid
flowchart LR
D[PLUMED syntax] ==> B[Metadynamics: cis-trans isomerization]
D[PLUMED syntax] ==> C[Bias-Exchange: cis-trans isomerization]
B[Metadynamics: cis-trans isomerization]==>E[WHAM: Free energy]
C[Bias-Exchange: cis-trans isomerization]==>F[WHAM: Free energy]
B[Metadynamics: cis-trans isomerization]==>H[FCAM: Free energy]
C[Bias-Exchange: cis-trans isomerization]==>I[FCAM: Free energy]
G[Tutorial Instructions]
L[Tutorial Files]

click B "2dmeta.html" "PLUMED input instructions for bi-dimensional metadynamics"
click C "bias_exchange.html" "PLUMED input instructions for bias-exchange metadynamics"
click D "../../../21/001/data/NAVIGATION.html" "A tutorial on the basic plumed syntax"
click E "https://github.com/metagui/metagui3" "metagu3: VMD plugin for cluster and free energy analysis (Giorgino et al. Comp Phys Comm 2017)"
click F "https://github.com/metagui/metagui3" "metagu3: VMD plugin for cluster and free energy analysis (Giorgino et al. Comp Phys Comm 2017)"
click G "https://github.com/fabsugar/plumed-tutorial-be-aapak/blob/main/protocol1_md-meta-be.pdf" "Tutorial Instructions"
click H "https://github.com/FCAM-NIH/FCAM" "FCAM: free energy calculation based on mean forces (Marinelli et al. JCTC 2021)"
click I "https://github.com/FCAM-NIH/FCAM" "FCAM: free energy calculation based on mean forces (Marinelli et al. JCTC 2021)"
click L "https://github.com/fabsugar/plumed-tutorial-be-aapak/blob/main/tutorial_files.zip" "Tutorial Files"
```
{% raw %}
<b><a href="https://www.plumed.org/doc-master/user-doc/html/actionlist/?actions=PRINT,METAD,RANDOM_EXCHANGES,TORSION,INCLUDE,DUMPFORCES" target="_blank">Click here</a> to open manual pages for actions discussed in this tutorial.</b>
{% endraw %}
