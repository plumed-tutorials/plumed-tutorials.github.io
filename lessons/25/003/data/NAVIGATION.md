# Defining custom machine learning CV with metatomic

[Metatomic](https://docs.metatensor.org/metatomic/) is a library to use
arbitrary machine learning models together with arbitrary simulation tools.
Here we show how to use the interface between metatomic and plumed to define
fully custom collective variables (CV). These CV can be defined using typical
machine learning tools, but any Python function based on PyTorch will also work,
allowing to define new CV extremely easily.

Through the use of PyTorch, you can focus on defining the CV itself, and
automatically get its gradients. You can also execute the code computing your CV
on GPUs and other accelerators.

Other tools are able to interact with CV defined as metatomic models, most
notably [chemiscope](https://chemiscope.org). You can therefore visualize how
complex CV act on representative structures before even starting a simulation,
and improve the Cv interactively.

## Free-energy surface of LJ38 cluster

The cluster of 38 atoms interacting through a Lennard-Jones potential is an
interesting benchmark system for collective variables, because its global
minimum energy structure is a truncated octahedron with `O_h` symmetry. The
potential energy surface also has a multi-funnel landscape, meaning the system
can easily get trapped in other local minima.

This tutorial contains a hands-on interactive tutorial (that you can also
download and run locally) that defines two different collective variables to
drive metadynamics for this system. The first CV is based on the histogram of
coordination number, and the second one uses a machine learning representation
(the SOAP spherical expansion) as a basis to define Steinhardt oder
parameters-like CVs.


{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/NAVIGATION.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="NAVIGATION.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="NAVIGATION.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<b name="data/NAVIGATION.md_working_1.datsoap" onclick='showPath("data/NAVIGATION.md_working_1.dat","data/NAVIGATION.md_working_1.datsoap","data/NAVIGATION.md_working_1.datsoap","brown")'>soap</b>: <span class="plumedtooltip" style="color:green">METATOMIC<span class="right">Use arbitrary machine learning models as collective variables. <a href="https://www.plumed.org/doc-master/user-doc/html/METATOMIC" style="color:green">More details</a><i></i></span></span> ...
    <span class="plumedtooltip">MODEL<span class="right">path to the exported metatomic model<i></i></span></span>=soap-cv.pt
    <span class="plumedtooltip">EXTENSIONS_DIRECTORY<span class="right">path to the directory containing TorchScript extensions to load<i></i></span></span>=./extensions/
    <span class="plumedtooltip">SPECIES1<span class="right">the indices of atoms in each PLUMED species<i></i></span></span>=1-38
    <span class="plumedtooltip">SPECIES_TO_TYPES<span class="right">mapping from PLUMED SPECIES to metatomic's atom types<i></i></span></span>=18
...
<br/><span style="display:none;" id="data/NAVIGATION.md_working_1.datsoap">The METATOMIC action with label <b>soap</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">soap.outputs</td><td>collective variable created by the metatomic model</td></tr><tr><td width="5%">soap.value</td><td>collective variable created by the metatomic model</td></tr></table></span><b name="data/NAVIGATION.md_working_1.dathistogram" onclick='showPath("data/NAVIGATION.md_working_1.dat","data/NAVIGATION.md_working_1.dathistogram","data/NAVIGATION.md_working_1.dathistogram","brown")'>histogram</b>: <span class="plumedtooltip" style="color:green">METATOMIC<span class="right">Use arbitrary machine learning models as collective variables. <a href="https://www.plumed.org/doc-master/user-doc/html/METATOMIC" style="color:green">More details</a><i></i></span></span> ...
    <span class="plumedtooltip">MODEL<span class="right">path to the exported metatomic model<i></i></span></span>=histo-cv.pt

    <span class="plumedtooltip">SPECIES1<span class="right">the indices of atoms in each PLUMED species<i></i></span></span>=1-38
    <span class="plumedtooltip">SPECIES_TO_TYPES<span class="right">mapping from PLUMED SPECIES to metatomic's atom types<i></i></span></span>=18
...
<br/><span style="display:none;" id="data/NAVIGATION.md_working_1.dathistogram">The METATOMIC action with label <b>histogram</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">histogram.outputs</td><td>collective variable created by the metatomic model</td></tr><tr><td width="5%">histogram.value</td><td>collective variable created by the metatomic model</td></tr></table></span><b name="data/NAVIGATION.md_working_1.datcv1" onclick='showPath("data/NAVIGATION.md_working_1.dat","data/NAVIGATION.md_working_1.datcv1","data/NAVIGATION.md_working_1.datcv1","brown")'>cv1</b>: <span class="plumedtooltip" style="color:green">SELECT_COMPONENTS<span class="right">Create a new value to hold a subset of the components that are in a vector or matrix <a href="https://www.plumed.org/doc-master/user-doc/html/SELECT_COMPONENTS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the value from which we are selecting components<i></i></span></span>=<b name="data/NAVIGATION.md_working_1.dathistogram">histogram</b> <span class="plumedtooltip">COMPONENTS<span class="right">the components in the input value that you woul like to build a new vector from<i></i></span></span>=1
<span style="display:none;" id="data/NAVIGATION.md_working_1.datcv1">The SELECT_COMPONENTS action with label <b>cv1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cv1.value</td><td>a vector containing the selected components</td></tr></table></span><b name="data/NAVIGATION.md_working_1.datcv2" onclick='showPath("data/NAVIGATION.md_working_1.dat","data/NAVIGATION.md_working_1.datcv2","data/NAVIGATION.md_working_1.datcv2","brown")'>cv2</b>: <span class="plumedtooltip" style="color:green">SELECT_COMPONENTS<span class="right">Create a new value to hold a subset of the components that are in a vector or matrix <a href="https://www.plumed.org/doc-master/user-doc/html/SELECT_COMPONENTS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the value from which we are selecting components<i></i></span></span>=<b name="data/NAVIGATION.md_working_1.dathistogram">histogram</b> <span class="plumedtooltip">COMPONENTS<span class="right">the components in the input value that you woul like to build a new vector from<i></i></span></span>=2

<span style="display:none;" id="data/NAVIGATION.md_working_1.datcv2">The SELECT_COMPONENTS action with label <b>cv2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cv2.value</td><td>a vector containing the selected components</td></tr></table></span><b name="data/NAVIGATION.md_working_1.datmtd" onclick='showPath("data/NAVIGATION.md_working_1.dat","data/NAVIGATION.md_working_1.datmtd","data/NAVIGATION.md_working_1.datmtd","brown")'>mtd</b>: <span class="plumedtooltip" style="color:green">METAD<span class="right">Used to performed metadynamics on one or more collective variables. <a href="https://www.plumed.org/doc-master/user-doc/html/METAD" style="color:green">More details</a><i></i></span></span> ...
    <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<b name="data/NAVIGATION.md_working_1.datcv1">cv1</b>,<b name="data/NAVIGATION.md_working_1.datcv2">cv2</b>
    <span class="plumedtooltip">HEIGHT<span class="right">the heights of the Gaussian hills<i></i></span></span>=0.04
    <span class="plumedtooltip">PACE<span class="right">the frequency for hill addition<i></i></span></span>=30
    <span class="plumedtooltip">SIGMA<span class="right">the widths of the Gaussian hills<i></i></span></span>=1.0,0.5
    <span class="plumedtooltip">GRID_MIN<span class="right">the lower bounds for the grid<i></i></span></span>=0,0
    <span class="plumedtooltip">GRID_MAX<span class="right">the upper bounds for the grid<i></i></span></span>=30,20
    <span class="plumedtooltip">GRID_BIN<span class="right">the number of bins for the grid<i></i></span></span>=300,200
    <span class="plumedtooltip">BIASFACTOR<span class="right">use well tempered metadynamics and use this bias factor<i></i></span></span>=40
    <span class="plumedtooltip">FILE<span class="right"> a file in which the list of added hills is stored<i></i></span></span>=HILLS
    <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is only needed if you are doing well-tempered metadynamics<i></i></span></span>=19.3
...
<span style="display:none;" id="data/NAVIGATION.md_working_1.datmtd">The METAD action with label <b>mtd</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">mtd.bias</td><td>the instantaneous value of the bias potential</td></tr></table></span></pre>
 {% endraw %} 

Depending on your previous experience, you may want to follow the lessons on
metadynamics first.


```mermaid
flowchart TD
A[Basic plumed syntax] ==> B[Metadynamics]
B ==> C([Defining and using custom CVs with metatomic])
subgraph D[Reference documentation]
    E[LAMMPS]
    F[i-PI]
    G[metatomic]
end
D -..-> C


click A "../../../21/001/data/NAVIGATION.html" "Follow this lecture for an introduction to PLUMED and enhanced sampling"
click B "../../../21/004/data/NAVIGATION.html" "Follow this lecture if you have never heard of metadynamics before"
click C "https://atomistic-cookbook.org/examples/metatomic-plumed/metatomic-plumed.html" "An interactive tutorial defining custom CV with metatomic and using them to run metadynamics in both i-PI and LAMMPS"
click E "https://docs.lammps.org/fix_plumed.html" "More information about the interface between LAMMPS and PLUMED"
click F "https://docs.ipi-code.org/input-tags.html#ffplumed" "More information about the interface between i-PI and PLUMED"
click G "https://docs.metatensor.org/metatomic/" "More information about metatomic"
```
{% raw %}
<b><a href="https://www.plumed.org/doc-master/user-doc/html/actionlist/?actions=METATOMIC,METAD,SELECT_COMPONENTS" target="_blank">Click here</a> to open manual pages for actions discussed in this tutorial.</b>
{% endraw %}
