## Associating PIVs to system configurations 
The following example shows how to associate a [PIV](https://www.plumed.org/doc-master/user-doc/html/_p_i_v.html) to a system configuration: 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/PIV_distance.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="PIV_distance.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="PIV_distance.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">PIV<div class="right">Calculates the PIV-distance. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_i_v.html" style="color:green">More details</a><i></i></div></div> ...
<div class="tooltip">LABEL<div class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></div></div>=<b name="data/PIV_distance.md_working_1.datc1" onclick='showPath("data/PIV_distance.md_working_1.dat","data/PIV_distance.md_working_1.datc1","data/PIV_distance.md_working_1.datc1","brown")'>c1</b>
<div class="tooltip">PIVATOMS<div class="right">Number of atoms to use for PIV<i></i></div></div>=1
<div class="tooltip">ATOMTYPES<div class="right">The atom types to use for PIV<i></i></div></div>=O
<div class="tooltip">PRECISION<div class="right">the precision for approximating reals with integers in sorting<i></i></div></div>=1000
<div class="tooltip">REF_FILE<div class="right">PDB file name that contains the ith reference structure<i></i></div></div>=Liq.pdb
<div class="tooltip">SORT<div class="right">Whether to sort or not the PIV block<i></i></div></div>=1
<div class="tooltip">SWITCH1<div class="right">The switching functions parameter<i></i></div></div>={RATIONAL R_0=0.4 MM=12 NN=4}
<div class="tooltip">NLIST<div class="right"> Use a neighbor list for distance calculations<i></i></div></div>
<div class="tooltip">NL_CUTOFF<div class="right">Neighbor lists cutoff<i></i></div></div>=1.2
<div class="tooltip">NL_STRIDE<div class="right">Update neighbor lists every NL_STRIDE steps<i></i></div></div>=10
<div class="tooltip">NL_SKIN<div class="right">The maximum atom displacement tolerated for the neighbor lists update<i></i></div></div>=0.1
... PIV
<br/><span style="display:none;" id="data/PIV_distance.md_working_1.datc1">The PIV action with label <b>c1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c1.value</td><td>the PIV-distance</td></tr></table></span><div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/PIV_distance.md_working_1.datc1">c1</b> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=colvar.dat <div class="tooltip">FMT<div class="right">the format that should be used to output real numbers<i></i></div></div>=%15.6f
</pre>
 {% endraw %} 

Oxigen atoms (ATOMTYPES=O) are used for the [PIV](https://www.plumed.org/doc-master/user-doc/html/_p_i_v.html) construction, and neighbor lists (NLIST) are used for the calculation of atom-atom distances. Distances are then mapped into numbers from 0 to 1 usign a switching function (SWITCH1={RATIONAL R_0=0.4 MM=12 NN=4}) with a precision of $10^{-3}$ (PRECISION=1000). A complete description of all the keywords can be found [here](https://www.plumed.org/doc-v2.9/user-doc/html/_p_i_v.html). 

When including the example above into a file (e.g. plumed.dat) and running 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/PIV_distance.md_working_2.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="PIV_distance.md_working_2.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="PIV_distance.md_working_2.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">plumed<div class="right">Embed a separate PLUMED instance. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_l_u_m_e_d.html" style="color:green">More details</a><i></i></div></div> driver mf_pdb Ihpdb plumed plumeddat
</pre>
 {% endraw %} 
one gets the [PIV](https://www.plumed.org/doc-master/user-doc/html/_p_i_v.html) distance between the configurations specified in the Ih.pdb and Liq.pdb files. Please note that the order of atoms in Ih.pdb and Liq.pdb files must be the same. 

Check that if one computes the distance between two identical configurations the result is zero. 
