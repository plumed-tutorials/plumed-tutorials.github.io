## Mapping a trajectory into PIV-PathCV space 

The simplest version of PathCV needs the specification of two reference configurations, and for each of them one can compute the [PIV](https://www.plumed.org/doc-master/user-doc/html/_p_i_v.html) as follows 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/PIV-PathCV_driver.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="PIV-PathCV_driver.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="PIV-PathCV_driver.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">PIV<div class="right">Calculates the PIV-distance. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_i_v.html" style="color:green">More details</a><i></i></div></div> ...
<div class="tooltip">LABEL<div class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></div></div>=<b name="data/PIV-PathCV_driver.md_working_1.datc1" onclick='showPath("data/PIV-PathCV_driver.md_working_1.dat","data/PIV-PathCV_driver.md_working_1.datc1","data/PIV-PathCV_driver.md_working_1.datc1","brown")'>c1</b>
<div class="tooltip">PRECISION<div class="right">the precision for approximating reals with integers in sorting<i></i></div></div>=1000
<div class="tooltip">VOLUME<div class="right">Scale atom-atom distances by the cubic root of the cell volume<i></i></div></div>=4.589575
<div class="tooltip">REF_FILE<div class="right">PDB file name that contains the ith reference structure<i></i></div></div>=Liq.pdb
<div class="tooltip">PIVATOMS<div class="right">Number of atoms to use for PIV<i></i></div></div>=2
<div class="tooltip">ATOMTYPES<div class="right">The atom types to use for PIV<i></i></div></div>=OW1,HW
<div class="tooltip">SORT<div class="right">Whether to sort or not the PIV block<i></i></div></div>=1,1,1
<div class="tooltip">SWITCH1<div class="right">The switching functions parameter<i></i></div></div>={RATIONAL R_0=0.4 MM=18 NN=4}
<div class="tooltip">SWITCH2<div class="right">The switching functions parameter<i></i></div></div>={RATIONAL R_0=0.4 MM=18 NN=4}
<div class="tooltip">SWITCH3<div class="right">The switching functions parameter<i></i></div></div>={RATIONAL R_0=0.4 MM=18 NN=4}
<div class="tooltip">NLIST<div class="right"> Use a neighbor list for distance calculations<i></i></div></div>
<div class="tooltip">NL_CUTOFF<div class="right">Neighbor lists cutoff<i></i></div></div>=0.6,0.6,0.6
<div class="tooltip">NL_STRIDE<div class="right">Update neighbor lists every NL_STRIDE steps<i></i></div></div>=10,10,10
<div class="tooltip">NL_SKIN<div class="right">The maximum atom displacement tolerated for the neighbor lists update<i></i></div></div>=0.1,0.1,0.1
<div class="tooltip">UPDATEPIV<div class="right">Frequency (in steps) at which the PIV is updated<i></i></div></div>=10
... PIV

<br/><span style="display:none;" id="data/PIV-PathCV_driver.md_working_1.datc1">The PIV action with label <b>c1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c1.value</td><td>the PIV-distance</td></tr></table></span><div class="tooltip" style="color:green">PIV<div class="right">Calculates the PIV-distance. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_i_v.html" style="color:green">More details</a><i></i></div></div> ...
<div class="tooltip">LABEL<div class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></div></div>=<b name="data/PIV-PathCV_driver.md_working_1.datc2" onclick='showPath("data/PIV-PathCV_driver.md_working_1.dat","data/PIV-PathCV_driver.md_working_1.datc2","data/PIV-PathCV_driver.md_working_1.datc2","brown")'>c2</b>
<div class="tooltip">PRECISION<div class="right">the precision for approximating reals with integers in sorting<i></i></div></div>=1000
<div class="tooltip">VOLUME<div class="right">Scale atom-atom distances by the cubic root of the cell volume<i></i></div></div>=4.589575
<div class="tooltip">REF_FILE<div class="right">PDB file name that contains the ith reference structure<i></i></div></div>=Ih.pdb
<div class="tooltip">PIVATOMS<div class="right">Number of atoms to use for PIV<i></i></div></div>=2
<div class="tooltip">ATOMTYPES<div class="right">The atom types to use for PIV<i></i></div></div>=OW1,HW
<div class="tooltip">SORT<div class="right">Whether to sort or not the PIV block<i></i></div></div>=1,1,1
<div class="tooltip">SWITCH1<div class="right">The switching functions parameter<i></i></div></div>={RATIONAL R_0=0.4 MM=18 NN=4}
<div class="tooltip">SWITCH2<div class="right">The switching functions parameter<i></i></div></div>={RATIONAL R_0=0.4 MM=18 NN=4}
<div class="tooltip">SWITCH3<div class="right">The switching functions parameter<i></i></div></div>={RATIONAL R_0=0.4 MM=18 NN=4}
<div class="tooltip">NLIST<div class="right"> Use a neighbor list for distance calculations<i></i></div></div>
<div class="tooltip">NL_CUTOFF<div class="right">Neighbor lists cutoff<i></i></div></div>=0.6,0.6,0.6
<div class="tooltip">NL_STRIDE<div class="right">Update neighbor lists every NL_STRIDE steps<i></i></div></div>=10,10,10
<div class="tooltip">NL_SKIN<div class="right">The maximum atom displacement tolerated for the neighbor lists update<i></i></div></div>=0.1,0.1,0.1
<div class="tooltip">UPDATEPIV<div class="right">Frequency (in steps) at which the PIV is updated<i></i></div></div>=10
... PIV
<span style="display:none;" id="data/PIV-PathCV_driver.md_working_1.datc2">The PIV action with label <b>c2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c2.value</td><td>the PIV-distance</td></tr></table></span></pre>
 {% endraw %} 

here the [PIV](https://www.plumed.org/doc-master/user-doc/html/_p_i_v.html) is computed using Hydrogen (HW) and Oxygen (OW) atoms as named in the Ih.pdb and Liq.pdb files. The [PIV](https://www.plumed.org/doc-master/user-doc/html/_p_i_v.html) version of the example above uses distances scaled by the cubic root of the ratio between a reference volume (VOLUME=4.589575) and the volume of the cell along the trajectory. 

PIV-PathCV collective variables (s and z) can then be computed by adding to the plumed.dat file the following lines: 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/PIV-PathCV_driver.md_working_2.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="PIV-PathCV_driver.md_working_2.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="PIV-PathCV_driver.md_working_2.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<b name="data/PIV-PathCV_driver.md_working_2.datp1" onclick='showPath("data/PIV-PathCV_driver.md_working_2.dat","data/PIV-PathCV_driver.md_working_2.datp1","data/PIV-PathCV_driver.md_working_2.datp1","brown")'>p1</b>: <div class="tooltip" style="color:green">FUNCPATHMSD<div class="right">This function calculates path collective variables. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_u_n_c_p_a_t_h_m_s_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the values from which the function is calculated<i></i></div></div>=c1,c2 <div class="tooltip">LAMBDA<div class="right">the lambda parameter is needed for smoothing, is in the units of plumed<i></i></div></div>=0.0810475
<span style="display:none;" id="data/PIV-PathCV_driver.md_working_2.datp1">The FUNCPATHMSD action with label <b>p1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">p1.s</td><td>the position on the path</td></tr><tr><td width="5%">p1.z</td><td>the distance from the path</td></tr></table></span><div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=c1,c2,<b name="data/PIV-PathCV_driver.md_working_2.datp1">p1.s</b>,<b name="data/PIV-PathCV_driver.md_working_2.datp1">p1.z</b> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=colvar.dat <div class="tooltip">FMT<div class="right">the format that should be used to output real numbers<i></i></div></div>=%15.6f
</pre>
 {% endraw %} 

Compute the the values of the PIV-PathCV along the provided trajectory (traj.xtc) as a function of time using the plumed driver: 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/PIV-PathCV_driver.md_working_3.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="PIV-PathCV_driver.md_working_3.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="PIV-PathCV_driver.md_working_3.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">plumed<div class="right">Embed a separate PLUMED instance. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_l_u_m_e_d.html" style="color:green">More details</a><i></i></div></div> driver mf_xtc trajxtc plumed plumeddat
</pre>
 {% endraw %} 
Please note that atoms need to be listed in the same order in all reference files and in the trajectory. 
