# Representing PLUMED inputs using flowcharts 

Ever since we wrote the PLUMED paper in 2014, I have wondered if we can automate the process of generating diagrams 
similar to the ones in that paper that show how Values and forces are passed between the various actions in the PLUMED input. 
If we could automate the generation of these diagrams, we could have similar charts for all the entries 
in the PLUMED nest. We could also have these diagrams for the example inputs in the tutorials and manuals. 

The time to implement these diagrams is now when we have changed the code so that actions can also pass vectors, 
scalars and grids between them, as discussed [here](Passing.md). I have thus written a command line tool that allows one to 
generate a graph from a plumed input. Consequentially, if I take the contents of the file plumed.dat below: 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/Graphs.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="Graphs.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="Graphs.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<b name="data/Graphs.md_working_1.datc1" onclick='showPath("data/Graphs.md_working_1.dat","data/Graphs.md_working_1.datc1","data/Graphs.md_working_1.datc1","violet")'>c1</b><span style="display:none;" id="data/Graphs.md_working_1.datc1">The COM action with label <b>c1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c1</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by COM action</td></tr></table></span>: <div class="tooltip" style="color:green">COM<div class="right">Calculate the center of mass for a group of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_m.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the list of atoms which are involved the virtual atom's definition<i></i></div></div>=1-10
<b name="data/Graphs.md_working_1.datc2" onclick='showPath("data/Graphs.md_working_1.dat","data/Graphs.md_working_1.datc2","data/Graphs.md_working_1.datc2","violet")'>c2</b><span style="display:none;" id="data/Graphs.md_working_1.datc2">The COM action with label <b>c2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c2</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by COM action</td></tr></table></span>: <div class="tooltip" style="color:green">COM<div class="right">Calculate the center of mass for a group of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_m.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the list of atoms which are involved the virtual atom's definition<i></i></div></div>=11-20
<b name="data/Graphs.md_working_1.datd1" onclick='showPath("data/Graphs.md_working_1.dat","data/Graphs.md_working_1.datd1","data/Graphs.md_working_1.datd1","black")'>d1</b><span style="display:none;" id="data/Graphs.md_working_1.datd1">The DISTANCE action with label <b>d1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d1.x</td><td width="5%"><font color="black">scalar</font></td><td>the x-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.y</td><td width="5%"><font color="black">scalar</font></td><td>the y-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.z</td><td width="5%"><font color="black">scalar</font></td><td>the z-component of the vector connecting the two atoms</td></tr></table></span>: <div class="tooltip" style="color:green">DISTANCE<div class="right">Calculate the distance between a pair of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_d_i_s_t_a_n_c_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the pair of atom that we are calculating the distance between<i></i></div></div>=<b name="data/Graphs.md_working_1.datc1">c1</b>,<b name="data/Graphs.md_working_1.datc2">c2</b> <div class="tooltip">COMPONENTS<div class="right"> calculate the x, y and z components of the distance separately and store them as label<i></i></div></div>
<span id="data/Graphs.md_working_1.datdefr_short"><b name="data/Graphs.md_working_1.datr" onclick='showPath("data/Graphs.md_working_1.dat","data/Graphs.md_working_1.datr","data/Graphs.md_working_1.datr","black")'>r</b><span style="display:none;" id="data/Graphs.md_working_1.datr">The RESTRAINT action with label <b>r</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">r.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">r.force2</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span>: <div class="tooltip" style="color:green">RESTRAINT<div class="right">Adds harmonic and/or linear restraints on one or more variables. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/Graphs.md_working_1.datdefr");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_r_e_s_t_r_a_i_n_t.html">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values the harmonic restraint acts upon<i></i></div></div>=<b name="data/Graphs.md_working_1.datd1">d1.z</b> <div class="tooltip">AT<div class="right">the position of the restraint<i></i></div></div>=1 <div class="tooltip">KAPPA<div class="right"> specifies that the restraint is harmonic and what the values of the force constants on each of the variables are<i></i></div></div>=1 
</span><span id="data/Graphs.md_working_1.datdefr_long" style="display:none;"><b name="data/Graphs.md_working_1.datr" onclick='showPath("data/Graphs.md_working_1.dat","data/Graphs.md_working_1.datr","data/Graphs.md_working_1.datr","black")'>r</b>: <div class="tooltip" style="color:green">RESTRAINT<div class="right">Adds harmonic and/or linear restraints on one or more variables. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/Graphs.md_working_1.datdefr");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_r_e_s_t_r_a_i_n_t.html">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values the harmonic restraint acts upon<i></i></div></div>=<b name="data/Graphs.md_working_1.datd1">d1.z</b> <div class="tooltip">AT<div class="right">the position of the restraint<i></i></div></div>=1 <div class="tooltip">KAPPA<div class="right"> specifies that the restraint is harmonic and what the values of the force constants on each of the variables are<i></i></div></div>=1  <div class="tooltip">SLOPE<div class="right"> specifies that the restraint is linear and what the values of the force constants on each of the variables are<i></i></div></div>=0.0
</span><b name="data/Graphs.md_working_1.datf1" onclick='showPath("data/Graphs.md_working_1.dat","data/Graphs.md_working_1.datf1","data/Graphs.md_working_1.datf1","black")'>f1</b><span style="display:none;" id="data/Graphs.md_working_1.datf1">The CUSTOM action with label <b>f1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">f1</td><td width="5%"><font color="black">scalar</font></td><td>an arbitrary function</td></tr></table></span>: <div class="tooltip" style="color:green">CUSTOM<div class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_u_s_t_o_m.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/Graphs.md_working_1.datd1">d1.x</b>,<b name="data/Graphs.md_working_1.datd1">d1.y</b> <div class="tooltip">FUNC<div class="right">the function you wish to evaluate<i></i></div></div>=x*x+y*y <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
<div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/Graphs.md_working_1.datd1">d1.x</b>,<b name="data/Graphs.md_working_1.datd1">d1.y</b>,<b name="data/Graphs.md_working_1.datf1">f1</b>,<b name="data/Graphs.md_working_1.datr">r.bias</b> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=colvar
</pre>
 {% endraw %} 

And run the command: 

```` 
plumed show_graph --plumed plumed.dat --out graph.md 
```` 

I can generate the graph shown below: 

```mermaid
flowchart TB 
MD(positions from MD)
Box("label=Box 
 PBC 
")
Box -- Box --> c1
linkStyle 0 stroke:red,color:red;
MD --> c1
linkStyle 1 stroke:violet,color:violet;
c1(["label=c1 
 COM 
"])
Box -- Box --> c2
linkStyle 2 stroke:red,color:red;
MD --> c2
linkStyle 3 stroke:violet,color:violet;
c2(["label=c2 
 COM 
"])
Box -- Box --> d1
linkStyle 4 stroke:red,color:red;
c1 -- c1 --> d1
linkStyle 5 stroke:violet,color:violet;
c2 -- c2 --> d1
linkStyle 6 stroke:violet,color:violet;
d1(["label=d1 
 DISTANCE 
"])
d1 -- d1.z --> r
r(["label=r 
 RESTRAINT 
"])
d1 -- d1.x --> f1
d1 -- d1.y --> f1
f1(["label=f1 
 CUSTOM
FUNC=x*x+y*y 
"])
d1 -- d1.x --> 8
d1 -- d1.y --> 8
f1 -- f1 --> 8
r -- r.bias --> 8
8("label=#64;8 
 PRINT
FILE=colvar 
")

```
{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/Graphs.md_working_2.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="Graphs.md_working_2.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="Graphs.md_working_2.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<b name="data/Graphs.md_working_2.datc1" onclick='showPath("data/Graphs.md_working_2.dat","data/Graphs.md_working_2.datc1","data/Graphs.md_working_2.datc1","violet")'>c1</b><span style="display:none;" id="data/Graphs.md_working_2.datc1">The COM action with label <b>c1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c1</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by COM action</td></tr></table></span>: <div class="tooltip" style="color:green">COM<div class="right">Calculate the center of mass for a group of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_m.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the list of atoms which are involved the virtual atom's definition<i></i></div></div>=1-10
<b name="data/Graphs.md_working_2.datc2" onclick='showPath("data/Graphs.md_working_2.dat","data/Graphs.md_working_2.datc2","data/Graphs.md_working_2.datc2","violet")'>c2</b><span style="display:none;" id="data/Graphs.md_working_2.datc2">The COM action with label <b>c2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c2</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by COM action</td></tr></table></span>: <div class="tooltip" style="color:green">COM<div class="right">Calculate the center of mass for a group of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_m.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the list of atoms which are involved the virtual atom's definition<i></i></div></div>=11-20
<b name="data/Graphs.md_working_2.datd1" onclick='showPath("data/Graphs.md_working_2.dat","data/Graphs.md_working_2.datd1","data/Graphs.md_working_2.datd1","black")'>d1</b><span style="display:none;" id="data/Graphs.md_working_2.datd1">The DISTANCE action with label <b>d1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d1.x</td><td width="5%"><font color="black">scalar</font></td><td>the x-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.y</td><td width="5%"><font color="black">scalar</font></td><td>the y-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.z</td><td width="5%"><font color="black">scalar</font></td><td>the z-component of the vector connecting the two atoms</td></tr></table></span>: <div class="tooltip" style="color:green">DISTANCE<div class="right">Calculate the distance between a pair of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_d_i_s_t_a_n_c_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the pair of atom that we are calculating the distance between<i></i></div></div>=<b name="data/Graphs.md_working_2.datc1">c1</b>,<b name="data/Graphs.md_working_2.datc2">c2</b> <div class="tooltip">COMPONENTS<div class="right"> calculate the x, y and z components of the distance separately and store them as label<i></i></div></div>
<span id="data/Graphs.md_working_2.datdefr_short"><b name="data/Graphs.md_working_2.datr" onclick='showPath("data/Graphs.md_working_2.dat","data/Graphs.md_working_2.datr","data/Graphs.md_working_2.datr","black")'>r</b><span style="display:none;" id="data/Graphs.md_working_2.datr">The RESTRAINT action with label <b>r</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">r.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">r.force2</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span>: <div class="tooltip" style="color:green">RESTRAINT<div class="right">Adds harmonic and/or linear restraints on one or more variables. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/Graphs.md_working_2.datdefr");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_r_e_s_t_r_a_i_n_t.html">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values the harmonic restraint acts upon<i></i></div></div>=<b name="data/Graphs.md_working_2.datd1">d1.z</b> <div class="tooltip">AT<div class="right">the position of the restraint<i></i></div></div>=1 <div class="tooltip">KAPPA<div class="right"> specifies that the restraint is harmonic and what the values of the force constants on each of the variables are<i></i></div></div>=1
</span><span id="data/Graphs.md_working_2.datdefr_long" style="display:none;"><b name="data/Graphs.md_working_2.datr" onclick='showPath("data/Graphs.md_working_2.dat","data/Graphs.md_working_2.datr","data/Graphs.md_working_2.datr","black")'>r</b>: <div class="tooltip" style="color:green">RESTRAINT<div class="right">Adds harmonic and/or linear restraints on one or more variables. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/Graphs.md_working_2.datdefr");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_r_e_s_t_r_a_i_n_t.html">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values the harmonic restraint acts upon<i></i></div></div>=<b name="data/Graphs.md_working_2.datd1">d1.z</b> <div class="tooltip">AT<div class="right">the position of the restraint<i></i></div></div>=1 <div class="tooltip">KAPPA<div class="right"> specifies that the restraint is harmonic and what the values of the force constants on each of the variables are<i></i></div></div>=1  <div class="tooltip">SLOPE<div class="right"> specifies that the restraint is linear and what the values of the force constants on each of the variables are<i></i></div></div>=0.0
</span><b name="data/Graphs.md_working_2.datf1" onclick='showPath("data/Graphs.md_working_2.dat","data/Graphs.md_working_2.datf1","data/Graphs.md_working_2.datf1","black")'>f1</b><span style="display:none;" id="data/Graphs.md_working_2.datf1">The CUSTOM action with label <b>f1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">f1</td><td width="5%"><font color="black">scalar</font></td><td>an arbitrary function</td></tr></table></span>: <div class="tooltip" style="color:green">CUSTOM<div class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_u_s_t_o_m.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/Graphs.md_working_2.datd1">d1.x</b>,<b name="data/Graphs.md_working_2.datd1">d1.y</b> <div class="tooltip">FUNC<div class="right">the function you wish to evaluate<i></i></div></div>=x*x+y*y <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
<div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/Graphs.md_working_2.datd1">d1.x</b>,<b name="data/Graphs.md_working_2.datd1">d1.y</b>,<b name="data/Graphs.md_working_2.datf1">f1</b>,<b name="data/Graphs.md_working_2.datr">r.bias</b> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=colvar
</pre>
 {% endraw %} 

The file `graph.md` output by the command above is renderable using [mermaid](https://mermaid.js.org/syntax/flowchart.html). You can see the resulting flow chart if you copy and paste the file's contents 
[here](https://mermaid.live/). I used Mermaid to build the charts, as you can insert Mermaid syntax into GitHub markdown. The rendered diagrams then 
appear when GitHub shows the rendered markdown online. 

Each node in the diagram above represents one of the actions from the PLUMED input file. The arrows then indicate how PLMD::Value 
objects are passed between the actions. 

The shape of the node tells you about the type of action: 

* Rectangular nodes with only outwards arrows are [PUT](https://www.plumed.org/doc-master/user-doc/html/_p_u_t.html) actions containing data passed from the MD code. These nodes cannot take PLMD::Value objects created in PLUMED as input. 
* Rectangular nodes are actions like [PRINT](https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html) that only take PLMD::Value as arguments. These nodes cannot create PLMD::Value objects and pass them to other actions. 
* Rounded nodes are actions that can take PLMD::Value objects created within PLUMED as input and pass on such objects as output. 

The arrows connecting the actions provide information about the PLMD::Value object being passed. 

* Passing of __scalars__ is indicated using __black arrows__ 
* Passing of __vectors__ is indicated using __blue arrows__ 
* Passing of __matrices__ is indicated using __red arrows__ 
* Passing of __grids__ is indicated using __greeen arrows__ 
* Passing of __atomic positions__ is indicated using __violet arrows__. An atomic position is just five PLMD::Value objects that are all vectors. These five vectors contain the x, y and z positions of the atoms and the masses and charges of the atoms. 

You can also show how forces are passed between actions by using the command: 

```` 
plumed show_graph --plumed plumed.dat --out graph.md --force 
```` 

When I run the command above on the plumed input above, I obtain the following flowchart: 

```mermaid
flowchart BT 
r(["label=r 
 RESTRAINT 
"])
r -- d1.z --> d1
d1(["label=d1 
 DISTANCE 
"])
c2(["label=c2 
 COM 
"])
c1(["label=c1 
 COM 
"])
Box("label=Box 
 PBC 
")
c1 -- Box --> Box
linkStyle 1 stroke:red,color:red;
c1 --> MD
linkStyle 2 stroke:violet,color:violet;
c2 -- Box --> Box
linkStyle 3 stroke:red,color:red;
c2 --> MD
linkStyle 4 stroke:violet,color:violet;
d1 -- Box --> Box
linkStyle 5 stroke:red,color:red;
d1 -- c1 --> c1
linkStyle 6 stroke:violet,color:violet;
d1 -- c2 --> c2
linkStyle 7 stroke:violet,color:violet;
MD(positions from MD)

```
{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/Graphs.md_working_3.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="Graphs.md_working_3.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="Graphs.md_working_3.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<b name="data/Graphs.md_working_3.datc1" onclick='showPath("data/Graphs.md_working_3.dat","data/Graphs.md_working_3.datc1","data/Graphs.md_working_3.datc1","violet")'>c1</b><span style="display:none;" id="data/Graphs.md_working_3.datc1">The COM action with label <b>c1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c1</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by COM action</td></tr></table></span>: <div class="tooltip" style="color:green">COM<div class="right">Calculate the center of mass for a group of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_m.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the list of atoms which are involved the virtual atom's definition<i></i></div></div>=1-10
<b name="data/Graphs.md_working_3.datc2" onclick='showPath("data/Graphs.md_working_3.dat","data/Graphs.md_working_3.datc2","data/Graphs.md_working_3.datc2","violet")'>c2</b><span style="display:none;" id="data/Graphs.md_working_3.datc2">The COM action with label <b>c2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c2</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by COM action</td></tr></table></span>: <div class="tooltip" style="color:green">COM<div class="right">Calculate the center of mass for a group of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_m.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the list of atoms which are involved the virtual atom's definition<i></i></div></div>=11-20
<b name="data/Graphs.md_working_3.datd1" onclick='showPath("data/Graphs.md_working_3.dat","data/Graphs.md_working_3.datd1","data/Graphs.md_working_3.datd1","black")'>d1</b><span style="display:none;" id="data/Graphs.md_working_3.datd1">The DISTANCE action with label <b>d1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d1.x</td><td width="5%"><font color="black">scalar</font></td><td>the x-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.y</td><td width="5%"><font color="black">scalar</font></td><td>the y-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.z</td><td width="5%"><font color="black">scalar</font></td><td>the z-component of the vector connecting the two atoms</td></tr></table></span>: <div class="tooltip" style="color:green">DISTANCE<div class="right">Calculate the distance between a pair of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_d_i_s_t_a_n_c_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the pair of atom that we are calculating the distance between<i></i></div></div>=<b name="data/Graphs.md_working_3.datc1">c1</b>,<b name="data/Graphs.md_working_3.datc2">c2</b> <div class="tooltip">COMPONENTS<div class="right"> calculate the x, y and z components of the distance separately and store them as label<i></i></div></div>
<span id="data/Graphs.md_working_3.datdefr_short"><b name="data/Graphs.md_working_3.datr" onclick='showPath("data/Graphs.md_working_3.dat","data/Graphs.md_working_3.datr","data/Graphs.md_working_3.datr","black")'>r</b><span style="display:none;" id="data/Graphs.md_working_3.datr">The RESTRAINT action with label <b>r</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">r.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">r.force2</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span>: <div class="tooltip" style="color:green">RESTRAINT<div class="right">Adds harmonic and/or linear restraints on one or more variables. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/Graphs.md_working_3.datdefr");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_r_e_s_t_r_a_i_n_t.html">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values the harmonic restraint acts upon<i></i></div></div>=<b name="data/Graphs.md_working_3.datd1">d1.z</b> <div class="tooltip">AT<div class="right">the position of the restraint<i></i></div></div>=1 <div class="tooltip">KAPPA<div class="right"> specifies that the restraint is harmonic and what the values of the force constants on each of the variables are<i></i></div></div>=1
</span><span id="data/Graphs.md_working_3.datdefr_long" style="display:none;"><b name="data/Graphs.md_working_3.datr" onclick='showPath("data/Graphs.md_working_3.dat","data/Graphs.md_working_3.datr","data/Graphs.md_working_3.datr","black")'>r</b>: <div class="tooltip" style="color:green">RESTRAINT<div class="right">Adds harmonic and/or linear restraints on one or more variables. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/Graphs.md_working_3.datdefr");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_r_e_s_t_r_a_i_n_t.html">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values the harmonic restraint acts upon<i></i></div></div>=<b name="data/Graphs.md_working_3.datd1">d1.z</b> <div class="tooltip">AT<div class="right">the position of the restraint<i></i></div></div>=1 <div class="tooltip">KAPPA<div class="right"> specifies that the restraint is harmonic and what the values of the force constants on each of the variables are<i></i></div></div>=1  <div class="tooltip">SLOPE<div class="right"> specifies that the restraint is linear and what the values of the force constants on each of the variables are<i></i></div></div>=0.0
</span><b name="data/Graphs.md_working_3.datf1" onclick='showPath("data/Graphs.md_working_3.dat","data/Graphs.md_working_3.datf1","data/Graphs.md_working_3.datf1","black")'>f1</b><span style="display:none;" id="data/Graphs.md_working_3.datf1">The CUSTOM action with label <b>f1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">f1</td><td width="5%"><font color="black">scalar</font></td><td>an arbitrary function</td></tr></table></span>: <div class="tooltip" style="color:green">CUSTOM<div class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_u_s_t_o_m.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/Graphs.md_working_3.datd1">d1.x</b>,<b name="data/Graphs.md_working_3.datd1">d1.y</b> <div class="tooltip">FUNC<div class="right">the function you wish to evaluate<i></i></div></div>=x*x+y*y <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
<div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/Graphs.md_working_3.datd1">d1.x</b>,<b name="data/Graphs.md_working_3.datd1">d1.y</b>,<b name="data/Graphs.md_working_3.datf1">f1</b>,<b name="data/Graphs.md_working_3.datr">r.bias</b> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=colvar
</pre>
 {% endraw %} 

Notice that fewer actions are shown in this new graph. This is because the graph above only shows actions that play some role in the force calculation. 

I have found these diagrammatic representations of PLUMED input files enormously beneficial when dealing with complicated PLUMED input files. I will thus use them extensively in these notes about the work that I have done in refining PLUMED. 