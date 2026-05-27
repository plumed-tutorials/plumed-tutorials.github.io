# Calculating the number of atoms/average CV in a part of the cell

There are times when you want to study how many atoms are in a particular part of the simulation cell.  For example, you might 
want to investigate how many gas atoms are within one of the pores of a zeolite.  Alternatively, you might be interested in the 
number of ions that have penetrated into the inner envelope of a membrane.  It is relatively easy to calculate such CVs in PLUMED.
For example, if you want to calculate the number of atoms that are within a sphere with radius 1.0 nm around atom 1 you can use an 
input something like this:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/Volumes.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="Volumes.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="Volumes.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span style="color:blue" class="comment"># This will output a vector with 99 components.  Each component of this vector is calculated</span>
<span style="color:blue" class="comment"># by applying a switching function on the distance between atom 1 and one of the atoms in </span>
<span style="color:blue" class="comment"># the system</span>
<b name="data/Volumes.md_working_1.datsp" onclick='showPath("data/Volumes.md_working_1.dat","data/Volumes.md_working_1.datsp","data/Volumes.md_working_1.datsp","blue")'>sp</b><span style="display:none;" id="data/Volumes.md_working_1.datsp">The INSPHERE action with label <b>sp</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">sp</td><td width="5%"><font color="blue">vector</font></td><td>vector of numbers between 0 and 1 that measure the degree to which each atom is within the volume of interest</td></tr></table></span>: <span class="plumedtooltip" style="color:green">INSPHERE<span class="right">This quantity can be used to calculate functions of the distribution of collective variables for the atoms that lie in a particular, user-specified part of of the cell. <a href="https://www.plumed.org/doc-master/user-doc/html/INSPHERE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that you would like to investigate<i></i></span></span>=2-100 <span class="plumedtooltip">CENTER<span class="right">the atom whose vicinity we are interested in examining<i></i></span></span>=1 <span class="plumedtooltip">RADIUS<span class="right">the switching function that tells us the extent of the sphereical region of interest. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=1.0}
<span style="color:blue" class="comment"># This adds together all the elements of sp</span>
<b name="data/Volumes.md_working_1.datsumsp" onclick='showPath("data/Volumes.md_working_1.dat","data/Volumes.md_working_1.datsumsp","data/Volumes.md_working_1.datsumsp","black")'>sumsp</b><span style="display:none;" id="data/Volumes.md_working_1.datsumsp">The SUM action with label <b>sumsp</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">sumsp</td><td width="5%"><font color="black">scalar</font></td><td>the SUM of the elements in the input value</td></tr></table></span>: <span class="plumedtooltip" style="color:green">SUM<span class="right">Calculate the sum of the arguments <a href="https://www.plumed.org/doc-master/user-doc/html/SUM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the vector/matrix/grid whose elements shuld be added together<i></i></span></span>=<b name="data/Volumes.md_working_1.datsp">sp</b> <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="color:blue" class="comment"># And this prints the final scalar quantity that tells you how many atoms are in the sphere </span>
<span style="color:blue" class="comment"># to a file.</span>
<span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/Volumes.md_working_1.datsumsp">sumsp</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
</pre>
 {% endraw %} 

This input is relatively simple and illustrates the procedure that PLUMED follows in calculating this quantity pretty clearly.

1. A vector `sp` is calculated.  Each element in this vector is between 0 and 1 and the $i$th element is one if atom $i$ is in the region of interest.
2. The elements of the vector are all added together.

Step 2 in this procedure is fixed but there are a variety of differnt ways of completing step 1 as there are a variety of ways of defining the region 
of interest.  The particular methods that are currently available are:

* INSPHERE - calculate whether atoms are within a spherical region centered on a particular atom.
* AROUND - calcualte the vector $(x,y,x)$ connecting each atom to a user-specified atom that is at the origin.  Then determine if $x_l < x < x_u$, $y_l < y < y_u$ and $z_l < z < z_u$, where $x_l$, $x_u$, $y_l$, $y_u, $z_l$ and $z_u$ are user specified parameters.
* INCYLINDER - calculate whether atoms are within a cylindrical region that has its long axis aligned with the $x$, $y$ or $z$ axis of the lab frame and that is centerd on a particular atom.
* CAVITY - calculate whether atoms are within a orthrhombic box whose orientation and size is determined based on the position of four atoms.
* TETRAPORE - calculate whether atoms are within a orthrhombic box whose orientation and size is determined based on the position of four atoms (the calculation of the box is done differently to the way it is done with CAVITY).
* INENVELOPE - use kernel density estimation to calculate the density of a particular atom type.  Then for each of the atoms, $i$, in a second (different) set to the one that was used to calculate the density determine if they are in a region where the density of the first atom type is large.  This action could be used to determine whether ions are in a membrane. 

## Using FIXEDATOM

You will notice that when we use these commands for calculating the number of atoms a part of the box there is always at least one atom that defines the position of the origin.  We do not use 
the positions that are calculated from the MD code directly and instead calculate the position of the atom of interest with respect to some other atom.  Calculating these vectors connecting 
pairs of atoms is essential.  If we were to use the positions that are passed from the MD code directly our CV would not be translationally invariant.  In other words, if we use the position that 
are passed from the MD code when the position of the center of mass of the atoms changes the values of the CV changes.

Using the position of atom 1 as the position of the ORIGIN as I did above might be useful in some cases.  If you want to look at what is going on in a particular part of the cell it is usually simpler
to define a virtual atom at the origin using FIXEDATOM like this:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/Volumes.md_working_2.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="Volumes.md_working_2.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="Volumes.md_working_2.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/Volumes.md_working_2.datdeff_short"><b name="data/Volumes.md_working_2.datf" onclick='showPath("data/Volumes.md_working_2.dat","data/Volumes.md_working_2.datf","data/Volumes.md_working_2.datf","violet")'>f</b><span style="display:none;" id="data/Volumes.md_working_2.datf">The FIXEDATOM action with label <b>f</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">f</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by FIXEDATOM action</td></tr></table></span>: <span class="plumedtooltip" style="color:green">FIXEDATOM<span class="right">Add a virtual atom in a fixed position. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/Volumes.md_working_2.datdeff");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/FIXEDATOM">More details</a><i></i></span></span> <span class="plumedtooltip">AT<span class="right">coordinates of the virtual atom<i></i></span></span>=0,0,0
</span><span id="data/Volumes.md_working_2.datdeff_long" style="display:none;"><b name="data/Volumes.md_working_2.datf" onclick='showPath("data/Volumes.md_working_2.dat","data/Volumes.md_working_2.datf","data/Volumes.md_working_2.datf","violet")'>f</b>: <span class="plumedtooltip" style="color:green">FIXEDATOM<span class="right">Add a virtual atom in a fixed position. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/Volumes.md_working_2.datdeff");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/FIXEDATOM">More details</a><i></i></span></span> <span class="plumedtooltip">AT<span class="right">coordinates of the virtual atom<i></i></span></span>=0,0,0  <span class="plumedtooltip">SET_MASS<span class="right"> mass of the virtual atom<i></i></span></span>=1 <span class="plumedtooltip">SET_CHARGE<span class="right"> charge of the virtual atom<i></i></span></span>=0
</span><b name="data/Volumes.md_working_2.datsp" onclick='showPath("data/Volumes.md_working_2.dat","data/Volumes.md_working_2.datsp","data/Volumes.md_working_2.datsp","blue")'>sp</b><span style="display:none;" id="data/Volumes.md_working_2.datsp">The INSPHERE action with label <b>sp</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">sp</td><td width="5%"><font color="blue">vector</font></td><td>vector of numbers between 0 and 1 that measure the degree to which each atom is within the volume of interest</td></tr></table></span>: <span class="plumedtooltip" style="color:green">INSPHERE<span class="right">This quantity can be used to calculate functions of the distribution of collective variables for the atoms that lie in a particular, user-specified part of of the cell. <a href="https://www.plumed.org/doc-master/user-doc/html/INSPHERE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">CENTER<span class="right">the atom whose vicinity we are interested in examining<i></i></span></span>=<b name="data/Volumes.md_working_2.datf">f</b> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that you would like to investigate<i></i></span></span>=1-100 <span class="plumedtooltip">RADIUS<span class="right">the switching function that tells us the extent of the sphereical region of interest. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=1.0}
<b name="data/Volumes.md_working_2.datsumsp" onclick='showPath("data/Volumes.md_working_2.dat","data/Volumes.md_working_2.datsumsp","data/Volumes.md_working_2.datsumsp","black")'>sumsp</b><span style="display:none;" id="data/Volumes.md_working_2.datsumsp">The SUM action with label <b>sumsp</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">sumsp</td><td width="5%"><font color="black">scalar</font></td><td>the SUM of the elements in the input value</td></tr></table></span>: <span class="plumedtooltip" style="color:green">SUM<span class="right">Calculate the sum of the arguments <a href="https://www.plumed.org/doc-master/user-doc/html/SUM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the vector/matrix/grid whose elements shuld be added together<i></i></span></span>=<b name="data/Volumes.md_working_2.datsp">sp</b> <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/Volumes.md_working_2.datsumsp">sumsp</b>
</pre>
 {% endraw %} 

As PBCs are applied on the distances calculated in the action `sp` using the FIXEDATOM `f` at (0,0,0) ensures that the sphere is centered on the center of the simulation cell.


## Calculating the average value of a CV in a region

Methods for using the functionality discussed above to calculate the average value of an order parameter in a particular part of the box are discussed at length in [this tutorial paper](https://pubs.acs.org/doi/10.1021/acs.jpcb.5c07562).
The paper also discusses how to ensure that such calculations run quickly.

## Conclusions

The functionality described above can be used to calculate the average value of any quantity in a region of interest.  It will also work with CVs such as LOCAL_Q6 or the LOCAL_AVERAGE
of a symmetry function.  Furthermore, even in these cases the task list is optimised so that CVs that do not contribute to the final CV value are not computed.
