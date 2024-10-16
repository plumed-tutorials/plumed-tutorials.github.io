# Passing atoms to/from PLUMED 

As discussed in [this article](MDInterfaceI.md), data is passed from the MD code to PLUMED by creating a [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) action. 
These [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) actions take the data from a void pointer that is passed to PLUMED from the MD code and transfer it into a 
PLMD::Value object. Passing a void pointer and using a [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) action to convert the data within it 
to a PLMD::Value is also used when the atomic positions, masses and charges are sent to PLUMED. However, 
there are some other subtleties for these quantities because MD codes use a domain decomposition and scatter the properties of atoms across 
multiple domains. We thus need to use the action [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) when passing these quantities to make sense of the 
information in the void pointers that the MD code passes. 

## Creating a [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) action 

A [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) can be created by using a call to plumed.cmd as follows: 

```c++ 
plumed.cmd("readInputLine dd: [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) NATOMS=20 VALUE1=vv UNIT1=length PERIODIC1=NO CONSTANT1=False"); 
``` 

The DOMAIN_DECOMPOSTION command above creates a [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) action with the label vv. The pointer to the data that needs to be transferred to the PLMD::Value 
object that is created by the [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) action is then set by using the command below: 

```c++ 
plumed.cmd("setInputValue vv, &val); 
``` 

Meanwhile, the pointer to the forces that should be modified is passed as follows: 

```c++ 
plumed.cmd("setValueForces vv", force); 
``` 

In other words, pointers to values and forces in the MD code are passed to [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) actions that are created by the DOMAIN_DECOMPOSION in 
[the way you pass data to other [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) actions](MDInterfaceI.md). 

The PLMD::Value objects created by a [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) action are always vectors with the same number of components as atoms in the system. Furthermore, you can create multiple [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) 
actions from a single [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) action. To see why this is useful, consider the following [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) command: 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/MDInterfaceII.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="MDInterfaceII.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="MDInterfaceII.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<b name="data/MDInterfaceII.md_working_1.datgromacs" onclick='showPath("data/MDInterfaceII.md_working_1.dat","data/MDInterfaceII.md_working_1.datgromacs","data/MDInterfaceII.md_working_1.datgromacs","brown")'>gromacs</b>: <div class="tooltip" style="color:green">DOMAIN_DECOMPOSITION<div class="right">Pass domain decomposed properties of atoms to PLUMED <a href="https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html" style="color:green">More details</a><i></i></div></div> ...
   <div class="tooltip">NATOMS<div class="right">the number of atoms across all the domains<i></i></div></div>=2000
   <div class="tooltip">VALUE1<div class="right">value to create for the domain decomposition<i></i></div></div>=myposx <div class="tooltip">UNIT1<div class="right">unit of the ith value that is being passed through the domain decomposition<i></i></div></div>=length <div class="tooltip">PERIODIC1<div class="right">if the value being passed to plumed is periodic then you should specify the periodicity of the function<i></i></div></div>=NO <div class="tooltip">CONSTANT1<div class="right">is the ith value that is being passed through the domain decomposition constant<i></i></div></div>=False <div class="tooltip">ROLE1<div class="right">Get the role this value plays in the code can be x/y/z/m/q to signify that this is x, y, z positions of atoms or masses or charges of atoms<i></i></div></div>=x
   <div class="tooltip">VALUE2<div class="right">value to create for the domain decomposition<i></i></div></div>=myposy <div class="tooltip">UNIT2<div class="right">unit of the ith value that is being passed through the domain decomposition<i></i></div></div>=length <div class="tooltip">PERIODIC2<div class="right">if the value being passed to plumed is periodic then you should specify the periodicity of the function<i></i></div></div>=NO <div class="tooltip">CONSTANT2<div class="right">is the ith value that is being passed through the domain decomposition constant<i></i></div></div>=False <div class="tooltip">ROLE2<div class="right">Get the role this value plays in the code can be x/y/z/m/q to signify that this is x, y, z positions of atoms or masses or charges of atoms<i></i></div></div>=y
   <div class="tooltip">VALUE3<div class="right">value to create for the domain decomposition<i></i></div></div>=myposz <div class="tooltip">UNIT3<div class="right">unit of the ith value that is being passed through the domain decomposition<i></i></div></div>=length <div class="tooltip">PERIODIC3<div class="right">if the value being passed to plumed is periodic then you should specify the periodicity of the function<i></i></div></div>=NO <div class="tooltip">CONSTANT3<div class="right">is the ith value that is being passed through the domain decomposition constant<i></i></div></div>=False <div class="tooltip">ROLE3<div class="right">Get the role this value plays in the code can be x/y/z/m/q to signify that this is x, y, z positions of atoms or masses or charges of atoms<i></i></div></div>=z
   <div class="tooltip">VALUE4<div class="right">value to create for the domain decomposition<i></i></div></div>=myMasses <div class="tooltip">UNIT4<div class="right">unit of the ith value that is being passed through the domain decomposition<i></i></div></div>=mass <div class="tooltip">PERIODIC4<div class="right">if the value being passed to plumed is periodic then you should specify the periodicity of the function<i></i></div></div>=NO <div class="tooltip">CONSTANT4<div class="right">is the ith value that is being passed through the domain decomposition constant<i></i></div></div>=True <div class="tooltip">ROLE4<div class="right">Get the role this value plays in the code can be x/y/z/m/q to signify that this is x, y, z positions of atoms or masses or charges of atoms<i></i></div></div>=m
   <div class="tooltip">VALUE5<div class="right">value to create for the domain decomposition<i></i></div></div>=myCharges <div class="tooltip">UNIT5<div class="right">unit of the ith value that is being passed through the domain decomposition<i></i></div></div>=charge <div class="tooltip">PERIODIC5<div class="right">if the value being passed to plumed is periodic then you should specify the periodicity of the function<i></i></div></div>=NO <div class="tooltip">CONSTANT5<div class="right">is the ith value that is being passed through the domain decomposition constant<i></i></div></div>=True <div class="tooltip">ROLE5<div class="right">Get the role this value plays in the code can be x/y/z/m/q to signify that this is x, y, z positions of atoms or masses or charges of atoms<i></i></div></div>=q
   <div class="tooltip">PBCLABEL<div class="right"> the label to use for the PBC action that will be created<i></i></div></div>=mybox
...
<span style="display:none;" id="data/MDInterfaceII.md_working_1.datgromacs">The DOMAIN_DECOMPOSITION action with label <b>gromacs</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">gromacs.value</td><td>the domain that each atom is within</td></tr></table></span></pre>
 {% endraw %} 

This action is created when you call `plumed.cmd("setNatoms",&natoms)` from gromacs. It makes 5 PLMD::Value called posx, posy, posz, Masses and Charges. 
These PLMD::Value objects then hold the x, y and z positions of the atoms and the masses and charges of the atoms. It is important to note that this command will 
also, create a PBC_ACTION to hold the cell. 

The ROLE keywords above are only needed because the five quantities passed by the command above play a unique role within PLUMED. If you pass 
some other quantities, this instruction is not required. PLMD::ActionAtomistic searches for atomic positions, masses and charges by looking for [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) Actions 
that have these five particular roles and for ActionWithVirtualAtom objects. 

## Differences from regular [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) actions 

[PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) actions created from a [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) action behave differently from other [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) actions. In particular: 

* If a [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) action creates a [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) action, then the [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) action depends on the [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) action. ActionToPutData::apply thus does nothing for these [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) actions. 
* Similarly, when [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) actions create [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) actions, data is transferred from the input pointer to the PLMD::Value object by the [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) action. When ActionToPutData::wait is called for these [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) Actions `wasset=true`, ActionToPutData::wait does nothing. 
* Lastly, if a constant [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) action is created by DOMAIN_DECOMPOSITION, the values in the vector are set during the first step of MD rather than during initialisation. 

These differences are necessary because [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) actions cannot understand the information in the pointers that are passed from the MD code. These pointers are only understandable if you know 
which atoms are on each processor. This information is only passed to the [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) action. [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) must translate the information passed from the MD code before it is 
passed back on through PLMD::Value objects created by the [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) actions. [DOMAIN_DECOMPOSITION](https://www.plumed.org/doc-master/user-doc/html/_d_o_m_a_i_n__d_e_c_o_m_p_o_s_i_t_i_o_n.html) thus keeps pointers to all the [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) actions that it creates. It sets the data in these action's PLMD::Value objects 
within `DomainDecomposition::share(const std::vector<AtomNumber>& unique)` and `DomainDecomposition::wait().` The forces on the PUT actions created by the DOMAIN_DECOMPOSITION action are added in `DomainDecomposition::apply()`. 

