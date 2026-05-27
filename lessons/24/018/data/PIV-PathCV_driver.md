## Mapping a trajectory into PIV-PathCV space

The simplest version of PathCV needs the specification of two reference configurations, and for each of them one can compute the PIV as follows

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/PIV-PathCV_driver.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="PIV-PathCV_driver.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="PIV-PathCV_driver.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span class="plumedtooltip" style="color:green">PIV<span class="right">Calculates the PIV-distance. <a href="https://www.plumed.org/doc-master/user-doc/html/PIV" style="color:green">More details</a><i></i></span></span> ...
<span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/PIV-PathCV_driver.md_working_1.datc1" onclick='showPath("data/PIV-PathCV_driver.md_working_1.dat","data/PIV-PathCV_driver.md_working_1.datc1","data/PIV-PathCV_driver.md_working_1.datc1","brown")'>c1</b>
<span class="plumedtooltip">PRECISION<span class="right">the precision for approximating reals with integers in sorting<i></i></span></span>=1000
<span class="plumedtooltip">VOLUME<span class="right">Scale atom-atom distances by the cubic root of the cell volume<i></i></span></span>=4.589575
<span class="plumedtooltip">REF_FILE<span class="right">PDB file name that contains the ith reference structure<i></i></span></span>=Liq.pdb
<span class="plumedtooltip">PIVATOMS<span class="right">Number of atoms to use for PIV<i></i></span></span>=2
<span class="plumedtooltip">ATOMTYPES<span class="right">The atom types to use for PIV<i></i></span></span>=OW1,HW
<span class="plumedtooltip">SORT<span class="right">Whether to sort or not the PIV block<i></i></span></span>=1,1,1
<span class="plumedtooltip">SWITCH1<span class="right">The switching functions parameter<i></i></span></span>={RATIONAL R_0=0.4 MM=18 NN=4}
<span class="plumedtooltip">SWITCH2<span class="right">The switching functions parameter<i></i></span></span>={RATIONAL R_0=0.4 MM=18 NN=4}
<span class="plumedtooltip">SWITCH3<span class="right">The switching functions parameter<i></i></span></span>={RATIONAL R_0=0.4 MM=18 NN=4}
<span class="plumedtooltip">NLIST<span class="right"> Use a neighbor list for distance calculations<i></i></span></span>
<span class="plumedtooltip">NL_CUTOFF<span class="right">Neighbor lists cutoff<i></i></span></span>=0.6,0.6,0.6
<span class="plumedtooltip">NL_STRIDE<span class="right">Update neighbor lists every NL_STRIDE steps<i></i></span></span>=10,10,10
<span class="plumedtooltip">NL_SKIN<span class="right">The maximum atom displacement tolerated for the neighbor lists update<i></i></span></span>=0.1,0.1,0.1
<span class="plumedtooltip">UPDATEPIV<span class="right">Frequency (in steps) at which the PIV is updated<i></i></span></span>=10
... PIV

<br/><span style="display:none;" id="data/PIV-PathCV_driver.md_working_1.datc1">The PIV action with label <b>c1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c1.value</td><td>the PIV-distance</td></tr></table></span><span class="plumedtooltip" style="color:green">PIV<span class="right">Calculates the PIV-distance. <a href="https://www.plumed.org/doc-master/user-doc/html/PIV" style="color:green">More details</a><i></i></span></span> ...
<span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/PIV-PathCV_driver.md_working_1.datc2" onclick='showPath("data/PIV-PathCV_driver.md_working_1.dat","data/PIV-PathCV_driver.md_working_1.datc2","data/PIV-PathCV_driver.md_working_1.datc2","brown")'>c2</b>
<span class="plumedtooltip">PRECISION<span class="right">the precision for approximating reals with integers in sorting<i></i></span></span>=1000
<span class="plumedtooltip">VOLUME<span class="right">Scale atom-atom distances by the cubic root of the cell volume<i></i></span></span>=4.589575
<span class="plumedtooltip">REF_FILE<span class="right">PDB file name that contains the ith reference structure<i></i></span></span>=Ih.pdb
<span class="plumedtooltip">PIVATOMS<span class="right">Number of atoms to use for PIV<i></i></span></span>=2
<span class="plumedtooltip">ATOMTYPES<span class="right">The atom types to use for PIV<i></i></span></span>=OW1,HW
<span class="plumedtooltip">SORT<span class="right">Whether to sort or not the PIV block<i></i></span></span>=1,1,1
<span class="plumedtooltip">SWITCH1<span class="right">The switching functions parameter<i></i></span></span>={RATIONAL R_0=0.4 MM=18 NN=4}
<span class="plumedtooltip">SWITCH2<span class="right">The switching functions parameter<i></i></span></span>={RATIONAL R_0=0.4 MM=18 NN=4}
<span class="plumedtooltip">SWITCH3<span class="right">The switching functions parameter<i></i></span></span>={RATIONAL R_0=0.4 MM=18 NN=4}
<span class="plumedtooltip">NLIST<span class="right"> Use a neighbor list for distance calculations<i></i></span></span>
<span class="plumedtooltip">NL_CUTOFF<span class="right">Neighbor lists cutoff<i></i></span></span>=0.6,0.6,0.6
<span class="plumedtooltip">NL_STRIDE<span class="right">Update neighbor lists every NL_STRIDE steps<i></i></span></span>=10,10,10
<span class="plumedtooltip">NL_SKIN<span class="right">The maximum atom displacement tolerated for the neighbor lists update<i></i></span></span>=0.1,0.1,0.1
<span class="plumedtooltip">UPDATEPIV<span class="right">Frequency (in steps) at which the PIV is updated<i></i></span></span>=10
... PIV
<span style="display:none;" id="data/PIV-PathCV_driver.md_working_1.datc2">The PIV action with label <b>c2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c2.value</td><td>the PIV-distance</td></tr></table></span></pre>
 {% endraw %} 

here the PIV is computed using Hydrogen (HW) and Oxygen (OW) atoms as named in the Ih.pdb and Liq.pdb files. The PIV version of the example above uses distances scaled by the cubic root of the ratio between a reference volume (VOLUME=4.589575) and the volume of the cell along the trajectory. 

PIV-PathCV collective variables (s and z) can then be computed by adding to the plumed.dat file the following lines:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/PIV-PathCV_driver.md_working_2.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="PIV-PathCV_driver.md_working_2.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="PIV-PathCV_driver.md_working_2.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<b name="data/PIV-PathCV_driver.md_working_2.datp1" onclick='showPath("data/PIV-PathCV_driver.md_working_2.dat","data/PIV-PathCV_driver.md_working_2.datp1","data/PIV-PathCV_driver.md_working_2.datp1","brown")'>p1</b>: <span class="plumedtooltip" style="color:green">FUNCPATHMSD<span class="right">This function calculates path collective variables. <a href="https://www.plumed.org/doc-master/user-doc/html/FUNCPATHMSD" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values from which the function is calculated<i></i></span></span>=c1,c2 <span class="plumedtooltip">LAMBDA<span class="right">the lambda parameter is needed for smoothing, is in the units of plumed<i></i></span></span>=0.0810475
<span style="display:none;" id="data/PIV-PathCV_driver.md_working_2.datp1">The FUNCPATHMSD action with label <b>p1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">p1.s</td><td>the position on the path</td></tr><tr><td width="5%">p1.z</td><td>the distance from the path</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=c1,c2,<b name="data/PIV-PathCV_driver.md_working_2.datp1">p1.s</b>,<b name="data/PIV-PathCV_driver.md_working_2.datp1">p1.z</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar.dat <span class="plumedtooltip">FMT<span class="right"> the format that should be used to output real numbers<i></i></span></span>=%15.6f
</pre>
 {% endraw %} 

Compute the the values of the PIV-PathCV along the provided trajectory (traj.xtc) as a function of time using the plumed driver:

{% raw %}
<pre class="plumedlisting">
<span id="cltool3defplumed_short"><b name="cltool3plumed" onclick='showPath("cltool3","cltool3plumed","cltool3plumed","brown")'>plumed</b> <span class="plumedtooltip" style="color:green">driver<span class="right">analyze trajectories with plumed This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("cltool3defplumed");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/driver">More details</a><i></i></span></span> <span class="plumedtooltip">--mf_xtc<span class="right"> molfile: the trajectory in xtc format <i></i></span></span> traj.xtc <span class="plumedtooltip">--plumed<span class="right"> specify the name of the plumed input file<i></i></span></span> plumed.dat
 
</span><span id="cltool3defplumed_long" style="display:none;"><span style="display:none;" id="cltool3plumed">The driver action with label <b>plumed</b> calculates something</span><b name="cltool3plumed" onclick='showPath("cltool3","cltool3plumed","cltool3plumed","brown")'>plumed</b> <span class="plumedtooltip" style="color:green">driver<span class="right">analyze trajectories with plumed This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("cltool3defplumed");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/driver">More details</a><i></i></span></span> <span class="plumedtooltip">--mf_xtc<span class="right"> molfile: the trajectory in xtc format <i></i></span></span> traj.xtc <span class="plumedtooltip">--plumed<span class="right"> specify the name of the plumed input file<i></i></span></span> plumed.dat
 <span class="plumedtooltip">--timestep<span class="right"> the timestep that was used in the calculation that produced this trajectory in picoseconds<i></i></span></span> 1.0 <span class="plumedtooltip">--trajectory-stride<span class="right"> the frequency with which frames were output to this trajectory during the simulation (0 means that the number of the step is read from the trajectory file, currently working only for xtc/trr files read with --ixtc/--trr)<i></i></span></span> 1 <span class="plumedtooltip">--multi<span class="right"> set number of replicas for multi environment (needs MPI)<i></i></span></span> 0 <span class="plumedtooltip">--dump-forces-fmt<span class="right"> the format to use to dump the forces<i></i></span></span> %%f 
</span></pre>
 {% endraw %} 
Please note that atoms need to be listed in the same order in all reference files and in the trajectory.
