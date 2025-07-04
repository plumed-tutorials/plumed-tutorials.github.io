# PLUMED Masterclass 22.11: Variationally Enhanced Sampling

## Author
Omar Valsson  
Department of Chemistry, University of North Texas   
Webpage: www.valsson.info  
July 4, 2022

## Aims

In this Masterclass, we will discuss how to run variationally enhanced sampling simulations with PLUMED. We will also understand how to analyze the results.

## Objectives

Once you have completed this Masterclass you will be able to:

- Run variationally enhanced sampling simulations biasing one and two CVs
- Assess the convergence of the simulation
- Perform reweighting from variationally enhanced sampling simulations

## Setting up PLUMED

For this masterclass you will need versions of PLUMED (with the VES module enabled) and GROMACS that are compiled using the MPI library. All the exercises were tested with PLUMED version 2.8.0 and GROMACS 2020.6. For example, to obtain these versions, you can follow the instructions at [this link](https://github.com/plumed/masterclass-2022).

The data needed to execute the exercises of this Masterclass can be found on [GitHub](https://github.com/valsson-group/masterclass-22-11).
You can clone this repository locally on your machine using the following command:

```
git clone https://github.com/valsson-group/masterclass-22-11.git
```

These files include the GROMACS and PLUMED files needed to run this tutorial, along with Jupyter notebook `Analysis.ipynb` that you can use to plot and analyze the results of the simulations. 

## Summary of Theory

Here, we will briefly summarize the theory behind variationally enhanced sampling (VES). For an full overview of VES, you should read the [original paper](https://doi.org/10.1103/PhysRevLett.113.090601), a  review in a [book chapter on VES](https://doi.org/10.1007/978-3-319-44677-6_50), or a recent [enhanced sampling review](https://doi.org/10.33011/livecoms.4.1.1583) that includes discussion about VES.

VES is based on the the following functional of the bias potential:

$$\Omega [V]  =
\frac{1}{\beta} \log
\frac
{\int d\mathbf{s} \ e^{-\beta \left[ F(\mathbf{s}) + V(\mathbf{s})\right]}}
{\int d\mathbf{s} \ e^{-\beta F(\mathbf{s})}}
+
\int d\mathbf{s} \ p_{\mathrm{tg}}(\mathbf{s}) \ V(\mathbf{s}),$$

where $\mathbf{s}$ are the CVs that we are biasing,
$p_{\mathrm{tg}}(\mathbf{s})$ is a predefined probability distribution that we will refer
to as the target distribution, and $F(\mathbf{s})$ is the free energy
surface. This functional can be shown to be convex and to have a minimum at:

$$V(\mathbf{s}) = -F(\mathbf{s})-{\frac {1}{\beta}} \log {p_{\mathrm{tg}}(\mathbf{s})}.$$

The last equation states that when we minimize the functional $\Omega [V]$,
we can obtain the free energy surface from the bias potential (and the target distribution).
We can choose the target distribution $p_{\mathrm{tg}}(\mathbf{s})$ at will and it is
the CV distribution that we obtain when minimizing $\Omega [V]$.

We put the variational principle to practice by expanding $V(\mathbf{s})$
in some basis set:

$$V(\mathbf{s}) = \sum\limits_{i} \alpha_i \ f_i(\mathbf{s}),$$

where $f_i(\mathbf{s})$ are the basis functions and the $\boldsymbol\alpha$ are the coefficients in the expansion.

We then need to find the coefficients $\boldsymbol\alpha$ that minimize $\Omega
[V]$. In principle one could use any optimization algorithm. In practice
the algorithm that has become the default choice for VES is the so-called
[averaged stochastic gradient descent algorithm](http://papers.nips.cc/paper/4900-non-strongly-convex-smooth-stochastic-approximation-with-convergence-rate-o1n.pdf).
In this algorithm the $\boldsymbol\alpha$ are evolved iteratively
according to:

$$\boldsymbol\alpha^{(n+1)} = \boldsymbol\alpha^{(n)}-\mu
 \left[
\nabla\Omega(\bar{\boldsymbol\alpha}^{(n)})+
H(\bar{\boldsymbol\alpha}^{(n)})[\boldsymbol\alpha^{(n)}-\bar{\boldsymbol\alpha}^{(n)}]
\right]$$

where $\mu$ is the step size,
$\bar{\boldsymbol\alpha}^{(n)}$ is the running average of $\boldsymbol\alpha^{(n)}$ at iteration $n$, and
$\nabla\Omega(\bar{\boldsymbol\alpha}^{(n)})$ and
$H(\bar{\boldsymbol\alpha}^{(n)})$ are the gradient and Hessian of $\Omega[V]$ evaluated at the running
average at iteration $n$, respectively.
The behavior of the coefficients will become apparent in the examples below.

As said above, we can choose the target distribution $p_{\mathrm{tg}}(\mathbf{s})$ at will.
The most simple choice would be a uniform target distribution. However, it has been found more optimal to
employ the so-called well-tempered distribution  (see [here](http://doi.org/10.1021/acs.jctc.5b00076)):

$$p_{\mathrm{tg}}(\mathbf{s}) =
\frac{[ P(\mathbf{s}) ]^{1/\gamma}}
{\int d\mathbf{s}\ [ P(\mathbf{s}) ]^{1/\gamma}}$$

where $\gamma$ is the so-called bias
factor and $P(\mathbf{s})$ is the unbiased CV distribution. Therefore the
well-tempered distribution is the unbiased distribution with enhanced fluctuations
and lowered barriers. This is the same distribution as sampled in well-tempered
metadynamics. The advantages of this distribution are that the features of the
FES (metastable states) are preserved and that the system is not forced to sample regions of high
free energy (that can represent un-physical configurations)
as it would if we had chosen the uniform target distribution.
There is a caveat though, the well-tempered $p_{\mathrm{tg}}(\mathbf{s})$ depends on 
$F(\mathbf{s})$ that is the function that we are trying to calculate.
One way to approach this problem is to calculate $p_{\mathrm{tg}}(\mathbf{s})$
self-consistently (see [here](http://doi.org/10.1021/acs.jctc.5b00076)), for instance at iteration $k$:

$$p^{(k+1)}(\mathbf{s})=\frac{e^{-(\beta/\gamma) F^{(k+1)}(\mathbf{s})}}{\int d\mathbf{s} \ e^{-(\beta/\gamma) F^{(k+1)}(\mathbf{s})}}$$

where:

$$F^{(k+1)}(\mathbf{s})=-V^{(k)}(\mathbf{s}) - \frac{1}{\beta} \log p^{(k)}(\mathbf{s})$$

Normally $p^{(0)}(\mathbf{s})$ is taken to be uniform.
Therefore the target distribution evolves in time until it becomes stationary
when the simulation has converged. It has been shown that in some cases the
convergence is faster using the well-tempered target distribution than using
the uniform $p(\mathbf{s})$  (see [here](http://doi.org/10.1021/acs.jctc.5b00076)).

## The System: Association/Dissociation of NaCl in Aqueous Solution

In this tutorial, we will consider the association/dissociation of NaCl in aqueous solution. The system consists of 1 Na atom, 1 Cl atom, and 107 water molecules for a total of 323 atoms. In an effort to speed up the simulations, we employ a rather small water box, and thus need to employ smaller cutoffs than usually used. Therefore, this simulation setup should not be used in production runs. Typically, the run should take around 15-20 minutes to run on a laptop using two MPI processes. By running the simulations on a cluster, you reduce the simulation time.

The most relevant CV for this system is the distance between the Na and Cl atoms
that is defined in PLUMED as
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span style="color:blue" class="comment"># Distance between Na and Cl atoms</span>
<b name="data/INSTRUCTIONS.md_working_1.datdist" onclick='showPath("data/INSTRUCTIONS.md_working_1.dat","data/INSTRUCTIONS.md_working_1.datdist","data/INSTRUCTIONS.md_working_1.datdist","black")'>dist</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_1.datdist">The DISTANCE action with label <b>dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist</td><td width="5%"><font color="black">scalar</font></td><td>the DISTANCE between this pair of atoms</td></tr></table></span>:  <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=322,323
</pre>
 {% endraw %} 

Furthermore, the NaCl association/dissociation is coupled to the collective motion
of the solvent. To measure that, we will use a CV that measures the solvation of the
Na atom. For this, we employ the coordination number of the Na atom with respect to
the oxygens of the water molecules that we define in PLUMED as
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_2.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_2.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_2.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span style="color:blue" class="comment"># Solvation of Na atom</span>
<span class="plumedtooltip" style="color:green">COORDINATION<span class="right">Calculate coordination numbers. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATION" style="color:green">More details</a><i></i></span></span> ...
 <span class="plumedtooltip">GROUPA<span class="right">First list of atoms<i></i></span></span>=322
 <span class="plumedtooltip">GROUPB<span class="right">Second list of atoms (if empty, N*(N-1)/2 pairs in GROUPA are counted)<i></i></span></span>=1-321:3
 <span class="plumedtooltip">SWITCH<span class="right">This keyword is used if you want to employ an alternative to the continuous switching function defined above. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=0.315 D_MAX=0.5 NN=12 MM=24}
 <span class="plumedtooltip">NLIST<span class="right"> Use a neighbor list to speed up the calculation<i></i></span></span>
 <span class="plumedtooltip">NL_CUTOFF<span class="right">The cutoff for the neighbor list<i></i></span></span>=0.55
 <span class="plumedtooltip">NL_STRIDE<span class="right">The frequency with which we are updating the atoms in the neighbor list<i></i></span></span>=10
 <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_2.datcoord" onclick='showPath("data/INSTRUCTIONS.md_working_2.dat","data/INSTRUCTIONS.md_working_2.datcoord","data/INSTRUCTIONS.md_working_2.datcoord","black")'>coord</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_2.datcoord">The COORDINATION action with label <b>coord</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">coord</td><td width="5%"><font color="black">scalar</font></td><td>the value of the coordination</td></tr></table></span>
... COORDINATION
</pre>
 {% endraw %} 

We will also limit CV space exploration by employing an upper wall on the distance between
Na and Cl atoms that is defined in PLUMED as
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_3.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_3.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_3.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/INSTRUCTIONS.md_working_3.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_3.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/INSTRUCTIONS.md_working_3.dat_hiddenpart1_long" style="display:none;"><span style="color:blue" class="comment"># Distance between Na and Cl atoms</span>
<b name="data/INSTRUCTIONS.md_working_3.datdist" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datdist","data/INSTRUCTIONS.md_working_3.datdist","black")'>dist</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datdist">The DISTANCE action with label <b>dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist</td><td width="5%"><font color="black">scalar</font></td><td>the DISTANCE between this pair of atoms</td></tr></table></span>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=322,323
<a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_3.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> ...
   <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_3.datdist">dist</b>
   <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=0.6
   <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=4000.0
   <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_3.datuwall" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datuwall","data/INSTRUCTIONS.md_working_3.datuwall","black")'>uwall</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datuwall">The UPPER_WALLS action with label <b>uwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">uwall.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">uwall.force2</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span>
... UPPER_WALLS
</pre>
 {% endraw %} 

## Exercise 1: Biasing with One Collective Variable

We will start by performing a simulation where we bias the Na-Cl distance.

Every VES simulation has three key ingredients:

- Basis set
- Target distribution
- Optimization algorithm

For the basis set, we will use the recently introduced [wavelet-based basis set](https://doi.org/10.1021/acs.jctc.2c00197) that are localized basis functions that have been shown to perform better than the previously used Chebyshev or Legendre polynomials. We will employ the least asymmetric variant of these wavelets or so-called symlets (as indicated by the `TYPE=SYMLETS` keyword). We will use an order 10 of the symlets or Sym10 (as indicated by the `ORDER=10` keyword). Furthermore information about the wavelets can be found in the reference above.

We need to select the range on which the bias potential is expanded. Here we will use the range from 0.2 nm to 0.7 nm (as indicated by the `MINIMUM=0.2` and `MAXIMUM=0.7` keywords). We also need to select the number of basis functions, and here we will use 26 basis functions (as indicated by the `NUM_BF=26` keyword). The PLUMED action corresponding to this setup is given by
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_4.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_4.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_4.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/INSTRUCTIONS.md_working_4.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/INSTRUCTIONS.md_working_4.dat_hiddenpart1_long" style="display:none;"><span style="color:blue" class="comment"># Distance between Na and Cl atoms</span>
<b name="data/INSTRUCTIONS.md_working_4.datdist" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datdist","data/INSTRUCTIONS.md_working_4.datdist","black")'>dist</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datdist">The DISTANCE action with label <b>dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist</td><td width="5%"><font color="black">scalar</font></td><td>the DISTANCE between this pair of atoms</td></tr></table></span>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=322,323

<span style="color:blue" class="comment"># Solvation of Na atom</span>
<span class="plumedtooltip" style="color:green">COORDINATION<span class="right">Calculate coordination numbers. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATION" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_4.datcoord" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datcoord","data/INSTRUCTIONS.md_working_4.datcoord","black")'>coord</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datcoord">The COORDINATION action with label <b>coord</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">coord</td><td width="5%"><font color="black">scalar</font></td><td>the value of the coordination</td></tr></table></span>
  <span class="plumedtooltip">GROUPA<span class="right">First list of atoms<i></i></span></span>=322
  <span class="plumedtooltip">GROUPB<span class="right">Second list of atoms (if empty, N*(N-1)/2 pairs in GROUPA are counted)<i></i></span></span>=1-321:3
  <span class="plumedtooltip">SWITCH<span class="right">This keyword is used if you want to employ an alternative to the continuous switching function defined above. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=0.315 D_MAX=0.5 NN=12 MM=24}
  <span class="plumedtooltip">NLIST<span class="right"> Use a neighbor list to speed up the calculation<i></i></span></span>
  <span class="plumedtooltip">NL_CUTOFF<span class="right">The cutoff for the neighbor list<i></i></span></span>=0.55
  <span class="plumedtooltip">NL_STRIDE<span class="right">The frequency with which we are updating the atoms in the neighbor list<i></i></span></span>=10
... COORDINATION
<a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span style="color:blue" class="comment"># Basisset for Na-Cl distance</span>
<span class="plumedtooltip" style="color:green">BF_WAVELETS<span class="right">Daubechies Wavelets basis functions. <a href="https://www.plumed.org/doc-master/user-doc/html/BF_WAVELETS" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_4.datbf1" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datbf1","data/INSTRUCTIONS.md_working_4.datbf1","brown")'>bf1</b>
  <span class="plumedtooltip">TYPE<span class="right">Specify the wavelet type<i></i></span></span>=SYMLETS
  <span class="plumedtooltip">ORDER<span class="right">The order of the basis function expansion<i></i></span></span>=10
  <span class="plumedtooltip">NUM_BF<span class="right">The number of basis functions that should be used<i></i></span></span>=26
  <span class="plumedtooltip">MINIMUM<span class="right">The minimum of the interval on which the basis functions are defined<i></i></span></span>=0.2
  <span class="plumedtooltip">MAXIMUM<span class="right">The maximum of the interval on which the basis functions are defined<i></i></span></span>=0.7
  <span class="plumedtooltip">TAILS_THRESHOLD<span class="right">The threshold for cutting off tail wavelets as a fraction of the maximum value<i></i></span></span>=0.01
... BF_WAVELETS
<span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datbf1">The BF_WAVELETS action with label <b>bf1</b> calculates something</span></pre>
 {% endraw %} 

For the target distribution, we employ a well-tempered distribution with a bias factor
of 10.
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_5.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_5.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_5.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/INSTRUCTIONS.md_working_5.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_5.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/INSTRUCTIONS.md_working_5.dat_hiddenpart1_long" style="display:none;"><span style="color:blue" class="comment"># Distance between Na and Cl atoms</span>
<b name="data/INSTRUCTIONS.md_working_5.datdist" onclick='showPath("data/INSTRUCTIONS.md_working_5.dat","data/INSTRUCTIONS.md_working_5.datdist","data/INSTRUCTIONS.md_working_5.datdist","black")'>dist</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_5.datdist">The DISTANCE action with label <b>dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist</td><td width="5%"><font color="black">scalar</font></td><td>the DISTANCE between this pair of atoms</td></tr></table></span>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=322,323

<span style="color:blue" class="comment"># Solvation of Na atom</span>
<span class="plumedtooltip" style="color:green">COORDINATION<span class="right">Calculate coordination numbers. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATION" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_5.datcoord" onclick='showPath("data/INSTRUCTIONS.md_working_5.dat","data/INSTRUCTIONS.md_working_5.datcoord","data/INSTRUCTIONS.md_working_5.datcoord","black")'>coord</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_5.datcoord">The COORDINATION action with label <b>coord</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">coord</td><td width="5%"><font color="black">scalar</font></td><td>the value of the coordination</td></tr></table></span>
  <span class="plumedtooltip">GROUPA<span class="right">First list of atoms<i></i></span></span>=322
  <span class="plumedtooltip">GROUPB<span class="right">Second list of atoms (if empty, N*(N-1)/2 pairs in GROUPA are counted)<i></i></span></span>=1-321:3
  <span class="plumedtooltip">SWITCH<span class="right">This keyword is used if you want to employ an alternative to the continuous switching function defined above. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=0.315 D_MAX=0.5 NN=12 MM=24}
  <span class="plumedtooltip">NLIST<span class="right"> Use a neighbor list to speed up the calculation<i></i></span></span>
  <span class="plumedtooltip">NL_CUTOFF<span class="right">The cutoff for the neighbor list<i></i></span></span>=0.55
  <span class="plumedtooltip">NL_STRIDE<span class="right">The frequency with which we are updating the atoms in the neighbor list<i></i></span></span>=10
... COORDINATION
<br/><span style="color:blue" class="comment"># Basisset for Na-Cl distance</span>
<span class="plumedtooltip" style="color:green">BF_WAVELETS<span class="right">Daubechies Wavelets basis functions. <a href="https://www.plumed.org/doc-master/user-doc/html/BF_WAVELETS" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_5.datbf1" onclick='showPath("data/INSTRUCTIONS.md_working_5.dat","data/INSTRUCTIONS.md_working_5.datbf1","data/INSTRUCTIONS.md_working_5.datbf1","brown")'>bf1</b>
  <span class="plumedtooltip">TYPE<span class="right">Specify the wavelet type<i></i></span></span>=SYMLETS
  <span class="plumedtooltip">ORDER<span class="right">The order of the basis function expansion<i></i></span></span>=10
  <span class="plumedtooltip">NUM_BF<span class="right">The number of basis functions that should be used<i></i></span></span>=26
  <span class="plumedtooltip">MINIMUM<span class="right">The minimum of the interval on which the basis functions are defined<i></i></span></span>=0.2
  <span class="plumedtooltip">MAXIMUM<span class="right">The maximum of the interval on which the basis functions are defined<i></i></span></span>=0.7
  <span class="plumedtooltip">TAILS_THRESHOLD<span class="right">The threshold for cutting off tail wavelets as a fraction of the maximum value<i></i></span></span>=0.01
... BF_WAVELETS
<a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_5.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span style="color:blue" class="comment"># Target distribution</span>
<span style="display:none;" id="data/INSTRUCTIONS.md_working_5.datbf1">The BF_WAVELETS action with label <b>bf1</b> calculates something</span><b name="data/INSTRUCTIONS.md_working_5.dattd" onclick='showPath("data/INSTRUCTIONS.md_working_5.dat","data/INSTRUCTIONS.md_working_5.dattd","data/INSTRUCTIONS.md_working_5.dattd","brown")'>td</b>: <span class="plumedtooltip" style="color:green">TD_WELLTEMPERED<span class="right">Well-tempered target distribution (dynamic). <a href="https://www.plumed.org/doc-master/user-doc/html/TD_WELLTEMPERED" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">BIASFACTOR<span class="right">The bias factor used for the well-tempered distribution<i></i></span></span>=10
<span style="display:none;" id="data/INSTRUCTIONS.md_working_5.dattd">The TD_WELLTEMPERED action with label <b>td</b> calculates something</span></pre>
 {% endraw %} 

Then we define the VES bias potential using the `VES_LINEAR_EXPANSION` action
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_6.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_6.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_6.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/INSTRUCTIONS.md_working_6.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_6.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/INSTRUCTIONS.md_working_6.dat_hiddenpart1_long" style="display:none;"><span style="color:blue" class="comment"># Distance between Na and Cl atoms</span>
<b name="data/INSTRUCTIONS.md_working_6.datdist" onclick='showPath("data/INSTRUCTIONS.md_working_6.dat","data/INSTRUCTIONS.md_working_6.datdist","data/INSTRUCTIONS.md_working_6.datdist","black")'>dist</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_6.datdist">The DISTANCE action with label <b>dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist</td><td width="5%"><font color="black">scalar</font></td><td>the DISTANCE between this pair of atoms</td></tr></table></span>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=322,323

<span style="color:blue" class="comment"># Solvation of Na atom</span>
<span class="plumedtooltip" style="color:green">COORDINATION<span class="right">Calculate coordination numbers. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATION" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_6.datcoord" onclick='showPath("data/INSTRUCTIONS.md_working_6.dat","data/INSTRUCTIONS.md_working_6.datcoord","data/INSTRUCTIONS.md_working_6.datcoord","black")'>coord</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_6.datcoord">The COORDINATION action with label <b>coord</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">coord</td><td width="5%"><font color="black">scalar</font></td><td>the value of the coordination</td></tr></table></span>
  <span class="plumedtooltip">GROUPA<span class="right">First list of atoms<i></i></span></span>=322
  <span class="plumedtooltip">GROUPB<span class="right">Second list of atoms (if empty, N*(N-1)/2 pairs in GROUPA are counted)<i></i></span></span>=1-321:3
  <span class="plumedtooltip">SWITCH<span class="right">This keyword is used if you want to employ an alternative to the continuous switching function defined above. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=0.315 D_MAX=0.5 NN=12 MM=24}
  <span class="plumedtooltip">NLIST<span class="right"> Use a neighbor list to speed up the calculation<i></i></span></span>
  <span class="plumedtooltip">NL_CUTOFF<span class="right">The cutoff for the neighbor list<i></i></span></span>=0.55
  <span class="plumedtooltip">NL_STRIDE<span class="right">The frequency with which we are updating the atoms in the neighbor list<i></i></span></span>=10
... COORDINATION
<br/><span style="color:blue" class="comment"># Basisset for Na-Cl distance</span>
<span class="plumedtooltip" style="color:green">BF_WAVELETS<span class="right">Daubechies Wavelets basis functions. <a href="https://www.plumed.org/doc-master/user-doc/html/BF_WAVELETS" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_6.datbf1" onclick='showPath("data/INSTRUCTIONS.md_working_6.dat","data/INSTRUCTIONS.md_working_6.datbf1","data/INSTRUCTIONS.md_working_6.datbf1","brown")'>bf1</b>
  <span class="plumedtooltip">TYPE<span class="right">Specify the wavelet type<i></i></span></span>=SYMLETS
  <span class="plumedtooltip">ORDER<span class="right">The order of the basis function expansion<i></i></span></span>=10
  <span class="plumedtooltip">NUM_BF<span class="right">The number of basis functions that should be used<i></i></span></span>=26
  <span class="plumedtooltip">MINIMUM<span class="right">The minimum of the interval on which the basis functions are defined<i></i></span></span>=0.2
  <span class="plumedtooltip">MAXIMUM<span class="right">The maximum of the interval on which the basis functions are defined<i></i></span></span>=0.7
  <span class="plumedtooltip">TAILS_THRESHOLD<span class="right">The threshold for cutting off tail wavelets as a fraction of the maximum value<i></i></span></span>=0.01
... BF_WAVELETS
<br/><span style="color:blue" class="comment"># Target distribution</span>
<span style="display:none;" id="data/INSTRUCTIONS.md_working_6.datbf1">The BF_WAVELETS action with label <b>bf1</b> calculates something</span><b name="data/INSTRUCTIONS.md_working_6.dattd" onclick='showPath("data/INSTRUCTIONS.md_working_6.dat","data/INSTRUCTIONS.md_working_6.dattd","data/INSTRUCTIONS.md_working_6.dattd","brown")'>td</b>: <span class="plumedtooltip" style="color:green">TD_WELLTEMPERED<span class="right">Well-tempered target distribution (dynamic). <a href="https://www.plumed.org/doc-master/user-doc/html/TD_WELLTEMPERED" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">BIASFACTOR<span class="right">The bias factor used for the well-tempered distribution<i></i></span></span>=10
<a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_6.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span id="data/INSTRUCTIONS.md_working_6.datdefves_short"><span style="display:none;" id="data/INSTRUCTIONS.md_working_6.dattd">The TD_WELLTEMPERED action with label <b>td</b> calculates something</span><span class="plumedtooltip" style="color:green">VES_LINEAR_EXPANSION<span class="right">Linear basis set expansion bias. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_6.datdefves");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/VES_LINEAR_EXPANSION">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_6.datves" onclick='showPath("data/INSTRUCTIONS.md_working_6.dat","data/INSTRUCTIONS.md_working_6.datves","data/INSTRUCTIONS.md_working_6.datves","black")'>ves</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_6.datves">The VES_LINEAR_EXPANSION action with label <b>ves</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">ves.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">ves.force2</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the squared force due to this bias potential.</td></tr></table></span>
  <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_6.datdist">dist</b>
  <span class="plumedtooltip">BASIS_FUNCTIONS<span class="right">the label of the one dimensional basis functions that should be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_6.datbf1">bf1</b>
  <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is needed if the MD code does not pass the temperature to PLUMED<i></i></span></span>=300.0
  <span class="plumedtooltip">GRID_BINS<span class="right">the number of bins used for the grid<i></i></span></span>=300
  <span class="plumedtooltip">OPTIMIZATION_THRESHOLD<span class="right">Threshold value to turn off optimization of localized basis functions<i></i></span></span>=0.000001
  <span class="plumedtooltip">TARGET_DISTRIBUTION<span class="right">the label of the target distribution to be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_6.dattd">td</b>
... VES_LINEAR_EXPANSION
</span><span id="data/INSTRUCTIONS.md_working_6.datdefves_long" style="display:none;"><span class="plumedtooltip" style="color:green">VES_LINEAR_EXPANSION<span class="right">Linear basis set expansion bias. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_6.datdefves");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/VES_LINEAR_EXPANSION">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_6.datves" onclick='showPath("data/INSTRUCTIONS.md_working_6.dat","data/INSTRUCTIONS.md_working_6.datves","data/INSTRUCTIONS.md_working_6.datves","black")'>ves</b>
  <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_6.datdist">dist</b>
  <span class="plumedtooltip">BASIS_FUNCTIONS<span class="right">the label of the one dimensional basis functions that should be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_6.datbf1">bf1</b>
  <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is needed if the MD code does not pass the temperature to PLUMED<i></i></span></span>=300.0
  <span class="plumedtooltip">GRID_BINS<span class="right">the number of bins used for the grid<i></i></span></span>=300
  <span class="plumedtooltip">OPTIMIZATION_THRESHOLD<span class="right">Threshold value to turn off optimization of localized basis functions<i></i></span></span>=0.000001
  <span class="plumedtooltip">TARGET_DISTRIBUTION<span class="right">the label of the target distribution to be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_6.dattd">td</b>
 <span class="plumedtooltip">GRID_FMT<span class="right"> the format to use when outputting the numbers in the grids<i></i></span></span>=%14.9f
... VES_LINEAR_EXPANSION
</span></pre>
 {% endraw %} 

Finally, we need to define the optimization algorithm. The standard is the averaged stochastic gradient descent (`OPT_AVERAGED_SGD`).
We need to define two parameters: the stride and the step size.
The stride (given by the keyword `STRIDE`) is the number of MD steps in which samples
are collected to calculate the gradient and hessian of $\Omega [V]$. The
step size (given by the keyword `STEPSIZE`) is the step by which the coefficients
are evolved at every optimization steps, given by $\mu$ in the equation above.
It has become
traditional to choose a stride of around 500-2000 MD steps. It must be noted that we
are not looking for an accurate estimation of the gradient, since for this we
would need to sample all the CV space. The step size in the
optimization has a strong connection with the height of typical barriers in
the system. The larger the barriers, the larger the step size needed such that
the bias can grow fast enough to overcome them. For this example we have
chosen a stride of 500 steps (i.e., 1 ps) and a step size of 5.0 kJ/mol.
We also need to choose how often we update the target distribution (given by the
keyword `TARGETDIST_STRIDE`) and we do this every 100 bias potential updates
(i.e., every 100 ps in the current case).

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_7.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_7.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_7.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/INSTRUCTIONS.md_working_7.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_7.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/INSTRUCTIONS.md_working_7.dat_hiddenpart1_long" style="display:none;"><span style="color:blue" class="comment"># Distance between Na and Cl atoms</span>
<b name="data/INSTRUCTIONS.md_working_7.datdist" onclick='showPath("data/INSTRUCTIONS.md_working_7.dat","data/INSTRUCTIONS.md_working_7.datdist","data/INSTRUCTIONS.md_working_7.datdist","black")'>dist</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_7.datdist">The DISTANCE action with label <b>dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist</td><td width="5%"><font color="black">scalar</font></td><td>the DISTANCE between this pair of atoms</td></tr></table></span>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=322,323

<span style="color:blue" class="comment"># Solvation of Na atom</span>
<span class="plumedtooltip" style="color:green">COORDINATION<span class="right">Calculate coordination numbers. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATION" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_7.datcoord" onclick='showPath("data/INSTRUCTIONS.md_working_7.dat","data/INSTRUCTIONS.md_working_7.datcoord","data/INSTRUCTIONS.md_working_7.datcoord","black")'>coord</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_7.datcoord">The COORDINATION action with label <b>coord</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">coord</td><td width="5%"><font color="black">scalar</font></td><td>the value of the coordination</td></tr></table></span>
  <span class="plumedtooltip">GROUPA<span class="right">First list of atoms<i></i></span></span>=322
  <span class="plumedtooltip">GROUPB<span class="right">Second list of atoms (if empty, N*(N-1)/2 pairs in GROUPA are counted)<i></i></span></span>=1-321:3
  <span class="plumedtooltip">SWITCH<span class="right">This keyword is used if you want to employ an alternative to the continuous switching function defined above. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=0.315 D_MAX=0.5 NN=12 MM=24}
  <span class="plumedtooltip">NLIST<span class="right"> Use a neighbor list to speed up the calculation<i></i></span></span>
  <span class="plumedtooltip">NL_CUTOFF<span class="right">The cutoff for the neighbor list<i></i></span></span>=0.55
  <span class="plumedtooltip">NL_STRIDE<span class="right">The frequency with which we are updating the atoms in the neighbor list<i></i></span></span>=10
... COORDINATION
<br/><span style="color:blue" class="comment"># Basisset for Na-Cl distance</span>
<span class="plumedtooltip" style="color:green">BF_WAVELETS<span class="right">Daubechies Wavelets basis functions. <a href="https://www.plumed.org/doc-master/user-doc/html/BF_WAVELETS" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_7.datbf1" onclick='showPath("data/INSTRUCTIONS.md_working_7.dat","data/INSTRUCTIONS.md_working_7.datbf1","data/INSTRUCTIONS.md_working_7.datbf1","brown")'>bf1</b>
  <span class="plumedtooltip">TYPE<span class="right">Specify the wavelet type<i></i></span></span>=SYMLETS
  <span class="plumedtooltip">ORDER<span class="right">The order of the basis function expansion<i></i></span></span>=10
  <span class="plumedtooltip">NUM_BF<span class="right">The number of basis functions that should be used<i></i></span></span>=26
  <span class="plumedtooltip">MINIMUM<span class="right">The minimum of the interval on which the basis functions are defined<i></i></span></span>=0.2
  <span class="plumedtooltip">MAXIMUM<span class="right">The maximum of the interval on which the basis functions are defined<i></i></span></span>=0.7
  <span class="plumedtooltip">TAILS_THRESHOLD<span class="right">The threshold for cutting off tail wavelets as a fraction of the maximum value<i></i></span></span>=0.01
... BF_WAVELETS
<br/><span style="color:blue" class="comment"># Target distribution</span>
<span style="display:none;" id="data/INSTRUCTIONS.md_working_7.datbf1">The BF_WAVELETS action with label <b>bf1</b> calculates something</span><b name="data/INSTRUCTIONS.md_working_7.dattd" onclick='showPath("data/INSTRUCTIONS.md_working_7.dat","data/INSTRUCTIONS.md_working_7.dattd","data/INSTRUCTIONS.md_working_7.dattd","brown")'>td</b>: <span class="plumedtooltip" style="color:green">TD_WELLTEMPERED<span class="right">Well-tempered target distribution (dynamic). <a href="https://www.plumed.org/doc-master/user-doc/html/TD_WELLTEMPERED" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">BIASFACTOR<span class="right">The bias factor used for the well-tempered distribution<i></i></span></span>=10

<span id="data/INSTRUCTIONS.md_working_7.datdefves_short"><span style="display:none;" id="data/INSTRUCTIONS.md_working_7.dattd">The TD_WELLTEMPERED action with label <b>td</b> calculates something</span><span class="plumedtooltip" style="color:green">VES_LINEAR_EXPANSION<span class="right">Linear basis set expansion bias. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_7.datdefves");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/VES_LINEAR_EXPANSION">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_7.datves" onclick='showPath("data/INSTRUCTIONS.md_working_7.dat","data/INSTRUCTIONS.md_working_7.datves","data/INSTRUCTIONS.md_working_7.datves","black")'>ves</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_7.datves">The VES_LINEAR_EXPANSION action with label <b>ves</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">ves.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">ves.force2</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the squared force due to this bias potential.</td></tr></table></span>
  <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_7.datdist">dist</b>
  <span class="plumedtooltip">BASIS_FUNCTIONS<span class="right">the label of the one dimensional basis functions that should be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_7.datbf1">bf1</b>
  <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is needed if the MD code does not pass the temperature to PLUMED<i></i></span></span>=300.0
  <span class="plumedtooltip">GRID_BINS<span class="right">the number of bins used for the grid<i></i></span></span>=300
  <span class="plumedtooltip">OPTIMIZATION_THRESHOLD<span class="right">Threshold value to turn off optimization of localized basis functions<i></i></span></span>=0.000001
  <span class="plumedtooltip">TARGET_DISTRIBUTION<span class="right">the label of the target distribution to be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_7.dattd">td</b>
... VES_LINEAR_EXPANSION
</span><span id="data/INSTRUCTIONS.md_working_7.datdefves_long" style="display:none;"><span class="plumedtooltip" style="color:green">VES_LINEAR_EXPANSION<span class="right">Linear basis set expansion bias. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_7.datdefves");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/VES_LINEAR_EXPANSION">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_7.datves" onclick='showPath("data/INSTRUCTIONS.md_working_7.dat","data/INSTRUCTIONS.md_working_7.datves","data/INSTRUCTIONS.md_working_7.datves","black")'>ves</b>
  <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_7.datdist">dist</b>
  <span class="plumedtooltip">BASIS_FUNCTIONS<span class="right">the label of the one dimensional basis functions that should be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_7.datbf1">bf1</b>
  <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is needed if the MD code does not pass the temperature to PLUMED<i></i></span></span>=300.0
  <span class="plumedtooltip">GRID_BINS<span class="right">the number of bins used for the grid<i></i></span></span>=300
  <span class="plumedtooltip">OPTIMIZATION_THRESHOLD<span class="right">Threshold value to turn off optimization of localized basis functions<i></i></span></span>=0.000001
  <span class="plumedtooltip">TARGET_DISTRIBUTION<span class="right">the label of the target distribution to be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_7.dattd">td</b>
 <span class="plumedtooltip">GRID_FMT<span class="right"> the format to use when outputting the numbers in the grids<i></i></span></span>=%14.9f
... VES_LINEAR_EXPANSION
</span><a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_7.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span id="data/INSTRUCTIONS.md_working_7.datdefopt_short"><span class="plumedtooltip" style="color:green">OPT_AVERAGED_SGD<span class="right">Averaged stochastic gradient decent with fixed step size. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_7.datdefopt");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/OPT_AVERAGED_SGD">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_7.datopt" onclick='showPath("data/INSTRUCTIONS.md_working_7.dat","data/INSTRUCTIONS.md_working_7.datopt","data/INSTRUCTIONS.md_working_7.datopt","brown")'>opt</b>
  <span class="plumedtooltip">BIAS<span class="right">the label of the VES bias to be optimized<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_7.datves">ves</b>
  <span class="plumedtooltip">STRIDE<span class="right">the frequency of updating the coefficients given in the number of MD steps<i></i></span></span>=500
  <span class="plumedtooltip">STEPSIZE<span class="right">the step size used for the optimization<i></i></span></span>=5.0
  <span class="plumedtooltip">FES_OUTPUT<span class="right">how often the FES(s) should be written out to file<i></i></span></span>=100
  <span class="plumedtooltip">BIAS_OUTPUT<span class="right">how often the bias(es) should be written out to file<i></i></span></span>=500
  <span class="plumedtooltip">COEFFS_OUTPUT<span class="right"> how often the coefficients should be written to file<i></i></span></span>=10
  <span class="plumedtooltip">TARGETDIST_STRIDE<span class="right">stride for updating a target distribution that is iteratively updated during the optimization<i></i></span></span>=100
  <span class="plumedtooltip">TARGETDIST_OUTPUT<span class="right">how often the dynamic target distribution(s) should be written out to file<i></i></span></span>=500
... OPT_AVERAGED_SGD
</span><span id="data/INSTRUCTIONS.md_working_7.datdefopt_long" style="display:none;"><span style="display:none;" id="data/INSTRUCTIONS.md_working_7.datopt">The OPT_AVERAGED_SGD action with label <b>opt</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">opt.value</td><td>a scalar</td></tr></table></span><span class="plumedtooltip" style="color:green">OPT_AVERAGED_SGD<span class="right">Averaged stochastic gradient decent with fixed step size. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_7.datdefopt");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/OPT_AVERAGED_SGD">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_7.datopt" onclick='showPath("data/INSTRUCTIONS.md_working_7.dat","data/INSTRUCTIONS.md_working_7.datopt","data/INSTRUCTIONS.md_working_7.datopt","brown")'>opt</b>
  <span class="plumedtooltip">BIAS<span class="right">the label of the VES bias to be optimized<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_7.datves">ves</b>
  <span class="plumedtooltip">STRIDE<span class="right">the frequency of updating the coefficients given in the number of MD steps<i></i></span></span>=500
  <span class="plumedtooltip">STEPSIZE<span class="right">the step size used for the optimization<i></i></span></span>=5.0
  <span class="plumedtooltip">FES_OUTPUT<span class="right">how often the FES(s) should be written out to file<i></i></span></span>=100
  <span class="plumedtooltip">BIAS_OUTPUT<span class="right">how often the bias(es) should be written out to file<i></i></span></span>=500
  <span class="plumedtooltip">COEFFS_OUTPUT<span class="right"> how often the coefficients should be written to file<i></i></span></span>=10
  <span class="plumedtooltip">TARGETDIST_STRIDE<span class="right">stride for updating a target distribution that is iteratively updated during the optimization<i></i></span></span>=100
  <span class="plumedtooltip">TARGETDIST_OUTPUT<span class="right">how often the dynamic target distribution(s) should be written out to file<i></i></span></span>=500
 <span class="plumedtooltip">COEFFS_FILE<span class="right"> the name of output file for the coefficients<i></i></span></span>=coeffs.data
... OPT_AVERAGED_SGD
</span></pre>
 {% endraw %} 
The other parameters are related to the outputting frequency of various output files.

Finally, we need to define the `PRINT` action to output all the variables
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_8.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_8.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_8.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/INSTRUCTIONS.md_working_8.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_8.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/INSTRUCTIONS.md_working_8.dat_hiddenpart1_long" style="display:none;"><span style="color:blue" class="comment"># Distance between Na and Cl atoms</span>
<b name="data/INSTRUCTIONS.md_working_8.datdist" onclick='showPath("data/INSTRUCTIONS.md_working_8.dat","data/INSTRUCTIONS.md_working_8.datdist","data/INSTRUCTIONS.md_working_8.datdist","black")'>dist</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_8.datdist">The DISTANCE action with label <b>dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist</td><td width="5%"><font color="black">scalar</font></td><td>the DISTANCE between this pair of atoms</td></tr></table></span>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=322,323

<span style="color:blue" class="comment"># Solvation of Na atom</span>
<span class="plumedtooltip" style="color:green">COORDINATION<span class="right">Calculate coordination numbers. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATION" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datcoord" onclick='showPath("data/INSTRUCTIONS.md_working_8.dat","data/INSTRUCTIONS.md_working_8.datcoord","data/INSTRUCTIONS.md_working_8.datcoord","black")'>coord</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_8.datcoord">The COORDINATION action with label <b>coord</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">coord</td><td width="5%"><font color="black">scalar</font></td><td>the value of the coordination</td></tr></table></span>
  <span class="plumedtooltip">GROUPA<span class="right">First list of atoms<i></i></span></span>=322
  <span class="plumedtooltip">GROUPB<span class="right">Second list of atoms (if empty, N*(N-1)/2 pairs in GROUPA are counted)<i></i></span></span>=1-321:3
  <span class="plumedtooltip">SWITCH<span class="right">This keyword is used if you want to employ an alternative to the continuous switching function defined above. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=0.315 D_MAX=0.5 NN=12 MM=24}
  <span class="plumedtooltip">NLIST<span class="right"> Use a neighbor list to speed up the calculation<i></i></span></span>
  <span class="plumedtooltip">NL_CUTOFF<span class="right">The cutoff for the neighbor list<i></i></span></span>=0.55
  <span class="plumedtooltip">NL_STRIDE<span class="right">The frequency with which we are updating the atoms in the neighbor list<i></i></span></span>=10
... COORDINATION
<br/><span style="color:blue" class="comment"># Basisset for Na-Cl distance</span>
<span class="plumedtooltip" style="color:green">BF_WAVELETS<span class="right">Daubechies Wavelets basis functions. <a href="https://www.plumed.org/doc-master/user-doc/html/BF_WAVELETS" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datbf1" onclick='showPath("data/INSTRUCTIONS.md_working_8.dat","data/INSTRUCTIONS.md_working_8.datbf1","data/INSTRUCTIONS.md_working_8.datbf1","brown")'>bf1</b>
  <span class="plumedtooltip">TYPE<span class="right">Specify the wavelet type<i></i></span></span>=SYMLETS
  <span class="plumedtooltip">ORDER<span class="right">The order of the basis function expansion<i></i></span></span>=10
  <span class="plumedtooltip">NUM_BF<span class="right">The number of basis functions that should be used<i></i></span></span>=26
  <span class="plumedtooltip">MINIMUM<span class="right">The minimum of the interval on which the basis functions are defined<i></i></span></span>=0.2
  <span class="plumedtooltip">MAXIMUM<span class="right">The maximum of the interval on which the basis functions are defined<i></i></span></span>=0.7
  <span class="plumedtooltip">TAILS_THRESHOLD<span class="right">The threshold for cutting off tail wavelets as a fraction of the maximum value<i></i></span></span>=0.01
... BF_WAVELETS
<br/><span style="color:blue" class="comment"># Target distribution</span>
<span style="display:none;" id="data/INSTRUCTIONS.md_working_8.datbf1">The BF_WAVELETS action with label <b>bf1</b> calculates something</span><b name="data/INSTRUCTIONS.md_working_8.dattd" onclick='showPath("data/INSTRUCTIONS.md_working_8.dat","data/INSTRUCTIONS.md_working_8.dattd","data/INSTRUCTIONS.md_working_8.dattd","brown")'>td</b>: <span class="plumedtooltip" style="color:green">TD_WELLTEMPERED<span class="right">Well-tempered target distribution (dynamic). <a href="https://www.plumed.org/doc-master/user-doc/html/TD_WELLTEMPERED" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">BIASFACTOR<span class="right">The bias factor used for the well-tempered distribution<i></i></span></span>=10

<span id="data/INSTRUCTIONS.md_working_8.datdefves_short"><span style="display:none;" id="data/INSTRUCTIONS.md_working_8.dattd">The TD_WELLTEMPERED action with label <b>td</b> calculates something</span><span class="plumedtooltip" style="color:green">VES_LINEAR_EXPANSION<span class="right">Linear basis set expansion bias. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_8.datdefves");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/VES_LINEAR_EXPANSION">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datves" onclick='showPath("data/INSTRUCTIONS.md_working_8.dat","data/INSTRUCTIONS.md_working_8.datves","data/INSTRUCTIONS.md_working_8.datves","black")'>ves</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_8.datves">The VES_LINEAR_EXPANSION action with label <b>ves</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">ves.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">ves.force2</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the squared force due to this bias potential.</td></tr></table></span>
  <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datdist">dist</b>
  <span class="plumedtooltip">BASIS_FUNCTIONS<span class="right">the label of the one dimensional basis functions that should be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datbf1">bf1</b>
  <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is needed if the MD code does not pass the temperature to PLUMED<i></i></span></span>=300.0
  <span class="plumedtooltip">GRID_BINS<span class="right">the number of bins used for the grid<i></i></span></span>=300
  <span class="plumedtooltip">OPTIMIZATION_THRESHOLD<span class="right">Threshold value to turn off optimization of localized basis functions<i></i></span></span>=0.000001
  <span class="plumedtooltip">TARGET_DISTRIBUTION<span class="right">the label of the target distribution to be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.dattd">td</b>
... VES_LINEAR_EXPANSION
</span><span id="data/INSTRUCTIONS.md_working_8.datdefves_long" style="display:none;"><span class="plumedtooltip" style="color:green">VES_LINEAR_EXPANSION<span class="right">Linear basis set expansion bias. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_8.datdefves");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/VES_LINEAR_EXPANSION">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datves" onclick='showPath("data/INSTRUCTIONS.md_working_8.dat","data/INSTRUCTIONS.md_working_8.datves","data/INSTRUCTIONS.md_working_8.datves","black")'>ves</b>
  <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datdist">dist</b>
  <span class="plumedtooltip">BASIS_FUNCTIONS<span class="right">the label of the one dimensional basis functions that should be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datbf1">bf1</b>
  <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is needed if the MD code does not pass the temperature to PLUMED<i></i></span></span>=300.0
  <span class="plumedtooltip">GRID_BINS<span class="right">the number of bins used for the grid<i></i></span></span>=300
  <span class="plumedtooltip">OPTIMIZATION_THRESHOLD<span class="right">Threshold value to turn off optimization of localized basis functions<i></i></span></span>=0.000001
  <span class="plumedtooltip">TARGET_DISTRIBUTION<span class="right">the label of the target distribution to be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.dattd">td</b>
 <span class="plumedtooltip">GRID_FMT<span class="right"> the format to use when outputting the numbers in the grids<i></i></span></span>=%14.9f
... VES_LINEAR_EXPANSION
</span><br/><span id="data/INSTRUCTIONS.md_working_8.datdefopt_short"><span class="plumedtooltip" style="color:green">OPT_AVERAGED_SGD<span class="right">Averaged stochastic gradient decent with fixed step size. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_8.datdefopt");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/OPT_AVERAGED_SGD">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datopt" onclick='showPath("data/INSTRUCTIONS.md_working_8.dat","data/INSTRUCTIONS.md_working_8.datopt","data/INSTRUCTIONS.md_working_8.datopt","brown")'>opt</b>
  <span class="plumedtooltip">BIAS<span class="right">the label of the VES bias to be optimized<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datves">ves</b>
  <span class="plumedtooltip">STRIDE<span class="right">the frequency of updating the coefficients given in the number of MD steps<i></i></span></span>=500
  <span class="plumedtooltip">STEPSIZE<span class="right">the step size used for the optimization<i></i></span></span>=5.0
  <span class="plumedtooltip">FES_OUTPUT<span class="right">how often the FES(s) should be written out to file<i></i></span></span>=100
  <span class="plumedtooltip">BIAS_OUTPUT<span class="right">how often the bias(es) should be written out to file<i></i></span></span>=1000
  <span class="plumedtooltip">COEFFS_OUTPUT<span class="right"> how often the coefficients should be written to file<i></i></span></span>=10
  <span class="plumedtooltip">TARGETDIST_STRIDE<span class="right">stride for updating a target distribution that is iteratively updated during the optimization<i></i></span></span>=100
  <span class="plumedtooltip">TARGETDIST_OUTPUT<span class="right">how often the dynamic target distribution(s) should be written out to file<i></i></span></span>=500
... OPT_AVERAGED_SGD
</span><span id="data/INSTRUCTIONS.md_working_8.datdefopt_long" style="display:none;"><span style="display:none;" id="data/INSTRUCTIONS.md_working_8.datopt">The OPT_AVERAGED_SGD action with label <b>opt</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">opt.value</td><td>a scalar</td></tr></table></span><span class="plumedtooltip" style="color:green">OPT_AVERAGED_SGD<span class="right">Averaged stochastic gradient decent with fixed step size. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_8.datdefopt");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/OPT_AVERAGED_SGD">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datopt" onclick='showPath("data/INSTRUCTIONS.md_working_8.dat","data/INSTRUCTIONS.md_working_8.datopt","data/INSTRUCTIONS.md_working_8.datopt","brown")'>opt</b>
  <span class="plumedtooltip">BIAS<span class="right">the label of the VES bias to be optimized<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datves">ves</b>
  <span class="plumedtooltip">STRIDE<span class="right">the frequency of updating the coefficients given in the number of MD steps<i></i></span></span>=500
  <span class="plumedtooltip">STEPSIZE<span class="right">the step size used for the optimization<i></i></span></span>=5.0
  <span class="plumedtooltip">FES_OUTPUT<span class="right">how often the FES(s) should be written out to file<i></i></span></span>=100
  <span class="plumedtooltip">BIAS_OUTPUT<span class="right">how often the bias(es) should be written out to file<i></i></span></span>=1000
  <span class="plumedtooltip">COEFFS_OUTPUT<span class="right"> how often the coefficients should be written to file<i></i></span></span>=10
  <span class="plumedtooltip">TARGETDIST_STRIDE<span class="right">stride for updating a target distribution that is iteratively updated during the optimization<i></i></span></span>=100
  <span class="plumedtooltip">TARGETDIST_OUTPUT<span class="right">how often the dynamic target distribution(s) should be written out to file<i></i></span></span>=500
 <span class="plumedtooltip">COEFFS_FILE<span class="right"> the name of output file for the coefficients<i></i></span></span>=coeffs.data
... OPT_AVERAGED_SGD
</span><br/><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> ...
   <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datdist">dist</b>
   <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=0.6
   <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=4000.0
   <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datuwall" onclick='showPath("data/INSTRUCTIONS.md_working_8.dat","data/INSTRUCTIONS.md_working_8.datuwall","data/INSTRUCTIONS.md_working_8.datuwall","black")'>uwall</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_8.datuwall">The UPPER_WALLS action with label <b>uwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">uwall.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">uwall.force2</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span>
...
<a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_8.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_8.datdist">dist</b>,<b name="data/INSTRUCTIONS.md_working_8.datcoord">coord</b>,<b name="data/INSTRUCTIONS.md_working_8.datves">ves.*</b>,<b name="data/INSTRUCTIONS.md_working_8.datuwall">uwall.*</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar.data <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=125
</pre>
 {% endraw %} 

The full PLUMED input file can be found in the Exercise-1 folder. There you also find all
the relevant GROMACS input file. First, you need to run the
`generate-tpr-file.sh` script that generates the GROMACS TPR file using the parameters defined in `MD-NPT.mdp` mdp file 
and the initial geometry defined using the `StartingGeometry` variable. You can then run the simulation using
the `run.sh` script
```
./generate-tpr-file.sh
./run.sh
```
The run might take around 15-20 minutes to run using two MPI processes. You can adjust the number of MPI processes used for the simulation using the `NumProcs` variable in the `run.sh` script.

At the end of simulation, you will get several files:
- `colvar.data`: Colvar file
- `coeffs.data` : Values of the coefficients $\boldsymbol\alpha$ and $\bar{\boldsymbol\alpha}$ at different iterations.
- `bias.<bias-label>.iter-<iteration-number>.data` : Bias potential at iteration <iteration-number>.
- `fes.<bias-name>.iter-<iteration-number>.data` : FES at iteration <iteration-number>.
- `targetdistribution.<bias-name>.iter-<iteration-number>.data` : Target distribution at iteration <iteration-number>.

To assess the simulation and its convergence, you should first look at the time evolution of the
biased CV and check that it is diffusive in CV space. Second, you should look at how the free energy surfaces behave as
a function of time by looking at the `fes.<bias-name>.iter-<iteration-number>.data` files at different number of iterations (the minimum of the FES is always aligned to zero
to facilitate comparison). To do this, you need to use your favorite way to plot datafiles (e.g., Matplotlib or Gnuplot). For instance, you can use the `Analysis.ipynb` Jupyter notebook provided. 

You can also visualize the trajectory by opening it with VMD by using the command
```
vmd NaCl_StartingStructure-1.gro NaCl_VES_NPT-300K.pbc-whole.xtc
```
The `NaCl_VES_NPT-300K.pbc-whole.xtc` is the trajectory file with the periodic boundary conditions made whole. This is done within the `run.sh` script.

The `coeffs.data` file includes the values of coefficients $\boldsymbol\alpha$ and $\bar{\boldsymbol\alpha}$ at different iterations. To extract the time evolution of
a given coefficient, you can use the `ExtractCoeff.sh` script, for example to extract
coefficient 3:
```
./ExtractCoeff.sh 3 > coeff.3.data
```
This will create a file with the first column the iteration number, the second
column the averaged coefficient $\bar{\boldsymbol\alpha}$, and the third column
the instantaneous coefficients $\boldsymbol\alpha$. You should create files for
different coefficient and visualize both the second and third columns to understand
how the coefficients converge.

## Exercise 2: Reweighting a VES Simulation
Apart from estimating the FES directly from the bias potential, you can also estimate
the FES through reweighting by histogramming where each configuration is weighted by the
bias acting on it, $e^{\beta V(\mathbf{s})}$. The VES bias acting at each time step
is given by the `ves.bias` variable in the `colvar.dat` file.

When doing performing reweighting, it is better to ignore the initial part of
the simulation where the bias potential is changing more rapidly. You can use the
`trim-colvar-file.py` python script in the Exercise-2 folder to do this
```
./trim-colvar-file.py --colvar-file ../Exercise-1/colvar.data --output-file colvar_reweight.data --time-min 400
```
where here we ignore the first 400 ps of the `colvar.data` file from the Exercise 1 and create
a new file called `colvar_reweight.data`.

We can then perform the reweighting for the distance using the following PLUMED input
(`plumed_reweight.dat` in the `Exercise-2` folder)
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_9.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_9.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_9.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<b name="data/INSTRUCTIONS.md_working_9.datdist" onclick='showPath("data/INSTRUCTIONS.md_working_9.dat","data/INSTRUCTIONS.md_working_9.datdist","data/INSTRUCTIONS.md_working_9.datdist","brown")'>dist</b>:   <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=colvar_reweight.data <span class="plumedtooltip">IGNORE_TIME<span class="right"> ignore the time in the colvar file<i></i></span></span> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=dist
<span style="display:none;" id="data/INSTRUCTIONS.md_working_9.datdist">The READ action with label <b>dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_9.datcoord" onclick='showPath("data/INSTRUCTIONS.md_working_9.dat","data/INSTRUCTIONS.md_working_9.datcoord","data/INSTRUCTIONS.md_working_9.datcoord","brown")'>coord</b>:  <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=colvar_reweight.data <span class="plumedtooltip">IGNORE_TIME<span class="right"> ignore the time in the colvar file<i></i></span></span> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=coord
<span style="display:none;" id="data/INSTRUCTIONS.md_working_9.datcoord">The READ action with label <b>coord</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">coord..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_9.datves" onclick='showPath("data/INSTRUCTIONS.md_working_9.dat","data/INSTRUCTIONS.md_working_9.datves","data/INSTRUCTIONS.md_working_9.datves","brown")'>ves</b>:    <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=colvar_reweight.data <span class="plumedtooltip">IGNORE_TIME<span class="right"> ignore the time in the colvar file<i></i></span></span> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=ves.bias

<span style="display:none;" id="data/INSTRUCTIONS.md_working_9.datves">The READ action with label <b>ves</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">ves..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_9.datweights" onclick='showPath("data/INSTRUCTIONS.md_working_9.dat","data/INSTRUCTIONS.md_working_9.datweights","data/INSTRUCTIONS.md_working_9.datweights","brown")'>weights</b>: <span class="plumedtooltip" style="color:green">REWEIGHT_BIAS<span class="right">Calculate weights for ensemble averages that negate the effect the bias has on the region of phase space explored <a href="https://www.plumed.org/doc-master/user-doc/html/REWEIGHT_BIAS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">TEMP<span class="right">the system temperature<i></i></span></span>=300 <span class="plumedtooltip">ARG<span class="right"> the biases that must be taken into account when reweighting<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_9.datves">ves.bias</b>

<span style="display:none;" id="data/INSTRUCTIONS.md_working_9.datweights">The REWEIGHT_BIAS action with label <b>weights</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">weights.value</td><td>the weight to use for this frame to negate the effect the bias</td></tr></table></span><span class="plumedtooltip" style="color:green">HISTOGRAM<span class="right">Accumulate the average probability density along a few CVs from a trajectory. <a href="https://www.plumed.org/doc-master/user-doc/html/HISTOGRAM" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">ARG<span class="right">the quantities that are being used to construct the histogram<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_9.datdist">dist</b>
  <span class="plumedtooltip">GRID_MIN<span class="right"> the lower bounds for the grid<i></i></span></span>=0.2
  <span class="plumedtooltip">GRID_MAX<span class="right"> the upper bounds for the grid<i></i></span></span>=0.7
  <span class="plumedtooltip">GRID_BIN<span class="right">the number of bins for the grid<i></i></span></span>=60
  <span class="plumedtooltip">KERNEL<span class="right"> the kernel function you are using<i></i></span></span>=DISCRETE
  <span class="plumedtooltip">LOGWEIGHTS<span class="right">the logarithm of the quantity to use as the weights when calculating averages<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_9.datweights">weights</b>
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_9.dathg_dist" onclick='showPath("data/INSTRUCTIONS.md_working_9.dat","data/INSTRUCTIONS.md_working_9.dathg_dist","data/INSTRUCTIONS.md_working_9.dathg_dist","brown")'>hg_dist</b>
... HISTOGRAM
<br/><span style="display:none;" id="data/INSTRUCTIONS.md_working_9.dathg_dist">The HISTOGRAM action with label <b>hg_dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">hg_dist.value</td><td>the estimate of the histogram as a function of the argument that was obtained</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_9.datfes_dist" onclick='showPath("data/INSTRUCTIONS.md_working_9.dat","data/INSTRUCTIONS.md_working_9.datfes_dist","data/INSTRUCTIONS.md_working_9.datfes_dist","brown")'>fes_dist</b>: <span class="plumedtooltip" style="color:green">CONVERT_TO_FES<span class="right">Convert a histogram to a free energy surface. <a href="https://www.plumed.org/doc-master/user-doc/html/CONVERT_TO_FES" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">You should use ARG instead of this keyword which was used in older versions of PLUMED and is provided for back compatibility only<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_9.dathg_dist">hg_dist</b> <span class="plumedtooltip">TEMP<span class="right">the temperature at which you are operating<i></i></span></span>=300 <span class="plumedtooltip">MINTOZERO<span class="right"> set the minimum in the free energy to be equal to zero<i></i></span></span>
<span style="display:none;" id="data/INSTRUCTIONS.md_working_9.datfes_dist">The CONVERT_TO_FES action with label <b>fes_dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">fes_dist.value</td><td>the free energy surface</td></tr></table></span><span class="plumedtooltip" style="color:green">DUMPGRID<span class="right">Output the function on the grid to a file with the PLUMED grid format. <a href="https://www.plumed.org/doc-master/user-doc/html/DUMPGRID" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">the grid you would like to print (can also use ARG for specifying what is being printed)<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_9.datfes_dist">fes_dist</b> <span class="plumedtooltip">FILE<span class="right"> the file on which to write the grid<i></i></span></span>=fes-reweight.dist.data <span class="plumedtooltip">FMT<span class="right">the format that should be used to output real numbers<i></i></span></span>=%24.16e
</pre>
 {% endraw %} 

You can run this input by using the PLUMED driver
```
plumed driver --plumed plumed_reweight.dat --noatoms
```

You should compare the resulting FES (the `fes-reweight.dist.data` file)
to the results obtained directly from the bias potential in Exercise 1.

We can also obtain the FES for CVs that are not biased in the VES simulation.
For example, we can obtain the two-dimensional FES for the distance and the
solvation CV given by the coordination number CV. For this, you will need to
add the following to the plumed_reweight.dat file and repeat the PLUMED driver run

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_10.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_10.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_10.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/INSTRUCTIONS.md_working_10.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_10.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/INSTRUCTIONS.md_working_10.dat_hiddenpart1_long" style="display:none;"><b name="data/INSTRUCTIONS.md_working_10.datdist" onclick='showPath("data/INSTRUCTIONS.md_working_10.dat","data/INSTRUCTIONS.md_working_10.datdist","data/INSTRUCTIONS.md_working_10.datdist","brown")'>dist</b>:   <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=colvar_reweight.data <span class="plumedtooltip">IGNORE_TIME<span class="right"> ignore the time in the colvar file<i></i></span></span> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=dist
<span style="display:none;" id="data/INSTRUCTIONS.md_working_10.datdist">The READ action with label <b>dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_10.datcoord" onclick='showPath("data/INSTRUCTIONS.md_working_10.dat","data/INSTRUCTIONS.md_working_10.datcoord","data/INSTRUCTIONS.md_working_10.datcoord","brown")'>coord</b>:  <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=colvar_reweight.data <span class="plumedtooltip">IGNORE_TIME<span class="right"> ignore the time in the colvar file<i></i></span></span> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=coord
<span style="display:none;" id="data/INSTRUCTIONS.md_working_10.datcoord">The READ action with label <b>coord</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">coord..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_10.datves" onclick='showPath("data/INSTRUCTIONS.md_working_10.dat","data/INSTRUCTIONS.md_working_10.datves","data/INSTRUCTIONS.md_working_10.datves","brown")'>ves</b>:    <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=colvar_reweight.data <span class="plumedtooltip">IGNORE_TIME<span class="right"> ignore the time in the colvar file<i></i></span></span> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=ves.bias

<span style="display:none;" id="data/INSTRUCTIONS.md_working_10.datves">The READ action with label <b>ves</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">ves..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_10.datweights" onclick='showPath("data/INSTRUCTIONS.md_working_10.dat","data/INSTRUCTIONS.md_working_10.datweights","data/INSTRUCTIONS.md_working_10.datweights","brown")'>weights</b>: <span class="plumedtooltip" style="color:green">REWEIGHT_BIAS<span class="right">Calculate weights for ensemble averages that negate the effect the bias has on the region of phase space explored <a href="https://www.plumed.org/doc-master/user-doc/html/REWEIGHT_BIAS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">TEMP<span class="right">the system temperature<i></i></span></span>=300 <span class="plumedtooltip">ARG<span class="right"> the biases that must be taken into account when reweighting<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_10.datves">ves.bias</b>
<a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_10.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span style="display:none;" id="data/INSTRUCTIONS.md_working_10.datweights">The REWEIGHT_BIAS action with label <b>weights</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">weights.value</td><td>the weight to use for this frame to negate the effect the bias</td></tr></table></span><span class="plumedtooltip" style="color:green">HISTOGRAM<span class="right">Accumulate the average probability density along a few CVs from a trajectory. <a href="https://www.plumed.org/doc-master/user-doc/html/HISTOGRAM" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">ARG<span class="right">the quantities that are being used to construct the histogram<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_10.datdist">dist</b>,<b name="data/INSTRUCTIONS.md_working_10.datcoord">coord</b>
  <span class="plumedtooltip">GRID_MIN<span class="right"> the lower bounds for the grid<i></i></span></span>=0.2,2.5
  <span class="plumedtooltip">GRID_MAX<span class="right"> the upper bounds for the grid<i></i></span></span>=0.7,7.5
  <span class="plumedtooltip">GRID_BIN<span class="right">the number of bins for the grid<i></i></span></span>=200,200
  <span class="plumedtooltip">BANDWIDTH<span class="right">the bandwidths for kernel density esimtation<i></i></span></span>=0.004,0.04
  <span class="plumedtooltip">LOGWEIGHTS<span class="right">the logarithm of the quantity to use as the weights when calculating averages<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_10.datweights">weights</b>
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_10.dathg_dist_coord" onclick='showPath("data/INSTRUCTIONS.md_working_10.dat","data/INSTRUCTIONS.md_working_10.dathg_dist_coord","data/INSTRUCTIONS.md_working_10.dathg_dist_coord","brown")'>hg_dist_coord</b>
... HISTOGRAM
<span style="display:none;" id="data/INSTRUCTIONS.md_working_10.dathg_dist_coord">The HISTOGRAM action with label <b>hg_dist_coord</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">hg_dist_coord.value</td><td>the estimate of the histogram as a function of the argument that was obtained</td></tr></table></span><b name="data/INSTRUCTIONS.md_working_10.datfes_dist_coord" onclick='showPath("data/INSTRUCTIONS.md_working_10.dat","data/INSTRUCTIONS.md_working_10.datfes_dist_coord","data/INSTRUCTIONS.md_working_10.datfes_dist_coord","brown")'>fes_dist_coord</b>: <span class="plumedtooltip" style="color:green">CONVERT_TO_FES<span class="right">Convert a histogram to a free energy surface. <a href="https://www.plumed.org/doc-master/user-doc/html/CONVERT_TO_FES" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">You should use ARG instead of this keyword which was used in older versions of PLUMED and is provided for back compatibility only<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_10.dathg_dist_coord">hg_dist_coord</b> <span class="plumedtooltip">TEMP<span class="right">the temperature at which you are operating<i></i></span></span>=300 <span class="plumedtooltip">MINTOZERO<span class="right"> set the minimum in the free energy to be equal to zero<i></i></span></span>
<span style="display:none;" id="data/INSTRUCTIONS.md_working_10.datfes_dist_coord">The CONVERT_TO_FES action with label <b>fes_dist_coord</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">fes_dist_coord.value</td><td>the free energy surface</td></tr></table></span><span class="plumedtooltip" style="color:green">DUMPGRID<span class="right">Output the function on the grid to a file with the PLUMED grid format. <a href="https://www.plumed.org/doc-master/user-doc/html/DUMPGRID" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">the grid you would like to print (can also use ARG for specifying what is being printed)<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_10.datfes_dist_coord">fes_dist_coord</b> <span class="plumedtooltip">FILE<span class="right"> the file on which to write the grid<i></i></span></span>=fes-reweight.dist-coord.data <span class="plumedtooltip">FMT<span class="right">the format that should be used to output real numbers<i></i></span></span>=%24.16e
</pre>
 {% endraw %} 
Note that here we use kernel density estimation with Gaussian kernels to
obtain smoother results.

You can also try to obtain the one-dimensional FES for the solvation CV by adjusting
the input above.

This will generate a two-dimensional FES that you can visualize.

## Exercise 3: Running Another Independent Simulation

To check the results, it is a good practice to run another independent simulation
using different initial conditions. You can achieve this here by changing the initial
geometry in the `generate-tpr-file.sh` script
```
StartingGeometry=NaCl_StartingStructure-2.gro
```
and regenerating the GROMACS tpr file. Do this and rerun the simulation,
check the convergence, and perform reweighting
as before. Make sure that you do this in a new clean folder that is separate from the run
in Exercise 1.

## Exercise 4: Biasing with Two Collective Variables

We will now bias also the solvation CV. To achieve this, we need first to setup
a separate basis set for the solvation CV, where again we use the symlets but
with a different range from 2.0 to 8.0
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_11.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_11.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_11.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/INSTRUCTIONS.md_working_11.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_11.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/INSTRUCTIONS.md_working_11.dat_hiddenpart1_long" style="display:none;"><span style="color:blue" class="comment"># Distance between Na and Cl atoms</span>
<b name="data/INSTRUCTIONS.md_working_11.datdist" onclick='showPath("data/INSTRUCTIONS.md_working_11.dat","data/INSTRUCTIONS.md_working_11.datdist","data/INSTRUCTIONS.md_working_11.datdist","black")'>dist</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_11.datdist">The DISTANCE action with label <b>dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist</td><td width="5%"><font color="black">scalar</font></td><td>the DISTANCE between this pair of atoms</td></tr></table></span>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=322,323

<span style="color:blue" class="comment"># Solvation of Na atom</span>
<span class="plumedtooltip" style="color:green">COORDINATION<span class="right">Calculate coordination numbers. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATION" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_11.datcoord" onclick='showPath("data/INSTRUCTIONS.md_working_11.dat","data/INSTRUCTIONS.md_working_11.datcoord","data/INSTRUCTIONS.md_working_11.datcoord","black")'>coord</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_11.datcoord">The COORDINATION action with label <b>coord</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">coord</td><td width="5%"><font color="black">scalar</font></td><td>the value of the coordination</td></tr></table></span>
  <span class="plumedtooltip">GROUPA<span class="right">First list of atoms<i></i></span></span>=322
  <span class="plumedtooltip">GROUPB<span class="right">Second list of atoms (if empty, N*(N-1)/2 pairs in GROUPA are counted)<i></i></span></span>=1-321:3
  <span class="plumedtooltip">SWITCH<span class="right">This keyword is used if you want to employ an alternative to the continuous switching function defined above. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=0.315 D_MAX=0.5 NN=12 MM=24}
  <span class="plumedtooltip">NLIST<span class="right"> Use a neighbor list to speed up the calculation<i></i></span></span>
  <span class="plumedtooltip">NL_CUTOFF<span class="right">The cutoff for the neighbor list<i></i></span></span>=0.55
  <span class="plumedtooltip">NL_STRIDE<span class="right">The frequency with which we are updating the atoms in the neighbor list<i></i></span></span>=10
... COORDINATION
<br/><span style="color:blue" class="comment"># Basisset for Na-Cl distance</span>
<span class="plumedtooltip" style="color:green">BF_WAVELETS<span class="right">Daubechies Wavelets basis functions. <a href="https://www.plumed.org/doc-master/user-doc/html/BF_WAVELETS" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_11.datbf1" onclick='showPath("data/INSTRUCTIONS.md_working_11.dat","data/INSTRUCTIONS.md_working_11.datbf1","data/INSTRUCTIONS.md_working_11.datbf1","brown")'>bf1</b>
  <span class="plumedtooltip">TYPE<span class="right">Specify the wavelet type<i></i></span></span>=SYMLETS
  <span class="plumedtooltip">ORDER<span class="right">The order of the basis function expansion<i></i></span></span>=10
  <span class="plumedtooltip">NUM_BF<span class="right">The number of basis functions that should be used<i></i></span></span>=26
  <span class="plumedtooltip">MINIMUM<span class="right">The minimum of the interval on which the basis functions are defined<i></i></span></span>=0.2
  <span class="plumedtooltip">MAXIMUM<span class="right">The maximum of the interval on which the basis functions are defined<i></i></span></span>=0.7
  <span class="plumedtooltip">TAILS_THRESHOLD<span class="right">The threshold for cutting off tail wavelets as a fraction of the maximum value<i></i></span></span>=0.01
... BF_WAVELETS
<a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_11.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span style="color:blue" class="comment"># Basisset for coordination number</span>
<span style="display:none;" id="data/INSTRUCTIONS.md_working_11.datbf1">The BF_WAVELETS action with label <b>bf1</b> calculates something</span><span class="plumedtooltip" style="color:green">BF_WAVELETS<span class="right">Daubechies Wavelets basis functions. <a href="https://www.plumed.org/doc-master/user-doc/html/BF_WAVELETS" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_11.datbf2" onclick='showPath("data/INSTRUCTIONS.md_working_11.dat","data/INSTRUCTIONS.md_working_11.datbf2","data/INSTRUCTIONS.md_working_11.datbf2","brown")'>bf2</b>
  <span class="plumedtooltip">TYPE<span class="right">Specify the wavelet type<i></i></span></span>=SYMLETS
  <span class="plumedtooltip">ORDER<span class="right">The order of the basis function expansion<i></i></span></span>=10
  <span class="plumedtooltip">NUM_BF<span class="right">The number of basis functions that should be used<i></i></span></span>=22
  <span class="plumedtooltip">MINIMUM<span class="right">The minimum of the interval on which the basis functions are defined<i></i></span></span>=2.5
  <span class="plumedtooltip">MAXIMUM<span class="right">The maximum of the interval on which the basis functions are defined<i></i></span></span>=7.5
  <span class="plumedtooltip">TAILS_THRESHOLD<span class="right">The threshold for cutting off tail wavelets as a fraction of the maximum value<i></i></span></span>=0.01
... BF_WAVELETS
<span style="display:none;" id="data/INSTRUCTIONS.md_working_11.datbf2">The BF_WAVELETS action with label <b>bf2</b> calculates something</span></pre>
 {% endraw %} 

We also need to change the relevant keywords in the `VES_LINEAR_EXPANSION` action,
namely the `ARG`, `BASIS_FUNCTIONS`, and `GRID_BINS` keywords
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_12.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_12.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_12.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/INSTRUCTIONS.md_working_12.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_12.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/INSTRUCTIONS.md_working_12.dat_hiddenpart1_long" style="display:none;"><span style="color:blue" class="comment"># Distance between Na and Cl atoms</span>
<b name="data/INSTRUCTIONS.md_working_12.datdist" onclick='showPath("data/INSTRUCTIONS.md_working_12.dat","data/INSTRUCTIONS.md_working_12.datdist","data/INSTRUCTIONS.md_working_12.datdist","black")'>dist</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_12.datdist">The DISTANCE action with label <b>dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist</td><td width="5%"><font color="black">scalar</font></td><td>the DISTANCE between this pair of atoms</td></tr></table></span>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=322,323

<span style="color:blue" class="comment"># Solvation of Na atom</span>
<span class="plumedtooltip" style="color:green">COORDINATION<span class="right">Calculate coordination numbers. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATION" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.datcoord" onclick='showPath("data/INSTRUCTIONS.md_working_12.dat","data/INSTRUCTIONS.md_working_12.datcoord","data/INSTRUCTIONS.md_working_12.datcoord","black")'>coord</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_12.datcoord">The COORDINATION action with label <b>coord</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">coord</td><td width="5%"><font color="black">scalar</font></td><td>the value of the coordination</td></tr></table></span>
  <span class="plumedtooltip">GROUPA<span class="right">First list of atoms<i></i></span></span>=322
  <span class="plumedtooltip">GROUPB<span class="right">Second list of atoms (if empty, N*(N-1)/2 pairs in GROUPA are counted)<i></i></span></span>=1-321:3
  <span class="plumedtooltip">SWITCH<span class="right">This keyword is used if you want to employ an alternative to the continuous switching function defined above. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=0.315 D_MAX=0.5 NN=12 MM=24}
  <span class="plumedtooltip">NLIST<span class="right"> Use a neighbor list to speed up the calculation<i></i></span></span>
  <span class="plumedtooltip">NL_CUTOFF<span class="right">The cutoff for the neighbor list<i></i></span></span>=0.55
  <span class="plumedtooltip">NL_STRIDE<span class="right">The frequency with which we are updating the atoms in the neighbor list<i></i></span></span>=10
... COORDINATION
<br/><span style="color:blue" class="comment"># Basisset for Na-Cl distance</span>
<span class="plumedtooltip" style="color:green">BF_WAVELETS<span class="right">Daubechies Wavelets basis functions. <a href="https://www.plumed.org/doc-master/user-doc/html/BF_WAVELETS" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.datbf1" onclick='showPath("data/INSTRUCTIONS.md_working_12.dat","data/INSTRUCTIONS.md_working_12.datbf1","data/INSTRUCTIONS.md_working_12.datbf1","brown")'>bf1</b>
  <span class="plumedtooltip">TYPE<span class="right">Specify the wavelet type<i></i></span></span>=SYMLETS
  <span class="plumedtooltip">ORDER<span class="right">The order of the basis function expansion<i></i></span></span>=10
  <span class="plumedtooltip">NUM_BF<span class="right">The number of basis functions that should be used<i></i></span></span>=26
  <span class="plumedtooltip">MINIMUM<span class="right">The minimum of the interval on which the basis functions are defined<i></i></span></span>=0.2
  <span class="plumedtooltip">MAXIMUM<span class="right">The maximum of the interval on which the basis functions are defined<i></i></span></span>=0.7
  <span class="plumedtooltip">TAILS_THRESHOLD<span class="right">The threshold for cutting off tail wavelets as a fraction of the maximum value<i></i></span></span>=0.01
... BF_WAVELETS
<br/><span style="color:blue" class="comment"># Basisset for coordination number</span>
<span style="display:none;" id="data/INSTRUCTIONS.md_working_12.datbf1">The BF_WAVELETS action with label <b>bf1</b> calculates something</span><span class="plumedtooltip" style="color:green">BF_WAVELETS<span class="right">Daubechies Wavelets basis functions. <a href="https://www.plumed.org/doc-master/user-doc/html/BF_WAVELETS" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.datbf2" onclick='showPath("data/INSTRUCTIONS.md_working_12.dat","data/INSTRUCTIONS.md_working_12.datbf2","data/INSTRUCTIONS.md_working_12.datbf2","brown")'>bf2</b>
  <span class="plumedtooltip">TYPE<span class="right">Specify the wavelet type<i></i></span></span>=SYMLETS
  <span class="plumedtooltip">ORDER<span class="right">The order of the basis function expansion<i></i></span></span>=10
  <span class="plumedtooltip">NUM_BF<span class="right">The number of basis functions that should be used<i></i></span></span>=26
  <span class="plumedtooltip">MINIMUM<span class="right">The minimum of the interval on which the basis functions are defined<i></i></span></span>=2.5
  <span class="plumedtooltip">MAXIMUM<span class="right">The maximum of the interval on which the basis functions are defined<i></i></span></span>=7.5
  <span class="plumedtooltip">TAILS_THRESHOLD<span class="right">The threshold for cutting off tail wavelets as a fraction of the maximum value<i></i></span></span>=0.01
... BF_WAVELETS

<br/><span style="color:blue" class="comment"># Target distribution</span>
<span style="display:none;" id="data/INSTRUCTIONS.md_working_12.datbf2">The BF_WAVELETS action with label <b>bf2</b> calculates something</span><b name="data/INSTRUCTIONS.md_working_12.dattd" onclick='showPath("data/INSTRUCTIONS.md_working_12.dat","data/INSTRUCTIONS.md_working_12.dattd","data/INSTRUCTIONS.md_working_12.dattd","brown")'>td</b>: <span class="plumedtooltip" style="color:green">TD_WELLTEMPERED<span class="right">Well-tempered target distribution (dynamic). <a href="https://www.plumed.org/doc-master/user-doc/html/TD_WELLTEMPERED" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">BIASFACTOR<span class="right">The bias factor used for the well-tempered distribution<i></i></span></span>=10
<a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_12.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span id="data/INSTRUCTIONS.md_working_12.datdefves_short"><span style="display:none;" id="data/INSTRUCTIONS.md_working_12.dattd">The TD_WELLTEMPERED action with label <b>td</b> calculates something</span><span class="plumedtooltip" style="color:green">VES_LINEAR_EXPANSION<span class="right">Linear basis set expansion bias. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_12.datdefves");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/VES_LINEAR_EXPANSION">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.datves" onclick='showPath("data/INSTRUCTIONS.md_working_12.dat","data/INSTRUCTIONS.md_working_12.datves","data/INSTRUCTIONS.md_working_12.datves","black")'>ves</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_12.datves">The VES_LINEAR_EXPANSION action with label <b>ves</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">ves.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">ves.force2</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the squared force due to this bias potential.</td></tr></table></span>
  <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.datdist">dist</b>,<b name="data/INSTRUCTIONS.md_working_12.datcoord">coord</b>
  <span class="plumedtooltip">BASIS_FUNCTIONS<span class="right">the label of the one dimensional basis functions that should be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.datbf1">bf1</b>,<b name="data/INSTRUCTIONS.md_working_12.datbf2">bf2</b>
  <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is needed if the MD code does not pass the temperature to PLUMED<i></i></span></span>=300.0
  <span class="plumedtooltip">GRID_BINS<span class="right">the number of bins used for the grid<i></i></span></span>=300,300
  <span class="plumedtooltip">OPTIMIZATION_THRESHOLD<span class="right">Threshold value to turn off optimization of localized basis functions<i></i></span></span>=0.000001
  <span class="plumedtooltip">TARGET_DISTRIBUTION<span class="right">the label of the target distribution to be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.dattd">td</b>
  <span class="plumedtooltip">PROJ_ARG1<span class="right">arguments for doing projections of the FES or the target distribution<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.datdist">dist</b>
  <span class="plumedtooltip">PROJ_ARG2<span class="right">arguments for doing projections of the FES or the target distribution<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.datcoord">coord</b>
... VES_LINEAR_EXPANSION
</span><span id="data/INSTRUCTIONS.md_working_12.datdefves_long" style="display:none;"><span class="plumedtooltip" style="color:green">VES_LINEAR_EXPANSION<span class="right">Linear basis set expansion bias. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_12.datdefves");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/VES_LINEAR_EXPANSION">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.datves" onclick='showPath("data/INSTRUCTIONS.md_working_12.dat","data/INSTRUCTIONS.md_working_12.datves","data/INSTRUCTIONS.md_working_12.datves","black")'>ves</b>
  <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.datdist">dist</b>,<b name="data/INSTRUCTIONS.md_working_12.datcoord">coord</b>
  <span class="plumedtooltip">BASIS_FUNCTIONS<span class="right">the label of the one dimensional basis functions that should be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.datbf1">bf1</b>,<b name="data/INSTRUCTIONS.md_working_12.datbf2">bf2</b>
  <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is needed if the MD code does not pass the temperature to PLUMED<i></i></span></span>=300.0
  <span class="plumedtooltip">GRID_BINS<span class="right">the number of bins used for the grid<i></i></span></span>=300,300
  <span class="plumedtooltip">OPTIMIZATION_THRESHOLD<span class="right">Threshold value to turn off optimization of localized basis functions<i></i></span></span>=0.000001
  <span class="plumedtooltip">TARGET_DISTRIBUTION<span class="right">the label of the target distribution to be used<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.dattd">td</b>
  <span class="plumedtooltip">PROJ_ARG1<span class="right">arguments for doing projections of the FES or the target distribution<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.datdist">dist</b>
  <span class="plumedtooltip">PROJ_ARG2<span class="right">arguments for doing projections of the FES or the target distribution<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_12.datcoord">coord</b>
 <span class="plumedtooltip">GRID_FMT<span class="right"> the format to use when outputting the numbers in the grids<i></i></span></span>=%14.9f
... VES_LINEAR_EXPANSION
</span></pre>
 {% endraw %} 
Additionally, we have turned on the calculation of the one-dimensional projection
of the FES on the two CVs (we also need to set the keyword
`FES_PROJ_OUTPUT=100` in `OPT_AVERAGED_SGD`). This is useful to assess the
convergence as this is
easier in one-dimension. We can also compare the projection to the results from
Exercise 1. These changes should be sufficient to do the simulations using two CVs.
You can see full input file in the `Exercise-4` folder.

Once you have performed this simulation, you should also try to reweight from
this simulations. Furthermore, if you have time, you should also try to perform
another independent simulation.

## Optional Exercises

The following three exercises are optional, but they will show you how different
parameters effect the results. You should base these exercises on the files from
the Exercise-1 folder and make the necessary changes. Make sure that you run these
simulations in separate folders and start from clean files from the Exercise-1 folder.

### Optional Exercise 5: Play with the Optimization Parameters

The main parameter in the optimization algorithm is the step size and
it is not always easy to choose this parameter. Luckily, the algorithm
is quite robust and will work for different step sizes.

Run different simulations using step sizes 0.5 and 50.0
and try to rationalize the behavior. Normally, when the step size is too large, the
system gets stuck in CV space and coefficients oscillate wildly. When the step size is
too small, the algorithm runs out of "steam" too fast and the simulation converges slowly.
These two extreme cases should be avoided.

### Optional Exercise 6: Uniform Target Distribution
Perform a simulation using an uniform target distribution and see how this changes
the results.

In this case, you need to change the target distribution to
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_13.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_13.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_13.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/INSTRUCTIONS.md_working_13.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_13.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/INSTRUCTIONS.md_working_13.dat_hiddenpart1_long" style="display:none;"><span style="color:blue" class="comment"># Distance between Na and Cl atoms</span>
<b name="data/INSTRUCTIONS.md_working_13.datdist" onclick='showPath("data/INSTRUCTIONS.md_working_13.dat","data/INSTRUCTIONS.md_working_13.datdist","data/INSTRUCTIONS.md_working_13.datdist","black")'>dist</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_13.datdist">The DISTANCE action with label <b>dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist</td><td width="5%"><font color="black">scalar</font></td><td>the DISTANCE between this pair of atoms</td></tr></table></span>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=322,323

<span style="color:blue" class="comment"># Solvation of Na atom</span>
<span class="plumedtooltip" style="color:green">COORDINATION<span class="right">Calculate coordination numbers. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATION" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_13.datcoord" onclick='showPath("data/INSTRUCTIONS.md_working_13.dat","data/INSTRUCTIONS.md_working_13.datcoord","data/INSTRUCTIONS.md_working_13.datcoord","black")'>coord</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_13.datcoord">The COORDINATION action with label <b>coord</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">coord</td><td width="5%"><font color="black">scalar</font></td><td>the value of the coordination</td></tr></table></span>
  <span class="plumedtooltip">GROUPA<span class="right">First list of atoms<i></i></span></span>=322
  <span class="plumedtooltip">GROUPB<span class="right">Second list of atoms (if empty, N*(N-1)/2 pairs in GROUPA are counted)<i></i></span></span>=1-321:3
  <span class="plumedtooltip">SWITCH<span class="right">This keyword is used if you want to employ an alternative to the continuous switching function defined above. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=0.315 D_MAX=0.5 NN=12 MM=24}
  <span class="plumedtooltip">NLIST<span class="right"> Use a neighbor list to speed up the calculation<i></i></span></span>
  <span class="plumedtooltip">NL_CUTOFF<span class="right">The cutoff for the neighbor list<i></i></span></span>=0.55
  <span class="plumedtooltip">NL_STRIDE<span class="right">The frequency with which we are updating the atoms in the neighbor list<i></i></span></span>=10
... COORDINATION
<br/><span style="color:blue" class="comment"># Basisset for Na-Cl distance</span>
<span class="plumedtooltip" style="color:green">BF_WAVELETS<span class="right">Daubechies Wavelets basis functions. <a href="https://www.plumed.org/doc-master/user-doc/html/BF_WAVELETS" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_13.datbf1" onclick='showPath("data/INSTRUCTIONS.md_working_13.dat","data/INSTRUCTIONS.md_working_13.datbf1","data/INSTRUCTIONS.md_working_13.datbf1","brown")'>bf1</b>
  <span class="plumedtooltip">TYPE<span class="right">Specify the wavelet type<i></i></span></span>=SYMLETS
  <span class="plumedtooltip">ORDER<span class="right">The order of the basis function expansion<i></i></span></span>=10
  <span class="plumedtooltip">NUM_BF<span class="right">The number of basis functions that should be used<i></i></span></span>=26
  <span class="plumedtooltip">MINIMUM<span class="right">The minimum of the interval on which the basis functions are defined<i></i></span></span>=0.2
  <span class="plumedtooltip">MAXIMUM<span class="right">The maximum of the interval on which the basis functions are defined<i></i></span></span>=0.7
  <span class="plumedtooltip">TAILS_THRESHOLD<span class="right">The threshold for cutting off tail wavelets as a fraction of the maximum value<i></i></span></span>=0.01
... BF_WAVELETS
<a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_13.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span style="color:blue" class="comment"># Target distribution</span>
<span style="display:none;" id="data/INSTRUCTIONS.md_working_13.datbf1">The BF_WAVELETS action with label <b>bf1</b> calculates something</span><b name="data/INSTRUCTIONS.md_working_13.dattd" onclick='showPath("data/INSTRUCTIONS.md_working_13.dat","data/INSTRUCTIONS.md_working_13.dattd","data/INSTRUCTIONS.md_working_13.dattd","brown")'>td</b>: <span class="plumedtooltip" style="color:green">TD_UNIFORM<span class="right">Uniform target distribution (static). <a href="https://www.plumed.org/doc-master/user-doc/html/TD_UNIFORM" style="color:green">More details</a><i></i></span></span>
<span style="display:none;" id="data/INSTRUCTIONS.md_working_13.dattd">The TD_UNIFORM action with label <b>td</b> calculates something</span></pre>
 {% endraw %} 
and remove the `TARGETDIST_STRIDE` and `TARGETDIST_OUTPUT` keywords from the \ref OPT_AVERAGED_SGD
action.

### Legendre polynomials basis function 
Perform a simulation using Legendre polynomials (`BF_LEGENDRE`) basis functions instead of the
wavelets and see how this will affect the result. As the Legendre polynomials are delocalized
basis functions, this should lead to more fluctuations in the bias potential as has been observed
in the [paper introducing the wavelets](https://doi.org/10.1021/acs.jctc.2c00197).

In this case, you need to change the basis set action in the PLUMED input to
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/INSTRUCTIONS.md_working_14.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_14.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="INSTRUCTIONS.md_working_14.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
</div>
</div>
<pre class="plumedlisting">
<span id="data/INSTRUCTIONS.md_working_14.dat_hiddenpart1_short"><a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_14.dat_hiddenpart1")'># --- Click here to reveal hidden parts of input file ---- 
</a></span><span id="data/INSTRUCTIONS.md_working_14.dat_hiddenpart1_long" style="display:none;"><span style="color:blue" class="comment"># Distance between Na and Cl atoms</span>
<b name="data/INSTRUCTIONS.md_working_14.datdist" onclick='showPath("data/INSTRUCTIONS.md_working_14.dat","data/INSTRUCTIONS.md_working_14.datdist","data/INSTRUCTIONS.md_working_14.datdist","black")'>dist</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_14.datdist">The DISTANCE action with label <b>dist</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dist</td><td width="5%"><font color="black">scalar</font></td><td>the DISTANCE between this pair of atoms</td></tr></table></span>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=322,323

<span style="color:blue" class="comment"># Solvation of Na atom</span>
<span class="plumedtooltip" style="color:green">COORDINATION<span class="right">Calculate coordination numbers. <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATION" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_14.datcoord" onclick='showPath("data/INSTRUCTIONS.md_working_14.dat","data/INSTRUCTIONS.md_working_14.datcoord","data/INSTRUCTIONS.md_working_14.datcoord","black")'>coord</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_14.datcoord">The COORDINATION action with label <b>coord</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">coord</td><td width="5%"><font color="black">scalar</font></td><td>the value of the coordination</td></tr></table></span>
  <span class="plumedtooltip">GROUPA<span class="right">First list of atoms<i></i></span></span>=322
  <span class="plumedtooltip">GROUPB<span class="right">Second list of atoms (if empty, N*(N-1)/2 pairs in GROUPA are counted)<i></i></span></span>=1-321:3
  <span class="plumedtooltip">SWITCH<span class="right">This keyword is used if you want to employ an alternative to the continuous switching function defined above. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=0.315 D_MAX=0.5 NN=12 MM=24}
  <span class="plumedtooltip">NLIST<span class="right"> Use a neighbor list to speed up the calculation<i></i></span></span>
  <span class="plumedtooltip">NL_CUTOFF<span class="right">The cutoff for the neighbor list<i></i></span></span>=0.55
  <span class="plumedtooltip">NL_STRIDE<span class="right">The frequency with which we are updating the atoms in the neighbor list<i></i></span></span>=10
... COORDINATION
<a class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_14.dat_hiddenpart1")'># --- Click here to hide input --- 
</a></span><span style="color:blue" class="comment"># Basisset for Na-Cl distance</span>
<span class="plumedtooltip" style="color:green">BF_LEGENDRE<span class="right">Legendre polynomials basis functions. <a href="https://www.plumed.org/doc-master/user-doc/html/BF_LEGENDRE" style="color:green">More details</a><i></i></span></span> ...
  <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/INSTRUCTIONS.md_working_14.datbf1" onclick='showPath("data/INSTRUCTIONS.md_working_14.dat","data/INSTRUCTIONS.md_working_14.datbf1","data/INSTRUCTIONS.md_working_14.datbf1","brown")'>bf1</b>
  <span class="plumedtooltip">ORDER<span class="right">The order of the basis function expansion<i></i></span></span>=20
  <span class="plumedtooltip">MINIMUM<span class="right">The minimum of the interval on which the basis functions are defined<i></i></span></span>=0.2
  <span class="plumedtooltip">MAXIMUM<span class="right">The maximum of the interval on which the basis functions are defined<i></i></span></span>=0.7
... BF_LEGENDRE
<span style="display:none;" id="data/INSTRUCTIONS.md_working_14.datbf1">The BF_LEGENDRE action with label <b>bf1</b> calculates something</span></pre>
 {% endraw %} 

## Additional comments

This should cover the basics of running VES simulations in PLUMED, but the following
comments might be of interest to some.

### Restarting
VES simulations can be easily restarted. The code will automatically output
all the file needed at the end of the simulation. To restart, you just need to
reset the simulation with your MD code in the traditional way and add a `RESET`
keyword to the top of the PLUMED input (for some codes like GROMACS, a restart is
automatically detected by PLUMED and thus this keyword is not needed).

### Multiple Walkers

VES simulations supports the usage of multiple walkers where different copies of the system share the same bias potential (i.e. coefficients) and cooperatively sample the averages needed for the gradient and Hessian. This can significantly help with convergence in difficult cases. It is of course best to start the different copies from different positions in CV space. To activate this option you just need to add the `MULTIPLE_WALKERS` keyword to the `OPT_AVERAGED_SGD` action. Note that this is only supported if the MD code support running multiple replicas connected via MPI (e.g., GROMACS or LAMMPS).


