# Passing atoms to/from PLUMED

As discussed in [this article](MDInterfaceI.md), data is passed from the MD code to PLUMED by creating a PUT action.
These PUT actions take the data from a void pointer that is passed to PLUMED from the MD code and transfer it into a 
PLMD::Value object. Passing a void pointer and using a PUT action to convert the data within it
to a PLMD::Value is also used when the atomic positions, masses and charges are sent to PLUMED. However, 
there are some other subtleties for these quantities because MD codes use a domain decomposition and scatter the properties of atoms across
multiple domains. We thus need to use the action DOMAIN_DECOMPOSITION when passing these quantities to make sense of the 
information in the void pointers that the MD code passes.

## Creating a DOMAIN_DECOMPOSITION action

A DOMAIN_DECOMPOSITION can be created by using a call to plumed.cmd as follows:

```c++
plumed.cmd("readInputLine dd: DOMAIN_DECOMPOSITION NATOMS=20 VALUE1=vv UNIT1=length PERIODIC1=NO CONSTANT1=False");
```

The DOMAIN_DECOMPOSTION command above creates a PUT action with the label vv. The pointer to the data that needs to be transferred to the PLMD::Value
object that is created by the PUT action is then set by using the command below:

```c++
plumed.cmd("setInputValue vv, &val);
```

Meanwhile, the pointer to the forces that should be modified is passed as follows:

```c++
plumed.cmd("setValueForces vv", force);
```

In other words, pointers to values and forces in the MD code are passed to PUT actions that are created by the DOMAIN_DECOMPOSION in 
[the way you pass data to other PUT actions](MDInterfaceI.md). 

The PLMD::Value objects created by a DOMAIN_DECOMPOSITION action are always vectors with the same number of components as atoms in the system. Furthermore, you can create multiple PUT
actions from a single DOMAIN_DECOMPOSITION action. To see why this is useful, consider the following DOMAIN_DECOMPOSITION command:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/MDInterfaceII.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="MDInterfaceII.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="MDInterfaceII.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<b name="data/MDInterfaceII.md_working_1.datgromacs" onclick='showPath("data/MDInterfaceII.md_working_1.dat","data/MDInterfaceII.md_working_1.datgromacs","data/MDInterfaceII.md_working_1.datgromacs","brown")'>gromacs</b>: <span class="plumedtooltip" style="color:green">DOMAIN_DECOMPOSITION<span class="right">Pass domain decomposed properties of atoms to PLUMED <a href="https://www.plumed.org/doc-master/user-doc/html/DOMAIN_DECOMPOSITION" style="color:green">More details</a><i></i></span></span> ...
   <span class="plumedtooltip">NATOMS<span class="right">the number of atoms across all the domains<i></i></span></span>=2000
   <span class="plumedtooltip">VALUE1<span class="right">value to create for the domain decomposition<i></i></span></span>=myposx <span class="plumedtooltip">UNIT1<span class="right">unit of the ith value that is being passed through the domain decomposition<i></i></span></span>=length <span class="plumedtooltip">PERIODIC1<span class="right">if the value being passed to plumed is periodic then you should specify the periodicity of the function<i></i></span></span>=NO <span class="plumedtooltip">CONSTANT1<span class="right">is the ith value that is being passed through the domain decomposition constant<i></i></span></span>=False <span class="plumedtooltip">ROLE1<span class="right">Get the role this value plays in the code can be x/y/z/m/q to signify that this is x, y, z positions of atoms or masses or charges of atoms<i></i></span></span>=x
   <span class="plumedtooltip">VALUE2<span class="right">value to create for the domain decomposition<i></i></span></span>=myposy <span class="plumedtooltip">UNIT2<span class="right">unit of the ith value that is being passed through the domain decomposition<i></i></span></span>=length <span class="plumedtooltip">PERIODIC2<span class="right">if the value being passed to plumed is periodic then you should specify the periodicity of the function<i></i></span></span>=NO <span class="plumedtooltip">CONSTANT2<span class="right">is the ith value that is being passed through the domain decomposition constant<i></i></span></span>=False <span class="plumedtooltip">ROLE2<span class="right">Get the role this value plays in the code can be x/y/z/m/q to signify that this is x, y, z positions of atoms or masses or charges of atoms<i></i></span></span>=y
   <span class="plumedtooltip">VALUE3<span class="right">value to create for the domain decomposition<i></i></span></span>=myposz <span class="plumedtooltip">UNIT3<span class="right">unit of the ith value that is being passed through the domain decomposition<i></i></span></span>=length <span class="plumedtooltip">PERIODIC3<span class="right">if the value being passed to plumed is periodic then you should specify the periodicity of the function<i></i></span></span>=NO <span class="plumedtooltip">CONSTANT3<span class="right">is the ith value that is being passed through the domain decomposition constant<i></i></span></span>=False <span class="plumedtooltip">ROLE3<span class="right">Get the role this value plays in the code can be x/y/z/m/q to signify that this is x, y, z positions of atoms or masses or charges of atoms<i></i></span></span>=z
   <span class="plumedtooltip">VALUE4<span class="right">value to create for the domain decomposition<i></i></span></span>=myMasses <span class="plumedtooltip">UNIT4<span class="right">unit of the ith value that is being passed through the domain decomposition<i></i></span></span>=mass <span class="plumedtooltip">PERIODIC4<span class="right">if the value being passed to plumed is periodic then you should specify the periodicity of the function<i></i></span></span>=NO <span class="plumedtooltip">CONSTANT4<span class="right">is the ith value that is being passed through the domain decomposition constant<i></i></span></span>=True <span class="plumedtooltip">ROLE4<span class="right">Get the role this value plays in the code can be x/y/z/m/q to signify that this is x, y, z positions of atoms or masses or charges of atoms<i></i></span></span>=m
   <span class="plumedtooltip">VALUE5<span class="right">value to create for the domain decomposition<i></i></span></span>=myCharges <span class="plumedtooltip">UNIT5<span class="right">unit of the ith value that is being passed through the domain decomposition<i></i></span></span>=charge <span class="plumedtooltip">PERIODIC5<span class="right">if the value being passed to plumed is periodic then you should specify the periodicity of the function<i></i></span></span>=NO <span class="plumedtooltip">CONSTANT5<span class="right">is the ith value that is being passed through the domain decomposition constant<i></i></span></span>=True <span class="plumedtooltip">ROLE5<span class="right">Get the role this value plays in the code can be x/y/z/m/q to signify that this is x, y, z positions of atoms or masses or charges of atoms<i></i></span></span>=q
   <span class="plumedtooltip">PBCLABEL<span class="right"> the label to use for the PBC action that will be created<i></i></span></span>=mybox
...
<span style="display:none;" id="data/MDInterfaceII.md_working_1.datgromacs">The DOMAIN_DECOMPOSITION action with label <b>gromacs</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">gromacs.value</td><td>the domain that each atom is within</td></tr></table></span></pre>
 {% endraw %} 

This action is created when you call `plumed.cmd("setNatoms",&natoms)` from gromacs. It makes 5 PLMD::Value called posx, posy, posz, Masses and Charges. 
These PLMD::Value objects then hold the x, y and z positions of the atoms and the masses and charges of the atoms. It is important to note that this command will 
also, create a PBC_ACTION to hold the cell.

The ROLE keywords above are only needed because the five quantities passed by the command above play a unique role within PLUMED. If you pass 
some other quantities, this instruction is not required. PLMD::ActionAtomistic searches for atomic positions, masses and charges by looking for PUT Actions
that have these five particular roles and for ActionWithVirtualAtom objects.

## Differences from regular PUT actions

PUT actions created from a DOMAIN_DECOMPOSITION action behave differently from other PUT actions. In particular:

* If a DOMAIN_DECOMPOSITION action creates a PUT action, then the PUT action depends on the DOMAIN_DECOMPOSITION action. ActionToPutData::apply thus does nothing for these PUT actions.
* Similarly, when DOMAIN_DECOMPOSITION actions create PUT actions, data is transferred from the input pointer to the PLMD::Value object by the DOMAIN_DECOMPOSITION action. When ActionToPutData::wait is called for these PUT Actions `wasset=true`, ActionToPutData::wait does nothing.
* Lastly, if a constant PUT action is created by DOMAIN_DECOMPOSITION, the values in the vector are set during the first step of MD rather than during initialisation. 

These differences are necessary because PUT actions cannot understand the information in the pointers that are passed from the MD code. These pointers are only understandable if you know 
which atoms are on each processor. This information is only passed to the DOMAIN_DECOMPOSITION action. DOMAIN_DECOMPOSITION must translate the information passed from the MD code before it is 
passed back on through PLMD::Value objects created by the PUT actions. DOMAIN_DECOMPOSITION thus keeps pointers to all the PUT actions that it creates. It sets the data in these action's PLMD::Value objects
within `DomainDecomposition::share(const std::vector<AtomNumber>& unique)` and `DomainDecomposition::wait().`  The forces on the PUT actions created by the DOMAIN_DECOMPOSITION action are added in `DomainDecomposition::apply()`.

