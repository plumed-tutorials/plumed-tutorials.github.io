# PLUMED Masterclass 22.12
# Liquid-solid chemical potential differences with the environment similarity CV 

Author: Pablo Piaggi

Date: July 18, 2022

## Aims

This Masterclass is an introduction to the use of the environment similarity CV available in PLUMED to the calculation of liquid-solid free energy differences (chemical potentials).

## Objectives

The objectives of this Masterclass are:
- Learn to define reference environments for a crystal structure and choose appropriate parameters
- Learn how to run **bulk interconversion** simulations in which the bulk liquid and the bulk solid are reversibly interconverted
- Learn how to run **biased coexistence** simulations (similar to interface pinning)
- Learn how to perform **thermodynamic integration** along isobars
- Understand the importance of finite size effects
- Understand the advantages and limitations of each method
- Understand how these methods complement each other

## Prerequisites

We assume that the person that will follow this tutorial is familiar with the Linux terminal, LAMMPS, and basic functionality of PLUMED.
Knowledge of one enhanced sampling technique, such as metadynamics, is recommended.
Familiarity with at least one plotting software is required, for instance, gnuplot, xmgrace, or python with matplotlib.

## Setting up PLUMED

We will use LAMMPS and PLUMED to perform the calculations.
Conda packages with the software required for this class have been prepared and you can install them following the instructions in [this link](https://github.com/plumed/masterclass-2022).
Make sure to install the conda package for LAMMPS.

The environment similarity CV is a part of the crystallization module and you will need to enable this module if you are compiling PLUMED on your own.
Also, LAMMPS has to be compiled with the following optional packages PLUMED, MANYBODY, EXTRA-DUMP, and EXTRA-FIX.

The data needed to run the exercises of this Masterclass can be found on [GitHub](https://github.com/PabloPiaggi/masterclass-22-12).
You can clone this repository locally on your machine using the following command:
```
git clone https://github.com/PabloPiaggi/masterclass-22-12
```

I suggest that you install the trajectory visualization software [Ovito](https://www.ovito.org/) before starting the tutorial.

## Summary of theory

We would like to define a per-atom quantity that tells us how similar the environments around atoms in the simulation box are to the environments found in some reference crystal structure.
Crystal structures are usually defined by a Bravais lattice with an associated basis of atoms.
An important consideration, that follows from the symmetry properties of lattices, is that the number of distinct environments that exist in a crystal structure is equal to the number of atoms in the basis $M$.
To judge if an environment is compatible with a given crystal structure, we will have to compare it against $M$ reference environments.

The environment similarity kernel is a way to quantify the similarity between environments.
This idea was introduced in [this article](https://aip.scitation.org/doi/full/10.1063/1.5102104) and is based on the [SOAP descriptors](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.87.184115) of Bartok et al.
Unlike SOAPs, this kernel will be non rotationally invariant and thus will break the SO(3) symmetry of space.
The starting point for the definition of our CV is the local atomic density around a given atom.
We consider an environment $\chi$ around this atom and we define the density by,
$\rho_{\chi}(\mathbf{r})=\sum\limits_{i\in\chi} \exp\left(- \frac{|\mathbf{r}_i-\mathbf{r}|^2} {2\sigma^2} \right),$
where $i$ runs over the neighbors in the environment $\chi$, $\sigma$ is a broadening parameter, and $\mathbf{r}_i$ are the
coordinates of the neighbors relative to the central atom.
We will see later how the best $\sigma$ can be rigorously determined.
We now define a single reference environment $\chi_0$ that contains $n$ reference positions $\{\mathbf{r}^0_1,...,\mathbf{r}^0_n\}$
that describe, for instance, the nearest neighbors in a given crystal structure.

The environments $\chi$ and $\chi_0$ are compared using the kernel,

$$ k_{\chi_0}(\chi)= \int d\mathbf{r} \rho_{\chi}(\mathbf{r}) \rho_{\chi_0}(\mathbf{r}) . $$

Combining the two equations above and performing the integration analytically we obtain,

$$ k_{\chi_0}(\chi)= \sum\limits_{i\in\chi} \sum\limits_{j\in\chi_0} \pi^{3/2} \sigma^3  \exp\left(-\frac{|\mathbf{r}_i-\mathbf{r}^0_j|^2} {4\sigma^2} \right). $$

The kernel is finally normalized, such that $k_{\chi_0}(\chi_{0})=1$, in the following way,

$$ \tilde{k}_{\chi_0}(\chi)=\frac{1}{n}\sum\limits_{i\in\chi}\sum\limits_{j\in\chi_0}\exp\left(-\frac{|\mathbf{r}_i-\mathbf{r}^0_j|^2}{4\sigma^2}\right), $$

The definition above is only useful for Bravais lattices since these have a single, unique atomic environment.
The kernel can be generalized to crystal structures described as a lattice with a basis of more than one atom.
As discussed above, in this case there is more than one type of environment.
We consider the case of $M$ environments $X = \chi_1,\chi_2,...,\chi_M$ and we define the kernel through a best match strategy:

$$ \tilde{k}_X(\chi)=\frac{1}{\lambda}\log\left(\sum_l \exp\left(\lambda\tilde{k}_{\chi_l}(\chi)\right)\right) $$

For a large enough $\lambda$ this expression will select the largest $\tilde{k}_{\chi_l}(\chi)$ with $\chi_l\in X$.

$\tilde{k}_X(\chi)$ is a per-atom quantity and we will have to compute global functions of these quantities, for instance, the mean or the number of atoms with at $\tilde{k}_X(\chi)$ larger than some value.

## The system: Sodium as the alanine dipeptide of solids

Alanine dipeptide is the prototypical system on which enhanced sampling methods are tested (and sometimes benchmarked) on.
The reasons behind this choice is that alanine dipeptide is a small and relatively simple molecule that nonetheless captures well the phenomenon of conformational isomerism with relatively large free energy barriers.
I argue that a similar system in the context of materials is sodium.
It crystallizes in the bcc structure which is one of the simplest crystal structures.
Also, it does not show the competition between fcc and hcp structures typical of systems that crystallize in these two compact structures.
This fact greatly simplifies the task of characterizing the structure: all that we can see is liquid or bcc environments.
We will use an embedded atom model (EAM) for sodium that is described in [this paper](https://aip.scitation.org/doi/full/10.1063/1.4916741).
The melting temperature is supposed to be 366 K. Let's see if we can reproduce that result.

## Exercises
### Exercise 1: Choosing reference environments and appropriate $\sigma$ values

In the case of the bcc structure, the reference environment for the environment similarity CV can be chosen automatically using the following PLUMED input:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span class="plumedtooltip" style="color:green">ENVIRONMENTSIMILARITY<span class="right">Measure how similar the environment around atoms is to that found in some reference crystal structure. <a href="https://www.plumed.org/doc-master/user-doc/html/ENVIRONMENTSIMILARITY" style="color:green">More details</a><i></i></span></span> ...
 <span class="plumedtooltip">SPECIES<span class="right">this keyword is used for colvars such as coordination number<i></i></span></span>=1-1024
 <span class="plumedtooltip">CRYSTAL_STRUCTURE<span class="right"> Targeted crystal structure<i></i></span></span>=BCC
 <span class="plumedtooltip">LATTICE_CONSTANTS<span class="right">Lattice constants<i></i></span></span>=0.423
 <span class="plumedtooltip">SIGMA<span class="right"> the width to use for the gaussian kernels<i></i></span></span>=0.07
...
</pre>
 {% endraw %} 

Here we have chosen the bcc crystal structure with a lattice constant of 0.423 nm which is appropriate for bcc sodium.
This choice will automatically build an environment with 14 nearest neighbors.
There are other structures for which environments can be built automatically, see the [manual page](https://www.plumed.org/doc-master/user-doc/html/_e_n_v_i_r_o_n_m_e_n_t_s_i_m_i_l_a_r_i_t_y.html) for further information.
Another option is to use CRYSTAL_STRUCTURE=CUSTOM and provide environments manually as PDB files using the REFERENCE keyword.
In this case, I suggest using the [Environment Finder](https://mybinder.org/v2/gh/PabloPiaggi/EnvironmentFinder/master?urlpath=apps%2FApp.ipynb) app to determine the appropriate environments for your structure.

In the PLUMED input above, we also have to determine the value for the SIGMA keyword.
The first exercise of this class is to determine this value.
Here is the rationale behind the choice.
We are trying to determine a per-atom quantity that is able to distinguish liquid from solid environments.
We should find a SIGMA such that the probability of mislabeling liquid atoms as solid, and viceversa, is minimized.
This can be done by computing the probability of finding a given value of $ \tilde{k}_X(\chi) $ in the bulk solid and the bulk liquid.
So, first things first, let's do a simulation of the bulk liquid and the bulk bcc solid!

If you are using the conda environment for the masterclass, activate it now,
\verbatim
conda activate plumed-masterclass-2022
\endverbatim
Now, cd to the folder ```1-distributions/bcc``` and run the command:
```
mpiexec lmp -in start.lmp > /dev/null &
```
Then cd to the folder ```1-distributions/liquid``` and run again the same command.
These commands will run simulations of the bulk liquid and bulk solid at 1 bar and 375 K.
I have chosen this temperature because it is close to coexistence for these phases.
The files start.lmp are the LAMMPS input and they specify that we are doing NPT simulations.
The output of these runs are in the files ```log.lammps```, ```dump.na```, and ```out.dcd```.
```log.lammps``` is a log file that also contains some thermodynamic ouput.
```dump.na``` is the trajectory in LAMMPS dump atom format and it is useful for visualization with [Ovito](https://www.ovito.org/).
```out.dcd``` is the trajectory in DCD format, which is useful to postprocess directly using PLUMED's driver, as we shall see.

Once that these simulations have completed, we will compute the distributions of the environment similarity kernel using this input

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_2.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_2.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_2.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span class="plumedtooltip" style="color:green">ENVIRONMENTSIMILARITY<span class="right">Measure how similar the environment around atoms is to that found in some reference crystal structure. <a href="https://www.plumed.org/doc-master/user-doc/html/ENVIRONMENTSIMILARITY" style="color:green">More details</a><i></i></span></span> ...
 <span class="plumedtooltip">SPECIES<span class="right">this keyword is used for colvars such as coordination number<i></i></span></span>=1-1024
 <span class="plumedtooltip">SIGMA<span class="right"> the width to use for the gaussian kernels<i></i></span></span>=replace
 <span class="plumedtooltip">CRYSTAL_STRUCTURE<span class="right"> Targeted crystal structure<i></i></span></span>=BCC
 <span class="plumedtooltip">LATTICE_CONSTANTS<span class="right">Lattice constants<i></i></span></span>=0.423
 <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_2.dats" onclick='showPath("data/INSTRUCTIONS.md_working_2.dat","data/INSTRUCTIONS.md_working_2.dats","data/INSTRUCTIONS.md_working_2.dats","brown")'>s</b>
 <span class="plumedtooltip">MEAN<span class="right"> calculate the mean of all the quantities<i></i></span></span>
...
<br/><span style="display:none;" id="data/INSTRUCTIONS.md_working_2.dats">The ENVIRONMENTSIMILARITY action with label <b>s</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">s.value</td><td>the environmental similar parameter for each of the input atoms</td></tr><tr><td width="5%">s.mean</td><td>the mean of the colvars</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_2.dathh" onclick='showPath("data/INSTRUCTIONS.md_working_2.dat","data/INSTRUCTIONS.md_working_2.dathh","data/INSTRUCTIONS.md_working_2.dathh","brown")'>hh</b>: <span class="plumedtooltip" style="color:green">HISTOGRAM<span class="right">Accumulate the average probability density along a few CVs from a trajectory. <a href="https://www.plumed.org/doc-master/user-doc/html/HISTOGRAM" style="color:green">More details</a><i></i></span></span> ...
   <span class="plumedtooltip">DATA<span class="right">an alternative to the ARG keyword<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_2.dats">s</b>
   <span class="plumedtooltip">GRID_MIN<span class="right"> the lower bounds for the grid<i></i></span></span>=-0.5
   <span class="plumedtooltip">GRID_MAX<span class="right"> the upper bounds for the grid<i></i></span></span>=2
   <span class="plumedtooltip">GRID_BIN<span class="right">the number of bins for the grid<i></i></span></span>=1000
   <span class="plumedtooltip">BANDWIDTH<span class="right">the bandwidths for kernel density esimtation<i></i></span></span>=0.01
...
<br/><span style="display:none;" id="data/INSTRUCTIONS.md_working_2.dathh">The HISTOGRAM action with label <b>hh</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">hh.value</td><td>the estimate of the histogram as a function of the argument that was obtained</td></tr></table></span><span class="plumedtooltip" style="color:green">DUMPGRID<span class="right">Output the function on the grid to a file with the PLUMED grid format. <a href="https://www.plumed.org/doc-master/user-doc/html/DUMPGRID" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">the grid you would like to print (can also use ARG for specifying what is being printed)<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_2.dathh">hh</b> <span class="plumedtooltip">FILE<span class="right"> the file on which to write the grid<i></i></span></span>=histo
</pre>
 {% endraw %} 

Here, SIGMA=replace has to be replaced by an appropriate value. 
The action HISTOGRAM will compute the normalized histogram using all per-atom values of the kernel and the action DUMPGRID will write it to a file named histo.
We have to compute these histograms for different values of SIGMA and this can be done with the script run.sh in the folder ```1-distributions``` (execute the command ```./run.sh > results.txt```).
This script will use the PLUMED driver and the DCD trajectory files to calculate the distributions of the environment similarity kernel.
Here's the command we are using inside run.sh to do this,
```
mpiexec plumed driver --plumed plumed.dat --mf_dcd out.dcd > plumed.out
```
but you don't need to execute this yourself because it is done in the script run.sh.
The script run.sh will also compute the overlap between the liquid and bcc distributions for different SIGMA.
The overlap $O(p,q)$ between two distributions $p(x)$ and $q(x)$ can be defined in a variety of ways. Here we use,

$$ O(p,q)=\int dx \min[p(x),q(x)] $$

The output of the script will have two columns, the sigma value used and the overlap between the liquid and solid distributions of the kernel for that sigma.
Plot sigma vs overlap. 
Nice results? Upload them to Slack!
The best choice of SIGMA will be the one that minimizes the overlap which in this case should be around 0.07 nm.
Did you get that result? Great! Then, let's move to the next task.

Now let's plot the distributions of the kernel in the liquid and in the solid.
Plot simultaneously the histograms in ```1-distributions/liquid/histo-0.07``` and ```1-distributions/bcc/histo-0.07``` (column 1 vs column 2).
How do the distributions look like? Do they have overlap?
Determine 1) the maximum for each distribution, and 2) the kernel value for which both distributions have equal values.
We will need these values for the next exercise!
Feel free to share these values and your plots on Slack as you get them.

### Exercise 2: Bulk interconversion

<p float="left">
  <img src="https://github.com/PabloPiaggi/masterclass-22-12/raw/main/interconversion.png" width="600"> 
</p>

We now move to the first method to calculate chemical potentials, the bulk interconversion method.
This method is based on simulating the reversible interconversion of the liquid to the solid and calculating the difference in chemical potential using:

$$ \Delta\mu=-\frac{1}{\beta N} \ln \left ( Z_\beta / Z_\alpha \right) $$

with $Z_\alpha$ and $Z_\beta$ the partition functions restricted to each phase.
These are computed with the formulae,

$$ Z_\alpha=\int\limits_{-\infty}^{s^*} ds \int d\mathbf{R} e^{-\beta [U(\mathbf{R},V)+PV]} \delta (s-s(\mathbf{R},V)) $$

$$ Z_\beta=\int\limits_{s^*}^{\infty} ds \int d\mathbf{R} e^{-\beta [U(\mathbf{R},V)+PV]} \delta (s-s(\mathbf{R},V)) $$

assuming that the collective variable $s$ can separate well the phases at threshold $s^*$.
The ratio of the partition functions is easy to calculate if we have a simulation in which both phases are visited, as we shall see below.

In a standard MD simulation we would only observe a single phase, and in order to see interconversion we need to apply a bias potential.
Here we will use OPES to construct a bias potential as a function of the environment similarity kernels.
If you prefer to use METAD or VES, you can do so, adapting the input accordingly.

The environment similarity kernel, which are per-atom quantities, can be combined into a global quantity by evaluating how many have a value larger than some threshold.
In file ```2-bulk-interconversion/250atoms/400K/plumed.dat``` we can see the input for a simulation with 250 atoms at 400 K,
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_3.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_3.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_3.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/INSTRUCTIONS.md_working_3.datcv_short"><span id="data/INSTRUCTIONS.md_working_3.datdefcv_short"><span class="plumedtooltip" style="color:green">ENVIRONMENTSIMILARITY<span class="right">Measure how similar the environment around atoms is to that found in some reference crystal structure. This action is <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_3.datcv");'>a shortcut</a> and it has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_3.datdefcv");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/ENVIRONMENTSIMILARITY">More details</a><i></i></span></span> ...
 <span class="plumedtooltip">SPECIES<span class="right">this keyword is used for colvars such as coordination number<i></i></span></span>=1-250
 <span class="plumedtooltip">SIGMA<span class="right"> the width to use for the gaussian kernels<i></i></span></span>=0.07
 <span class="plumedtooltip">CRYSTAL_STRUCTURE<span class="right"> Targeted crystal structure<i></i></span></span>=BCC
 <span class="plumedtooltip">LATTICE_CONSTANTS<span class="right">Lattice constants<i></i></span></span>=0.423
 <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_3.datcv" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datcv","data/INSTRUCTIONS.md_working_3.datcv_shortcut","blue")'>cv</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datcv_shortcut">The ENVIRONMENTSIMILARITY action with label <b>cv</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cv</td><td width="5%"><font color="blue">vector</font></td><td>the environmental similar parameter for each of the input atoms</td></tr><tr><td width="5%">cv_morethan</td><td width="5%"><font color="black">scalar</font></td><td>the number of colvars that have a value more than a threshold</td></tr><tr><td width="5%">cv_mean</td><td width="5%"><font color="black">scalar</font></td><td>the mean of the colvars</td></tr></table></span>
 <span class="plumedtooltip">MORE_THAN<span class="right">calculate the number of variables that are more than a certain target value. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/MORE_THAN">MORE_THAN</a>.<i></i></span></span>={CUBIC D_0=0.38 D_MAX=0.80}
 <span class="plumedtooltip">MEAN<span class="right"> calculate the mean of all the quantities<i></i></span></span>
...
</span><span id="data/INSTRUCTIONS.md_working_3.datdefcv_long" style="display:none;"><span class="plumedtooltip" style="color:green">ENVIRONMENTSIMILARITY<span class="right">Measure how similar the environment around atoms is to that found in some reference crystal structure. This action is <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_3.datcv");'>a shortcut</a> and uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_3.datdefcv");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/ENVIRONMENTSIMILARITY">More details</a><i></i></span></span> ...
 <span class="plumedtooltip">SPECIES<span class="right">this keyword is used for colvars such as coordination number<i></i></span></span>=1-250
 <span class="plumedtooltip">SIGMA<span class="right"> the width to use for the gaussian kernels<i></i></span></span>=0.07
 <span class="plumedtooltip">CRYSTAL_STRUCTURE<span class="right"> Targeted crystal structure<i></i></span></span>=BCC
 <span class="plumedtooltip">LATTICE_CONSTANTS<span class="right">Lattice constants<i></i></span></span>=0.423
 <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_3.datcv" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datcv","data/INSTRUCTIONS.md_working_3.datcv_shortcut","blue")'>cv</b>
 <span class="plumedtooltip">MORE_THAN<span class="right">calculate the number of variables that are more than a certain target value. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/MORE_THAN">MORE_THAN</a>.<i></i></span></span>={CUBIC D_0=0.38 D_MAX=0.80}
 <span class="plumedtooltip">MEAN<span class="right"> calculate the mean of all the quantities<i></i></span></span>
 <span class="plumedtooltip">CUTOFF<span class="right"> how many multiples of sigma would you like to consider beyond the maximum distance in the environment<i></i></span></span>=3 <span class="plumedtooltip">LCUTOFF<span class="right"> any atoms separated by less than this tolerance should be ignored<i></i></span></span>=0.0001
...
</span></span><span id="data/INSTRUCTIONS.md_working_3.datcv_long" style="display:none;"><span style="color:blue" class="comment"># PLUMED interprets the command:
</span><span class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_3.datcv")'># ENVIRONMENTSIMILARITY ...</span>
<span style="color:blue" class="comment">#  SPECIES=1-250</span>
<span style="color:blue" class="comment">#  SIGMA=0.07</span>
<span style="color:blue" class="comment">#  CRYSTAL_STRUCTURE=BCC</span>
<span style="color:blue" class="comment">#  LATTICE_CONSTANTS=0.423</span>
<span style="color:blue" class="comment">#  LABEL=cv</span>
<span style="color:blue" class="comment">#  MORE_THAN={CUBIC D_0=0.38 D_MAX=0.80}</span>
<span style="color:blue" class="comment">#  MEAN</span>
<span style="color:blue" class="comment"># ...</span>
<span style="color:blue" class="comment"># as follows (Click the red comment above to revert to the short version of the input):</span>
<b name="data/INSTRUCTIONS.md_working_3.datcv_cmat" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datcv_cmat","data/INSTRUCTIONS.md_working_3.datcv_cmat","red")'>cv_cmat</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datcv_cmat">The DISTANCE_MATRIX action with label <b>cv_cmat</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cv_cmat.w</td><td width="5%"><font color="red">matrix</font></td><td>a matrix containing the weights for the bonds between each pair of atoms</td></tr><tr><td width="5%">cv_cmat.x</td><td width="5%"><font color="red">matrix</font></td><td>the projection of the bond on the x axis</td></tr><tr><td width="5%">cv_cmat.y</td><td width="5%"><font color="red">matrix</font></td><td>the projection of the bond on the y axis</td></tr><tr><td width="5%">cv_cmat.z</td><td width="5%"><font color="red">matrix</font></td><td>the projection of the bond on the z axis</td></tr></table></span>: <span class="plumedtooltip" style="color:green">DISTANCE_MATRIX<span class="right">Calculate a matrix of distances between atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE_MATRIX" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">COMPONENTS<span class="right"> also calculate the components of the vector connecting the atoms in the contact matrix<i></i></span></span> <span class="plumedtooltip">GROUP<span class="right">the atoms for which you would like to calculate the adjacency matrix<i></i></span></span>=1-250 <span class="plumedtooltip">CUTOFF<span class="right"> ignore distances that have a value larger than this cutoff<i></i></span></span>=0.633
<b name="data/INSTRUCTIONS.md_working_3.datcv_grp" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datcv_grp","data/INSTRUCTIONS.md_working_3.datcv_grp","violet")'>cv_grp</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datcv_grp">The GROUP action with label <b>cv_grp</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cv_grp</td><td width="5%"><font color="violet">atoms</font></td><td>indices of atoms specified in GROUP</td></tr></table></span>: <span class="plumedtooltip" style="color:green">GROUP<span class="right">Define a group of atoms so that a particular list of atoms can be referenced with a single label in definitions of CVs or virtual atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/GROUP" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the numerical indexes for the set of atoms in the group<i></i></span></span>=1-250
<b name="data/INSTRUCTIONS.md_working_3.datcv_ones" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datcv_ones","data/INSTRUCTIONS.md_working_3.datcv_ones","blue")'>cv_ones</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datcv_ones">The CONSTANT action with label <b>cv_ones</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cv_ones</td><td width="5%"><font color="blue">vector</font></td><td>the constant value that was read from the plumed input</td></tr></table></span>: <span class="plumedtooltip" style="color:green">ONES<span class="right">Create a constant vector with all elements equal to one <a href="https://www.plumed.org/doc-master/user-doc/html/ONES" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">SIZE<span class="right">the number of ones that you would like to create<i></i></span></span>=250
<b name="data/INSTRUCTIONS.md_working_3.datcv_matenv1" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datcv_matenv1","data/INSTRUCTIONS.md_working_3.datcv_matenv1","red")'>cv_matenv1</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datcv_matenv1">The CUSTOM action with label <b>cv_matenv1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cv_matenv1</td><td width="5%"><font color="red">matrix</font></td><td>the matrix obtained by doing an element-wise application of an arbitrary function to the input matrix</td></tr></table></span>: <span class="plumedtooltip" style="color:green">CUSTOM<span class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/CUSTOM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_3.datcv_cmat">cv_cmat.x</b>,<b name="data/INSTRUCTIONS.md_working_3.datcv_cmat">cv_cmat.y</b>,<b name="data/INSTRUCTIONS.md_working_3.datcv_cmat">cv_cmat.z</b>,<b name="data/INSTRUCTIONS.md_working_3.datcv_cmat">cv_cmat.w</b> <span class="plumedtooltip">VAR<span class="right">the names to give each of the arguments in the function<i></i></span></span>=x,y,z,w <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO <span class="plumedtooltip">FUNC<span class="right">the function you wish to evaluate<i></i></span></span>=(step(w-0.0001)*step(0.633-w)/14)*(exp(-((x-0.2115)^2+(y-0.2115)^2+(z-0.2115)^2)/(4*0.0049))+exp(-((x--0.2115)^2+(y--0.2115)^2+(z--0.2115)^2)/(4*0.0049))+exp(-((x--0.2115)^2+(y-0.2115)^2+(z-0.2115)^2)/(4*0.0049))+exp(-((x-0.2115)^2+(y--0.2115)^2+(z-0.2115)^2)/(4*0.0049))+exp(-((x-0.2115)^2+(y-0.2115)^2+(z--0.2115)^2)/(4*0.0049))+exp(-((x--0.2115)^2+(y--0.2115)^2+(z-0.2115)^2)/(4*0.0049))+exp(-((x-0.2115)^2+(y--0.2115)^2+(z--0.2115)^2)/(4*0.0049))+exp(-((x--0.2115)^2+(y-0.2115)^2+(z--0.2115)^2)/(4*0.0049))+exp(-((x-0.423)^2+(y-0)^2+(z-0)^2)/(4*0.0049))+exp(-((x-0)^2+(y-0.423)^2+(z-0)^2)/(4*0.0049))+exp(-((x-0)^2+(y-0)^2+(z-0.423)^2)/(4*0.0049))+exp(-((x--0.423)^2+(y-0)^2+(z-0)^2)/(4*0.0049))+exp(-((x-0)^2+(y--0.423)^2+(z-0)^2)/(4*0.0049))+exp(-((x-0)^2+(y-0)^2+(z--0.423)^2)/(4*0.0049)))
<b name="data/INSTRUCTIONS.md_working_3.datcv" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datcv","data/INSTRUCTIONS.md_working_3.datcv","blue")'>cv</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datcv">The MATRIX_VECTOR_PRODUCT action with label <b>cv</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cv</td><td width="5%"><font color="blue">vector</font></td><td>the vector that is obtained by taking the product between the matrix and the vector that were input</td></tr></table></span>: <span class="plumedtooltip" style="color:green">MATRIX_VECTOR_PRODUCT<span class="right">Calculate the product of the matrix and the vector <a href="https://www.plumed.org/doc-master/user-doc/html/MATRIX_VECTOR_PRODUCT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the label for the matrix and the vector/scalar that are being multiplied<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_3.datcv_matenv1">cv_matenv1</b>,<b name="data/INSTRUCTIONS.md_working_3.datcv_ones">cv_ones</b>
<b name="data/INSTRUCTIONS.md_working_3.datcv_mt" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datcv_mt","data/INSTRUCTIONS.md_working_3.datcv_mt","blue")'>cv_mt</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datcv_mt">The MORE_THAN action with label <b>cv_mt</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cv_mt</td><td width="5%"><font color="blue">vector</font></td><td>the vector obtained by doing an element-wise application of a function that is one if the if the input is more than a threshold to the input vectors</td></tr></table></span>: <span class="plumedtooltip" style="color:green">MORE_THAN<span class="right">Use a switching function to determine how many of the input variables are more than a certain cutoff. <a href="https://www.plumed.org/doc-master/user-doc/html/MORE_THAN" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_3.datcv">cv</b> <span class="plumedtooltip">SWITCH<span class="right">This keyword is used if you want to employ an alternative to the continuous swiching function defined above<i></i></span></span>={CUBIC D_0=0.38 D_MAX=0.80}
<b name="data/INSTRUCTIONS.md_working_3.datcv_morethan" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datcv_morethan","data/INSTRUCTIONS.md_working_3.datcv_morethan","black")'>cv_morethan</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datcv_morethan">The SUM action with label <b>cv_morethan</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cv_morethan</td><td width="5%"><font color="black">scalar</font></td><td>the SUM of the elements in the input value</td></tr></table></span>: <span class="plumedtooltip" style="color:green">SUM<span class="right">Calculate the sum of the arguments <a href="https://www.plumed.org/doc-master/user-doc/html/SUM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the vector/matrix/grid whose elements shuld be added together<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_3.datcv_mt">cv_mt</b> <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<b name="data/INSTRUCTIONS.md_working_3.datcv_mean" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datcv_mean","data/INSTRUCTIONS.md_working_3.datcv_mean","black")'>cv_mean</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datcv_mean">The MEAN action with label <b>cv_mean</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">cv_mean</td><td width="5%"><font color="black">scalar</font></td><td>the MEAN of the elements in the input value</td></tr></table></span>: <span class="plumedtooltip" style="color:green">MEAN<span class="right">Calculate the arithmetic mean of the elements in a vector <a href="https://www.plumed.org/doc-master/user-doc/html/MEAN" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the vector/matrix/grid whose elements shuld be added together<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_3.datcv">cv</b> <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="color:blue"># --- End of included input --- </span></span></pre>
 {% endraw %} 
Here you see that we are calculating the MEAN and the number of atoms that have a value of the kernel MORE_THAN something.
Here, instead of having a strict threshold at some value, we have a continuous and differentiable switching function that is 0 below 0.38, 1 above 0.80, and changes smoothly from 0 to 1 between these values.
The values for D_0 and D_MAX have been chosen based on the maxima of the distributions determined in the previous exercise. Did you get those values right? I hope you did.

The input for OPES is very simple,
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_4.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_4.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_4.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<b name="data/INSTRUCTIONS.md_working_4.datopes" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datopes","data/INSTRUCTIONS.md_working_4.datopes","brown")'>opes</b>: <span class="plumedtooltip" style="color:green">OPES_METAD<span class="right">On-the-fly probability enhanced sampling with metadynamics-like target distribution. <a href="https://www.plumed.org/doc-master/user-doc/html/OPES_METAD" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=cv.morethan <span class="plumedtooltip">PACE<span class="right">the frequency for kernel deposition<i></i></span></span>=500 <span class="plumedtooltip">BARRIER<span class="right">the free energy barrier to be overcome<i></i></span></span>=100 <span class="plumedtooltip">TEMP<span class="right"> temperature<i></i></span></span>=400 <span class="plumedtooltip">STRIDE<span class="right">the frequency with which the forces due to the bias should be calculated<i></i></span></span>=2
<span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datopes">The OPES_METAD action with label <b>opes</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">opes.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">opes.rct</td><td>estimate of c(t)</td></tr><tr><td width="5%">opes.zed</td><td>estimate of Z_n</td></tr><tr><td width="5%">opes.neff</td><td>effective sample size</td></tr><tr><td width="5%">opes.nker</td><td>total number of compressed kernels used to represent the bias</td></tr></table></span></pre>
 {% endraw %} 
and uses the morethan value described above as CV.
We estimate a barrier of less than 100 kJ/mol and that's the rationale behind the choice of BARRIER.
If you are using well tempered METAD you might want to use a biasfactor of around 40.
The other keywords are fairly standard.

We will also use a trick to avoid forming structures that have orientations different from the one that we are trying to form.
This will be discussed during the lecture and the PLUMED input is:
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_5.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_5.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_5.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<b name="data/INSTRUCTIONS.md_working_5.datq6" onclick='showPath("data/INSTRUCTIONS.md_working_5.dat","data/INSTRUCTIONS.md_working_5.datq6","data/INSTRUCTIONS.md_working_5.datq6","brown")'>q6</b>: <span class="plumedtooltip" style="color:green">Q6<span class="right">Calculate sixth order Steinhardt parameters. <a href="https://www.plumed.org/doc-master/user-doc/html/Q6" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">SPECIES<span class="right">the list of atoms for which the symmetry function is being calculated and the atoms that can be in the environments<i></i></span></span>=1-250 <span class="plumedtooltip">SWITCH<span class="right">the switching function that it used in the construction of the contact matrix. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={CUBIC D_0=0.4 D_MAX=0.5} <span class="plumedtooltip">VMEAN<span class="right"> calculate the norm of the mean vector<i></i></span></span>
<span style="display:none;" id="data/INSTRUCTIONS.md_working_5.datq6">The Q6 action with label <b>q6</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">q6._vmean</td><td>the norm of the mean vector</td></tr><tr><td width="5%">q6.value</td><td>the norms of the vectors of spherical harmonic coefficients</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_5.datdiff" onclick='showPath("data/INSTRUCTIONS.md_working_5.dat","data/INSTRUCTIONS.md_working_5.datdiff","data/INSTRUCTIONS.md_working_5.datdiff","brown")'>diff</b>: <span class="plumedtooltip" style="color:green">MATHEVAL<span class="right">An alias to the CUSTOM function that can also be used to calaculate combinations of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/MATHEVAL" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_5.datq6">q6.vmean</b>,cv.mean <span class="plumedtooltip">FUNC<span class="right">the function you wish to evaluate<i></i></span></span>=(x-0.0604)/(0.397-0.0604)-(y-0.387)/(0.756-0.387) <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="display:none;" id="data/INSTRUCTIONS.md_working_5.datdiff">The MATHEVAL action with label <b>diff</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">diff.value</td><td>an arbitrary function</td></tr></table></span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_5.datdiff">diff</b> <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=0.1 <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=100000 <span class="plumedtooltip">EXP<span class="right"> the powers for the walls<i></i></span></span>=2 <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_5.datuwall" onclick='showPath("data/INSTRUCTIONS.md_working_5.dat","data/INSTRUCTIONS.md_working_5.datuwall","data/INSTRUCTIONS.md_working_5.datuwall","brown")'>uwall</b> <span class="plumedtooltip">STRIDE<span class="right">the frequency with which the forces due to the bias should be calculated<i></i></span></span>=2
<span style="display:none;" id="data/INSTRUCTIONS.md_working_5.datuwall">The UPPER_WALLS action with label <b>uwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">uwall.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">uwall.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span></pre>
 {% endraw %} 
In a nutshell, we are limiting the increase of Q6 (rotationally invariant) not followed by an increase in ENVIRONMENTSIMILARITY (non rotationally invariant).

The first task of this exercise is to run a few simulations at different temperatures (say, 380 K, 400 K, 420K, or more if you have a computer cluster available).
In order to run the simulation you have to execute on the folder ```2-bulk-interconversion/250atoms/400K``` the command:
```
mpiexec lmp -in start.lmp > /dev/null &
```
10 or 20 ns of simulation should suffice, but you may run them for (much) longer if you are using a computer cluster.
To run simulations at other temperatures, copy the folder 400K, for example,
```
cp -r 400K 380K
```
And edit the files plumed.dat and start.lmp to change the temperature from 400 K to 380 K.
The lines where you should change the temperatures are highlighted!
You can run as many simulations as you want to, but at least two are required.
Each simulation should take about 2 hours to get ~10 ns if you are running on ~8 cores.

Now that the simulations are running, let's start analyzing them.
You don't have to wait until they finish to start with the analysis.
The most useful output of these simulations is in the file ```COLVAR```.
For instance, the first column is the time, the third column is the environment similarity morethan value, and the fourth column is the OPES bias.
Let's plot time vs environment similarity morethan (column 1 vs column 3).
What is happening during the simulation?
Are there transitions between liquid and solid phases?
I suggest that you also visualize the trajectory in file ```dump.na``` using Ovito.
Try the modifiers Smooth Trajectory (with window size 5) and Polyhedral Template Matching.
Is the bcc solid forming?
Is it well aligned with the simulation box?
It is also interesting to compute the free energy surface (FES).
I provide a simple script fes.py to do this with python, numpy and matplotlib and you can run it using,
```
python fes.py
```
This script is based in constructing a histogram $h(s)$ with weights $e^{\beta V}$ where $V$ the bias potential.
The FES is then obtained using,

$$ G(s)=-\frac{1}{\beta}\ln h(s) $$

You can plot the FES at all the temperatures you have run simulations at.
How does the FES look like?
What does each basin represent?
How do they change with temperature?
Don't forget to upload your plots to Slack!

Now let's move to the most important task of this section, the calculation of differences in chemical potentials.
I prepared a basic python script that you can use to computed the difference in chemical potential between the liquid and the solid.
You can find it in ```2-bulk-interconversion/250atoms/chemical_potentials.py```.
You have to edit the highlighted lines to include more temperatures in the calculation and in the plot that it will generate.
If you have at least two temperatures, it will fit a straight line and estimate the coexistence temperature from the condition that the chemical potential difference is zero at coexistence.
Do the chemical potential differences depend linearly on the temperature?
What melting temperature do you find?
How does it compare with the reference value (366 K) that has been reported?

If you have enough computer resources and time, I suggest that you repeat the exercise with a larger system, for instance, with 1024 atoms.
I prepared input files in the folder ```2-bulk-interconversion/1024atoms/400K```.
Do you find the same chemical potentials and coexistence temperature?
Remember that the difference in chemical potential and coexistence temperature depend linearly on $1/N$ with $N$ the system size.
You can use this fact to extrapolate to the thermodynamic limit.
Did you get a better coexistence temperature now?
Which system sizes are big enough to make an error of about 1 K in the coexistence temperature?

### Exercise 3: Biased coexistence

<p float="left">
  <img src="https://github.com/PabloPiaggi/masterclass-22-12/raw/main/coexistence.png" width="600"> 
</p>

In this section we will use a different method to calculate the difference in chemical potential between the liquid and the solid.
I call it **biased coexistence** and it is a generalization of the [interface pinning](https://aip.scitation.org/doi/full/10.1063/1.4818747) method.
The idea of the method is to simulate the liquid and the solid (or any pair of phases) in direct coexistence.
Then, we add a bias potential such that we sample reversibly the growth and melting of a portion of the system, for instance, one layer of the solid.
From this simulation we can compute the free energy as a function of the number of solid-like atoms in the system $G(N)$.
This quantity is connected to the chemical potential in the following way,

$$G(N) \approx \Delta\mu N + const $$

This equation is an approximation and rests on several assumptions, yet it tells us that the chemical potential is the slope of the FES with respect to N.

The files to perform a biased coexistence simulation with 2048 atoms can be found in the folder ```3-biased-coexistence/2048atoms/400K```.
The LAMMPS input script start.lmp will do a lot of things automatically for us:
- Create a bcc crystal and equilibrate it in NPT
- Determine the equilibrium box dimensions and fix the lengths in x and y to their equilibrium value at the simulated temperature
- Replicate the crystal along the z axis and melt half of the crystal in the box
- Equilibrate the liquid-solid surface under the constraint of having around half the atoms with solid-like environments in the NPzT ensemble
- Production run with a bias potential in the NPzT ensemble

The equilibration under a constraint is done using the following PLUMED input found on plumed.equil.dat,
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_6.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_6.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_6.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<b name="data/INSTRUCTIONS.md_working_6.datuwall" onclick='showPath("data/INSTRUCTIONS.md_working_6.dat","data/INSTRUCTIONS.md_working_6.datuwall","data/INSTRUCTIONS.md_working_6.datuwall","brown")'>uwall</b>: <span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=cv.morethan <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=1152. <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=0.1 <span class="plumedtooltip">EXP<span class="right"> the powers for the walls<i></i></span></span>=2 <span class="plumedtooltip">STRIDE<span class="right">the frequency with which the forces due to the bias should be calculated<i></i></span></span>=2
<span style="display:none;" id="data/INSTRUCTIONS.md_working_6.datuwall">The UPPER_WALLS action with label <b>uwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">uwall.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">uwall.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_6.datlwall" onclick='showPath("data/INSTRUCTIONS.md_working_6.dat","data/INSTRUCTIONS.md_working_6.datlwall","data/INSTRUCTIONS.md_working_6.datlwall","brown")'>lwall</b>: <span class="plumedtooltip" style="color:green">LOWER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/LOWER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=cv.morethan <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=896. <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=0.1 <span class="plumedtooltip">EXP<span class="right"> the powers for the walls<i></i></span></span>=2 <span class="plumedtooltip">STRIDE<span class="right">the frequency with which the forces due to the bias should be calculated<i></i></span></span>=2
<span style="display:none;" id="data/INSTRUCTIONS.md_working_6.datlwall">The LOWER_WALLS action with label <b>lwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">lwall.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">lwall.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span></pre>
 {% endraw %} 
And in the production run, the bias is defined in file plumed.dat and is,
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_7.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_7.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_7.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<b name="data/INSTRUCTIONS.md_working_7.datopes" onclick='showPath("data/INSTRUCTIONS.md_working_7.dat","data/INSTRUCTIONS.md_working_7.datopes","data/INSTRUCTIONS.md_working_7.datopes","brown")'>opes</b>: <span class="plumedtooltip" style="color:green">OPES_METAD<span class="right">On-the-fly probability enhanced sampling with metadynamics-like target distribution. <a href="https://www.plumed.org/doc-master/user-doc/html/OPES_METAD" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=cv.morethan <span class="plumedtooltip">PACE<span class="right">the frequency for kernel deposition<i></i></span></span>=500 <span class="plumedtooltip">BARRIER<span class="right">the free energy barrier to be overcome<i></i></span></span>=100 <span class="plumedtooltip">TEMP<span class="right"> temperature<i></i></span></span>=400 <span class="plumedtooltip">STRIDE<span class="right">the frequency with which the forces due to the bias should be calculated<i></i></span></span>=2

<span style="display:none;" id="data/INSTRUCTIONS.md_working_7.datopes">The OPES_METAD action with label <b>opes</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">opes.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">opes.rct</td><td>estimate of c(t)</td></tr><tr><td width="5%">opes.zed</td><td>estimate of Z_n</td></tr><tr><td width="5%">opes.neff</td><td>effective sample size</td></tr><tr><td width="5%">opes.nker</td><td>total number of compressed kernels used to represent the bias</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_7.datuwall" onclick='showPath("data/INSTRUCTIONS.md_working_7.dat","data/INSTRUCTIONS.md_working_7.datuwall","data/INSTRUCTIONS.md_working_7.datuwall","brown")'>uwall</b>: <span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=cv.morethan <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=1152. <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=0.1 <span class="plumedtooltip">EXP<span class="right"> the powers for the walls<i></i></span></span>=2 <span class="plumedtooltip">STRIDE<span class="right">the frequency with which the forces due to the bias should be calculated<i></i></span></span>=2
<span style="display:none;" id="data/INSTRUCTIONS.md_working_7.datuwall">The UPPER_WALLS action with label <b>uwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">uwall.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">uwall.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_7.datlwall" onclick='showPath("data/INSTRUCTIONS.md_working_7.dat","data/INSTRUCTIONS.md_working_7.datlwall","data/INSTRUCTIONS.md_working_7.datlwall","brown")'>lwall</b>: <span class="plumedtooltip" style="color:green">LOWER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/LOWER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=cv.morethan <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=896. <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=0.1 <span class="plumedtooltip">EXP<span class="right"> the powers for the walls<i></i></span></span>=2 <span class="plumedtooltip">STRIDE<span class="right">the frequency with which the forces due to the bias should be calculated<i></i></span></span>=2
<span style="display:none;" id="data/INSTRUCTIONS.md_working_7.datlwall">The LOWER_WALLS action with label <b>lwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">lwall.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">lwall.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span></pre>
 {% endraw %} 

Run the simulation at 400 K using the command,
```
mpiexec lmp -in start.lmp > /dev/null &
```
I estimate that you need at least 3 ns of simulation to see reasonable results and this should take a couple of hours on ~8 cores.
If you are running on a computer cluster, run it for longer.
I suggest that you repeat the simulations at different temperatures, for instance, 360 K, 380 K, and 400 K, and you may do more temperatures if you have the computational resources.
The lines of the input scripts plumed.dat and start.lmp where the temperature has to be changed are clearly highlighted.

Let's see the progress of our simulation by plotting time vs environment similarity morethan (column 1 vs 3) on the COLVAR file.
How does it look like? What is happening to the system under the action of the OPES bias and the walls?
You can visualize the trajectory dump.na using Ovito.
Now we shall calculate the chemical potential from the slope of the FES with respect to the number of solid-like atoms.
In order to do this, we will use the script ```chemical_potential_bc.py``` found on folder ```3-biased-coexistence/2048atoms```.
This script will compute the FES, fit a straight line to get the slope (chemical potentials), plot the chemical potentials vs temperature, and get the coexistence temperature.
Depending on how many temperatures you have performed, go into the script and add more temperatures.
The line that you need to change has been highlighted.
The FES is computed from the histogram with weights $e^{\beta V}$ where $V$ is the bias potential.
Are the FES linear with the number of solid-like atoms?
What melting temperature did you find?

Note that we are computing a "strict" morethan value for the environment similarity kernel that we use for post-processing.
This definition can't be used for biasing but it is a better way to count solid-like atoms and we use it to construct the FES.
The definition of the "strict" version is,
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_8.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_8.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_8.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span class="plumedtooltip" style="color:green">ENVIRONMENTSIMILARITY<span class="right">Measure how similar the environment around atoms is to that found in some reference crystal structure. <a href="https://www.plumed.org/doc-master/user-doc/html/ENVIRONMENTSIMILARITY" style="color:green">More details</a><i></i></span></span> ...
 <span class="plumedtooltip">SPECIES<span class="right">this keyword is used for colvars such as coordination number<i></i></span></span>=1-2048
 <span class="plumedtooltip">SIGMA<span class="right"> the width to use for the gaussian kernels<i></i></span></span>=0.07
 <span class="plumedtooltip">CRYSTAL_STRUCTURE<span class="right"> Targeted crystal structure<i></i></span></span>=BCC
 <span class="plumedtooltip">LATTICE_CONSTANTS<span class="right">Lattice constants<i></i></span></span>=0.423
 <span class="plumedtooltip">MORE_THAN<span class="right">calculate the number of variables that are more than a certain target value. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/MORE_THAN">MORE_THAN</a>.<i></i></span></span>={CUBIC D_0=0.5525 D_MAX=0.55251}
...
</pre>
 {% endraw %} 
and is in column 13 of the COLVAR file.

Discuss the advantages and disadvantages of the two methods presented above.
Which one did you like best? Why?

### Exercise 4: Thermodynamic integration along isobars

Perhaps the simplest method to compute chemical potential differences is thermodynamic integration.
Here we will discuss the version of the method in which the integration is performed along isobars.
It is very cheap and easy.
What's the catch?
You have to know the chemical potential difference for some thermodynamic condition in order to use it.
It is therefore a perfect complement for the methods described above.
PLUMED is not required for this exercise, but we will use the results obtained here to validate the methods described above.

The method relies on the following thermodynamic identity,

$$ \frac{\Delta\mu(T,P)}{T}=\frac{\Delta\mu(T_0,P)}{T_0}-\int\limits_{T_0}^T\frac{\Delta h(T',P)}{T'^2}dT' $$

where $T_0$ is the reference temperature at which $\Delta\mu$ is known, and $\Delta h$ is the per-atom enthalpy difference.
If  $T_0$ is the coexistence temperature, the first term on the RHS vanishes.

In order to use this method, we shall compute the enthalpy for the liquid and the solid at several temperatures and pressures.
Example scripts are given in folders 4-thermodynamic-integration/liquid and 4-thermodynamic-integration/bcc .
You can use the script newtemp.sh to create folders to run simulations at different temperatures between 330 K and 410 K in steps of 10 K.
It is used in the following way,
```
./newtemp.sh 400 
```
to create the folder ```400K``` with inputs for the simulation at a temperature of 400 K.
The command to run the LAMMPS input scripts start.lmp is the same as the one above.
The simulations should be fast, a couple of minutes each one, and they will output a file thermo.txt that has the enthalpy.
I prepared a python script ```chemical_potentials_ti.py``` located in folder ```4-thermodynamic-integration``` that plots the enthalpies vs temperature, performs the integration, and then plots the chemical potential differences vs temperature.
How do these chemical potentials compare with the ones obtained with other methods?

## Final thoughts

We have discussed three methods to calculate chemical potential differences between the liquid and a solid.
There are other methods that are not described here because they are not based on enhanced sampling techniques.
Also, an important tool to study phase equilibria is the integration of the Clausius-Clapeyron equation to trace coexistence lines.
The latter method is an important complement to the methods discussed in this tutorial and extremely useful when computing phase diagrams in the temperature-pressure plane.
