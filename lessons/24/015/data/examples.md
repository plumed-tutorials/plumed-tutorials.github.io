# Examples 

All the example are run withing the same environment of the installation procedure 
```bash 
source ./pycvenv/bin/activate 
``` 
Things to know: 
- I am always using "path/to" for indication the directory that contain a file 
- Python will communicate with plumed using a module called "plumedCommunications" that is embedded with `PythonCVInterface.so` 


### Getting the manual 

This is a bonus, but can be helpful: 

###### plumed.dat 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/examples.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="examples.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="examples.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></td></tr><tr><td style="padding:1px"><img src="https://img.shields.io/badge/with-LOAD-yellow.svg" alt="tested on master" /></td></tr>
</table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">LOAD<div class="right">Loads a library, possibly defining new actions. <a href="https://www.plumed.org/doc-master/user-doc/html/_l_o_a_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">file to be loaded<i></i></div></div>=/path/to/PythonCVInterface.so
<br/><span style="display:none;" id="data/examples.md_working_1.dat">The LOAD action with label <b></b> calculates something</span><b name="data/examples.md_working_1.datcvdist" onclick='showPath("data/examples.md_working_1.dat","data/examples.md_working_1.datcvdist","data/examples.md_working_1.datcvdist","brown")'>cvdist</b>: <div class="tooltip" style="color:green">PYCVINTERFACE<div class="right">This action is not part of PLUMED and was included by using a LOAD command <a href="https://www.plumed.org/doc-master/user-doc/html/_l_o_a_d.html" style="color:green">More details</a><i></i></div></div> IMPORT=pyhelp
<span style="display:none;" id="data/examples.md_working_1.datcvdist">The PYCVINTERFACE action with label <b>cvdist</b> calculates something</span></pre>
 {% endraw %} 
###### pyhelp.py 
```python 
import plumedCommunications 
import pydoc 

def plumedInit(_): 
with open('PythonCVInterface.help.txt', 'w') as f: 
h = pydoc.Helper(output=f) 
h(plumedCommunications.PythonCVInterface) 
with open('PythonFunction.help.txt', 'w') as f: 
h = pydoc.Helper(output=f) 
h(plumedCommunications.PythonFunction) 
with open('plumedCommunications.help.txt', 'w') as f: 
h = pydoc.Helper(output=f) 
h(plumedCommunications) 
with open('plumedCommunications.defaults.help.txt', 'w') as f: 
h = pydoc.Helper(output=f) 
h(plumedCommunications.defaults) 
return {"Value":plumedCommunications.defaults.COMPONENT_NODEV, "ATOMS":"1"} 

def plumedCalculate(_): 
return 0 
``` 
Then run with 
`plumed driver --plumed plumed.dat --ixyz traj.xyz` 

This thing will not have any results on the trajectory, but you will get the manual of the interface in a few txt files. 

Or alternatively you can run: 
###### pyhelp_html.py 
```python 
import plumedCommunications 
import pydoc 

def plumedInit(_): 
pydoc.writedoc(plumedCommunications) 
pydoc.writedoc(plumedCommunications.defaults) 
return {"Value":plumedCommunications.defaults.COMPONENT_NODEV, "ATOMS":"1"} 

def plumedCalculate(_): 
return 0 
``` 
To get an extreme bare-bones HTML documentation, that you can browse 
by running `python -m http.server` and then going to the address that appears on the terminal, that usually is 0.0.0.0:8000, with your internet browser. 

### Distance (with PBC) 

In this example we show how to use the PBCs in a calculation: 

###### plumed.dat 
{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/examples.md_working_2.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="examples.md_working_2.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="examples.md_working_2.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></td></tr><tr><td style="padding:1px"><img src="https://img.shields.io/badge/with-LOAD-yellow.svg" alt="tested on master" /></td></tr>
</table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">LOAD<div class="right">Loads a library, possibly defining new actions. <a href="https://www.plumed.org/doc-master/user-doc/html/_l_o_a_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">file to be loaded<i></i></div></div>=path/to/PythonCVInterface.so
<br/><span style="display:none;" id="data/examples.md_working_2.dat">The LOAD action with label <b></b> calculates something</span><b name="data/examples.md_working_2.datcvPY" onclick='showPath("data/examples.md_working_2.dat","data/examples.md_working_2.datcvPY","data/examples.md_working_2.datcvPY","brown")'>cvPY</b>: <div class="tooltip" style="color:green">PYCVINTERFACE<div class="right">This action is not part of PLUMED and was included by using a LOAD command <a href="https://www.plumed.org/doc-master/user-doc/html/_l_o_a_d.html" style="color:green">More details</a><i></i></div></div> ATOMS=1,4 IMPORT=pydistancePBCs CALCULATE=pydist
<br/><b name="data/examples.md_working_2.datcvCPP" onclick='showPath("data/examples.md_working_2.dat","data/examples.md_working_2.datcvCPP","data/examples.md_working_2.datcvCPP","brown")'>cvCPP</b>: <div class="tooltip" style="color:green">DISTANCE<div class="right">Calculate the distance between a pair of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_d_i_s_t_a_n_c_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the pair of atom that we are calculating the distance between<i></i></div></div>=1,4
<br/><span style="display:none;" id="data/examples.md_working_2.datcvCPP">The DISTANCE action with label <b>cvCPP</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cvCPP.value</td><td>the DISTANCE between this pair of atoms</td></tr></table></span><div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=colvar.out <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>
</pre>
 {% endraw %} 
###### pydistancePBCs.py 
```python 
import numpy as np 
import plumedCommunications 

plumedInit={"Value":plumedCommunications.defaults.COMPONENT_NODEV} 

def pydist(action: plumedCommunications.PythonCVInterface): 
at: np.ndarray = action.getPositions() 

d = at[0] - at[1] 
d = action.getPbc().apply([d]) 
assert d.shape[1] == 3, "d is not a (*,3) array" 
d = np.linalg.norm(d[0]) 

return d 

``` 
Here we are getting the pbc calculator from plumed and "patching" the distances with it by using the method `apply` like in C++ plumed, but on a `list/np.ndarray` that must be shaped `[nat,3]` 

### Periodicity 

This is just an example on how the user can work with the periodicity of the retuned variables 
###### plumed.dat 
{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/examples.md_working_3.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="examples.md_working_3.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="examples.md_working_3.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></td></tr><tr><td style="padding:1px"><img src="https://img.shields.io/badge/with-LOAD-yellow.svg" alt="tested on master" /></td></tr>
</table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">LOAD<div class="right">Loads a library, possibly defining new actions. <a href="https://www.plumed.org/doc-master/user-doc/html/_l_o_a_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">file to be loaded<i></i></div></div>=path/to/PythonCVInterface.so
<br/><span style="display:none;" id="data/examples.md_working_3.dat">The LOAD action with label <b></b> calculates something</span><b name="data/examples.md_working_3.datcvPY" onclick='showPath("data/examples.md_working_3.dat","data/examples.md_working_3.datcvPY","data/examples.md_working_3.datcvPY","brown")'>cvPY</b>: <div class="tooltip" style="color:green">PYCVINTERFACE<div class="right">This action is not part of PLUMED and was included by using a LOAD command <a href="https://www.plumed.org/doc-master/user-doc/html/_l_o_a_d.html" style="color:green">More details</a><i></i></div></div> IMPORT=periodicity
<br/><div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=colvar.out <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>
</pre>
 {% endraw %} 

###### periodicity.py 
```python 
import plumedCommunications as PLMD 
import numpy 

plumedInit = dict( 
COMPONENTS=dict( 
nonPeriodic=dict(period=None), 
Periodic={"period": ["0", "1.3"]}, 
PeriodicPI={"period": ["0", "pi"]}, 
), 
ATOMS="1,2", 
) 

def plumedCalculate(action: PLMD.PythonCVInterface): 
ret = { 
"nonPeriodic": action.getStep(), 
"Periodic": action.getStep(), 
"PeriodicPI": action.getStep(), 
} 

return ret 
``` 

### Getting simulation information 

###### plumed.dat 
{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/examples.md_working_4.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="examples.md_working_4.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="examples.md_working_4.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></td></tr><tr><td style="padding:1px"><img src="https://img.shields.io/badge/with-LOAD-yellow.svg" alt="tested on master" /></td></tr>
</table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">LOAD<div class="right">Loads a library, possibly defining new actions. <a href="https://www.plumed.org/doc-master/user-doc/html/_l_o_a_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">file to be loaded<i></i></div></div>=path/to/PythonCVInterface.so
<br/><span style="display:none;" id="data/examples.md_working_4.dat">The LOAD action with label <b></b> calculates something</span><b name="data/examples.md_working_4.datcvPY" onclick='showPath("data/examples.md_working_4.dat","data/examples.md_working_4.datcvPY","data/examples.md_working_4.datcvPY","brown")'>cvPY</b>: <div class="tooltip" style="color:green">PYCVINTERFACE<div class="right">This action is not part of PLUMED and was included by using a LOAD command <a href="https://www.plumed.org/doc-master/user-doc/html/_l_o_a_d.html" style="color:green">More details</a><i></i></div></div> ATOMS=2,4 IMPORT=mdInfo PREPARE=myPrepare
<br/><div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=colvar.out <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>
</pre>
 {% endraw %} 

###### mdInfo.py 
```python 
import plumedCommunications as PLMD 

def plumedInit(action: PLMD.PythonCVInterface): 
myPrint(f"action label: {action.label}") 
return{"Value": PLMD.defaults.COMPONENT_NODEV,} 

def myPrepare(action: PLMD.PythonCVInterface): 
print(f"@step {action.getStep()}") 
print(f"{action.getTime()=}") 
print(f"{action.getTimeStep()=}") 
print(f"{action.isRestart()=}") 
print(f"{action.isExchangeStep()=}") 
return {} 

def plumedCalculate(action: PLMD.PythonCVInterface): 
return 0.0 
``` 