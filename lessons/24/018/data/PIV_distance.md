## Associating PIVs to system configurations
The following example shows how to associate a PIV to a system configuration:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/PIV_distance.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="PIV_distance.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="PIV_distance.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span class="plumedtooltip" style="color:green">PIV<span class="right">Calculates the PIV-distance. <a href="https://www.plumed.org/doc-master/user-doc/html/PIV" style="color:green">More details</a><i></i></span></span> ...
<span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/PIV_distance.md_working_1.datc1" onclick='showPath("data/PIV_distance.md_working_1.dat","data/PIV_distance.md_working_1.datc1","data/PIV_distance.md_working_1.datc1","brown")'>c1</b>
<span class="plumedtooltip">PIVATOMS<span class="right">Number of atoms to use for PIV<i></i></span></span>=1
<span class="plumedtooltip">ATOMTYPES<span class="right">The atom types to use for PIV<i></i></span></span>=O
<span class="plumedtooltip">PRECISION<span class="right">the precision for approximating reals with integers in sorting<i></i></span></span>=1000
<span class="plumedtooltip">REF_FILE<span class="right">PDB file name that contains the ith reference structure<i></i></span></span>=Liq.pdb
<span class="plumedtooltip">SORT<span class="right">Whether to sort or not the PIV block<i></i></span></span>=1
<span class="plumedtooltip">SWITCH1<span class="right">The switching functions parameter<i></i></span></span>={RATIONAL R_0=0.4 MM=12 NN=4}
<span class="plumedtooltip">NLIST<span class="right"> Use a neighbor list for distance calculations<i></i></span></span>
<span class="plumedtooltip">NL_CUTOFF<span class="right">Neighbor lists cutoff<i></i></span></span>=1.2
<span class="plumedtooltip">NL_STRIDE<span class="right">Update neighbor lists every NL_STRIDE steps<i></i></span></span>=10
<span class="plumedtooltip">NL_SKIN<span class="right">The maximum atom displacement tolerated for the neighbor lists update<i></i></span></span>=0.1
... PIV
<br/><span style="display:none;" id="data/PIV_distance.md_working_1.datc1">The PIV action with label <b>c1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c1.value</td><td>the PIV-distance</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/PIV_distance.md_working_1.datc1">c1</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar.dat <span class="plumedtooltip">FMT<span class="right"> the format that should be used to output real numbers<i></i></span></span>=%15.6f
</pre>
 {% endraw %} 

Oxigen atoms (ATOMTYPES=O) are used for the PIV construction, and neighbor lists (NLIST) are used for the calculation of atom-atom distances. Distances are then mapped into numbers from 0 to 1 usign a switching function (SWITCH1={RATIONAL R_0=0.4 MM=12 NN=4}) with a precision of $10^{-3}$ (PRECISION=1000). A complete description of all the keywords can be found [here](https://www.plumed.org/doc-v2.9/user-doc/html/_p_i_v.html).

When including the example above into a file (e.g. plumed.dat) and running 

{% raw %}
<pre class="plumedlisting">
<span id="cltool2defplumed_short"><b name="cltool2plumed" onclick='showPath("cltool2","cltool2plumed","cltool2plumed","brown")'>plumed</b> <span class="plumedtooltip" style="color:green">driver<span class="right">analyze trajectories with plumed This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("cltool2defplumed");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/driver">More details</a><i></i></span></span> <span class="plumedtooltip">--mf_pdb<span class="right"> molfile: the trajectory in pdb format <i></i></span></span> Ih.pdb <span class="plumedtooltip">--plumed<span class="right"> specify the name of the plumed input file<i></i></span></span> plumed.dat
 
</span><span id="cltool2defplumed_long" style="display:none;"><span style="display:none;" id="cltool2plumed">The driver action with label <b>plumed</b> calculates something</span><b name="cltool2plumed" onclick='showPath("cltool2","cltool2plumed","cltool2plumed","brown")'>plumed</b> <span class="plumedtooltip" style="color:green">driver<span class="right">analyze trajectories with plumed This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("cltool2defplumed");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/driver">More details</a><i></i></span></span> <span class="plumedtooltip">--mf_pdb<span class="right"> molfile: the trajectory in pdb format <i></i></span></span> Ih.pdb <span class="plumedtooltip">--plumed<span class="right"> specify the name of the plumed input file<i></i></span></span> plumed.dat
 <span class="plumedtooltip">--timestep<span class="right"> the timestep that was used in the calculation that produced this trajectory in picoseconds<i></i></span></span> 1.0 <span class="plumedtooltip">--trajectory-stride<span class="right"> the frequency with which frames were output to this trajectory during the simulation (0 means that the number of the step is read from the trajectory file, currently working only for xtc/trr files read with --ixtc/--trr)<i></i></span></span> 1 <span class="plumedtooltip">--multi<span class="right"> set number of replicas for multi environment (needs MPI)<i></i></span></span> 0 <span class="plumedtooltip">--dump-forces-fmt<span class="right"> the format to use to dump the forces<i></i></span></span> %%f 
</span></pre>
 {% endraw %} 
one gets the PIV distance between the configurations specified in the Ih.pdb and Liq.pdb files. Please note that the order of atoms in Ih.pdb and Liq.pdb files must be the same.

Check that if one computes the distance between two identical configurations the result is zero.
