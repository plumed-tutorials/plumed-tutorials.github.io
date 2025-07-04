```mermaid
flowchart TB
A[ref. PIV] ==> D[PIV distance]
B[ref. PathCV] ==> D
C[ref. PIV-PathCV] ==> D
D ==> E[PIV-PathCV mapping]
E ==> F[PIV-PathCV metadynamics]
click A "https://pubs.aip.org/aip/jcp/article-abstract/139/7/074101/73227/Structural-cluster-analysis-of-chemical-reactions?redirectedFrom=fulltext" "reference for PIV"
click B "https://pubs.aip.org/aip/jcp/article-abstract/126/5/054103/187372/From-A-to-B-in-free-energy-space?redirectedFrom=fulltext" "reference for PathCV"
click C "https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.119.245701" "reference for PIV-PathCV"
click D "PIV_distance.html" "Associating PIVs to system configurations PIVs and cmputing distances"
click E "PIV-PathCV_driver.html" "Mapping a trajectory into PIV-PathCV space"
click F "PIV-PathCV_meta.html" "Biasing a simulation in the PIV-PathCV space"
```
{% raw %}
<b><a href="https://www.plumed.org/doc-master/user-doc/html/actionlist/?actions=PRINT,UPPER_WALLS,METAD,FUNCPATHMSD,CELL,PIV,LOWER_WALLS" target="_blank">Click here</a> to open manual pages for actions discussed in this tutorial.</b>
{% endraw %}
