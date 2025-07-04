# PLUMED Masterclass 22.8: Modelling Concentration-driven processes with PLUMED



## Origin 



This masterclass was authored by Matteo Salvalaglio on May 20, 2022



## Aims



This Masterclass aims to introduce users to the tools available via PLUMED to analyze and perform simulations of concentration-driven processes such as nucleation, growth, and diffusion. 



## Objectives



Once this Masterclass is completed, users will be able to:



- Write a PLUMED input file to analyze a trajectory with multicolvars.

- Use the Depth-First-Search tools available in PLUMED to characterize clusters of atoms in an existing vapour condensation trajectory.

- Write a PLUMED input file to analyze the condensation of a simple liquid phase from vapour.  

- Write a PLUMED input file for CmuMD, and perform a CmuMD simulation of liquid condensation at constant driving force.

- Write a PLUMED input file for CmuMD, and perform a CmuMD simulation to model steady-state diffusive flux across a simulation box. 



## Prerequisites



We assume that you are familiar with PLUMED. However, the 2021 PLUMED Masterclass is a great place to start if you are not.



## Setting up the software 



Follow the instructions provided [here](https://urldefense.com/v3/__https://github.com/plumed/masterclass-2022__;!!JFdNOqOXpB6UZW0!5LDzfOpI0a0QUEAXjfWbM4f1ubgf4gC-ELH4qKstVB9wJwXRDKOjaCtm52xOb0YEw5tvTtPxyw$ ) to install gromacs+plumed2.8 compiled with [CmuMD](https://urldefense.com/v3/__https://github.com/mme-ucl/CmuMD__;!!JFdNOqOXpB6UZW0!5LDzfOpI0a0QUEAXjfWbM4f1ubgf4gC-ELH4qKstVB9wJwXRDKOjaCtm52xOb0YEw5sp2Fhg_A$ ).



## Background Overview 



PLUMED facilitates the calculation of functions of atom coordinates and the introduction of bias potentials in atomistic simulations. 



In this tutorial, we review how to use PLUMED functionalities for two complementary tasks: 

- Calculating collective variables that capture processes of assembly/disassembly such as the nucleation, condensation, dissolution etc. (Ex. 1, 2)

- Introducing biasing forces through CmuMD, a [method](https://urldefense.com/v3/__https://aip.scitation.org/doi/abs/10.1063/1.4917200__;!!JFdNOqOXpB6UZW0!5LDzfOpI0a0QUEAXjfWbM4f1ubgf4gC-ELH4qKstVB9wJwXRDKOjaCtm52xOb0YEw5vzGbfc4A$ ) that mimics open-boundary conditions and allows for mitigation of finite-size effects. (Ex. 3, 4)



## Resources



The data needed to complete the exercises of this Masterclass can be found on [GitHub](https://github.com/mme-ucl/PLUMED_MClass_22-08).

You can clone this repository locally on your machine using the following command:



````

git clone https://github.com/mme-ucl/PLUMED_MClass_22-08 

````



## Solution



The solution of this masterclass is available on GitHub as a [jupyter notebook](https://github.com/mme-ucl/PLUMED_MClass_22-08/blob/main/Solution/Solution.ipynb). 



## Exercise 1: analysis of a nucleation trajectory I 



We can start by using plumed to analyze a trajectory and identify the total number of atoms belonging to a liquid phase condensing from a supersaturated vapour in a long unbiased MD simulation.



To this aim, a typical choice is the implementation of a criterion inspired by the work of Ten Wolde and Frenkel: all the atoms with a threshold number of nearest neighbours larger than a threshold is considered as part of the liquid phase. 



In PLUMED this criterion can be readily implemented using the multicolvar [COORDINATIONNUMBER](https://www.plumed.org/doc-master/user-doc/html/_c_o_o_r_d_i_n_a_t_i_o_n_n_u_m_b_e_r.html): 



{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span style="color:blue" class="comment"># LIQUID-like atoms</span>
<br/><span id="data/INSTRUCTIONS.md_working_1.datlq_short"><b name="data/INSTRUCTIONS.md_working_1.datlq" onclick='showPath("data/INSTRUCTIONS.md_working_1.dat","data/INSTRUCTIONS.md_working_1.datlq","data/INSTRUCTIONS.md_working_1.datlq_shortcut","blue")'>lq</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_1.datlq_shortcut">The COORDINATIONNUMBER action with label <b>lq</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">lq</td><td width="5%"><font color="blue">vector</font></td><td>the coordination numbers of the specified atoms</td></tr><tr><td width="5%">lq_morethan</td><td width="5%"><font color="black">scalar</font></td><td>the number of colvars that have a value more than a threshold</td></tr></table></span>: <span class="plumedtooltip" style="color:green">COORDINATIONNUMBER<span class="right">Calculate the coordination numbers of atoms so that you can then calculate functions of the distribution of This action is <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_1.datlq");'>a shortcut</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATIONNUMBER">More details</a><i></i></span></span> <span class="plumedtooltip">SPECIES<span class="right">the list of atoms for which the symmetry function is being calculated and the atoms that can be in the environments<i></i></span></span>=1-10000 <span class="plumedtooltip">SWITCH<span class="right">the switching function that it used in the construction of the contact matrix. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={CUBIC D_0=0.45 D_MAX=0.55} <span class="plumedtooltip">MORE_THAN<span class="right">calculate the number of variables that are more than a certain target value. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/MORE_THAN">MORE_THAN</a>.<i></i></span></span>={RATIONAL R_0=5.0 D_MAX=10.0}
</span><span id="data/INSTRUCTIONS.md_working_1.datlq_long" style="display:none;"><span style="color:blue" class="comment"># PLUMED interprets the command:
</span><span class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_1.datlq")'># lq: COORDINATIONNUMBER SPECIES=1-10000 SWITCH={CUBIC D_0=0.45 D_MAX=0.55} MORE_THAN={RATIONAL R_0=5.0 D_MAX=10.0}</span>
<span style="color:blue" class="comment"># as follows (Click the red comment above to revert to the short version of the input):</span>
<b name="data/INSTRUCTIONS.md_working_1.datlq_grp" onclick='showPath("data/INSTRUCTIONS.md_working_1.dat","data/INSTRUCTIONS.md_working_1.datlq_grp","data/INSTRUCTIONS.md_working_1.datlq_grp","violet")'>lq_grp</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_1.datlq_grp">The GROUP action with label <b>lq_grp</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">lq_grp</td><td width="5%"><font color="violet">atoms</font></td><td>indices of atoms specified in GROUP</td></tr></table></span>: <span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the numerical indexes for the set of atoms in the group<i></i></span></span>=1-10000
<b name="data/INSTRUCTIONS.md_working_1.datlq_mat" onclick='showPath("data/INSTRUCTIONS.md_working_1.dat","data/INSTRUCTIONS.md_working_1.datlq_mat","data/INSTRUCTIONS.md_working_1.datlq_mat","red")'>lq_mat</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_1.datlq_mat">The CONTACT_MATRIX action with label <b>lq_mat</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">lq_mat</td><td width="5%"><font color="red">matrix</font></td><td>a matrix containing the weights for the bonds between each pair of atoms</td></tr></table></span>: <span class="plumedtooltip" style="color:green">CONTACT_MATRIX<span class="right">Adjacency matrix in which two atoms are adjacent if they are within a certain cutoff. <a href="https://www.plumed.org/doc-master/user-doc/html/CONTACT_MATRIX" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GROUP<span class="right">specifies the list of atoms that should be assumed indistinguishable<i></i></span></span>=1-10000 <span class="plumedtooltip">SWITCH<span class="right">the input for the switching function that acts upon the distance between each pair of atoms. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={CUBIC D_0=0.45 D_MAX=0.55}
<b name="data/INSTRUCTIONS.md_working_1.datlq_ones" onclick='showPath("data/INSTRUCTIONS.md_working_1.dat","data/INSTRUCTIONS.md_working_1.datlq_ones","data/INSTRUCTIONS.md_working_1.datlq_ones","blue")'>lq_ones</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_1.datlq_ones">The CONSTANT action with label <b>lq_ones</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">lq_ones</td><td width="5%"><font color="blue">vector</font></td><td>the constant value that was read from the plumed input</td></tr></table></span>: <span class="plumedtooltip" style="color:green">ONES<span class="right">Create a constant vector with all elements equal to one <a href="https://www.plumed.org/doc-master/user-doc/html/ONES" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">SIZE<span class="right">the number of ones that you would like to create<i></i></span></span>=10000
<b name="data/INSTRUCTIONS.md_working_1.datlq" onclick='showPath("data/INSTRUCTIONS.md_working_1.dat","data/INSTRUCTIONS.md_working_1.datlq","data/INSTRUCTIONS.md_working_1.datlq","blue")'>lq</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_1.datlq">The MATRIX_VECTOR_PRODUCT action with label <b>lq</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">lq</td><td width="5%"><font color="blue">vector</font></td><td>the vector that is obtained by taking the product between the matrix and the vector that were input</td></tr></table></span>: <span class="plumedtooltip" style="color:green">MATRIX_VECTOR_PRODUCT<span class="right">Calculate the product of the matrix and the vector <a href="https://www.plumed.org/doc-master/user-doc/html/MATRIX_VECTOR_PRODUCT" style="color:green">More details</a><i></i></span></span>  <span class="plumedtooltip">ARG<span class="right">the label for the matrix and the vector/scalar that are being multiplied<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_1.datlq_mat">lq_mat</b>,<b name="data/INSTRUCTIONS.md_working_1.datlq_ones">lq_ones</b>
<b name="data/INSTRUCTIONS.md_working_1.datlq_mt" onclick='showPath("data/INSTRUCTIONS.md_working_1.dat","data/INSTRUCTIONS.md_working_1.datlq_mt","data/INSTRUCTIONS.md_working_1.datlq_mt","blue")'>lq_mt</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_1.datlq_mt">The MORE_THAN action with label <b>lq_mt</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">lq_mt</td><td width="5%"><font color="blue">vector</font></td><td>the vector obtained by doing an element-wise application of a function that is one if the if the input is more than a threshold to the input vectors</td></tr></table></span>: <span class="plumedtooltip" style="color:green">MORE_THAN<span class="right">Use a switching function to determine how many of the input variables are more than a certain cutoff. <a href="https://www.plumed.org/doc-master/user-doc/html/MORE_THAN" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_1.datlq">lq</b> <span class="plumedtooltip">SWITCH<span class="right">This keyword is used if you want to employ an alternative to the continuous swiching function defined above<i></i></span></span>={RATIONAL R_0=5.0 D_MAX=10.0}
<b name="data/INSTRUCTIONS.md_working_1.datlq_morethan" onclick='showPath("data/INSTRUCTIONS.md_working_1.dat","data/INSTRUCTIONS.md_working_1.datlq_morethan","data/INSTRUCTIONS.md_working_1.datlq_morethan","black")'>lq_morethan</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_1.datlq_morethan">The SUM action with label <b>lq_morethan</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">lq_morethan</td><td width="5%"><font color="black">scalar</font></td><td>the SUM of the elements in the input value</td></tr></table></span>: <span class="plumedtooltip" style="color:green">SUM<span class="right">Calculate the sum of the arguments <a href="https://www.plumed.org/doc-master/user-doc/html/SUM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the vector/matrix/grid whose elements shuld be added together<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_1.datlq_mt">lq_mt</b> <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="color:blue"># --- End of included input --- </span></span><br/><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_1.datlq">lq.morethan</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=1 <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=nliquid.dat
</pre>
 {% endraw %} 



The time evolution of the number of atoms in the liquid phase can be computed by analyzing the trajectory using the [driver](https://www.plumed.org/doc-master/user-doc/html/driver.html) functionality (where liquid.dat is the plumed file for this analysis). 



````

plumed driver --mf_xtc LJvap_to_liq_red.xtc --plumed liquid.dat

````



### Try on your own



Using other MultiColvar keywords can you count the number of atoms on the surface of the clusters forming in this trajectory? Can you estimate how the surface to volume ratio of the droplets forming in the system changes directly within PLUMED? 



### Available data



The MD trajectory that we will analyze can be found in the folder called `data`:

- `LJvap.gro`: reference conformation of 10000 LJ particles in a metastable vapour phase.

- `LJvap_to_liq.xtc`: trajectory.



## Exercise 2: analysis of a nucleation trajectory II



In certain contexts, it can be helpful to characterize the phase transition by following analyzing the population of clusters that form during the nucleation process. In PLUMED, this is possible by taking advantage of the [DFSCLUSTERING](https://www.plumed.org/doc-master/user-doc/html/_d_f_s_c_l_u_s_t_e_r_i_n_g.html) algorithm, which builds on the construction of a [CONTACT_MATRIX](https://www.plumed.org/doc-master/user-doc/html/_c_o_n_t_a_c_t__m_a_t_r_i_x.html) to identify clusters of atoms with specific properties. 



Here we analyse the clusters distribution emerging in the trajectory `LJvap_to_liq.xtc`, focussing on the number of clusters, and following the evolution of the four largest clusters in the system: 



{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_2.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_2.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_2.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span style="color:blue" class="comment"># Identify liquid-like atoms</span>
<br/><b name="data/INSTRUCTIONS.md_working_2.datlq" onclick='showPath("data/INSTRUCTIONS.md_working_2.dat","data/INSTRUCTIONS.md_working_2.datlq","data/INSTRUCTIONS.md_working_2.datlq","brown")'>lq</b>: <span class="plumedtooltip" style="color:green">COORDINATIONNUMBER<span class="right">Calculate the coordination numbers of atoms so that you can then calculate functions of the distribution of <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATIONNUMBER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">SPECIES<span class="right">the list of atoms for which the symmetry function is being calculated and the atoms that can be in the environments<i></i></span></span>=1-10000 <span class="plumedtooltip">SWITCH<span class="right">the switching function that it used in the construction of the contact matrix. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={CUBIC D_0=0.45  D_MAX=0.55} <span class="plumedtooltip">MORE_THAN<span class="right">calculate the number of variables that are more than a certain target value. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/MORE_THAN">MORE_THAN</a>.<i></i></span></span>={RATIONAL R_0=5.0 D_MAX=10.0}


<br/><span style="color:blue" class="comment"># Define a contact matrix &amp; perfom DFS clustering </span>
<br/><span style="display:none;" id="data/INSTRUCTIONS.md_working_2.datlq">The COORDINATIONNUMBER action with label <b>lq</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">lq.morethan</td><td>the number of colvars that have a value more than a threshold</td></tr><tr><td width="5%">lq.value</td><td>the coordination numbers of the specified atoms</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_2.datcm" onclick='showPath("data/INSTRUCTIONS.md_working_2.dat","data/INSTRUCTIONS.md_working_2.datcm","data/INSTRUCTIONS.md_working_2.datcm","brown")'>cm</b>: <span class="plumedtooltip" style="color:green">CONTACT_MATRIX<span class="right">Adjacency matrix in which two atoms are adjacent if they are within a certain cutoff. <a href="https://www.plumed.org/doc-master/user-doc/html/CONTACT_MATRIX" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the atoms for which you would like to calculate the adjacency matrix<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_2.datlq">lq</b>  <span class="plumedtooltip">SWITCH<span class="right">the input for the switching function that acts upon the distance between each pair of atoms. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={CUBIC D_0=0.45  D_MAX=0.55}
<br/><span style="display:none;" id="data/INSTRUCTIONS.md_working_2.datcm">The CONTACT_MATRIX action with label <b>cm</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cm.value</td><td>a matrix containing the weights for the bonds between each pair of atoms</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_2.datdfs" onclick='showPath("data/INSTRUCTIONS.md_working_2.dat","data/INSTRUCTIONS.md_working_2.datdfs","data/INSTRUCTIONS.md_working_2.datdfs","brown")'>dfs</b>: <span class="plumedtooltip" style="color:green">DFSCLUSTERING<span class="right">Find the connected components of the matrix using the depth first search clustering algorithm. <a href="https://www.plumed.org/doc-master/user-doc/html/DFSCLUSTERING" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">MATRIX<span class="right">You should use ARG instead of this keyword which was used in older versions of PLUMED and is provided for back compatibility only<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_2.datcm">cm</b>



<span style="color:blue" class="comment"># Compute the size of the four largest clusters</span>
<br/><span style="display:none;" id="data/INSTRUCTIONS.md_working_2.datdfs">The DFSCLUSTERING action with label <b>dfs</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dfs.value</td><td>vector with length that is equal to the number of rows in the input matrix</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_2.datcluster_1" onclick='showPath("data/INSTRUCTIONS.md_working_2.dat","data/INSTRUCTIONS.md_working_2.datcluster_1","data/INSTRUCTIONS.md_working_2.datcluster_1","brown")'>cluster_1</b>: <span class="plumedtooltip" style="color:green">CLUSTER_NATOMS<span class="right">Calculate the number of atoms in the cluster of interest <a href="https://www.plumed.org/doc-master/user-doc/html/CLUSTER_NATOMS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">CLUSTERS<span class="right">the label of the action that does the clustering<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_2.datdfs">dfs</b> <span class="plumedtooltip">CLUSTER<span class="right"> which cluster would you like to look at 1 is the largest cluster, 2 is the second largest, 3 is the the third largest and so on<i></i></span></span>=1    

<span style="display:none;" id="data/INSTRUCTIONS.md_working_2.datcluster_1">The CLUSTER_NATOMS action with label <b>cluster_1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cluster_1.value</td><td>the number of atoms in the cluster</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_2.datcluster_2" onclick='showPath("data/INSTRUCTIONS.md_working_2.dat","data/INSTRUCTIONS.md_working_2.datcluster_2","data/INSTRUCTIONS.md_working_2.datcluster_2","brown")'>cluster_2</b>: <span class="plumedtooltip" style="color:green">CLUSTER_NATOMS<span class="right">Calculate the number of atoms in the cluster of interest <a href="https://www.plumed.org/doc-master/user-doc/html/CLUSTER_NATOMS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">CLUSTERS<span class="right">the label of the action that does the clustering<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_2.datdfs">dfs</b> <span class="plumedtooltip">CLUSTER<span class="right"> which cluster would you like to look at 1 is the largest cluster, 2 is the second largest, 3 is the the third largest and so on<i></i></span></span>=2

<span style="display:none;" id="data/INSTRUCTIONS.md_working_2.datcluster_2">The CLUSTER_NATOMS action with label <b>cluster_2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cluster_2.value</td><td>the number of atoms in the cluster</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_2.datcluster_3" onclick='showPath("data/INSTRUCTIONS.md_working_2.dat","data/INSTRUCTIONS.md_working_2.datcluster_3","data/INSTRUCTIONS.md_working_2.datcluster_3","brown")'>cluster_3</b>: <span class="plumedtooltip" style="color:green">CLUSTER_NATOMS<span class="right">Calculate the number of atoms in the cluster of interest <a href="https://www.plumed.org/doc-master/user-doc/html/CLUSTER_NATOMS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">CLUSTERS<span class="right">the label of the action that does the clustering<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_2.datdfs">dfs</b> <span class="plumedtooltip">CLUSTER<span class="right"> which cluster would you like to look at 1 is the largest cluster, 2 is the second largest, 3 is the the third largest and so on<i></i></span></span>=3

<span style="display:none;" id="data/INSTRUCTIONS.md_working_2.datcluster_3">The CLUSTER_NATOMS action with label <b>cluster_3</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cluster_3.value</td><td>the number of atoms in the cluster</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_2.datcluster_4" onclick='showPath("data/INSTRUCTIONS.md_working_2.dat","data/INSTRUCTIONS.md_working_2.datcluster_4","data/INSTRUCTIONS.md_working_2.datcluster_4","brown")'>cluster_4</b>: <span class="plumedtooltip" style="color:green">CLUSTER_NATOMS<span class="right">Calculate the number of atoms in the cluster of interest <a href="https://www.plumed.org/doc-master/user-doc/html/CLUSTER_NATOMS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">CLUSTERS<span class="right">the label of the action that does the clustering<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_2.datdfs">dfs</b> <span class="plumedtooltip">CLUSTER<span class="right"> which cluster would you like to look at 1 is the largest cluster, 2 is the second largest, 3 is the the third largest and so on<i></i></span></span>=4



<span style="color:blue" class="comment"># Compute the number of clusters  </span>
<br/><span style="display:none;" id="data/INSTRUCTIONS.md_working_2.datcluster_4">The CLUSTER_NATOMS action with label <b>cluster_4</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cluster_4.value</td><td>the number of atoms in the cluster</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_2.datnclust" onclick='showPath("data/INSTRUCTIONS.md_working_2.dat","data/INSTRUCTIONS.md_working_2.datnclust","data/INSTRUCTIONS.md_working_2.datnclust","brown")'>nclust</b>: <span class="plumedtooltip" style="color:green">CLUSTER_DISTRIBUTION<span class="right">Calculate functions of the distribution of properties in your connected components. <a href="https://www.plumed.org/doc-master/user-doc/html/CLUSTER_DISTRIBUTION" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">CLUSTERS<span class="right">the label of the action that does the clustering<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_2.datdfs">dfs</b> <span class="plumedtooltip">MORE_THAN<span class="right">calculate the number of variables that are more than a certain target value. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/MORE_THAN">MORE_THAN</a>.<i></i></span></span>={GAUSSIAN D_0=D_0=1.95 R_0=0.01 D_MAX=1.99}


<br/><span style="color:blue" class="comment"># PRINT to file</span>
<br/><span style="display:none;" id="data/INSTRUCTIONS.md_working_2.datnclust">The CLUSTER_DISTRIBUTION action with label <b>nclust</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">nclust.morethan</td><td>the number of colvars that have a value more than a threshold</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_2.datlq">lq.morethan</b>,<b name="data/INSTRUCTIONS.md_working_2.datnclust">nclust.*</b>,<b name="data/INSTRUCTIONS.md_working_2.datcluster_1">cluster_1</b>,<b name="data/INSTRUCTIONS.md_working_2.datcluster_2">cluster_2</b>,<b name="data/INSTRUCTIONS.md_working_2.datcluster_3">cluster_3</b>,<b name="data/INSTRUCTIONS.md_working_2.datcluster_4">cluster_4</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=1  <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=clusters.dat



<span style="display:none;" id="data/INSTRUCTIONS.md_working_2.dat">The PRINT action with label <b></b> calculates something</span><span class="plumedtooltip" style="color:green">FLUSH<span class="right">This command instructs plumed to flush all the open files with a user specified frequency. <a href="https://www.plumed.org/doc-master/user-doc/html/FLUSH" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">STRIDE<span class="right">the frequency with which all the open files should be flushed<i></i></span></span>=1
</pre>
 {% endraw %} 



### Try on your own



Modifying the setup above, can you compute the number of clusters with a size larger than 20 LJ particles? 



### Available data



The MD trajectory that we will analyze can be found in the folder called `data`:

- `LJvap.gro`: reference conformation of 10000 LJ particles in a metastable vapour phase.

- `LJvap_to_liq.xtc`: trajectory.



## Exercise 3: Steady-state diffusive flux with CmuMD



In the two examples discussed in Exercises 1 and 2 it is apparent that the process of condensation reaches steady state due to finite-size effects. However, looking at the process more carefully, one can notice that the driving force leading to phase separation is far from constant.

C$\mu$MD allows using PLUMED to apply ad-hoc forces and keep constant the composition of spatial regions of the simulation box called control regions. This feature allows to model processes driven by concentration in steady, out-of-equilibrium conditions. 



The first example we will focus on is a purely diffusive process in a LJ vapour. 



A PLUMED file that allows imposing a steady concentration difference with CmuMD looks like: 



{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_3.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_3.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_3.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span style="color:blue" class="comment"># Define groups of atoms</span>
<br/><b name="data/INSTRUCTIONS.md_working_3.datLJ" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datLJ","data/INSTRUCTIONS.md_working_3.datLJ","brown")'>LJ</b>: <span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the numerical indexes for the set of atoms in the group<i></i></span></span>=1-1000:1 



<span style="color:blue" class="comment"># Provide parameters for the CV</span>
<br/><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datLJ">The GROUP action with label <b>LJ</b> calculates something</span><b name="data/INSTRUCTIONS.md_working_3.datleft" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datleft","data/INSTRUCTIONS.md_working_3.datleft","brown")'>left</b>:  <span class="plumedtooltip" style="color:green">CMUMD<span class="right">This action is not part of PLUMED and was included by using a LOAD command <a href="https://www.plumed.org/doc-master/user-doc/html/LOAD" style="color:green">More details</a><i></i></span></span> GROUP=lj NSV=1 FIXED=0.5 DCR=0.25 CRSIZE=0.1 WF=0.0001  ASYMM=-1 NINT=0.1 NZ=291

<b name="data/INSTRUCTIONS.md_working_3.datright" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datright","data/INSTRUCTIONS.md_working_3.datright","brown")'>right</b>:  <span class="plumedtooltip" style="color:green">CMUMD<span class="right">This action is not part of PLUMED and was included by using a LOAD command <a href="https://www.plumed.org/doc-master/user-doc/html/LOAD" style="color:green">More details</a><i></i></span></span> GROUP=lj NSV=1 FIXED=0.5 DCR=0.25 CRSIZE=0.1 WF=0.0001  ASYMM=1 NINT=0.1 NZ=291



<span style="color:blue" class="comment"># CmuMD is implemented as a restraint on the densities of species in CR</span>
<br/><b name="data/INSTRUCTIONS.md_working_3.datrleft" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datrleft","data/INSTRUCTIONS.md_working_3.datrleft","brown")'>rleft</b>:  <span class="plumedtooltip" style="color:green">RESTRAINT<span class="right">Adds harmonic and/or linear restraints on one or more variables. <a href="https://www.plumed.org/doc-master/user-doc/html/RESTRAINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values the harmonic restraint acts upon<i></i></span></span>=left <span class="plumedtooltip">AT<span class="right">the position of the restraint<i></i></span></span>=1.4 <span class="plumedtooltip">KAPPA<span class="right"> specifies that the restraint is harmonic and what the values of the force constants on each of the variables are<i></i></span></span>=1000.0 

<span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datrleft">The RESTRAINT action with label <b>rleft</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">rleft.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">rleft.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_3.datrright" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datrright","data/INSTRUCTIONS.md_working_3.datrright","brown")'>rright</b>: <span class="plumedtooltip" style="color:green">RESTRAINT<span class="right">Adds harmonic and/or linear restraints on one or more variables. <a href="https://www.plumed.org/doc-master/user-doc/html/RESTRAINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values the harmonic restraint acts upon<i></i></span></span>=right <span class="plumedtooltip">AT<span class="right">the position of the restraint<i></i></span></span>=0.05 <span class="plumedtooltip">KAPPA<span class="right"> specifies that the restraint is harmonic and what the values of the force constants on each of the variables are<i></i></span></span>=2000.0 



<span style="color:blue" class="comment"># Report the densities and bias</span>
<br/><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datrright">The RESTRAINT action with label <b>rright</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">rright.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">rright.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> ...

<span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=left,right,<b name="data/INSTRUCTIONS.md_working_3.datrleft">rleft.bias</b>,<b name="data/INSTRUCTIONS.md_working_3.datrright">rright.bias</b>

<span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=10

<span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=CMUMD_log

... PRINT
</pre>
 {% endraw %} 



We can run a CMUMD simulation under these conditions as: 



````

gmx_mpi mdrun --plumed cmumd_diff.dat

````



### Try on your own 



Perform simulations at varying concentration differences.

Compute the concentration gradient across the simulation box as a function of the concentration difference between left and right controlled volumes.



### Available data 



In the folder `data`:

- `LJ_diffusion.gro`: reference conformation of 1000 LJ particles.

- `LJ_diffusion.xtc`: trajectory evolving under the effect of the stationary concentration gradient. 

 

## Exercise 4: Steady-state condensation process with C$\mu$MD



The fourth exercise combines aspects of the previous three. We will use CmuMD to control the driving force associated with the growth of a dense phase represented by a slab at the center of a simulation box. 



Similarly to the diffusion case the plumed file that can be used to perform this type of simulation reads: 



{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_4.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_4.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_4.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span style="color:blue" class="comment"># Define groups of atoms</span>
<br/><b name="data/INSTRUCTIONS.md_working_4.datLJ" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datLJ","data/INSTRUCTIONS.md_working_4.datLJ","brown")'>LJ</b>: <span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the numerical indexes for the set of atoms in the group<i></i></span></span>=1001-2000:1



<span style="color:blue" class="comment"># Provide parameters for the CV</span>
<br/><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datLJ">The GROUP action with label <b>LJ</b> calculates something</span><b name="data/INSTRUCTIONS.md_working_4.datleft" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datleft","data/INSTRUCTIONS.md_working_4.datleft","brown")'>left</b>:  <span class="plumedtooltip" style="color:green">CMUMD<span class="right">This action is not part of PLUMED and was included by using a LOAD command <a href="https://www.plumed.org/doc-master/user-doc/html/LOAD" style="color:green">More details</a><i></i></span></span> GROUP=lj NSV=1 FIXED=0.4 DCR=0.25 CRSIZE=0.1 WF=0.0001  ASYMM=-1 NINT=0.1 NZ=291

<b name="data/INSTRUCTIONS.md_working_4.datright" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datright","data/INSTRUCTIONS.md_working_4.datright","brown")'>right</b>:  <span class="plumedtooltip" style="color:green">CMUMD<span class="right">This action is not part of PLUMED and was included by using a LOAD command <a href="https://www.plumed.org/doc-master/user-doc/html/LOAD" style="color:green">More details</a><i></i></span></span> GROUP=lj NSV=1 FIXED=0.6 DCR=0.25 CRSIZE=0.1 WF=0.0001  ASYMM=1 NINT=0.1 NZ=291



<span style="color:blue" class="comment"># CmuMD is implemented as a restraint on the densities of species in CR</span>
<br/><b name="data/INSTRUCTIONS.md_working_4.datleft" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datleft","data/INSTRUCTIONS.md_working_4.datleft","brown")'>left</b>:  <span class="plumedtooltip" style="color:green">RESTRAINT<span class="right">Adds harmonic and/or linear restraints on one or more variables. <a href="https://www.plumed.org/doc-master/user-doc/html/RESTRAINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values the harmonic restraint acts upon<i></i></span></span>=left <span class="plumedtooltip">AT<span class="right">the position of the restraint<i></i></span></span>=3. <span class="plumedtooltip">KAPPA<span class="right"> specifies that the restraint is harmonic and what the values of the force constants on each of the variables are<i></i></span></span>=2000.0 

<span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datleft">The RESTRAINT action with label <b>left</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">left.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">left.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_4.datright" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datright","data/INSTRUCTIONS.md_working_4.datright","brown")'>right</b>: <span class="plumedtooltip" style="color:green">RESTRAINT<span class="right">Adds harmonic and/or linear restraints on one or more variables. <a href="https://www.plumed.org/doc-master/user-doc/html/RESTRAINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values the harmonic restraint acts upon<i></i></span></span>=right <span class="plumedtooltip">AT<span class="right">the position of the restraint<i></i></span></span>=3. <span class="plumedtooltip">KAPPA<span class="right"> specifies that the restraint is harmonic and what the values of the force constants on each of the variables are<i></i></span></span>=2000.0 



<span style="color:blue" class="comment"># Report the densities and bias</span>
<br/><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datright">The RESTRAINT action with label <b>right</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">right.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">right.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> ...

<span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_4.datleft">left</b>,<b name="data/INSTRUCTIONS.md_working_4.datright">right</b>,rleft.bias,rright.bias

<span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=10

<span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=CMUMD_log

... PRINT
</pre>
 {% endraw %} 



### Available data 



In the folder `data`, a CmuMD trajectory ready for analysis can be found together with the gromacs input files necessary to setup and run it. 

- `LJ_slab.gro`: reference conformation of 1000 LJ particles.

- `LJ_slab.xtc`: trajectory evolving under the effect of the stationary concentration gradient. 

- `md_input_LJ_slab`: MD input files





### Try on your own 



- Setup and run CMUMD simulations for the LJ slab system at varying CR concentrations. 

- Use the multicolvar-based approach discussed in Ex1 to follow the condensation process.  

- Use the graph-based approach discussed in Ex2 to follow the condensation process.

- Monitor the density profile across the simulation box. 

