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
<span style="color:blue" class="comment"># by applying a switching function on the distance between atom 1 and one of the atoms in the system</span>
<b name="data/Volumes.md_working_1.datsp" onclick='showPath("data/Volumes.md_working_1.dat","data/Volumes.md_working_1.datsp","data/Volumes.md_working_1.datsp","blue")'>sp</b><span style="display:none;" id="data/Volumes.md_working_1.datsp">The INSPHERE action with label <b>sp</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">sp</td><td width="5%"><font color="blue">vector</font></td><td>vector of numbers between 0 and 1 that measure the degree to which each atom is within the volume of interest</td></tr></table></span>: <span class="plumedtooltip" style="color:green">INSPHERE<span class="right">This quantity can be used to calculate functions of the distribution of collective variables for the atoms that lie in a particular, user-specified part of of the cell. <a href="https://www.plumed.org/doc-master/user-doc/html/INSPHERE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that you would like to investigate<i></i></span></span>=2-100 <span class="plumedtooltip">CENTER<span class="right">the atom whose vicinity we are interested in examining<i></i></span></span>=1 <span class="plumedtooltip">RADIUS<span class="right">the switching function that tells us the extent of the sphereical region of interest. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=1.0}
<span style="color:blue" class="comment"># This adds together all the elements of sp</span>
<b name="data/Volumes.md_working_1.datsumsp" onclick='showPath("data/Volumes.md_working_1.dat","data/Volumes.md_working_1.datsumsp","data/Volumes.md_working_1.datsumsp","black")'>sumsp</b><span style="display:none;" id="data/Volumes.md_working_1.datsumsp">The SUM action with label <b>sumsp</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">sumsp</td><td width="5%"><font color="black">scalar</font></td><td>the SUM of the elements in the input value</td></tr></table></span>: <span class="plumedtooltip" style="color:green">SUM<span class="right">Calculate the sum of the arguments <a href="https://www.plumed.org/doc-master/user-doc/html/SUM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the vector/matrix/grid whose elements shuld be added together<i></i></span></span>=<b name="data/Volumes.md_working_1.datsp">sp</b> <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="color:blue" class="comment"># And this prints the final scalar quantity that tells you how many atoms are in the sphere to a file.</span>
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

You may be wondering why, in the inputs that I have shown thus far, vectors that tell us whether each atom is inside or outside the region of interest are computed and exposed in the input.
The reason is that these vectors are useful in other cases.  For example, we can calculate the average value of the coordination numbers of the atoms that are within a sphere.  This quantity would 
be defined as:

$$
c_v = \frac{ \sum_i v_i c_i }{ \sum_i v_i }
$$

In this expression the sum runs over all atoms.  $c_i$ is the coordination number of atom $i$ and $v_i$ is a scalar that tells you that atom $i$ is within the region of interest.
You can implement this CV in PLUMED using the following input:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/Volumes.md_working_3.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="Volumes.md_working_3.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="Volumes.md_working_3.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/Volumes.md_working_3.datdeff_short"><b name="data/Volumes.md_working_3.datf" onclick='showPath("data/Volumes.md_working_3.dat","data/Volumes.md_working_3.datf","data/Volumes.md_working_3.datf","violet")'>f</b><span style="display:none;" id="data/Volumes.md_working_3.datf">The FIXEDATOM action with label <b>f</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">f</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by FIXEDATOM action</td></tr></table></span>: <span class="plumedtooltip" style="color:green">FIXEDATOM<span class="right">Add a virtual atom in a fixed position. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/Volumes.md_working_3.datdeff");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/FIXEDATOM">More details</a><i></i></span></span> <span class="plumedtooltip">AT<span class="right">coordinates of the virtual atom<i></i></span></span>=0,0,0
</span><span id="data/Volumes.md_working_3.datdeff_long" style="display:none;"><b name="data/Volumes.md_working_3.datf" onclick='showPath("data/Volumes.md_working_3.dat","data/Volumes.md_working_3.datf","data/Volumes.md_working_3.datf","violet")'>f</b>: <span class="plumedtooltip" style="color:green">FIXEDATOM<span class="right">Add a virtual atom in a fixed position. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/Volumes.md_working_3.datdeff");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/FIXEDATOM">More details</a><i></i></span></span> <span class="plumedtooltip">AT<span class="right">coordinates of the virtual atom<i></i></span></span>=0,0,0  <span class="plumedtooltip">SET_MASS<span class="right"> mass of the virtual atom<i></i></span></span>=1 <span class="plumedtooltip">SET_CHARGE<span class="right"> charge of the virtual atom<i></i></span></span>=0
</span><span style="color:blue" class="comment"># Calculate the coordination numbers in the usual way</span>
<b name="data/Volumes.md_working_3.datcmat" onclick='showPath("data/Volumes.md_working_3.dat","data/Volumes.md_working_3.datcmat","data/Volumes.md_working_3.datcmat","red")'>cmat</b><span style="display:none;" id="data/Volumes.md_working_3.datcmat">The CONTACT_MATRIX action with label <b>cmat</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cmat</td><td width="5%"><font color="red">matrix</font></td><td>a matrix containing the weights for the bonds between each pair of atoms</td></tr></table></span>: <span class="plumedtooltip" style="color:green">CONTACT_MATRIX<span class="right">Adjacency matrix in which two atoms are adjacent if they are within a certain cutoff. <a href="https://www.plumed.org/doc-master/user-doc/html/CONTACT_MATRIX" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GROUP<span class="right">specifies the list of atoms that should be assumed indistinguishable<i></i></span></span>=1-100 <span class="plumedtooltip">SWITCH<span class="right">the input for the switching function that acts upon the distance between each pair of atoms. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=0.1}
<span id="data/Volumes.md_working_3.datones_short"><b name="data/Volumes.md_working_3.datones" onclick='showPath("data/Volumes.md_working_3.dat","data/Volumes.md_working_3.datones","data/Volumes.md_working_3.datones_shortcut","blue")'>ones</b><span style="display:none;" id="data/Volumes.md_working_3.datones_shortcut">The ONES action with label <b>ones</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">ones</td><td width="5%"><font color="blue">vector</font></td><td>a vector of ones with the required number of elements</td></tr></table></span>: <span class="plumedtooltip" style="color:green">ONES<span class="right">Create a constant vector with all elements equal to one This action is <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/Volumes.md_working_3.datones");'>a shortcut</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/ONES">More details</a><i></i></span></span> <span class="plumedtooltip">SIZE<span class="right">the number of ones that you would like to create<i></i></span></span>=100
</span><span id="data/Volumes.md_working_3.datones_long" style="display:none;"><span style="color:blue" class="comment"># PLUMED interprets the command:
</span><span class="toggler" style="color:red" onclick='toggleDisplay("data/Volumes.md_working_3.datones")'># ones: ONES SIZE=100</span>
<span style="color:blue" class="comment"># as follows (Click the red comment above to revert to the short version of the input):</span>
<b name="data/Volumes.md_working_3.datones" onclick='showPath("data/Volumes.md_working_3.dat","data/Volumes.md_working_3.datones","data/Volumes.md_working_3.datones","blue")'>ones</b><span style="display:none;" id="data/Volumes.md_working_3.datones">The CONSTANT action with label <b>ones</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">ones</td><td width="5%"><font color="blue">vector</font></td><td>the constant value that was read from the plumed input</td></tr></table></span>: <span class="plumedtooltip" style="color:green">CONSTANT<span class="right">Create a constant value that can be passed to actions <a href="https://www.plumed.org/doc-master/user-doc/html/CONSTANT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NOLOG<span class="right"> do not report all the read in scalars in the log<i></i></span></span> <span class="plumedtooltip">VALUES<span class="right">the numbers that are in your constant value<i></i></span></span>=1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1
<span style="color:blue"># --- End of included input --- </span></span><b name="data/Volumes.md_working_3.datc1" onclick='showPath("data/Volumes.md_working_3.dat","data/Volumes.md_working_3.datc1","data/Volumes.md_working_3.datc1","blue")'>c1</b><span style="display:none;" id="data/Volumes.md_working_3.datc1">The MATRIX_VECTOR_PRODUCT action with label <b>c1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c1</td><td width="5%"><font color="blue">vector</font></td><td>the vector that is obtained by taking the product between the matrix and the vector that were input</td></tr></table></span>: <span class="plumedtooltip" style="color:green">MATRIX_VECTOR_PRODUCT<span class="right">Calculate the product of the matrix and the vector <a href="https://www.plumed.org/doc-master/user-doc/html/MATRIX_VECTOR_PRODUCT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the label for the matrix and the vector/scalar that are being multiplied<i></i></span></span>=<b name="data/Volumes.md_working_3.datcmat">cmat</b>,<b name="data/Volumes.md_working_3.datones">ones</b>
<span style="color:blue" class="comment"># Now calculate whether each atom is within the region of interest.  These is the vector of 100 v_i values in the expression above.</span>
<b name="data/Volumes.md_working_3.datsp" onclick='showPath("data/Volumes.md_working_3.dat","data/Volumes.md_working_3.datsp","data/Volumes.md_working_3.datsp","blue")'>sp</b><span style="display:none;" id="data/Volumes.md_working_3.datsp">The INSPHERE action with label <b>sp</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">sp</td><td width="5%"><font color="blue">vector</font></td><td>vector of numbers between 0 and 1 that measure the degree to which each atom is within the volume of interest</td></tr></table></span>: <span class="plumedtooltip" style="color:green">INSPHERE<span class="right">This quantity can be used to calculate functions of the distribution of collective variables for the atoms that lie in a particular, user-specified part of of the cell. <a href="https://www.plumed.org/doc-master/user-doc/html/INSPHERE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that you would like to investigate<i></i></span></span>=1-100 <span class="plumedtooltip">CENTER<span class="right">the atom whose vicinity we are interested in examining<i></i></span></span>=<b name="data/Volumes.md_working_3.datf">f</b> <span class="plumedtooltip">RADIUS<span class="right">the switching function that tells us the extent of the sphereical region of interest. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=1.0}
<span style="color:blue" class="comment"># Now calculate another vector of v_i c_i values.  This action returns a vector with 100 elements.</span>
<b name="data/Volumes.md_working_3.datnumf" onclick='showPath("data/Volumes.md_working_3.dat","data/Volumes.md_working_3.datnumf","data/Volumes.md_working_3.datnumf","blue")'>numf</b><span style="display:none;" id="data/Volumes.md_working_3.datnumf">The CUSTOM action with label <b>numf</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">numf</td><td width="5%"><font color="blue">vector</font></td><td>the vector obtained by doing an element-wise application of an arbitrary function to the input vectors</td></tr></table></span>: <span class="plumedtooltip" style="color:green">CUSTOM<span class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/CUSTOM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<b name="data/Volumes.md_working_3.datsp">sp</b>,<b name="data/Volumes.md_working_3.datc1">c1</b> <span class="plumedtooltip">FUNC<span class="right">the function you wish to evaluate<i></i></span></span>=x*y <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="color:blue" class="comment"># Calculate the sum in the numeration of the expression above.</span>
<b name="data/Volumes.md_working_3.datnumer" onclick='showPath("data/Volumes.md_working_3.dat","data/Volumes.md_working_3.datnumer","data/Volumes.md_working_3.datnumer","black")'>numer</b><span style="display:none;" id="data/Volumes.md_working_3.datnumer">The SUM action with label <b>numer</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">numer</td><td width="5%"><font color="black">scalar</font></td><td>the SUM of the elements in the input value</td></tr></table></span>: <span class="plumedtooltip" style="color:green">SUM<span class="right">Calculate the sum of the arguments <a href="https://www.plumed.org/doc-master/user-doc/html/SUM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the vector/matrix/grid whose elements shuld be added together<i></i></span></span>=<b name="data/Volumes.md_working_3.datnumf">numf</b> <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="color:blue" class="comment"># Calculate the sum in the denominator of the expression above</span>
<b name="data/Volumes.md_working_3.datdenom" onclick='showPath("data/Volumes.md_working_3.dat","data/Volumes.md_working_3.datdenom","data/Volumes.md_working_3.datdenom","black")'>denom</b><span style="display:none;" id="data/Volumes.md_working_3.datdenom">The SUM action with label <b>denom</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">denom</td><td width="5%"><font color="black">scalar</font></td><td>the SUM of the elements in the input value</td></tr></table></span>: <span class="plumedtooltip" style="color:green">SUM<span class="right">Calculate the sum of the arguments <a href="https://www.plumed.org/doc-master/user-doc/html/SUM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the vector/matrix/grid whose elements shuld be added together<i></i></span></span>=<b name="data/Volumes.md_working_3.datsp">sp</b> <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="color:blue" class="comment"># And calculate the final quotient of interest</span>
<b name="data/Volumes.md_working_3.dats" onclick='showPath("data/Volumes.md_working_3.dat","data/Volumes.md_working_3.dats","data/Volumes.md_working_3.dats","black")'>s</b><span style="display:none;" id="data/Volumes.md_working_3.dats">The CUSTOM action with label <b>s</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">s</td><td width="5%"><font color="black">scalar</font></td><td>an arbitrary function</td></tr></table></span>: <span class="plumedtooltip" style="color:green">CUSTOM<span class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/CUSTOM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<b name="data/Volumes.md_working_3.datnumer">numer</b>,<b name="data/Volumes.md_working_3.datdenom">denom</b> <span class="plumedtooltip">FUNC<span class="right">the function you wish to evaluate<i></i></span></span>=x/y <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="color:blue" class="comment"># Print the final scalar value of the CV to a file</span>
<span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/Volumes.md_working_3.dats">s</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
</pre>
 {% endraw %} 

If you look at the graph for this input you can see that the numerator and denominator of the quotient above are calculating using a single loop over $i$

```mermaid
flowchart TB 
MD(positions from MD)
Box("label=Box 
 PBC 
")
f(["label=f 
 FIXEDATOM 
"])
Box -- Box --> cmat
linkStyle 0 stroke:red,color:red;
MD --> cmat
linkStyle 1 stroke:violet,color:violet;
cmat(["label=cmat 
 CONTACT_MATRIX 
"])
ones(["label=ones 
 CONSTANT 
"])
cmat -- cmat --> c1
linkStyle 2 stroke:red,color:red;
ones -- ones --> c1
linkStyle 3 stroke:blue,color:blue;
c1(["label=c1 
 MATRIX_VECTOR_PRODUCT 
"])
Box -- Box --> sp
linkStyle 4 stroke:red,color:red;
MD --> sp
linkStyle 5 stroke:violet,color:violet;
f -- f --> sp
linkStyle 6 stroke:violet,color:violet;
sp(["label=sp 
 INSPHERE_CALC 
"])
sp -- sp --> numf
linkStyle 7 stroke:blue,color:blue;
c1 -- c1 --> numf
linkStyle 8 stroke:blue,color:blue;
numf(["label=numf 
 CUSTOM
FUNC=x*y 
"])
numf -- numf --> numer
linkStyle 9 stroke:blue,color:blue;
numer(["label=numer 
 SUM 
"])
sp -- sp --> denom
linkStyle 10 stroke:blue,color:blue;
denom(["label=denom 
 SUM 
"])
numer -- numer --> s
denom -- denom --> s
s(["label=s 
 CUSTOM
FUNC=x/y 
"])
s -- s --> 15
15("label=#64;15 
 PRINT
FILE=colvar 
")

```

There is no passing of vectors between actions here.  The $i$th element of the vectors `sp` and `numf` are calculated immediately after the $i$th element of `c1` has been computed.
Furthremore, to make this code is made even more rapid as we use the INSPHERE action to determine which coordination numbers need to be calculated.  In other words, PLUMED only calculates
the coordination numbers of those atoms thare are within the region of interest.  Those that are not within this region, which we do not need to calculate the CV, are not computed. 

## Conclusions

The functionality described above can be used to calculate the average value of any quantity in a region of interest.  It will also work with CVs such as LOCAL_Q6 or the LOCAL_AVERAGE
of a symmetry function.  Furthermore, even in these cases the task list is optimised so that CVs that do not contribute to the final CV value are not computed.
