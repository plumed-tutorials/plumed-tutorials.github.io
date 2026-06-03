##### [&larr; Home](NAVIGATION.md)

### Input

Files needed to complete this tutorial are provided in the `data` directory available in the [GitHub repository](https://github.com/jakryd/plumed2-maze-tutorial).

#### Groups

We first define the groups of atoms consisting of T4L (atoms 1-2634) and benzene (atoms 2635-2646) and their center of masses. These definitions will be passed to an optimizer later. 

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/input.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="input.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="input.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the numerical indexes for the set of atoms in the group<i></i></span></span>=2635-2646 <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_1.datgroup_bnz" onclick='showPath("data/input.md_working_1.dat","data/input.md_working_1.datgroup_bnz","data/input.md_working_1.datgroup_bnz","violet")'>group_bnz</b><span style="display:none;" id="data/input.md_working_1.datgroup_bnz">The GROUP action with label <b>group_bnz</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">group_bnz</td><td width="5%"><font color="violet">atoms</font></td><td>indices of atoms specified in GROUP</td></tr></table></span>
<span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the numerical indexes for the set of atoms in the group<i></i></span></span>=1-2634 <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_1.datgroup_t4l" onclick='showPath("data/input.md_working_1.dat","data/input.md_working_1.datgroup_t4l","data/input.md_working_1.datgroup_t4l","violet")'>group_t4l</b><span style="display:none;" id="data/input.md_working_1.datgroup_t4l">The GROUP action with label <b>group_t4l</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">group_t4l</td><td width="5%"><font color="violet">atoms</font></td><td>indices of atoms specified in GROUP</td></tr></table></span>
<br/><span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=<b name="data/input.md_working_1.datgroup_bnz">group_bnz</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_1.datcenter_bnz" onclick='showPath("data/input.md_working_1.dat","data/input.md_working_1.datcenter_bnz","data/input.md_working_1.datcenter_bnz","violet")'>center_bnz</b><span style="display:none;" id="data/input.md_working_1.datcenter_bnz">The CENTER_FAST action with label <b>center_bnz</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">center_bnz</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by CENTER_FAST action</td></tr></table></span>
<span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=<b name="data/input.md_working_1.datgroup_t4l">group_t4l</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_1.datcenter_t4l" onclick='showPath("data/input.md_working_1.dat","data/input.md_working_1.datcenter_t4l","data/input.md_working_1.datcenter_t4l","violet")'>center_t4l</b><span style="display:none;" id="data/input.md_working_1.datcenter_t4l">The CENTER_FAST action with label <b>center_t4l</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">center_t4l</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by CENTER_FAST action</td></tr></table></span>
</pre>
 {% endraw %} 

#### Optimizer and Loss Function

Next, we declare an optimizer that will find a suboptimal (in terms of loss function) unbinding direction for the ligand. For this purpose, we will use the simulated annealing algorithm (`MAZE_OPT_ANNEALING`). The optimization will be run during the MD simulation every `STRIDE` MD steps (here 1 ns) with 1000 iterations to converge (`N_ITER`).

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/input.md_working_2.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="input.md_working_2.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="input.md_working_2.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/input.md_working_2.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/input.md_working_2.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/input.md_working_2.dat_hiddenpart1_long" style="display:none;"><span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the numerical indexes for the set of atoms in the group<i></i></span></span>=2635-2646 <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_2.datgroup_bnz" onclick='showPath("data/input.md_working_2.dat","data/input.md_working_2.datgroup_bnz","data/input.md_working_2.datgroup_bnz","brown")'>group_bnz</b>
<span style="display:none;" id="data/input.md_working_2.datgroup_bnz">The GROUP action with label <b>group_bnz</b> calculates something</span><span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the numerical indexes for the set of atoms in the group<i></i></span></span>=1-2634 <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_2.datgroup_t4l" onclick='showPath("data/input.md_working_2.dat","data/input.md_working_2.datgroup_t4l","data/input.md_working_2.datgroup_t4l","brown")'>group_t4l</b>
<br/><span style="display:none;" id="data/input.md_working_2.datgroup_t4l">The GROUP action with label <b>group_t4l</b> calculates something</span><span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=<b name="data/input.md_working_2.datgroup_bnz">group_bnz</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_2.datcenter_bnz" onclick='showPath("data/input.md_working_2.dat","data/input.md_working_2.datcenter_bnz","data/input.md_working_2.datcenter_bnz","brown")'>center_bnz</b>
<span style="display:none;" id="data/input.md_working_2.datcenter_bnz">The CENTER action with label <b>center_bnz</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">center_bnz.value</td><td>the position of the center of mass</td></tr></table></span><span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=<b name="data/input.md_working_2.datgroup_t4l">group_t4l</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_2.datcenter_t4l" onclick='showPath("data/input.md_working_2.dat","data/input.md_working_2.datcenter_t4l","data/input.md_working_2.datcenter_t4l","brown")'>center_t4l</b>
<a class="toggler" style="color:red" onclick='toggleDisplay("data/input.md_working_2.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span style="display:none;" id="data/input.md_working_2.datcenter_t4l">The CENTER action with label <b>center_t4l</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">center_t4l.value</td><td>the position of the center of mass</td></tr></table></span><span class="plumedtooltip" style="color:green">MAZE_OPT_ANNEALING<span class="right">This action is not part of PLUMED and was included by using a LOAD command <a href="https://www.plumed.org/doc-master/user-doc/html/LOAD" style="color:green">More details</a><i></i></span></span> ...
  LABEL=<b name="data/input.md_working_2.datopt" onclick='showPath("data/input.md_working_2.dat","data/input.md_working_2.datopt","data/input.md_working_2.datopt","brown")'>opt</b>

  GROUPA=<b name="data/input.md_working_2.datgroup_bnz">group_bnz</b>
  GROUPB=<b name="data/input.md_working_2.datgroup_t4l">group_t4l</b>

  SWITCH={EXP R_0=0.2}

  STRIDE=500000

  N_ITER=1000

  BETA=0.9
  BETA_FACTOR=1.005
  BETA_SCHEDULE=GEOM

  RANDOM_SEED=111
  
  NLIST
  NL_CUTOFF=0.6
  NL_STRIDE=100
...
<span style="display:none;" id="data/input.md_working_2.datopt">The MAZE_OPT_ANNEALING action with label <b>opt</b> calculates something</span></pre>
 {% endraw %} 

The `BETA` options are required to select an annealing scheme. Here, we will start with an inverse temperature parameter $\beta=0.9$ multiplied by a factor of 1.005 every iteration (`BETA_SCHEDULE=GEOM`). This is a standard setup -- interested readers can read more about it [here](https://en.wikipedia.org/wiki/Simulated_annealing)).

To speed up calculations, we will use a neighbor list `NLIST` with a cutoff of 0.6 nm for distances between ligand-protein atom pairs (see [PLUMED Neighbor Lists](https://www.plumed.org/doc-v2.9/user-doc/html/_neighbour.html)). The neighbor list will be recalculated every 100 steps (`NL_STRIDE`).

The `SWITCH` keyword specifies the loss function to optimize. The same functionality is provided for switching functions required to define collective variables such as coordination numbers. See [here](https://www.plumed.org/doc-v2.9/user-doc/html/switchingfunction.html) for switching functions available in PLUMED. Here, we will use an exponential loss function as explained in [Background](background.md).

#### Bias

Having defined the optimizer, we will pass it to the adaptive bias potential (see [here](background.md#adaptive-biasing)). The bias will be used to steer benzene in the optimal direction found by simulated annealing. This also requires a collective variable with Cartesian components to drive the ligand toward solvent. 

*Note* Biasing absolute positions of any system can result in problems (see a detailed explanation [here](https://www.plumed.org/doc-v2.9/user-doc/html/_p_o_s_i_t_i_o_n.html)) and may require additional position restraints. Thus, it is required that it must be a distance with `COMPONENTS`. As such, the biasing corresponds to a relative position, and additional restraints are not required. 

The `HEIGHT` and `RATE` keywords give the scale constant and rate, respectively.

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/input.md_working_3.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="input.md_working_3.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="input.md_working_3.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/input.md_working_3.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/input.md_working_3.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/input.md_working_3.dat_hiddenpart1_long" style="display:none;"><span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the numerical indexes for the set of atoms in the group<i></i></span></span>=2635-2646 <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_3.datgroup_bnz" onclick='showPath("data/input.md_working_3.dat","data/input.md_working_3.datgroup_bnz","data/input.md_working_3.datgroup_bnz","brown")'>group_bnz</b>
<span style="display:none;" id="data/input.md_working_3.datgroup_bnz">The GROUP action with label <b>group_bnz</b> calculates something</span><span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the numerical indexes for the set of atoms in the group<i></i></span></span>=1-2634 <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_3.datgroup_t4l" onclick='showPath("data/input.md_working_3.dat","data/input.md_working_3.datgroup_t4l","data/input.md_working_3.datgroup_t4l","brown")'>group_t4l</b>
<br/><span style="display:none;" id="data/input.md_working_3.datgroup_t4l">The GROUP action with label <b>group_t4l</b> calculates something</span><span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=<b name="data/input.md_working_3.datgroup_bnz">group_bnz</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_3.datcenter_bnz" onclick='showPath("data/input.md_working_3.dat","data/input.md_working_3.datcenter_bnz","data/input.md_working_3.datcenter_bnz","brown")'>center_bnz</b>
<span style="display:none;" id="data/input.md_working_3.datcenter_bnz">The CENTER action with label <b>center_bnz</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">center_bnz.value</td><td>the position of the center of mass</td></tr></table></span><span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=<b name="data/input.md_working_3.datgroup_t4l">group_t4l</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_3.datcenter_t4l" onclick='showPath("data/input.md_working_3.dat","data/input.md_working_3.datcenter_t4l","data/input.md_working_3.datcenter_t4l","brown")'>center_t4l</b>
<br/><span style="display:none;" id="data/input.md_working_3.datcenter_t4l">The CENTER action with label <b>center_t4l</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">center_t4l.value</td><td>the position of the center of mass</td></tr></table></span><span class="plumedtooltip" style="color:green">MAZE_OPT_ANNEALING<span class="right">This action is not part of PLUMED and was included by using a LOAD command <a href="https://www.plumed.org/doc-master/user-doc/html/LOAD" style="color:green">More details</a><i></i></span></span> ...
  LABEL=<b name="data/input.md_working_3.datopt" onclick='showPath("data/input.md_working_3.dat","data/input.md_working_3.datopt","data/input.md_working_3.datopt","brown")'>opt</b>

  GROUPA=<b name="data/input.md_working_3.datgroup_bnz">group_bnz</b>
  GROUPB=<b name="data/input.md_working_3.datgroup_t4l">group_t4l</b>

  SWITCH={EXP R_0=0.2}

  STRIDE=500000

  N_ITER=1000

  BETA=0.9
  BETA_FACTOR=1.005
  BETA_SCHEDULE=GEOM

  RANDOM_SEED=111
  
  NLIST
  NL_CUTOFF=0.6
  NL_STRIDE=100
...
<a class="toggler" style="color:red" onclick='toggleDisplay("data/input.md_working_3.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=<b name="data/input.md_working_3.datcenter_bnz">center_bnz</b>,<b name="data/input.md_working_3.datcenter_t4l">center_t4l</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_3.datdist" onclick='showPath("data/input.md_working_3.dat","data/input.md_working_3.datdist","data/input.md_working_3.datdist","brown")'>dist</b> <span class="plumedtooltip">COMPONENTS<span class="right"> calculate the x, y and z components of the distance separately and store them as label<i></i></span></span>
<br/><span style="display:none;" id="data/input.md_working_3.datdist">The DISTANCE action with label <b>dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist.x</td><td>the x-component of the vector connecting the two atoms</td></tr><tr><td width="5%">dist.y</td><td>the y-component of the vector connecting the two atoms</td></tr><tr><td width="5%">dist.z</td><td>the z-component of the vector connecting the two atoms</td></tr><tr><td width="5%">dist.value</td><td>the DISTANCE between this pair of atoms</td></tr></table></span><span class="plumedtooltip" style="color:green">MAZE_OPT_BIAS<span class="right">This action is not part of PLUMED and was included by using a LOAD command <a href="https://www.plumed.org/doc-master/user-doc/html/LOAD" style="color:green">More details</a><i></i></span></span> ...
  LABEL=<b name="data/input.md_working_3.datbias" onclick='showPath("data/input.md_working_3.dat","data/input.md_working_3.datbias","data/input.md_working_3.datbias","brown")'>bias</b>

  ARG=<b name="data/input.md_working_3.datdist">dist.x</b>,<b name="data/input.md_working_3.datdist">dist.y</b>,<b name="data/input.md_working_3.datdist">dist.z</b>

  HEIGHT=1000.0

  RATE=0.001

  OPTIMIZER=opt
...
<span style="display:none;" id="data/input.md_working_3.datbias">The MAZE_OPT_BIAS action with label <b>bias</b> calculates something</span></pre>
 {% endraw %} 

We will also define a committor indicator to halt the simulation once benzene enters the solvent, which occurs approximately when the distance between the ligand and the protein exceeds 3 nm.

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/input.md_working_4.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="input.md_working_4.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="input.md_working_4.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/input.md_working_4.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/input.md_working_4.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/input.md_working_4.dat_hiddenpart1_long" style="display:none;"><span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the numerical indexes for the set of atoms in the group<i></i></span></span>=2635-2646 <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_4.datgroup_bnz" onclick='showPath("data/input.md_working_4.dat","data/input.md_working_4.datgroup_bnz","data/input.md_working_4.datgroup_bnz","violet")'>group_bnz</b><span style="display:none;" id="data/input.md_working_4.datgroup_bnz">The GROUP action with label <b>group_bnz</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">group_bnz</td><td width="5%"><font color="violet">atoms</font></td><td>indices of atoms specified in GROUP</td></tr></table></span>
<span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the numerical indexes for the set of atoms in the group<i></i></span></span>=1-2634 <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_4.datgroup_t4l" onclick='showPath("data/input.md_working_4.dat","data/input.md_working_4.datgroup_t4l","data/input.md_working_4.datgroup_t4l","violet")'>group_t4l</b><span style="display:none;" id="data/input.md_working_4.datgroup_t4l">The GROUP action with label <b>group_t4l</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">group_t4l</td><td width="5%"><font color="violet">atoms</font></td><td>indices of atoms specified in GROUP</td></tr></table></span>
<br/><span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=<b name="data/input.md_working_4.datgroup_bnz">group_bnz</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_4.datcenter_bnz" onclick='showPath("data/input.md_working_4.dat","data/input.md_working_4.datcenter_bnz","data/input.md_working_4.datcenter_bnz","violet")'>center_bnz</b><span style="display:none;" id="data/input.md_working_4.datcenter_bnz">The CENTER_FAST action with label <b>center_bnz</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">center_bnz</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by CENTER_FAST action</td></tr></table></span>
<span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=<b name="data/input.md_working_4.datgroup_t4l">group_t4l</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_4.datcenter_t4l" onclick='showPath("data/input.md_working_4.dat","data/input.md_working_4.datcenter_t4l","data/input.md_working_4.datcenter_t4l","violet")'>center_t4l</b><span style="display:none;" id="data/input.md_working_4.datcenter_t4l">The CENTER_FAST action with label <b>center_t4l</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">center_t4l</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by CENTER_FAST action</td></tr></table></span>
<a class="toggler" style="color:red" onclick='toggleDisplay("data/input.md_working_4.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=<b name="data/input.md_working_4.datcenter_bnz">center_bnz</b>,<b name="data/input.md_working_4.datcenter_t4l">center_t4l</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/input.md_working_4.datdist_d" onclick='showPath("data/input.md_working_4.dat","data/input.md_working_4.datdist_d","data/input.md_working_4.datdist_d","black")'>dist_d</b><span style="display:none;" id="data/input.md_working_4.datdist_d">The DISTANCE action with label <b>dist_d</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist_d</td><td width="5%"><font color="black">scalar</font></td><td>the DISTANCE between this pair of atoms</td></tr></table></span>
<br/><span class="plumedtooltip" style="color:green">COMMITTOR<span class="right">Does a committor analysis. <a href="https://www.plumed.org/doc-master/user-doc/html/COMMITTOR" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">ARG<span class="right">the labels of the values which is being used to define the committor surface<i></i></span></span>=<b name="data/input.md_working_4.datdist_d">dist_d</b>
  <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the CVs are analyzed<i></i></span></span>=5000
  <span class="plumedtooltip">BASIN_LL1<span class="right">List of lower limits for basin #<i></i></span></span>=3
  <span class="plumedtooltip">BASIN_UL1<span class="right">List of upper limits for basin #<i></i></span></span>=10
...
</pre>
 {% endraw %} 

#### Simulation

We are ready to run the simulation.

The simulation will save two files: `colvar.dat` and `optimizer.dat`. The `colvar.dat` file contains all the information we want to save using the `PRINT` action, while the `optimizer.dat` file contains data related to the optimization results (see [here](https://github.com/jakryd/plumed2-maze-tutorial/tree/main/data)).

##### [Results &rarr;](results.md)
