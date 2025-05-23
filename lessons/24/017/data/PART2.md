# Part 2: Design a barrier-flattening potential

Now that we have a clear picture about the free-energy surface (FES) we can devise a strategy to accelerate the dynamics along the most probable reaction pathway.

The idea behind this approach is to lower the free energy barrier between the bound and the unbound states in the hope of increasing the reaction rate in both directions. In the language of transition state theory (TST), this corresponds to decreasing the (Gibbs) free energy of activation for both the forward and backward processes ($\Delta^\ddagger G_\pm$) in order to increase the corresponding rate constants,

$$
\begin{equation}
k_\pm \propto e^{-\frac{\Delta^\ddagger G_\pm}{k_B T}}.
\end{equation}
$$

We will use the FES previously computed to craft a barrier-flattening bias. For this, no further simulation is needed as we can directly predict the shape of the FES for any bias potential that is a function of the same variables,

$$
\begin{equation}
G(x, y) = G_0(x, y) + U_\text{bias}(x, y).
\end{equation}
$$

## Choosing a functional form

The choice of $U_\text{bias}$ is rather free, but we need to take some constraints into account:
- It should be continuous
- Far away from the barrier, the bias should be flat so as to minimally affect the thermodynamic ensemble
- The bias should avoid creating stable intermediates

### Instructions

1) Propose a candidate functional form matching the above criteria.

> [!TIP] Tip 1
> Try to transform the input variables so as to make it easier to fit the barrier with common functions (exp, cos, polynomials, etc.)

> [!TIP] Tip 2
> Use Heaviside step functions to restrict the bias to the section of the CV-space you are interested in. Make sure the resulting potential is continuous (and it’s probably a good idea if it’s differentiable too) everywhere the system can go.

2) Using the reweighted FES computed in [Part 1](PART1.md), predict the shape of the biased FES and plot it.

3) Adjust the parameters and/or the functional form until you are satisfied with the resulting free-energy barrier.

### Results

Here is our proposition. For convenience, we defined new variables $X$ and $Y$ as:

$$
\begin{align}
X &= n_{O_P} - n_{O_W} + 6 \\
Y &= n_{O_P} + n_{O_W} - 6
\end{align}
$$

where $X$ can be interpreted as the advancement of the O<sub>W</sub>/O<sub>P</sub> exchange ($X = 0$ is the unbound state, $X = 1$ represents the addition of O<sub>P</sub> to the inner-sphere, and $X = 2$ complete departure of the supranumerary O<sub>W</sub> atom) and $Y$ is the excess coordination relative to the basal $n = 6$.

![Bias design figure](solutions/figures/bias_design_xy.png)

<details><summary>(Click to) See the functional form details.</summary>

$$
U_\text{bias}(X', Y') = -1.875 \cdot\theta(X')\theta(2-X')\theta(Y')\theta(2 - Y')(1 - \cos(X'\pi))(1 - \cos(Y'\pi)) \\
X' = X + 0.12 (1 - \cos(X\pi)) \\
Y' = 2.8Y - 0.7(1 - \cos(X\pi))
$$

![Bias design figure](solutions/figures/bias_design_XY.png)
</details>

Your solution will probably look different, and that's OK since precise shape of the barrier should not matter too much.

## Testing the barrier-flattening bias

Once you are satisfied with functional form of your bias, you can implement it in a Plumed file.

### Instructions

1) Prepare a new directory for the bias testing simulation (you can reuse the same input files as previously).

2) Write a `plumed_bias.dat` file implementing the chosen bias. You will to define a [`CUSTOM`](https://www.plumed.org/doc-v2.9/user-doc/html/_c_u_s_t_o_m.html) collective variable and turn its output value into a biasing potential with [`BIASVALUE`](https://www.plumed.org/doc-v2.9/user-doc/html/_b_i_a_s_v_a_l_u_e.html). 

3) To avoid wasting time with free diffusion of the ion in the simulation box, restrain the Mg<sup>2+</sup> in the vicinity of the O<sub>P</sub> atoms. For example you can use an upper wall on the minimum Mg—O<sub>P</sub> distance to restrain it under $1~\text{nm}$ using the [`DISTANCES`](https://www.plumed.org/doc-v2.9/user-doc/html/_d_i_s_t_a_n_c_e_s.html) multicolvar with the appropriate keyword.

4) Run the simulation.

5) In a Python notebook, plot the timeseries for the two CVs of interest as well as $U_\text{bias}(t)$.

### Template PLUMED file

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/solutions/inputs/plumed_bias.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="plumed_bias.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="plumed_bias.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
<div class="headerBadge"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/solutions/inputs/plumed_bias.dat")' onmousedown='toggleDisplay("data/solutions/inputs/plumed_bias.dat")'/></div>
</div>
</div>
<div id="data/solutions/inputs/plumed_bias.dat_short">
<pre class="plumedlisting">
<span style="color:blue" class="comment"># Barrier-flattening bias for accelerating Mg (un)binding to phosphate oxygen</span>
<b name="data/solutions/inputs/plumed_bias.datmg" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.datmg","data/solutions/inputs/plumed_bias.datmg","brown")'>mg</b>: <span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<span style="display:none;" id="data/solutions/inputs/plumed_bias.datmg">The GROUP action with label <b>mg</b> calculates something</span><b name="data/solutions/inputs/plumed_bias.datop" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.datop","data/solutions/inputs/plumed_bias.datop","brown")'>op</b>: <span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<span style="display:none;" id="data/solutions/inputs/plumed_bias.datop">The GROUP action with label <b>op</b> calculates something</span><b name="data/solutions/inputs/plumed_bias.datow" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.datow","data/solutions/inputs/plumed_bias.datow","brown")'>ow</b>: <span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<br/><span style="display:none;" id="data/solutions/inputs/plumed_bias.datow">The GROUP action with label <b>ow</b> calculates something</span><b name="data/solutions/inputs/plumed_bias.datnop" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.datnop","data/solutions/inputs/plumed_bias.datnop","brown")'>nop</b>: <span class="plumedtooltip" style="color:green">COORDINATION<span class="right">Calculate coordination numbers. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATION" style="color:green">More details</a><i></i></span></span> ...
   <span style="background-color:yellow">__FILL__</span>
...
<br/><span style="display:none;" id="data/solutions/inputs/plumed_bias.datnop">The COORDINATION action with label <b>nop</b> calculates the value of the coordination</span><b name="data/solutions/inputs/plumed_bias.datnow" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.datnow","data/solutions/inputs/plumed_bias.datnow","brown")'>now</b>: <span class="plumedtooltip" style="color:green">COORDINATION<span class="right">Calculate coordination numbers. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATION" style="color:green">More details</a><i></i></span></span> ...
   <span style="background-color:yellow">__FILL__</span>
...
<br/><span style="display:none;" id="data/solutions/inputs/plumed_bias.datnow">The COORDINATION action with label <b>now</b> calculates the value of the coordination</span><b name="data/solutions/inputs/plumed_bias.datdop" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.datdop","data/solutions/inputs/plumed_bias.datdop","brown")'>dop</b>: <span class="plumedtooltip" style="color:green">DISTANCES<span class="right">Calculate the distances between multiple piars of atoms <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCES" style="color:green">More details</a><i></i></span></span> ...
   <span style="background-color:yellow">__FILL__</span>
...
<br/><span style="display:none;" id="data/solutions/inputs/plumed_bias.datdop">The DISTANCES action with label <b>dop</b> calculates the DISTANCES between the each pair of atoms that were specified</span><b name="data/solutions/inputs/plumed_bias.datuwall" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.datuwall","data/solutions/inputs/plumed_bias.datuwall","brown")'>uwall</b>: <span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<br/><span style="display:none;" id="data/solutions/inputs/plumed_bias.datuwall">The UPPER_WALLS action with label <b>uwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">uwall.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">uwall.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span><b name="data/solutions/inputs/plumed_bias.datbias_fn" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.datbias_fn","data/solutions/inputs/plumed_bias.datbias_fn","brown")'>bias_fn</b>: <span class="plumedtooltip" style="color:green">CUSTOM<span class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/CUSTOM" style="color:green">More details</a><i></i></span></span> ...
   <span style="background-color:yellow">__FILL__</span>
...
<br/><span style="display:none;" id="data/solutions/inputs/plumed_bias.datbias_fn">The CUSTOM action with label <b>bias_fn</b> calculates an arbitrary function</span><b name="data/solutions/inputs/plumed_bias.datbias" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.datbias","data/solutions/inputs/plumed_bias.datbias","brown")'>bias</b>: <span class="plumedtooltip" style="color:green">BIASVALUE<span class="right">Takes the value of one variable and use it as a bias <a href="https://www.plumed.org/doc-master/user-doc/html/BIASVALUE" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<br/><span style="display:none;" id="data/solutions/inputs/plumed_bias.datbias">The BIASVALUE action with label <b>bias</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">bias.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">bias._bias</td><td>one or multiple instances of this quantity can be referenced elsewhere in the input file</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/solutions/inputs/plumed_bias.datnop">nop</b>,<b name="data/solutions/inputs/plumed_bias.datnow">now</b>,<b name="data/solutions/inputs/plumed_bias.datdop">dop.lowest</b>,<b name="data/solutions/inputs/plumed_bias.datuwall">uwall.bias</b>,<b name="data/solutions/inputs/plumed_bias.datbias">bias.bias</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=500 <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=<b name="data/solutions/inputs/plumed_bias.datbias">bias.COLVAR</b>
</pre></div>
<div style="display:none;" id="data/solutions/inputs/plumed_bias.dat_long"><pre class="plumedlisting">
<span style="color:blue" class="comment"># Barrier-flattening bias for accelerating Mg (un)binding to phosphate oxygen</span>
<br/><b name="data/solutions/inputs/plumed_bias.dat_solmg" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.dat_solmg","data/solutions/inputs/plumed_bias.dat_solmg","brown")'>mg</b>: <span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the numerical indexes for the set of atoms in the group<i></i></span></span>=60
<span style="display:none;" id="data/solutions/inputs/plumed_bias.dat_solmg">The GROUP action with label <b>mg</b> calculates something</span><b name="data/solutions/inputs/plumed_bias.dat_solop" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.dat_solop","data/solutions/inputs/plumed_bias.dat_solop","brown")'>op</b>: <span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NDX_FILE<span class="right">the name of index file (gromacs syntax)<i></i></span></span>=index_diuridine.ndx <span class="plumedtooltip">NDX_GROUP<span class="right">the name of the group to be imported (gromacs syntax) - first group found is used by default<i></i></span></span>=O_Phosphate
<span style="display:none;" id="data/solutions/inputs/plumed_bias.dat_solop">The GROUP action with label <b>op</b> calculates something</span><b name="data/solutions/inputs/plumed_bias.dat_solow" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.dat_solow","data/solutions/inputs/plumed_bias.dat_solow","brown")'>ow</b>: <span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NDX_FILE<span class="right">the name of index file (gromacs syntax)<i></i></span></span>=index_diuridine.ndx <span class="plumedtooltip">NDX_GROUP<span class="right">the name of the group to be imported (gromacs syntax) - first group found is used by default<i></i></span></span>=O_Water

<span style="display:none;" id="data/solutions/inputs/plumed_bias.dat_solow">The GROUP action with label <b>ow</b> calculates something</span><b name="data/solutions/inputs/plumed_bias.dat_solnop" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.dat_solnop","data/solutions/inputs/plumed_bias.dat_solnop","brown")'>nop</b>: <span class="plumedtooltip" style="color:green">COORDINATION<span class="right">Calculate coordination numbers. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATION" style="color:green">More details</a><i></i></span></span> ...
   <span class="plumedtooltip">GROUPA<span class="right">First list of atoms<i></i></span></span>=<b name="data/solutions/inputs/plumed_bias.dat_solmg">mg</b>
   <span class="plumedtooltip">GROUPB<span class="right">Second list of atoms (if empty, N*(N-1)/2 pairs in GROUPA are counted)<i></i></span></span>=<b name="data/solutions/inputs/plumed_bias.dat_solop">op</b>
   <span class="plumedtooltip">SWITCH<span class="right">This keyword is used if you want to employ an alternative to the continuous switching function defined above. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={COSINUS D_0=0.18 R_0=0.24}
...
<br/><span style="display:none;" id="data/solutions/inputs/plumed_bias.dat_solnop">The COORDINATION action with label <b>nop</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">nop.value</td><td>the value of the coordination</td></tr></table></span><b name="data/solutions/inputs/plumed_bias.dat_solnow" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.dat_solnow","data/solutions/inputs/plumed_bias.dat_solnow","brown")'>now</b>: <span class="plumedtooltip" style="color:green">COORDINATION<span class="right">Calculate coordination numbers. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATION" style="color:green">More details</a><i></i></span></span> ...
   <span class="plumedtooltip">GROUPA<span class="right">First list of atoms<i></i></span></span>=<b name="data/solutions/inputs/plumed_bias.dat_solmg">mg</b>
   <span class="plumedtooltip">GROUPB<span class="right">Second list of atoms (if empty, N*(N-1)/2 pairs in GROUPA are counted)<i></i></span></span>=<b name="data/solutions/inputs/plumed_bias.dat_solow">ow</b>
   <span class="plumedtooltip">SWITCH<span class="right">This keyword is used if you want to employ an alternative to the continuous switching function defined above. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={COSINUS D_0=0.18 R_0=0.24}
...
<br/><span style="display:none;" id="data/solutions/inputs/plumed_bias.dat_solnow">The COORDINATION action with label <b>now</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">now.value</td><td>the value of the coordination</td></tr></table></span><b name="data/solutions/inputs/plumed_bias.dat_soldop" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.dat_soldop","data/solutions/inputs/plumed_bias.dat_soldop","brown")'>dop</b>: <span class="plumedtooltip" style="color:green">DISTANCES<span class="right">Calculate the distances between multiple piars of atoms <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCES" style="color:green">More details</a><i></i></span></span> ...
   <span class="plumedtooltip">GROUPA<span class="right">Calculate the distances between all the atoms in GROUPA and all the atoms in GROUPB<i></i></span></span>=<b name="data/solutions/inputs/plumed_bias.dat_solmg">mg</b>
   <span class="plumedtooltip">GROUPB<span class="right">Calculate the distances between all the atoms in GROUPA and all the atoms in GROUPB<i></i></span></span>=<b name="data/solutions/inputs/plumed_bias.dat_solop">op</b>
   <span class="plumedtooltip">LOWEST<span class="right"> this flag allows you to recover the lowest of these variables<i></i></span></span>
...
<br/><span style="display:none;" id="data/solutions/inputs/plumed_bias.dat_soldop">The DISTANCES action with label <b>dop</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dop.lowest</td><td>the smallest of the colvars</td></tr><tr><td width="5%">dop.value</td><td>the DISTANCES between the each pair of atoms that were specified</td></tr></table></span><b name="data/solutions/inputs/plumed_bias.dat_soluwall" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.dat_soluwall","data/solutions/inputs/plumed_bias.dat_soluwall","brown")'>uwall</b>: <span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=<b name="data/solutions/inputs/plumed_bias.dat_soldop">dop.lowest</b> <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=1 <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=500

<span style="display:none;" id="data/solutions/inputs/plumed_bias.dat_soluwall">The UPPER_WALLS action with label <b>uwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">uwall.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">uwall.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span><b name="data/solutions/inputs/plumed_bias.dat_solbias_fn" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.dat_solbias_fn","data/solutions/inputs/plumed_bias.dat_solbias_fn","brown")'>bias_fn</b>: <span class="plumedtooltip" style="color:green">CUSTOM<span class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/CUSTOM" style="color:green">More details</a><i></i></span></span> ...
   <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<b name="data/solutions/inputs/plumed_bias.dat_solnop">nop</b>,<b name="data/solutions/inputs/plumed_bias.dat_solnow">now</b>
   <span class="plumedtooltip">VAR<span class="right">the names to give each of the arguments in the function<i></i></span></span>=<b name="data/solutions/inputs/plumed_bias.dat_solnop">nop</b>,<b name="data/solutions/inputs/plumed_bias.dat_solnow">now</b>
   <span class="plumedtooltip">FUNC<span class="right">the function you wish to evaluate<i></i></span></span>=-1.875*step(X)*step(2-X)*step(Y)*step(2-Y)*(1-cos(X*pi))*(1-cos(Y*pi));X=x+0.12*(1-cos(x*pi));Y=2.8*y-0.7*(1-cos(x*pi));x=1.039661*(nop-now)+6;y=1.039661*(nop+now)-6
   <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
...
<br/><span style="display:none;" id="data/solutions/inputs/plumed_bias.dat_solbias_fn">The CUSTOM action with label <b>bias_fn</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">bias_fn.value</td><td>an arbitrary function</td></tr></table></span><b name="data/solutions/inputs/plumed_bias.dat_solbias" onclick='showPath("data/solutions/inputs/plumed_bias.dat","data/solutions/inputs/plumed_bias.dat_solbias","data/solutions/inputs/plumed_bias.dat_solbias","brown")'>bias</b>: <span class="plumedtooltip" style="color:green">BIASVALUE<span class="right">Takes the value of one variable and use it as a bias <a href="https://www.plumed.org/doc-master/user-doc/html/BIASVALUE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the scalar/vector arguments whose values will be used as a bias on the system<i></i></span></span>=<b name="data/solutions/inputs/plumed_bias.dat_solbias_fn">bias_fn</b>

<span style="display:none;" id="data/solutions/inputs/plumed_bias.dat_solbias">The BIASVALUE action with label <b>bias</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">bias.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">bias._bias</td><td>one or multiple instances of this quantity can be referenced elsewhere in the input file</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/solutions/inputs/plumed_bias.dat_solnop">nop</b>,<b name="data/solutions/inputs/plumed_bias.dat_solnow">now</b>,<b name="data/solutions/inputs/plumed_bias.dat_soldop">dop.lowest</b>,<b name="data/solutions/inputs/plumed_bias.dat_soluwall">uwall.bias</b>,<b name="data/solutions/inputs/plumed_bias.dat_solbias">bias.bias</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=500 <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=<b name="data/solutions/inputs/plumed_bias.dat_solbias">bias.COLVAR</b>
</pre></div>

 {% endraw %} 

### Results

![Bias test timeseries figure](solutions/figures/bias_timeseries.png)

## Reweighting

If we want to recover the original statistics implied by the force field, we need to reweight out the contribution of our accelerating bias. Each frame of the biased trajectory will receive a weight

$$
\begin{equation}
w(t) \propto \frac{p_0(t)}{p_\text{bias}(t)} = \frac{e^{-\beta U_0(t)}}{e^{-\beta [U_0(t) + U_\text{bias}(t)]}} = e^{\beta U_\text{bias}(t)}.
\end{equation}
$$

Any observable we are interested in can then be estimated using a weighted average on the $N$ frames from our biased trajectory as

$$
\begin{equation}
\langle \mathcal{O} \rangle_{p_0} \approx \frac{1}{N} \sum_{i=1}^{N} w(t_i)\mathcal{O}(t_i).
\end{equation}
$$

The quality of our estimation, however, will depend on the phase space overlap between the biased and unbiased ensembles. A generic way of evaluating the efficiency of our reweighting scheme is to use the Kish effective sample size,

$$
\begin{equation}
N_\text{Kish} = \frac{(\sum_{i=1}^{N}w_i)^2}{\sum_{i=1}^{N}w_i^2}.
\end{equation}
$$

We can interpret $N_\text{Kish}$ as the effective number of sample frames that contribute to the weighted average. In the worst case scenario, $N_\text{Kish} = 1$ and only one frame has a non-zero weight, resulting in a very poor estimate of $\langle \mathcal{O} \rangle_{p_0}$. The higher $N_\text{Kish}$, the better the statistics, with a maximum value at $N_\text{Kish} = N$ for trivial reweighting (e.g. for a constant bias).

### Instructions

1) Compute the Kish effective sample size corresponding to reweighting the simulation to the original force field.

> <details><summary><b>Q:</b> How do you expect the Kish size to vary when increasing the number of magnesium ions (each ion contributing one bias potential) and RNA binding sites?</summary>
> <b>A</b>: Assuming independent Mg<sup>2+</sup>/binding site pairs, we expect the Kish size to decrease faster than linearly with the number of ions. This is because, for a frame to have a significant weight, all biases should simultaneously have a small contribution, <i>i.e.</i> be far from the barrier. This becomes combinatorially unlikely as the number of Mg<sup>2+</sup> increases.</details>

