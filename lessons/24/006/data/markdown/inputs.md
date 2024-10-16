<h3>Input files</h3> 

All files and data required to perform this tutorial are on the [GitHub repository](https://github.com/blake-armstrong/binding-tutorial-PLUMED). They can either be accessed by cloning the repository to your machine; 

``` 
git clone https://github.com/blake-armstrong/binding-tutorial-PLUMED 
``` 

or by following the download instructions in the `README.md` page on the repository to download the basic ZIP file. 

Once downloaded, the input files required to run a simulation with OpenMM and PLUMED are provided in the `simulation_files` directory. Included in the `scripts` directory are bash scripts that will automate setting up the multiple-walker simulation files and will analyse the output for you. These scripts are not strictly necessary to perform this tutorial, as the actions they perform can be carried out manually by the user. All the data has already been produced and analysed, and is presented in the 'data' directory. We will discuss how that data was produced and analysed so you can do it all yourself. 

<h3>OpennMM & PLUMED Installation</h3> 

The first thing we need to do is get a working installation of OpenMM and openmmplumed. [Comprehensive installation instructions for OpenMM](http://docs.openmm.org/latest/userguide/application/01_getting_started.html). We recommend using `conda`, as it is the most straight forward way to install the software without needing to worry about dependencies. See [instructions for installing conda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html). After testing the installation with: 

``` 
python -m openmm.testInstallation 
``` 

All platforms available to you will be shown. In this tutorial we use the CPU platform, and the input files provided set up a simulation to use the CPU platform, which every user should have available by default. The [instructions to install the OpenMM PLUMED plugin](https://github.com/openmm/openmm-plumed) are also very simple when using conda. This will also install the command line plumed tool which will be used for analysis later on. 

<h3>Running a simulation</h3> 

Running the bash script `setup_walkers.sh` 

``` 
bash scripts/setup_walkers.sh 
``` 

or 

``` 
bash scripts/setup_walkers.sh NUMWALKERS 
``` 

will create a set of directory trees within the `data` directory labelled with cylinder radii ranging from 0.0 nm to 0.5 nm. `NUMWALKERS` is an integer for the number of walkers desired with the default being 4 (NB this can be changed but must be greater than 1 for multiple walker metadynamics). These directories are where the multiple walker simulations will be run for systems with various radii for the flat-bottom cylindrical restraining potential. This setup script has been included so that the user can play around with different numbers of walkers in an easy way, if they so desire. By default, it will create directories and setups for four walkers. The details on how to run a single walker are discussed further later. 

If we navigate to the directory for a radius of 0.0 nm, 

``` 
cd data/radius_0.0 
``` 

here we will find a `run.sh` script here that will handle submitting the run.py job for each walker. The `run.py` file (which is located in the `simulation_files` directory) will allow us to run our simulation using OpenMM through its Python API. The `plumed.inp` file which contains the PLUMED specifics. There is an 'analysis.sh' script here as well, which will handle the analysis of our simulation output, which is discussed [here](analysis.md). 

There is [extensive documentation for using the OpenMM Python API](http://docs.openmm.org/latest/userguide/application/02_running_sims.html) which we direct you to if you cannot understand some component of the `run.py` file while we briefly discuss it here. 

<h4>run.py</h4> 

``` 
import openmm as mm 
import openmm.app as app 
import openmm.unit as unit 
from openmmplumed import PlumedForce 
``` 

These lines give us access to the OpenMM code, and the OpenMM PLUMED plugin that can parse a PLUMED input file, interpret it, and provide the instructions to OpenMM. 

``` 
coordinates = "coord.pdb" # Name of our coordinates file. 
forcefield = "argon.xml" # Name of our force field file. 
plumed_file = "plumed.inp" # Name of our PLUMED input file. 
temperature = 300 * unit.kelvin # Simulation temperature. 
timestep = 1e-3 * unit.picosecond # Simulation timestep. 
trel = 1 / unit.picosecond # Thermostat relaxation constant for the Langevin thermostat. 
thermo_file = "output.out" # Name of the file to write our periodic simulation output to. 
nthermo = 10000 # How often to periodicly write simulation output (in steps). 
traj_file = "trajectory.dcd" # Name of the file to periodicly write our system coordinates to. 
ntraj = 10000 # How often to periodicly write our system coordinates (in steps). 
nsteps = 2000000 # Total number of steps to simulate for (this corresponds to 2 ns). 
``` 

Simulation parameter definitions that will be used further in the file. When providing a unit with a dimension, we make use of the OpenMM unit object. By default, each walker will run for 2 ns which should take 5 - 10 minutes to complete. This should be enough to produce a PMF that is sufficiently converged to analyse for our purposes due to the simplicity of the model system. 


``` 
pdb = app.PDBFile(coordinates) 
forcefield = app.ForceField(forcefield) 
platform = mm.Platform.getPlatformByName("CPU") 
properties = {} 

system = forcefield.createSystem( 
pdb.topology, 
nonbondedMethod=app.CutoffNonPeriodic, # Run a non-periodic simulation. 
nonbondedCutoff=0.9 * unit.nanometer, 
useDispersionCorrection=False, 
constraints=None, 
rigidWater=False, 
) 
``` 

The details of this section are better explained in the [OpenMM docs](http://docs.openmm.org/latest/userguide/application/02_running_sims.html). 


``` 
for n, force in enumerate(system.getForces()): 
if force.getName() == "CMMotionRemover": 
system.removeForce(n) 
break 
``` 
This section is needed to prevent the thermal energy from being removed from the system as we have only one particle. It is not important to understand, as it would not generally be necessary for a real simulation. 

``` 
with open(plumed_file, "r") as f: 
script = f.read() 
system.addForce(PlumedForce(script)) 
``` 
This is where a PLUMED input script is read and our forces will be created and added to the system. 

``` 
integrator = mm.LangevinMiddleIntegrator(temperature, trel, timestep) 

simulation = app.Simulation(pdb.topology, system, integrator, platform, properties) 

simulation.context.setPositions(pdb.positions) 
simulation.context.setVelocitiesToTemperature(temperature, random.randrange(99999)) 

simulation.reporters.append( 
app.StateDataReporter( 
thermo_file, 
nthermo, 
separator="\t", 
step=False, 
time=True, 
potentialEnergy=True, 
kineticEnergy=False, 
totalEnergy=False, 
temperature=True, 
volume=True, 
density=True, 
progress=False, 
remainingTime=False, 
speed=True, 
elapsedTime=False, 
) 
) 

simulation.reporters.append(app.DCDReporter(traj_file, ntraj, enforcePeriodicBox=False)) 

simulation.reporters.append( 
app.StateDataReporter( 
stdout, 
int(nsteps / 50), 
separator="\t", 
step=False, 
time=False, 
potentialEnergy=True, 
kineticEnergy=False, 
totalEnergy=False, 
temperature=True, 
volume=True, 
density=False, 
progress=True, 
remainingTime=True, 
speed=True, 
elapsedTime=True, 
totalSteps=nsteps, 
) 
) 

simulation.step(nsteps) 
``` 

The details of this section are better explained in the [OpenMM docs](http://docs.openmm.org/latest/userguide/application/02_running_sims.html). 

<h4>plumed.inp</h4> 

Here we will discuss all of the sections of the PLUMED input file (plumed.inp). 


{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/markdown/inputs.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="inputs.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="inputs.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">RESTART<div class="right">Activate restart. <a href="https://www.plumed.org/doc-master/user-doc/html/_r_e_s_t_a_r_t.html" style="color:green">More details</a><i></i></div></div>
</pre>
 {% endraw %} 
Required for multiple walkers. Ensures each walker reads HILLS from all walkers when initialised. 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/markdown/inputs.md_working_2.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="inputs.md_working_2.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="inputs.md_working_2.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">UNITS<div class="right">This command sets the internal units for the code. <a href="https://www.plumed.org/doc-master/user-doc/html/_u_n_i_t_s.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ENERGY<div class="right">the units of energy<i></i></div></div>=kj/mol <div class="tooltip">LENGTH<div class="right">the units of lengths<i></i></div></div>=nm <div class="tooltip">TIME<div class="right">the units of time<i></i></div></div>=ps
</pre>
 {% endraw %} 
Simulation units. Same as OpenMM units for consistency. Not a necessity. 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/markdown/inputs.md_working_3.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="inputs.md_working_3.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="inputs.md_working_3.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<span id="data/markdown/inputs.md_working_3.datdeffixed1_short"><b name="data/markdown/inputs.md_working_3.datfixed1" onclick='showPath("data/markdown/inputs.md_working_3.dat","data/markdown/inputs.md_working_3.datfixed1","data/markdown/inputs.md_working_3.datfixed1","violet")'>fixed1</b><span style="display:none;" id="data/markdown/inputs.md_working_3.datfixed1">The FIXEDATOM action with label <b>fixed1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">fixed1</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by FIXEDATOM action</td></tr></table></span>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/markdown/inputs.md_working_3.datdeffixed1");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.50
</span><span id="data/markdown/inputs.md_working_3.datdeffixed1_long" style="display:none;"><b name="data/markdown/inputs.md_working_3.datfixed1" onclick='showPath("data/markdown/inputs.md_working_3.dat","data/markdown/inputs.md_working_3.datfixed1","data/markdown/inputs.md_working_3.datfixed1","violet")'>fixed1</b>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/markdown/inputs.md_working_3.datdeffixed1");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.50  <div class="tooltip">SET_MASS<div class="right"> mass of the virtual atom<i></i></div></div>=1 <div class="tooltip">SET_CHARGE<div class="right"> charge of the virtual atom<i></i></div></div>=0
</span><b name="data/markdown/inputs.md_working_3.datd1" onclick='showPath("data/markdown/inputs.md_working_3.dat","data/markdown/inputs.md_working_3.datd1","data/markdown/inputs.md_working_3.datd1","black")'>d1</b><span style="display:none;" id="data/markdown/inputs.md_working_3.datd1">The DISTANCE action with label <b>d1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d1.x</td><td width="5%"><font color="black">scalar</font></td><td>the x-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.y</td><td width="5%"><font color="black">scalar</font></td><td>the y-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.z</td><td width="5%"><font color="black">scalar</font></td><td>the z-component of the vector connecting the two atoms</td></tr></table></span>: <div class="tooltip" style="color:green">DISTANCE<div class="right">Calculate the distance between a pair of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_d_i_s_t_a_n_c_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the pair of atom that we are calculating the distance between<i></i></div></div>=<b name="data/markdown/inputs.md_working_3.datfixed1">fixed1</b>,1 <div class="tooltip">NOPBC<div class="right"> ignore the periodic boundary conditions when calculating distances<i></i></div></div> <div class="tooltip">COMPONENTS<div class="right"> calculate the x, y and z components of the distance separately and store them as label<i></i></div></div>
</pre>
 {% endraw %} 
Here we define our z-distance that we will use for the collective variable. We define a fixed point at the middle of our cubic simulation box (50 Å in each direction) and calculate the distance between the fixed point and our one particle, and save it to the `d1` variable. 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/markdown/inputs.md_working_4.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="inputs.md_working_4.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="inputs.md_working_4.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<span id="data/markdown/inputs.md_working_4.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/markdown/inputs.md_working_4.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/markdown/inputs.md_working_4.dat_hiddenpart1_long" style="display:none;"><span id="data/markdown/inputs.md_working_4.datdeffixed1_short"><b name="data/markdown/inputs.md_working_4.datfixed1" onclick='showPath("data/markdown/inputs.md_working_4.dat","data/markdown/inputs.md_working_4.datfixed1","data/markdown/inputs.md_working_4.datfixed1","violet")'>fixed1</b><span style="display:none;" id="data/markdown/inputs.md_working_4.datfixed1">The FIXEDATOM action with label <b>fixed1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">fixed1</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by FIXEDATOM action</td></tr></table></span>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/markdown/inputs.md_working_4.datdeffixed1");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.50
</span><span id="data/markdown/inputs.md_working_4.datdeffixed1_long" style="display:none;"><b name="data/markdown/inputs.md_working_4.datfixed1" onclick='showPath("data/markdown/inputs.md_working_4.dat","data/markdown/inputs.md_working_4.datfixed1","data/markdown/inputs.md_working_4.datfixed1","violet")'>fixed1</b>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/markdown/inputs.md_working_4.datdeffixed1");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.50  <div class="tooltip">SET_MASS<div class="right"> mass of the virtual atom<i></i></div></div>=1 <div class="tooltip">SET_CHARGE<div class="right"> charge of the virtual atom<i></i></div></div>=0
</span><b name="data/markdown/inputs.md_working_4.datd1" onclick='showPath("data/markdown/inputs.md_working_4.dat","data/markdown/inputs.md_working_4.datd1","data/markdown/inputs.md_working_4.datd1","black")'>d1</b><span style="display:none;" id="data/markdown/inputs.md_working_4.datd1">The DISTANCE action with label <b>d1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d1.x</td><td width="5%"><font color="black">scalar</font></td><td>the x-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.y</td><td width="5%"><font color="black">scalar</font></td><td>the y-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.z</td><td width="5%"><font color="black">scalar</font></td><td>the z-component of the vector connecting the two atoms</td></tr></table></span>: <div class="tooltip" style="color:green">DISTANCE<div class="right">Calculate the distance between a pair of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_d_i_s_t_a_n_c_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the pair of atom that we are calculating the distance between<i></i></div></div>=<b name="data/markdown/inputs.md_working_4.datfixed1">fixed1</b>,1 <div class="tooltip">NOPBC<div class="right"> ignore the periodic boundary conditions when calculating distances<i></i></div></div> <div class="tooltip">COMPONENTS<div class="right"> calculate the x, y and z components of the distance separately and store them as label<i></i></div></div>
<a class="toggler" style="color:red" onclick='toggleDisplay("data/markdown/inputs.md_working_4.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><b name="data/markdown/inputs.md_working_4.datrd" onclick='showPath("data/markdown/inputs.md_working_4.dat","data/markdown/inputs.md_working_4.datrd","data/markdown/inputs.md_working_4.datrd","black")'>rd</b><span style="display:none;" id="data/markdown/inputs.md_working_4.datrd">The CUSTOM action with label <b>rd</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">rd</td><td width="5%"><font color="black">scalar</font></td><td>an arbitrary function</td></tr></table></span>: <div class="tooltip" style="color:green">CUSTOM<div class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_u_s_t_o_m.html" style="color:green">More details</a><i></i></div></div> ...

   <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/markdown/inputs.md_working_4.datd1">d1.x</b>,<b name="data/markdown/inputs.md_working_4.datd1">d1.y</b>
   <div class="tooltip">VAR<div class="right">the names to give each of the arguments in the function<i></i></div></div>=x,y
   <div class="tooltip">FUNC<div class="right">the function you wish to evaluate<i></i></div></div>=0.5*14473*(max(0,sqrt(x^2+y^2)-0.0))^2
   <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
...
<br/><b name="data/markdown/inputs.md_working_4.datrdb" onclick='showPath("data/markdown/inputs.md_working_4.dat","data/markdown/inputs.md_working_4.datrdb","data/markdown/inputs.md_working_4.datrdb","black")'>rdb</b><span style="display:none;" id="data/markdown/inputs.md_working_4.datrdb">The BIASVALUE action with label <b>rdb</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">rdb.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">rdb.rd_bias</td><td width="5%"><font color="black">scalar</font></td><td>one or multiple instances of this quantity can be referenced elsewhere in the input file. these quantities will named with  the arguments of the bias followed by the character string _bias. These quantities tell the user how much the bias is due to each of the colvars. This particular component measures this quantity for the input CV named rd</td></tr></table></span>: <div class="tooltip" style="color:green">BIASVALUE<div class="right">Takes the value of one variable and use it as a bias <a href="https://www.plumed.org/doc-master/user-doc/html/_b_i_a_s_v_a_l_u_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the scalar/vector arguments whose values will be used as a bias on the system<i></i></div></div>=<b name="data/markdown/inputs.md_working_4.datrd">rd</b>
</pre>
 {% endraw %} 
Here we use the x and y components of the d1 variable to create `rd`, the flat-bottomed cylindrical restraining potential. We then tell PLUMED to actually use the potential to apply forces throughout the simulation, and not just record its value. 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/markdown/inputs.md_working_5.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="inputs.md_working_5.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="inputs.md_working_5.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<span id="data/markdown/inputs.md_working_5.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/markdown/inputs.md_working_5.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/markdown/inputs.md_working_5.dat_hiddenpart1_long" style="display:none;"><span id="data/markdown/inputs.md_working_5.datdeffixed1_short"><b name="data/markdown/inputs.md_working_5.datfixed1" onclick='showPath("data/markdown/inputs.md_working_5.dat","data/markdown/inputs.md_working_5.datfixed1","data/markdown/inputs.md_working_5.datfixed1","violet")'>fixed1</b><span style="display:none;" id="data/markdown/inputs.md_working_5.datfixed1">The FIXEDATOM action with label <b>fixed1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">fixed1</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by FIXEDATOM action</td></tr></table></span>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/markdown/inputs.md_working_5.datdeffixed1");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.50
</span><span id="data/markdown/inputs.md_working_5.datdeffixed1_long" style="display:none;"><b name="data/markdown/inputs.md_working_5.datfixed1" onclick='showPath("data/markdown/inputs.md_working_5.dat","data/markdown/inputs.md_working_5.datfixed1","data/markdown/inputs.md_working_5.datfixed1","violet")'>fixed1</b>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/markdown/inputs.md_working_5.datdeffixed1");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.50  <div class="tooltip">SET_MASS<div class="right"> mass of the virtual atom<i></i></div></div>=1 <div class="tooltip">SET_CHARGE<div class="right"> charge of the virtual atom<i></i></div></div>=0
</span><b name="data/markdown/inputs.md_working_5.datd1" onclick='showPath("data/markdown/inputs.md_working_5.dat","data/markdown/inputs.md_working_5.datd1","data/markdown/inputs.md_working_5.datd1","black")'>d1</b><span style="display:none;" id="data/markdown/inputs.md_working_5.datd1">The DISTANCE action with label <b>d1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d1.x</td><td width="5%"><font color="black">scalar</font></td><td>the x-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.y</td><td width="5%"><font color="black">scalar</font></td><td>the y-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.z</td><td width="5%"><font color="black">scalar</font></td><td>the z-component of the vector connecting the two atoms</td></tr></table></span>: <div class="tooltip" style="color:green">DISTANCE<div class="right">Calculate the distance between a pair of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_d_i_s_t_a_n_c_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the pair of atom that we are calculating the distance between<i></i></div></div>=<b name="data/markdown/inputs.md_working_5.datfixed1">fixed1</b>,1 <div class="tooltip">NOPBC<div class="right"> ignore the periodic boundary conditions when calculating distances<i></i></div></div> <div class="tooltip">COMPONENTS<div class="right"> calculate the x, y and z components of the distance separately and store them as label<i></i></div></div>
<a class="toggler" style="color:red" onclick='toggleDisplay("data/markdown/inputs.md_working_5.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><b name="data/markdown/inputs.md_working_5.datuwall" onclick='showPath("data/markdown/inputs.md_working_5.dat","data/markdown/inputs.md_working_5.datuwall","data/markdown/inputs.md_working_5.datuwall","black")'>uwall</b><span style="display:none;" id="data/markdown/inputs.md_working_5.datuwall">The UPPER_WALLS action with label <b>uwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">uwall.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">uwall.force2</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span>: <div class="tooltip" style="color:green">UPPER_WALLS<div class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/_u_p_p_e_r__w_a_l_l_s.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the arguments on which the bias is acting<i></i></div></div>=<b name="data/markdown/inputs.md_working_5.datd1">d1.z</b>  <div class="tooltip">AT<div class="right">the positions of the wall<i></i></div></div>=1.500 <div class="tooltip">KAPPA<div class="right">the force constant for the wall<i></i></div></div>=14473
<b name="data/markdown/inputs.md_working_5.datlwall" onclick='showPath("data/markdown/inputs.md_working_5.dat","data/markdown/inputs.md_working_5.datlwall","data/markdown/inputs.md_working_5.datlwall","black")'>lwall</b><span style="display:none;" id="data/markdown/inputs.md_working_5.datlwall">The LOWER_WALLS action with label <b>lwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">lwall.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">lwall.force2</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span>: <div class="tooltip" style="color:green">LOWER_WALLS<div class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/_l_o_w_e_r__w_a_l_l_s.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the arguments on which the bias is acting<i></i></div></div>=<b name="data/markdown/inputs.md_working_5.datd1">d1.z</b> <div class="tooltip">AT<div class="right">the positions of the wall<i></i></div></div>=-0.125 <div class="tooltip">KAPPA<div class="right">the force constant for the wall<i></i></div></div>=14473
</pre>
 {% endraw %} 

Here we define upper and lower harmonic walls in the z-dimension. The lower wall emulates the repulsion of a surface, and starts acting on the particle at -0.125 nm in the z direction. The upper wall prevents the binding atom from going too far from the `surface` in the z-direction, and starts acting at 1.5 nm. 


{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/markdown/inputs.md_working_6.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="inputs.md_working_6.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="inputs.md_working_6.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<span id="data/markdown/inputs.md_working_6.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/markdown/inputs.md_working_6.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/markdown/inputs.md_working_6.dat_hiddenpart1_long" style="display:none;"><span id="data/markdown/inputs.md_working_6.datdeffixed1_short"><b name="data/markdown/inputs.md_working_6.datfixed1" onclick='showPath("data/markdown/inputs.md_working_6.dat","data/markdown/inputs.md_working_6.datfixed1","data/markdown/inputs.md_working_6.datfixed1","violet")'>fixed1</b><span style="display:none;" id="data/markdown/inputs.md_working_6.datfixed1">The FIXEDATOM action with label <b>fixed1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">fixed1</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by FIXEDATOM action</td></tr></table></span>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/markdown/inputs.md_working_6.datdeffixed1");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.50
</span><span id="data/markdown/inputs.md_working_6.datdeffixed1_long" style="display:none;"><b name="data/markdown/inputs.md_working_6.datfixed1" onclick='showPath("data/markdown/inputs.md_working_6.dat","data/markdown/inputs.md_working_6.datfixed1","data/markdown/inputs.md_working_6.datfixed1","violet")'>fixed1</b>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/markdown/inputs.md_working_6.datdeffixed1");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.50  <div class="tooltip">SET_MASS<div class="right"> mass of the virtual atom<i></i></div></div>=1 <div class="tooltip">SET_CHARGE<div class="right"> charge of the virtual atom<i></i></div></div>=0
</span><b name="data/markdown/inputs.md_working_6.datd1" onclick='showPath("data/markdown/inputs.md_working_6.dat","data/markdown/inputs.md_working_6.datd1","data/markdown/inputs.md_working_6.datd1","black")'>d1</b><span style="display:none;" id="data/markdown/inputs.md_working_6.datd1">The DISTANCE action with label <b>d1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d1.x</td><td width="5%"><font color="black">scalar</font></td><td>the x-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.y</td><td width="5%"><font color="black">scalar</font></td><td>the y-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.z</td><td width="5%"><font color="black">scalar</font></td><td>the z-component of the vector connecting the two atoms</td></tr></table></span>: <div class="tooltip" style="color:green">DISTANCE<div class="right">Calculate the distance between a pair of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_d_i_s_t_a_n_c_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the pair of atom that we are calculating the distance between<i></i></div></div>=<b name="data/markdown/inputs.md_working_6.datfixed1">fixed1</b>,1 <div class="tooltip">NOPBC<div class="right"> ignore the periodic boundary conditions when calculating distances<i></i></div></div> <div class="tooltip">COMPONENTS<div class="right"> calculate the x, y and z components of the distance separately and store them as label<i></i></div></div>
<a class="toggler" style="color:red" onclick='toggleDisplay("data/markdown/inputs.md_working_6.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span id="data/markdown/inputs.md_working_6.datdeffixed2_short"><b name="data/markdown/inputs.md_working_6.datfixed2" onclick='showPath("data/markdown/inputs.md_working_6.dat","data/markdown/inputs.md_working_6.datfixed2","data/markdown/inputs.md_working_6.datfixed2","violet")'>fixed2</b><span style="display:none;" id="data/markdown/inputs.md_working_6.datfixed2">The FIXEDATOM action with label <b>fixed2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">fixed2</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by FIXEDATOM action</td></tr></table></span>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/markdown/inputs.md_working_6.datdeffixed2");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.80
</span><span id="data/markdown/inputs.md_working_6.datdeffixed2_long" style="display:none;"><b name="data/markdown/inputs.md_working_6.datfixed2" onclick='showPath("data/markdown/inputs.md_working_6.dat","data/markdown/inputs.md_working_6.datfixed2","data/markdown/inputs.md_working_6.datfixed2","violet")'>fixed2</b>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/markdown/inputs.md_working_6.datdeffixed2");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.80  <div class="tooltip">SET_MASS<div class="right"> mass of the virtual atom<i></i></div></div>=1 <div class="tooltip">SET_CHARGE<div class="right"> charge of the virtual atom<i></i></div></div>=0
</span><b name="data/markdown/inputs.md_working_6.datd2" onclick='showPath("data/markdown/inputs.md_working_6.dat","data/markdown/inputs.md_working_6.datd2","data/markdown/inputs.md_working_6.datd2","black")'>d2</b><span style="display:none;" id="data/markdown/inputs.md_working_6.datd2">The DISTANCE action with label <b>d2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d2.x</td><td width="5%"><font color="black">scalar</font></td><td>the x-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d2.y</td><td width="5%"><font color="black">scalar</font></td><td>the y-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d2.z</td><td width="5%"><font color="black">scalar</font></td><td>the z-component of the vector connecting the two atoms</td></tr></table></span>: <div class="tooltip" style="color:green">DISTANCE<div class="right">Calculate the distance between a pair of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_d_i_s_t_a_n_c_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the pair of atom that we are calculating the distance between<i></i></div></div>=<b name="data/markdown/inputs.md_working_6.datfixed2">fixed2</b>,1 <div class="tooltip">NOPBC<div class="right"> ignore the periodic boundary conditions when calculating distances<i></i></div></div> <div class="tooltip">COMPONENTS<div class="right"> calculate the x, y and z components of the distance separately and store them as label<i></i></div></div>
<br/><b name="data/markdown/inputs.md_working_6.datrd1" onclick='showPath("data/markdown/inputs.md_working_6.dat","data/markdown/inputs.md_working_6.datrd1","data/markdown/inputs.md_working_6.datrd1","black")'>rd1</b><span style="display:none;" id="data/markdown/inputs.md_working_6.datrd1">The CUSTOM action with label <b>rd1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">rd1</td><td width="5%"><font color="black">scalar</font></td><td>an arbitrary function</td></tr></table></span>: <div class="tooltip" style="color:green">CUSTOM<div class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_u_s_t_o_m.html" style="color:green">More details</a><i></i></div></div> ...

   <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/markdown/inputs.md_working_6.datd1">d1.x</b>,<b name="data/markdown/inputs.md_working_6.datd1">d1.y</b>,<b name="data/markdown/inputs.md_working_6.datd1">d1.z</b>
   <div class="tooltip">VAR<div class="right">the names to give each of the arguments in the function<i></i></div></div>=ax,ay,az
   <div class="tooltip">FUNC<div class="right">the function you wish to evaluate<i></i></div></div>=sqrt(ax^2+ay^2+az^2
   <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
...
<br/><b name="data/markdown/inputs.md_working_6.datrd2" onclick='showPath("data/markdown/inputs.md_working_6.dat","data/markdown/inputs.md_working_6.datrd2","data/markdown/inputs.md_working_6.datrd2","black")'>rd2</b><span style="display:none;" id="data/markdown/inputs.md_working_6.datrd2">The CUSTOM action with label <b>rd2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">rd2</td><td width="5%"><font color="black">scalar</font></td><td>an arbitrary function</td></tr></table></span>: <div class="tooltip" style="color:green">CUSTOM<div class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_u_s_t_o_m.html" style="color:green">More details</a><i></i></div></div> ...

   <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/markdown/inputs.md_working_6.datd2">d2.x</b>,<b name="data/markdown/inputs.md_working_6.datd2">d2.y</b>,<b name="data/markdown/inputs.md_working_6.datd2">d2.z</b>
   <div class="tooltip">VAR<div class="right">the names to give each of the arguments in the function<i></i></div></div>=bx,by,bz
   <div class="tooltip">FUNC<div class="right">the function you wish to evaluate<i></i></div></div>=sqrt(bx^2+by^2+bz^2
   <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
...
<br/><b name="data/markdown/inputs.md_working_6.datg" onclick='showPath("data/markdown/inputs.md_working_6.dat","data/markdown/inputs.md_working_6.datg","data/markdown/inputs.md_working_6.datg","black")'>g</b><span style="display:none;" id="data/markdown/inputs.md_working_6.datg">The CUSTOM action with label <b>g</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">g</td><td width="5%"><font color="black">scalar</font></td><td>an arbitrary function</td></tr></table></span>: <div class="tooltip" style="color:green">CUSTOM<div class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_u_s_t_o_m.html" style="color:green">More details</a><i></i></div></div> ...

   <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/markdown/inputs.md_working_6.datrd1">rd1</b>,<b name="data/markdown/inputs.md_working_6.datrd2">rd2</b>
   <div class="tooltip">VAR<div class="right">the names to give each of the arguments in the function<i></i></div></div>=x,y
   <div class="tooltip">FUNC<div class="right">the function you wish to evaluate<i></i></div></div>=-30*exp(-((x)^2/(2*(0.1^2))))+15*exp(-((y)^2/(2*(0.1^2
   <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
...
<br/><b name="data/markdown/inputs.md_working_6.datpes" onclick='showPath("data/markdown/inputs.md_working_6.dat","data/markdown/inputs.md_working_6.datpes","data/markdown/inputs.md_working_6.datpes","black")'>pes</b><span style="display:none;" id="data/markdown/inputs.md_working_6.datpes">The BIASVALUE action with label <b>pes</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">pes.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">pes.g_bias</td><td width="5%"><font color="black">scalar</font></td><td>one or multiple instances of this quantity can be referenced elsewhere in the input file. these quantities will named with  the arguments of the bias followed by the character string _bias. These quantities tell the user how much the bias is due to each of the colvars. This particular component measures this quantity for the input CV named g</td></tr></table></span>: <div class="tooltip" style="color:green">BIASVALUE<div class="right">Takes the value of one variable and use it as a bias <a href="https://www.plumed.org/doc-master/user-doc/html/_b_i_a_s_v_a_l_u_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the scalar/vector arguments whose values will be used as a bias on the system<i></i></div></div>=<b name="data/markdown/inputs.md_working_6.datg">g</b>
</pre>
 {% endraw %} 

The following is used to create an arbitrary potential energy surface that mimics the binding profile of an atom normal to a surface. There will be a minimum at [2.5, 2.5, 2.5] nm to represent a stable surface site and a maximum at [2.5, 2.5, 2.8] nm to represent a barrier for leaving the surface. 


{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/markdown/inputs.md_working_7.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="inputs.md_working_7.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="inputs.md_working_7.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<span id="data/markdown/inputs.md_working_7.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/markdown/inputs.md_working_7.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/markdown/inputs.md_working_7.dat_hiddenpart1_long" style="display:none;"><span id="data/markdown/inputs.md_working_7.datdeffixed1_short"><b name="data/markdown/inputs.md_working_7.datfixed1" onclick='showPath("data/markdown/inputs.md_working_7.dat","data/markdown/inputs.md_working_7.datfixed1","data/markdown/inputs.md_working_7.datfixed1","violet")'>fixed1</b><span style="display:none;" id="data/markdown/inputs.md_working_7.datfixed1">The FIXEDATOM action with label <b>fixed1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">fixed1</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by FIXEDATOM action</td></tr></table></span>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/markdown/inputs.md_working_7.datdeffixed1");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.50
</span><span id="data/markdown/inputs.md_working_7.datdeffixed1_long" style="display:none;"><b name="data/markdown/inputs.md_working_7.datfixed1" onclick='showPath("data/markdown/inputs.md_working_7.dat","data/markdown/inputs.md_working_7.datfixed1","data/markdown/inputs.md_working_7.datfixed1","violet")'>fixed1</b>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/markdown/inputs.md_working_7.datdeffixed1");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.50  <div class="tooltip">SET_MASS<div class="right"> mass of the virtual atom<i></i></div></div>=1 <div class="tooltip">SET_CHARGE<div class="right"> charge of the virtual atom<i></i></div></div>=0
</span><b name="data/markdown/inputs.md_working_7.datd1" onclick='showPath("data/markdown/inputs.md_working_7.dat","data/markdown/inputs.md_working_7.datd1","data/markdown/inputs.md_working_7.datd1","black")'>d1</b><span style="display:none;" id="data/markdown/inputs.md_working_7.datd1">The DISTANCE action with label <b>d1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d1.x</td><td width="5%"><font color="black">scalar</font></td><td>the x-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.y</td><td width="5%"><font color="black">scalar</font></td><td>the y-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.z</td><td width="5%"><font color="black">scalar</font></td><td>the z-component of the vector connecting the two atoms</td></tr></table></span>: <div class="tooltip" style="color:green">DISTANCE<div class="right">Calculate the distance between a pair of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_d_i_s_t_a_n_c_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the pair of atom that we are calculating the distance between<i></i></div></div>=<b name="data/markdown/inputs.md_working_7.datfixed1">fixed1</b>,1 <div class="tooltip">NOPBC<div class="right"> ignore the periodic boundary conditions when calculating distances<i></i></div></div> <div class="tooltip">COMPONENTS<div class="right"> calculate the x, y and z components of the distance separately and store them as label<i></i></div></div>
<br/><span id="data/markdown/inputs.md_working_7.datdeffixed2_short"><b name="data/markdown/inputs.md_working_7.datfixed2" onclick='showPath("data/markdown/inputs.md_working_7.dat","data/markdown/inputs.md_working_7.datfixed2","data/markdown/inputs.md_working_7.datfixed2","violet")'>fixed2</b><span style="display:none;" id="data/markdown/inputs.md_working_7.datfixed2">The FIXEDATOM action with label <b>fixed2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">fixed2</td><td width="5%"><font color="violet">atoms</font></td><td>virtual atom calculated by FIXEDATOM action</td></tr></table></span>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/markdown/inputs.md_working_7.datdeffixed2");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.80
</span><span id="data/markdown/inputs.md_working_7.datdeffixed2_long" style="display:none;"><b name="data/markdown/inputs.md_working_7.datfixed2" onclick='showPath("data/markdown/inputs.md_working_7.dat","data/markdown/inputs.md_working_7.datfixed2","data/markdown/inputs.md_working_7.datfixed2","violet")'>fixed2</b>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/markdown/inputs.md_working_7.datdeffixed2");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.80  <div class="tooltip">SET_MASS<div class="right"> mass of the virtual atom<i></i></div></div>=1 <div class="tooltip">SET_CHARGE<div class="right"> charge of the virtual atom<i></i></div></div>=0
</span><b name="data/markdown/inputs.md_working_7.datd2" onclick='showPath("data/markdown/inputs.md_working_7.dat","data/markdown/inputs.md_working_7.datd2","data/markdown/inputs.md_working_7.datd2","black")'>d2</b><span style="display:none;" id="data/markdown/inputs.md_working_7.datd2">The DISTANCE action with label <b>d2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d2.x</td><td width="5%"><font color="black">scalar</font></td><td>the x-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d2.y</td><td width="5%"><font color="black">scalar</font></td><td>the y-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d2.z</td><td width="5%"><font color="black">scalar</font></td><td>the z-component of the vector connecting the two atoms</td></tr></table></span>: <div class="tooltip" style="color:green">DISTANCE<div class="right">Calculate the distance between a pair of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_d_i_s_t_a_n_c_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the pair of atom that we are calculating the distance between<i></i></div></div>=<b name="data/markdown/inputs.md_working_7.datfixed2">fixed2</b>,1 <div class="tooltip">NOPBC<div class="right"> ignore the periodic boundary conditions when calculating distances<i></i></div></div> <div class="tooltip">COMPONENTS<div class="right"> calculate the x, y and z components of the distance separately and store them as label<i></i></div></div>
<br/><b name="data/markdown/inputs.md_working_7.datrd1" onclick='showPath("data/markdown/inputs.md_working_7.dat","data/markdown/inputs.md_working_7.datrd1","data/markdown/inputs.md_working_7.datrd1","black")'>rd1</b><span style="display:none;" id="data/markdown/inputs.md_working_7.datrd1">The CUSTOM action with label <b>rd1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">rd1</td><td width="5%"><font color="black">scalar</font></td><td>an arbitrary function</td></tr></table></span>: <div class="tooltip" style="color:green">CUSTOM<div class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_u_s_t_o_m.html" style="color:green">More details</a><i></i></div></div> ...

   <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/markdown/inputs.md_working_7.datd1">d1.x</b>,<b name="data/markdown/inputs.md_working_7.datd1">d1.y</b>,<b name="data/markdown/inputs.md_working_7.datd1">d1.z</b>
   <div class="tooltip">VAR<div class="right">the names to give each of the arguments in the function<i></i></div></div>=ax,ay,az
   <div class="tooltip">FUNC<div class="right">the function you wish to evaluate<i></i></div></div>=sqrt(ax^2+ay^2+az^2
   <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
...
<br/><b name="data/markdown/inputs.md_working_7.datrd2" onclick='showPath("data/markdown/inputs.md_working_7.dat","data/markdown/inputs.md_working_7.datrd2","data/markdown/inputs.md_working_7.datrd2","black")'>rd2</b><span style="display:none;" id="data/markdown/inputs.md_working_7.datrd2">The CUSTOM action with label <b>rd2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">rd2</td><td width="5%"><font color="black">scalar</font></td><td>an arbitrary function</td></tr></table></span>: <div class="tooltip" style="color:green">CUSTOM<div class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_u_s_t_o_m.html" style="color:green">More details</a><i></i></div></div> ...

   <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/markdown/inputs.md_working_7.datd2">d2.x</b>,<b name="data/markdown/inputs.md_working_7.datd2">d2.y</b>,<b name="data/markdown/inputs.md_working_7.datd2">d2.z</b>
   <div class="tooltip">VAR<div class="right">the names to give each of the arguments in the function<i></i></div></div>=bx,by,bz
   <div class="tooltip">FUNC<div class="right">the function you wish to evaluate<i></i></div></div>=sqrt(bx^2+by^2+bz^2
   <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
...
<br/><b name="data/markdown/inputs.md_working_7.datg" onclick='showPath("data/markdown/inputs.md_working_7.dat","data/markdown/inputs.md_working_7.datg","data/markdown/inputs.md_working_7.datg","black")'>g</b><span style="display:none;" id="data/markdown/inputs.md_working_7.datg">The CUSTOM action with label <b>g</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">g</td><td width="5%"><font color="black">scalar</font></td><td>an arbitrary function</td></tr></table></span>: <div class="tooltip" style="color:green">CUSTOM<div class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_u_s_t_o_m.html" style="color:green">More details</a><i></i></div></div> ...

   <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/markdown/inputs.md_working_7.datrd1">rd1</b>,<b name="data/markdown/inputs.md_working_7.datrd2">rd2</b>
   <div class="tooltip">VAR<div class="right">the names to give each of the arguments in the function<i></i></div></div>=x,y
   <div class="tooltip">FUNC<div class="right">the function you wish to evaluate<i></i></div></div>=-30*exp(-((x)^2/(2*(0.1^2))))+15*exp(-((y)^2/(2*(0.1^2
   <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
...
<br/><b name="data/markdown/inputs.md_working_7.datpes" onclick='showPath("data/markdown/inputs.md_working_7.dat","data/markdown/inputs.md_working_7.datpes","data/markdown/inputs.md_working_7.datpes","black")'>pes</b><span style="display:none;" id="data/markdown/inputs.md_working_7.datpes">The BIASVALUE action with label <b>pes</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">pes.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">pes.g_bias</td><td width="5%"><font color="black">scalar</font></td><td>one or multiple instances of this quantity can be referenced elsewhere in the input file. these quantities will named with  the arguments of the bias followed by the character string _bias. These quantities tell the user how much the bias is due to each of the colvars. This particular component measures this quantity for the input CV named g</td></tr></table></span>: <div class="tooltip" style="color:green">BIASVALUE<div class="right">Takes the value of one variable and use it as a bias <a href="https://www.plumed.org/doc-master/user-doc/html/_b_i_a_s_v_a_l_u_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the scalar/vector arguments whose values will be used as a bias on the system<i></i></div></div>=<b name="data/markdown/inputs.md_working_7.datg">g</b>
<a class="toggler" style="color:red" onclick='toggleDisplay("data/markdown/inputs.md_working_7.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=colvar <div class="tooltip">STRIDE<div class="right"> the frequency with which the quantities of interest should be output<i></i></div></div>=1000 <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>
</pre>
 {% endraw %} 
This will output a collective variable file to monitor that everything in the simulation is proceeding as expected. 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/markdown/inputs.md_working_8.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="inputs.md_working_8.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="inputs.md_working_8.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">FLUSH<div class="right">This command instructs plumed to flush all the open files with a user specified frequency. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_l_u_s_h.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">STRIDE<div class="right">the frequency with which all the open files should be flushed<i></i></div></div>=1000
</pre>
 {% endraw %} 
This will flush the output every 1000 steps, allowing us to monitor that everything within PLUMED is working as it should while the simulation is running. 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/markdown/inputs.md_working_9.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="inputs.md_working_9.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="inputs.md_working_9.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<span id="data/markdown/inputs.md_working_9.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/markdown/inputs.md_working_9.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/markdown/inputs.md_working_9.dat_hiddenpart1_long" style="display:none;"><b name="data/markdown/inputs.md_working_9.datfixed1" onclick='showPath("data/markdown/inputs.md_working_9.dat","data/markdown/inputs.md_working_9.datfixed1","data/markdown/inputs.md_working_9.datfixed1","brown")'>fixed1</b>: <div class="tooltip" style="color:green">FIXEDATOM<div class="right">Add a virtual atom in a fixed position. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_i_x_e_d_a_t_o_m.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">AT<div class="right">coordinates of the virtual atom<i></i></div></div>=2.50,2.50,2.50
<span style="display:none;" id="data/markdown/inputs.md_working_9.datfixed1">The FIXEDATOM action with label <b>fixed1</b> calculates something</span><b name="data/markdown/inputs.md_working_9.datd1" onclick='showPath("data/markdown/inputs.md_working_9.dat","data/markdown/inputs.md_working_9.datd1","data/markdown/inputs.md_working_9.datd1","brown")'>d1</b>: <div class="tooltip" style="color:green">DISTANCE<div class="right">Calculate the distance between a pair of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/_d_i_s_t_a_n_c_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the pair of atom that we are calculating the distance between<i></i></div></div>=<b name="data/markdown/inputs.md_working_9.datfixed1">fixed1</b>,1 <div class="tooltip">NOPBC<div class="right"> ignore the periodic boundary conditions when calculating distances<i></i></div></div> <div class="tooltip">COMPONENTS<div class="right"> calculate the x, y and z components of the distance separately and store them as label<i></i></div></div>
<a class="toggler" style="color:red" onclick='toggleDisplay("data/markdown/inputs.md_working_9.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span style="color:blue" class="comment">#SETTINGS NREPLICAS=3</span>
<span style="display:none;" id="data/markdown/inputs.md_working_9.datd1">The DISTANCE action with label <b>d1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d1.x</td><td>the x-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.y</td><td>the y-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.z</td><td>the z-component of the vector connecting the two atoms</td></tr><tr><td width="5%">d1.value</td><td>the DISTANCE between this pair of atoms</td></tr></table></span><div class="tooltip" style="color:green">METAD<div class="right">Used to performed metadynamics on one or more collective variables. <a href="https://www.plumed.org/doc-master/user-doc/html/_m_e_t_a_d.html" style="color:green">More details</a><i></i></div></div> ...
  <div class="tooltip">ARG<div class="right">the labels of the scalars on which the bias will act<i></i></div></div>=<b name="data/markdown/inputs.md_working_9.datd1">d1.z</b>                      <span style="color:blue" class="comment"># Active CV.</span>
  <div class="tooltip">HEIGHT<div class="right">the heights of the Gaussian hills<i></i></div></div>=2.5                    <span style="color:blue" class="comment"># Gaussian height. Approximately kBT in this case.</span>
  <div class="tooltip">SIGMA<div class="right">the widths of the Gaussian hills<i></i></div></div>=0.01                    <span style="color:blue" class="comment"># gaussian width.</span>
  <div class="tooltip">PACE<div class="right">the frequency for hill addition<i></i></div></div>=1000                     <span style="color:blue" class="comment"># Gaussian deposition pace.</span>
  <div class="tooltip">BIASFACTOR<div class="right">use well tempered metadynamics and use this bias factor<i></i></div></div>=18 <div class="tooltip">TEMP<div class="right">the system temperature - this is only needed if you are doing well-tempered metadynamics<i></i></div></div>=300        <span style="color:blue" class="comment"># Well-tempered parameters.</span>
  <div class="tooltip">GRID_MIN<div class="right">the lower bounds for the grid<i></i></div></div>=-0.5                 <span style="color:blue" class="comment"># Grid parameters for d1.z CV.</span>
  <div class="tooltip">GRID_MAX<div class="right">the upper bounds for the grid<i></i></div></div>=1.8                  <span style="color:blue" class="comment">#</span>
  <div class="tooltip">WALKERS_DIR<div class="right">shared directory with the hills files from all the walkers<i></i></div></div>=../BIAS           <span style="color:blue" class="comment"># Multiple walkers directory for reading/writing BIAS.</span>
  <div class="tooltip">WALKERS_RSTRIDE<div class="right">stride for reading hills files<i></i></div></div>=1000          <span style="color:blue" class="comment"># Multiple walkers reading pace.</span>
  <div class="tooltip">WALKERS_ID<div class="right">walker id<i></i></div></div>=REPLACEWALKERID    <span style="color:blue" class="comment"># ID of current walker.</span>
  <div class="tooltip">WALKERS_N<div class="right">number of walkers<i></i></div></div>=REPLACETOTALWALKERS <span style="color:blue" class="comment"># Total number of walkers.</span>
... METAD
</pre>
 {% endraw %} 

This tells PLUMED to run multiple walker metadynamics with a collective variable defined as the z-component of the `d1` distance. WALKERS_ID and WALKERS_N are set to placeholder names which will get replaced when submitting the job through the `run.sh` script. While the multiple walkers run, the HILLS files will be written to and read from the 'BIAS' directory. If you wish to run a single walker simulation, the `RESTART` keyword should be removed, alongside the last four lines inside the `METAD` section. The `HILLS` file will then be written inside the current directory instead of a dedicated `BIAS` directory. The analysis scripts will then need to be modified accordingly. 

<h4>run.sh</h4> 

The `run.sh` file will handle submitting all of the walkers for a given simulation. 

``` 
export OPENMM_CPU_THREADS=1 
``` 
The `OPENMM_CPU_THREADS` environmental variable is used for OpenMM to assign the number of threads per job on the CPU. If this isn't set OpenMM will use all of your available CPU cores. In our case where our system only has one atom, it is the most efficient to run with only one thread per walker. 

``` 
pids="" 
for w in Walker_*; do 
cd ${w} 
pid=$(python3 ../../scripts/run.py > screen.out & echo $!) 
echo "Running ${w} with PID ${pid}" 
pids="${pids}${pid} " 
cd .. 
done 
echo "To kill walkers call ' kill -9 ${pids} '" 
``` 

This for loop iterates through every walker directory and runs `python3 ../../simulation_files/run.py` to begin the metadynamics simulation, and submits the job as a background process with `&`. The script saves the process ID and outputs it to the screen afterwards to make it easy to kill the background processes if something goes wrong. On UNIX-based operating systems you can run either the `top` or `htop` command to monitor the background processes. 

<h4>Beginning the simulation</h4> 

To begin your simulations for a given radius run the command `bash run.sh` from the `data/radius_0.x` directory. If you do not modify the `run.py` file, each walker will run for 100 ns to give a combined time of 400 ns. This amount of time is enough for the PMFs to adequately converge. Feel free to run for longer to get an even smoother profile! Once your simulations have finished running, it is time to [analyse](analysis.md). 

--- 

[Back to binding tutorial main page.](../NAVIGATION.md) 
