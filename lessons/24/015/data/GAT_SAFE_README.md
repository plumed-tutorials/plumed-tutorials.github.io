# Using PyCV 
## Installation 

_Note that currently we are working on a simpler installation procedure, and some names may change. The actual version cannot be called from within the plumed python interface_ 

For compiling the plugin you just need pybind11 and numpy. 
I always recommend creating and ad-hoc environment for your projects: 
```bash 
python3 -m venv pycvenv 
source ./pycvenv/bin/activate 
pip install -U pip 
pip install -r requirements.txt 
``` 
The requirements.txt file is in the home of the plug in (`plumeddir/plugins/pycv`) 

If you have a plumed that supports plumed mklib with multiple files you can simply 
```bash 
./standaloneCompile.sh 
``` 
This usually goes smooth, especially if plumed has already found the necessary python configuration and `plumed --no-mpi config makefile_conf | grep canPyCV` returns `canPyCV=yes`. 

After running `./standaloneCompile.sh` you should have a `PythonCVInterface.so` file into the pycv directory 

### The basics 

When using PyCV the user will need to create a module[^1] that must at least contain an initialization dictionary and a calculate function 

[^1]: a module is a `.py` file or a directory that contains a `__init__.py`, here we will only show `py` files 

#### What to write in the plumed.dat (PYCVINTERFACE) 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/GAT_SAFE_README.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="GAT_SAFE_README.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="GAT_SAFE_README.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<b name="data/GAT_SAFE_README.md_working_1.datcvPY" onclick='showPath("data/GAT_SAFE_README.md_working_1.dat","data/GAT_SAFE_README.md_working_1.datcvPY","data/GAT_SAFE_README.md_working_1.datcvPY","brown")'>cvPY</b>: <div class="tooltip" style="color:green">PYCVINTERFACE<div class="right">This action is not part of PLUMED and was included by using a LOAD command <a href="https://www.plumed.org/doc-master/user-doc/html/_l_o_a_d.html" style="color:green">More details</a><i></i></div></div> ATOMS=1,4 IMPORT=pydistancePBCs CALCULATE=pydist
<span style="display:none;" id="data/GAT_SAFE_README.md_working_1.datcvPY">The PYCVINTERFACE action with label <b>cvPY</b> calculates something</span></pre>
 {% endraw %} 

- `IMPORT` this is the only mandatory keyword, this indicates the python module to load 
- `INIT` indicates the function to call at initialization. Defaults to `plumedInit` 
- `COMPONENTS` can be specified either in python or in the plumed.dat 
- `NOPBC` can be specified either in python or in the plumed.dat 
- `ATOMS`, `GROUPA`,`GROUPB`, using `GROUP*` will make plumed set up a neighbor list between the groups, or group A, whereas with ATOMS all the atom will be passed 
- `PAIR`,`NLIST`,`NL_CUTOFF`,`NL_STRIDE` can only be specified in the plumed.dat ~to be verified~ 
- `CALCULATE` indicates the function to call at calculate time. Defaults to `plumedCalculate` 
- `PREPARE` indicates the function to call at prepare time. Ignored if not specified 
- `UPDATE` indicates the function to call at update time. Ignored if not specified 

#### What to write in the plumed.dat (PYFUNCTION) 
{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/GAT_SAFE_README.md_working_2.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="GAT_SAFE_README.md_working_2.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="GAT_SAFE_README.md_working_2.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<b name="data/GAT_SAFE_README.md_working_2.datd1" onclick='showPath("data/GAT_SAFE_README.md_working_2.dat","data/GAT_SAFE_README.md_working_2.datd1","data/GAT_SAFE_README.md_working_2.datd1","brown")'>d1</b>: <div class="tooltip" style="color:green">DISTANCE<div class="right">Calculate the distance between a pair of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_d_i_s_t_a_n_c_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the pair of atom that we are calculating the distance between<i></i></div></div>=1,2
<span style="display:none;" id="data/GAT_SAFE_README.md_working_2.datd1">The DISTANCE action with label <b>d1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d1.value</td><td>the DISTANCE between this pair of atoms</td></tr></table></span><b name="data/GAT_SAFE_README.md_working_2.datd2" onclick='showPath("data/GAT_SAFE_README.md_working_2.dat","data/GAT_SAFE_README.md_working_2.datd2","data/GAT_SAFE_README.md_working_2.datd2","brown")'>d2</b>: <div class="tooltip" style="color:green">DISTANCE<div class="right">Calculate the distance between a pair of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_d_i_s_t_a_n_c_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the pair of atom that we are calculating the distance between<i></i></div></div>=1,3 
<br/><span style="display:none;" id="data/GAT_SAFE_README.md_working_2.datd2">The DISTANCE action with label <b>d2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d2.value</td><td>the DISTANCE between this pair of atoms</td></tr></table></span><b name="data/GAT_SAFE_README.md_working_2.datfPY" onclick='showPath("data/GAT_SAFE_README.md_working_2.dat","data/GAT_SAFE_README.md_working_2.datfPY","data/GAT_SAFE_README.md_working_2.datfPY","brown")'>fPY</b>: <div class="tooltip" style="color:green">PYFUNCTION<div class="right">This action is not part of PLUMED and was included by using a LOAD command <a href="https://www.plumed.org/doc-master/user-doc/html/_l_o_a_d.html" style="color:green">More details</a><i></i></div></div> IMPORT=pycvfunc CALCULATE=plumedCalculate ARG=<b name="data/GAT_SAFE_README.md_working_2.datd1">d1</b>,<b name="data/GAT_SAFE_README.md_working_2.datd2">d2</b>
<span style="display:none;" id="data/GAT_SAFE_README.md_working_2.datfPY">The PYFUNCTION action with label <b>fPY</b> calculates something</span></pre>
 {% endraw %} 

- `IMPORT` this is the only mandatory keyword, this indicates the python module to load 
- `INIT` indicates the function to call at initialization. Defaults to `plumedInit` 
- `COMPONENTS` can be specified either in python or in the plumed.dat 
- `CALCULATE` indicates the function to call at calculate time. Defaults to `plumedCalculate` 
- `ARG` the list of arguments, to be specified in the plumed.dat 

PYFUNCTION is simpler: but needs to get the arguments from the plumed object 

```python 
import plumedCommunications as PLMD 
import numpy 

plumedInit={"Value": PLMD.defaults.COMPONENT_NODEV} 

def plumedCalculate(action: PLMD.PythonFunction): 
arg = [action.argument(0),action.argument(1)] 
return arg[0]*arg[0]*arg[1] 
``` 
#### The functions 

For both PYFUNCTION and PYCVINTERFACE the function called by plumed must accept a specific object. 
- PYCVINTERFACE functions will expect a `plumedCommunications.PythonCVInterface` object 
- PYFUNCTION functions will expect a `plumedCommunications.PythonFunction` object 

These objects are used to retrieve data and settings from plumed. Plumed will get data back with the `data` attribute (see [below](#the-data-attribute)) but mainly with the use of returned dictionaries. 

In the [examples](examples.md#getting-the-manual) I show how to retrieve the manual for those objects 


#### Initialization 

If in the plumed.dat `INIT` is not specified, plumed will search for an object "plumedInit", 
that can be either a function that returns a dict or a dict 
This dict MUST contain at least the information about the presence of the 
derivatives and on the periodicity of the variable. 
We will refer to this dict as "the _init dict_" from now. 

The _init dict_ will tell plumed how many components the calculate function will 
return and how they shall behave. 
Along this the dict can contain all the keyword that are compatible with 
PYCVINTERFACE. 
Mind that if the same keyword is specified both in the _init dict_ and in the 
plumed file the calculation will be aborted to avoid unwanted settings conflicts. 
In case of flags the dict entry must be a boolean, differently from the standard 
plumed input. 


The only keyword that can only be specified in python is `COMPONENTS`. 
The `COMPONENTS` key must point to a dict that has as keys the names of the 
components. 
Each component dictionary must have two keys: 
- `"period"`: `None` of a list of two values, min and max (like `[0,1]` or also 
strings like `["0.5*pi","2*pi"]`) 
- `"derivative"`: `True` or `False` 
If you want to use a single component you can create the `"COMPONENTS"` dict 
with as single key, the name will be ignored. 
In the previous example the key `"Value"` is used instead of `"COMPONENTS"`: 
it is a shorter form for `"COMPONENTS":{"any":{...}}`. 
To avoid confusion you cannot specify both `"COMPONENTS"` and `"Value"` in the 
same dict. 

To speed up the declarations of the components the `plumedCommunications` module 
contains a submodule `defaults` with the default dictionaries already set up: 
- `plumedCommunications.defaults.COMPONENT={"period":None, "derivative":True}` 
- `plumedCommunications.defaults.COMPONENT_NODEV={"period":None, "derivative":False}` 

#### Calculate 

If `CALCULATE` is not specified, plumed will search for a function named 
"plumedCalculate" plumed will read the variable returned accordingly to what it 
was specified in the initialization dict. 

The calculate function must, as all the other functions accept a 
`plumedCommunications.PythonCVInterface` (or a `plumedCommunications.PythonFunction` in case of a pyfunction) object as only input. 

The calculate function must either return a float or a tuple or, in the case of 
multiple components, a dict whose keys are the name of the components, whose 
elements are either float or tuple. 

Plumed will assign automatically the result to the CV (to the key named 
element), if the name of the component is missing the calculation will be 
interrupted with an error message. 
If derivatives are disabled it will expect a float(or a double). 
In case of activated derivatives it will interrupt the calculation if the 
return value would not be a tuple. 
The tuple should be (float, ndArray(nat,3),ndArray(3,3)) with the first 
elements the value, the second the atomic derivatives and the third the box 
derivative (that can also have shape(9), with format (x_x, x_y, x_z, y_x, y_y, 
y_z, z_x, z_y, z_z)), if the box derivative are not present a WARNING will be 
raised, but the calculation won't be interrupted. 

#### Prepare 

If the `PREPARE` keyword is used, the defined function will be called at 
prepare time, before calculate. 
The returned "prepare" dictionary can contain a `"setAtomRequest"` key with a parseable 
ATOM string, like in the standard plumed input (or a list of indexes, 0 based). 
```python 
#this , with "PREPARE=changeAtom" in the plumed file will select a new atom at each new step 
def changeAtom(plmdAction: plumedCommunications.PythonCVInterface): 
toret = {"setAtomRequest": f"1, {int(plmdAction.getStep()) + 2}"} 
if plmdAction.getStep() == 3: 
toret["setAtomRequest"] = "1,2" 
return toret 
``` 
#### Update 

If the `UPDATE` keyword is used, the defined function will be called at update 
time, after calculate. As now plumed will ignore the return of this function 
(but it stills need to return a dict) and it is intended to accumulate things 
or post process data afer calculate 

In the example `plmdAction.data["pycv"]=0` is initialized in `pyinit` and its 
value is updated in calculate. 


#### The `data` attribute 
The plumedCommunications.PythonCVInterface has a `data` attribute that is a 
dictionary and can be used to store data during the calculations 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/GAT_SAFE_README.md_working_3.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="GAT_SAFE_README.md_working_3.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="GAT_SAFE_README.md_working_3.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<b name="data/GAT_SAFE_README.md_working_3.datcv1" onclick='showPath("data/GAT_SAFE_README.md_working_3.dat","data/GAT_SAFE_README.md_working_3.datcv1","data/GAT_SAFE_README.md_working_3.datcv1","brown")'>cv1</b>: <div class="tooltip" style="color:green">PYCVINTERFACE<div class="right">This action is not part of PLUMED and was included by using a LOAD command <a href="https://www.plumed.org/doc-master/user-doc/html/_l_o_a_d.html" style="color:green">More details</a><i></i></div></div>  ...
  ATOMS=<div class="tooltip">@mdatoms<div class="right">refers to all the MD codes atoms but not PLUMEDs vatoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_group.html">Click here</a> for more information. <i></i></div></div>
  IMPORT=pycvPersistentData
  CALCULATE=pydist
  INIT=pyinit
...
<br/><div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=colvar.out <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>
</pre>
 {% endraw %} 

```python 
import plumedCommunications as PLMD 
from plumedCommunications.defaults import COMPONENT_NODEV 

def pyinit(plmdAction: PLMD.PythonCVInterface): 
plmdAction.data["pycv"]=0 
print(f"{plmdAction.data=}", file=log) 
return {"Value":COMPONENT_NODEV} 

def pydist(plmdAction: PLMD.PythonCVInterface): 
plmdAction.data["pycv"]+=plmdAction.getStep() 
d=plmdAction.data["pycv"] 
return d 
``` 