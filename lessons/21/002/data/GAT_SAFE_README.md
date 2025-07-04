# PLUMED Masterclass 21.2: Statistical errors in MD

## Aims

In this Masterclass, we will discuss how to report the results from molecular simulations.  
We will emphasize that any result that we get from any simulation is a random variable.
To make the result reproducible, we must characterize the distribution
that has been sampled.  It is not sufficient to report the averages.

## Objectives

Once you have completed this Masterclass you will be able to:

- Use PLUMED to calculate time averages and histograms from biased and unbiased simulation data.
- Use PLUMED to perform block averaging.
- Calculate error bars on-time averages computed form biased and unbiased simulation data using the central limit theorem and non-parametric bootstrap.
 
## Setting up PLUMED

If you have not yet set up PLUMED, you can find information about installing it [here](https://www.plumed.org/doc-v2.8/user-doc/html/masterclass-21-1.html). Please ensure that you have setup PLUMED on your machine before starting the exercises.

## Resources

The data needed to execute the exercises of this Masterclass can be found on [GitHub](https://github.com/plumed/masterclass-21-2).
You can clone this repository locally on your machine using the following command:

````
git clone https://github.com/plumed/masterclass-21-2.git
````

The data you need is in the folder called `data`.  You will find the following files in that folder:

- `uncorrelated_data`: you will analyze this data set in the first six exercises that follow
- `correlated_data`: you will analyze this data set in exercise 7
- `weighted_data`: you will analyze this data in exercise 8

In exercise 9, you will pull everything together by generating a metadynamics trajectory.  This exercise draws together all the ideas from exercises 1-8 by getting you to run a metadynamics simulation and extract the free energy surface.  In the `data` folder, you will thus also find the following files, which 
are the input for the metadynamics simulation:

- in: The input file for simplemd that contains the parameters for the MD simulation.
- input.xyz: An initial configuration for the cluster that we are studying in this tutorial. 

Notice that PLUMED input files have not been provided in the GitHub repository.  You must prepare these input files yourself using the templates below.

We would recommend that you run each exercise in separate sub-directories inside the root directory `masterclass-21-2`.

## Background

In other lessons you have seen how PLUMED can be used to calculate the value of a collective variables, $s(\mathbf{x})$,
from the positions of the atoms, $\mathbf{x}$.  You should also have seen that doing so allows you to describe the conformational 
changes or chemical reactions that have occured during your molecular dynamics trajectory.  We will build on this idea in this tutorial
by recalling that the values for collective variable we calculate for the frames of a constant-temperature molecular dynamics trajectory 
are samples from the probability distribution for [the canonical (NVT) ensemble](https://www.notion.so/The-canonical-NVT-ensemble-112c3f99f215472cae55d5f6c36f4599):

$$
P(s') = \frac{ \int \textrm{d}x \textrm{d}p \delta( s(x) - s') e^{-\frac{H(x,p)}{k_B T}} }{ \int \textrm{d}x\textrm{d}p e^{-\frac{H(x,p)}{k_B T}} }
$$

where $k_B$ is Boltzmann's constant, $T$ is the temperature $H(x,p)$ is the Hamiltonian and $\delta$ is a Dirac delta function.  Notice also that the integrals 
in the numerator and denominator are integrals over all of [phase space](https://www.notion.so/Microstates-phase-space-and-the-principle-of-equal-a-priori-probabilities-9dbd484a47654bff858313634f01d875).  If $N$ is 
the number of atoms in our system we must, therefore, integrate over each of the $3N$ momentum ( $p$ )
and $3N$ position ( $x$ ) coordinates when calculating these integrals.  

It is only possible to calculate the integrals in the quotient above exactly for elementary physical systems.  For more complex systems we thus assume that we 
can extract information on $P(s')$ by sampling from this distribution multiple times (using molecular dynamics or Monte Carlo) and using the tools of [statistics](https://www.notion.so/940bd09c5be343888244beb21ed4a166?v=6bb0bd98d8fc47a081164069121ee396).
Critically, however, any result we get from such simulations is a [random variable](https://www.notion.so/Random-variables-8aad5b4c3453423da3069168228fe890). <b>To make our results [reproducible](https://www.notion.so/Reproducibility-2494dddd51a14d34bddbb40bb32f7ebc) 
we thus need to characterize the [distribution](https://www.notion.so/The-cumulative-probability-distribution-function-dc346bc8b4f1440b8d075f8c8d2b0f53) sampled in our simulation.</b>  
Reporting only the average value we get is not sufficient as any [averages we take are random](https://www.notion.so/Sample-mean-583d58d7001343c68a7956a1b9f19f4b). 

<em>Links to background information on statistical mechanics and statistics are provided throughout this tutorial.  You can complete the tutorial without looking at the information at these links.
However, we hope that the information we have provided through these links will prove useful if you want to do a more in-depth study of the topic.</em> 

## Exercises

### Exercise 1: Calculating the average value of a CV 

We will start our study of averaging by estimating the [ensemble](https://www.notion.so/Ensembles-7b8b836f8ce44f9b8830ebb0fd00fea8) average of the CV.  The ensemble average for $s(x)$ is given by:

$$
\langle s \rangle = \frac{ \int \textrm{d}x \textrm{d}p s(x) e^{-\frac{H(x,p)}{k_B T}} }{ \int \textrm{d}x\textrm{d}p e^{-\frac{H(x,p)}{k_B T}} }
$$ 

In statistics, the quantity known as the ensemble average in statistical mechanics is referred to as the [expectation](https://www.notion.so/Expectation-c877d8e2ab444b818fae6c053598e0af) of the random variable's 
[distribution](https://www.notion.so/The-cumulative-probability-distribution-function-dc346bc8b4f1440b8d075f8c8d2b0f53).
The expectation of a random variable is often esimated by taking multiple identical samples from the distribution, $X_i$ and computing a [sample mean](https://www.notion.so/Sample-mean-583d58d7001343c68a7956a1b9f19f4b) as follows:

$$
\overline{X} = \frac{1}{N} \sum_{i=1}^N X_i
$$

We can do the same with the data from our MD trajectory.  We replace the $X_i$ in the equation above with the CV values calculated for each of our trajectory frames.

To calculate averages using PLUMED, you can use the input file below.  This input calculates averages for the data in the `uncorrelated_data` file you downloaded when you collected the GitHub repository.  

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/work/plumed_ex1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="plumed_ex1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="plumed_ex1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
<div class="headerBadge"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/work/plumed_ex1.dat")' onmousedown='toggleDisplay("data/work/plumed_ex1.dat")'/></div>
</div>
</div>
<div id="data/work/plumed_ex1.dat_short">
<pre class="plumedlisting">
<b name="data/work/plumed_ex1.datdata" onclick='showPath("data/work/plumed_ex1.dat","data/work/plumed_ex1.datdata","data/work/plumed_ex1.datdata","brown")'>data</b>: <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=<span style="background-color:yellow">__FILL__</span>
<span style="display:none;" id="data/work/plumed_ex1.datdata">The READ action with label <b>data</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">data..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/work/plumed_ex1.datav" onclick='showPath("data/work/plumed_ex1.dat","data/work/plumed_ex1.datav","data/work/plumed_ex1.datav","brown")'>av</b>: <span class="plumedtooltip" style="color:green">AVERAGE<span class="right">Calculate the ensemble average of a collective variable <a href="https://www.plumed.org/doc-master/user-doc/html/AVERAGE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantity that is being averaged<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1
<span style="display:none;" id="data/work/plumed_ex1.datav">The AVERAGE action with label <b>av</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">av.value</td><td>the value of the average</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/work/plumed_ex1.datav">av</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
</pre></div>
<div style="display:none;" id="data/work/plumed_ex1.dat_long"><pre class="plumedlisting">
<b name="data/work/plumed_ex1.dat_soldata" onclick='showPath("data/work/plumed_ex1.dat","data/work/plumed_ex1.dat_soldata","data/work/plumed_ex1.dat_soldata","brown")'>data</b>: <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=../data/uncorrelated_data <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=rand
<span style="display:none;" id="data/work/plumed_ex1.dat_soldata">The READ action with label <b>data</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">data..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/work/plumed_ex1.dat_solav" onclick='showPath("data/work/plumed_ex1.dat","data/work/plumed_ex1.dat_solav","data/work/plumed_ex1.dat_solav","brown")'>av</b>: <span class="plumedtooltip" style="color:green">AVERAGE<span class="right">Calculate the ensemble average of a collective variable <a href="https://www.plumed.org/doc-master/user-doc/html/AVERAGE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantity that is being averaged<i></i></span></span>=<b name="data/work/plumed_ex1.dat_soldata">data</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1
<span style="display:none;" id="data/work/plumed_ex1.dat_solav">The AVERAGE action with label <b>av</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">av.value</td><td>the value of the average</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/work/plumed_ex1.dat_solav">av</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
</pre></div>

 {% endraw %} 

<b>Copy the input to a file called plumed.dat, fill in the blanks and  run the calculation by executing the following command:</b>

````
> plumed driver --noatoms
````

The `colvar` file that is output by PLUMED contains the average computed value from progressively larger and larger numbers of CV values.  You should thus 
be able to use the data in `colvar` to produce a graph that shows the average as a function of the number of variables it is computed from as shown below.

![Average CV as a function of the number of variables it is computed from](figures/masterclass-21-2-average.png) 

The fluctuations in the average get smaller as this quantity is computed from larger numbers of random variables.  We say that the average thus converges to the ensemble average, which is zero for the graph above. 

### Exercise 2: Calculating the free energy

We can estimate the distribution for our CV, $P(s')$, by calculating [a histogram](https://www.notion.so/Histogram-2d2527795f0140008b318d3bc958ee4c).  The histogram we obtain is a 
sample from [a multinomial distribution](https://www.notion.so/Multinomial-distribution-f378b34a38564f6999e184cd2df53f5c) so we can estimate parameters for the multinomial by using 
[likelihood maximisation](https://www.notion.so/Maximum-likelihood-e74a16b691284896bb2bbd5cff502f6d).  Once we have the marginal 
distribution, $P(s')$ we can then calculate the [free energy](https://www.notion.so/Thermodynamic-potentials-dd0dcbab15cd437b91e803ac7fbd1bf8), $F(s')$ as a function of $s(x)$ as $F(s')$ is related to $P(s')$ by:

$$
F(s') = - k_B T \ln P(s')
$$

If we estimate $P(s')$ using likelihood maximisation we can thus get an estimate of the free energy surface.  To estimate the free energy surface 
for the data in `uncorrelated_data` using PLUMED in this way we can use the input file:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/work/plumed_ex2.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="plumed_ex2.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="plumed_ex2.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
<div class="headerBadge"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/work/plumed_ex2.dat")' onmousedown='toggleDisplay("data/work/plumed_ex2.dat")'/></div>
</div>
</div>
<div id="data/work/plumed_ex2.dat_short">
<pre class="plumedlisting">
<span style="color:blue" class="comment"># We use natural units here so that kBT is set to 1</span>
<span class="plumedtooltip" style="color:green">UNITS<span class="right">This command sets the internal units for the code. <a href="https://www.plumed.org/doc-master/user-doc/html/UNITS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NATURAL<span class="right"> use natural units<i></i></span></span>
<span style="display:none;" id="data/work/plumed_ex2.dat">The UNITS action with label <b></b> calculates something</span><b name="data/work/plumed_ex2.datdata" onclick='showPath("data/work/plumed_ex2.dat","data/work/plumed_ex2.datdata","data/work/plumed_ex2.datdata","brown")'>data</b>: <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
<span style="display:none;" id="data/work/plumed_ex2.datdata">The READ action with label <b>data</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">data..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/work/plumed_ex2.dathhh" onclick='showPath("data/work/plumed_ex2.dat","data/work/plumed_ex2.dathhh","data/work/plumed_ex2.dathhh","brown")'>hhh</b>: <span class="plumedtooltip" style="color:green">HISTOGRAM<span class="right">Accumulate the average probability density along a few CVs from a trajectory. <a href="https://www.plumed.org/doc-master/user-doc/html/HISTOGRAM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantities that are being used to construct the histogram<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1 <span style="background-color:yellow">__FILL__</span>=-4.5 <span style="background-color:yellow">__FILL__</span>=4.5 <span style="background-color:yellow">__FILL__</span>=100 <span style="background-color:yellow">__FILL__</span>=DISCRETE
<span style="display:none;" id="data/work/plumed_ex2.dathhh">The HISTOGRAM action with label <b>hhh</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">hhh.value</td><td>the estimate of the histogram as a function of the argument that was obtained</td></tr></table></span><b name="data/work/plumed_ex2.datfes" onclick='showPath("data/work/plumed_ex2.dat","data/work/plumed_ex2.datfes","data/work/plumed_ex2.datfes","brown")'>fes</b>: <span class="plumedtooltip" style="color:green">CONVERT_TO_FES<span class="right">Convert a histogram to a free energy surface. <a href="https://www.plumed.org/doc-master/user-doc/html/CONVERT_TO_FES" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">You should use ARG instead of this keyword which was used in older versions of PLUMED and is provided for back compatibility only<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">TEMP<span class="right">the temperature at which you are operating<i></i></span></span>=1  <span style="color:blue" class="comment"># This sets k_B T = 1 </span>
<span style="display:none;" id="data/work/plumed_ex2.datfes">The CONVERT_TO_FES action with label <b>fes</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">fes.value</td><td>the free energy surface</td></tr></table></span><span class="plumedtooltip" style="color:green">DUMPGRID<span class="right">Output the function on the grid to a file with the PLUMED grid format. <a href="https://www.plumed.org/doc-master/user-doc/html/DUMPGRID" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">the grid you would like to print (can also use ARG for specifying what is being printed)<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">FILE<span class="right"> the file on which to write the grid<i></i></span></span>=<b name="data/work/plumed_ex2.datfes">fes.dat</b>
</pre></div>
<div style="display:none;" id="data/work/plumed_ex2.dat_long"><pre class="plumedlisting">
<span style="color:blue" class="comment"># We use natural units here so that kBT is set to 1</span>
<span class="plumedtooltip" style="color:green">UNITS<span class="right">This command sets the internal units for the code. <a href="https://www.plumed.org/doc-master/user-doc/html/UNITS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NATURAL<span class="right"> use natural units<i></i></span></span>
<span style="display:none;" id="data/work/plumed_ex2.dat_sol">The UNITS action with label <b></b> calculates something</span><b name="data/work/plumed_ex2.dat_soldata" onclick='showPath("data/work/plumed_ex2.dat","data/work/plumed_ex2.dat_soldata","data/work/plumed_ex2.dat_soldata","brown")'>data</b>: <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=<b name="data/work/plumed_ex2.dat_sol">../data/uncorrelated_data</b> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=rand
<span style="display:none;" id="data/work/plumed_ex2.dat_soldata">The READ action with label <b>data</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">data..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/work/plumed_ex2.dat_solhhh" onclick='showPath("data/work/plumed_ex2.dat","data/work/plumed_ex2.dat_solhhh","data/work/plumed_ex2.dat_solhhh","brown")'>hhh</b>: <span class="plumedtooltip" style="color:green">HISTOGRAM<span class="right">Accumulate the average probability density along a few CVs from a trajectory. <a href="https://www.plumed.org/doc-master/user-doc/html/HISTOGRAM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantities that are being used to construct the histogram<i></i></span></span>=<b name="data/work/plumed_ex2.dat_soldata">data</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1 <span class="plumedtooltip">GRID_MIN<span class="right"> the lower bounds for the grid<i></i></span></span>=-4.5 <span class="plumedtooltip">GRID_MAX<span class="right"> the upper bounds for the grid<i></i></span></span>=4.5 <span class="plumedtooltip">GRID_BIN<span class="right">the number of bins for the grid<i></i></span></span>=100 <span class="plumedtooltip">KERNEL<span class="right"> the kernel function you are using<i></i></span></span>=DISCRETE
<span style="display:none;" id="data/work/plumed_ex2.dat_solhhh">The HISTOGRAM action with label <b>hhh</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">hhh.value</td><td>the estimate of the histogram as a function of the argument that was obtained</td></tr></table></span><b name="data/work/plumed_ex2.dat_solfes" onclick='showPath("data/work/plumed_ex2.dat","data/work/plumed_ex2.dat_solfes","data/work/plumed_ex2.dat_solfes","brown")'>fes</b>: <span class="plumedtooltip" style="color:green">CONVERT_TO_FES<span class="right">Convert a histogram to a free energy surface. <a href="https://www.plumed.org/doc-master/user-doc/html/CONVERT_TO_FES" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">You should use ARG instead of this keyword which was used in older versions of PLUMED and is provided for back compatibility only<i></i></span></span>=<b name="data/work/plumed_ex2.dat_solhhh">hhh</b> <span class="plumedtooltip">TEMP<span class="right">the temperature at which you are operating<i></i></span></span>=1
<span style="display:none;" id="data/work/plumed_ex2.dat_solfes">The CONVERT_TO_FES action with label <b>fes</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">fes.value</td><td>the free energy surface</td></tr></table></span><span class="plumedtooltip" style="color:green">DUMPGRID<span class="right">Output the function on the grid to a file with the PLUMED grid format. <a href="https://www.plumed.org/doc-master/user-doc/html/DUMPGRID" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">the grid you would like to print (can also use ARG for specifying what is being printed)<i></i></span></span>=<b name="data/work/plumed_ex2.dat_solfes">fes</b> <span class="plumedtooltip">FILE<span class="right"> the file on which to write the grid<i></i></span></span>=<b name="data/work/plumed_ex2.dat_solfes">fes.dat</b>
</pre></div>

 {% endraw %} 

<b>Copy this input to a file called plumed.dat, fill in the blanks so that you have a grid that runs from -4 to +4 with 100 bins.  Run the calculation by executing the following command:</b>

````
> plumed driver --noatoms
````

The `--noatoms` flag here is needed since `plumed driver` is commonly used to analize a trajectory of atomic coordinates, but here we are using it to directly analyze a collective variable.

You should see that the free energy curve for this data set looks like this:

![The free energy as a function of the CV for the data in uncorrelated_data](figures/masterclass-21-2-fes1.png)

As you can see, there is a single minimum in this free energy surface.

#### Exercise 3: Calculating the fluctuations for a CV

Physical systems spend the majority of their time fluctuating around minima in the free energy landscape.  Let's suppose that this minima is at $\mu$ and lets 
use the Taylor series to write an expression for the free energy at $s'$ as follows:

$$
F(s) = F(\mu) + F'(\mu)(s-\mu) + \frac{F''(\mu)(s-\mu)^2}{2!} + \dots + \frac{F^{(n)}(\mu)(s-\mu)^n}{n!} + \dots
$$

In this expression $F'(\mu)$, $F''(\mu)$ and $F^{(n)}(\mu)$ are the first, second and nth derivatives of the free energy at $\mu$.  We know there is a minimum at 
$\mu$ so $F'(\mu)=0$.  If we truncate the expansion at second order we can, therefore, write:

$$
F(s) \approx F(\mu) + \frac{F''(\mu)(s-\mu)^2}{2} 
$$ 

We now recall that $F(s) = - k_B T \ln P(s')$ and thus write:

$$
P(s) = \exp\left( -\frac{F(s)}{k_B T} \right) \approx \exp\left( -\frac{F(\mu) + \frac{F''(\mu)(s-\mu)^2}{2} }{k_B T} \right) = \exp\left( -\frac{F(\mu)}{k_B T} \right)\exp\left( - \frac{F''(\mu)(s-\mu)^2}{2k_B T} \right)
$$

The first term in the final product here is a constant that does not depend on $s$, while the second is a Gaussian centered on $\mu$ with $\sigma^2 = \frac{k_B T}{F''(\mu)}$.  
We can assume that the constant term in the product above normalizes the distribution. The derivation above, therefore, suggests that our CV values are all samples from a 
[normal distribution](https://www.notion.so/Normal-random-variable-86cae0d838314a3cb8aead626dc6647e).  We thus no longer need to estimate the histogram to get information on $P(s')$.  If $P(s')$ is 
indeed a normal distribution, it is fully characterized if we have the two parameters 
$\mu$ and $\sigma$.

Statistics tells us that if we have $N$ identical normal random variables, $X_i$ we can estimate [the mean](https://www.notion.so/Sample-mean-583d58d7001343c68a7956a1b9f19f4b) $\mu$
and [the standard deviation](https://www.notion.so/Variance-3688f3132bd64d3fbc2f022d7ee17e88) $\sigma$ using:

$$
\mu = \frac{1}{N} \sum X_i \qquad \qquad \sigma = \sqrt{ \frac{N}{N-1} \left[ \frac{1}{N} \sum_{i=1}^N X_i^2 - \left( \frac{1}{N}\sum_{i=1}^N X_i \right)^2 \right] }
$$

We learned how to estimate $\mu$ using these expressions in exercise 1.  To estimate $\sigma^2$ for the data in `uncorrelated_data` using PLUMED 
and the expression above we can use the following input file:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/work/plumed_ex3.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="plumed_ex3.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="plumed_ex3.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
<div class="headerBadge"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/work/plumed_ex3.dat")' onmousedown='toggleDisplay("data/work/plumed_ex3.dat")'/></div>
</div>
</div>
<div id="data/work/plumed_ex3.dat_short">
<pre class="plumedlisting">
<span class="plumedtooltip" style="color:green">UNITS<span class="right">This command sets the internal units for the code. <a href="https://www.plumed.org/doc-master/user-doc/html/UNITS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NATURAL<span class="right"> use natural units<i></i></span></span>
<span style="display:none;" id="data/work/plumed_ex3.dat">The UNITS action with label <b></b> calculates something</span><b name="data/work/plumed_ex3.datdata" onclick='showPath("data/work/plumed_ex3.dat","data/work/plumed_ex3.datdata","data/work/plumed_ex3.datdata","brown")'>data</b>: <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=<span style="background-color:yellow">__FILL__</span>
<span style="color:blue" class="comment"># This line should calculate the square of the quantity read in from the file above</span>
<span style="display:none;" id="data/work/plumed_ex3.datdata">The READ action with label <b>data</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">data..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/work/plumed_ex3.datd2" onclick='showPath("data/work/plumed_ex3.dat","data/work/plumed_ex3.datd2","data/work/plumed_ex3.datd2","brown")'>d2</b>: <span class="plumedtooltip" style="color:green">CUSTOM<span class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/CUSTOM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">FUNC<span class="right">the function you wish to evaluate<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="color:blue" class="comment"># Calculate the average from the read-in data</span>
<span style="display:none;" id="data/work/plumed_ex3.datd2">The CUSTOM action with label <b>d2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d2.value</td><td>an arbitrary function</td></tr></table></span><b name="data/work/plumed_ex3.datav" onclick='showPath("data/work/plumed_ex3.dat","data/work/plumed_ex3.datav","data/work/plumed_ex3.datav","brown")'>av</b>: <span class="plumedtooltip" style="color:green">AVERAGE<span class="right">Calculate the ensemble average of a collective variable <a href="https://www.plumed.org/doc-master/user-doc/html/AVERAGE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantity that is being averaged<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1
<span style="color:blue" class="comment"># Calculate the average of the squares of the read in data</span>
<span style="display:none;" id="data/work/plumed_ex3.datav">The AVERAGE action with label <b>av</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">av.value</td><td>the value of the average</td></tr></table></span><b name="data/work/plumed_ex3.datav2" onclick='showPath("data/work/plumed_ex3.dat","data/work/plumed_ex3.datav2","data/work/plumed_ex3.datav2","brown")'>av2</b>: <span class="plumedtooltip" style="color:green">AVERAGE<span class="right">Calculate the ensemble average of a collective variable <a href="https://www.plumed.org/doc-master/user-doc/html/AVERAGE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantity that is being averaged<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1
<span style="color:blue" class="comment"># Evaluate the variance using the expression above</span>
<span style="display:none;" id="data/work/plumed_ex3.datav2">The AVERAGE action with label <b>av2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">av2.value</td><td>the value of the average</td></tr></table></span><b name="data/work/plumed_ex3.datvar" onclick='showPath("data/work/plumed_ex3.dat","data/work/plumed_ex3.datvar","data/work/plumed_ex3.datvar","brown")'>var</b>: <span class="plumedtooltip" style="color:green">CUSTOM<span class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/CUSTOM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">FUNC<span class="right">the function you wish to evaluate<i></i></span></span>=y-x*x <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="color:blue" class="comment"># Print the variance</span>
<span style="display:none;" id="data/work/plumed_ex3.datvar">The CUSTOM action with label <b>var</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">var.value</td><td>an arbitrary function</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
</pre></div>
<div style="display:none;" id="data/work/plumed_ex3.dat_long"><pre class="plumedlisting">
<span class="plumedtooltip" style="color:green">UNITS<span class="right">This command sets the internal units for the code. <a href="https://www.plumed.org/doc-master/user-doc/html/UNITS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NATURAL<span class="right"> use natural units<i></i></span></span>
<span style="display:none;" id="data/work/plumed_ex3.dat_sol">The UNITS action with label <b></b> calculates something</span><b name="data/work/plumed_ex3.dat_soldata" onclick='showPath("data/work/plumed_ex3.dat","data/work/plumed_ex3.dat_soldata","data/work/plumed_ex3.dat_soldata","brown")'>data</b>: <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=<b name="data/work/plumed_ex3.dat_sol">../data/uncorrelated_data</b> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=rand
<span style="color:blue" class="comment"># This line should calculate the square of the quantity read in from the file above</span>
<span style="display:none;" id="data/work/plumed_ex3.dat_soldata">The READ action with label <b>data</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">data..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/work/plumed_ex3.dat_sold2" onclick='showPath("data/work/plumed_ex3.dat","data/work/plumed_ex3.dat_sold2","data/work/plumed_ex3.dat_sold2","brown")'>d2</b>: <span class="plumedtooltip" style="color:green">CUSTOM<span class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/CUSTOM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<b name="data/work/plumed_ex3.dat_soldata">data</b> <span class="plumedtooltip">FUNC<span class="right">the function you wish to evaluate<i></i></span></span>=x*x <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="color:blue" class="comment"># Calculate the average from the read-in data</span>
<span style="display:none;" id="data/work/plumed_ex3.dat_sold2">The CUSTOM action with label <b>d2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d2.value</td><td>an arbitrary function</td></tr></table></span><b name="data/work/plumed_ex3.dat_solav" onclick='showPath("data/work/plumed_ex3.dat","data/work/plumed_ex3.dat_solav","data/work/plumed_ex3.dat_solav","brown")'>av</b>: <span class="plumedtooltip" style="color:green">AVERAGE<span class="right">Calculate the ensemble average of a collective variable <a href="https://www.plumed.org/doc-master/user-doc/html/AVERAGE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantity that is being averaged<i></i></span></span>=<b name="data/work/plumed_ex3.dat_soldata">data</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1
<span style="color:blue" class="comment"># Calculate the average of the squares of the read in data</span>
<span style="display:none;" id="data/work/plumed_ex3.dat_solav">The AVERAGE action with label <b>av</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">av.value</td><td>the value of the average</td></tr></table></span><b name="data/work/plumed_ex3.dat_solav2" onclick='showPath("data/work/plumed_ex3.dat","data/work/plumed_ex3.dat_solav2","data/work/plumed_ex3.dat_solav2","brown")'>av2</b>: <span class="plumedtooltip" style="color:green">AVERAGE<span class="right">Calculate the ensemble average of a collective variable <a href="https://www.plumed.org/doc-master/user-doc/html/AVERAGE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantity that is being averaged<i></i></span></span>=<b name="data/work/plumed_ex3.dat_sold2">d2</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1
<span style="color:blue" class="comment"># Evaluate the variance using the expression above</span>
<span style="display:none;" id="data/work/plumed_ex3.dat_solav2">The AVERAGE action with label <b>av2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">av2.value</td><td>the value of the average</td></tr></table></span><b name="data/work/plumed_ex3.dat_solvar" onclick='showPath("data/work/plumed_ex3.dat","data/work/plumed_ex3.dat_solvar","data/work/plumed_ex3.dat_solvar","brown")'>var</b>: <span class="plumedtooltip" style="color:green">CUSTOM<span class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/CUSTOM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<b name="data/work/plumed_ex3.dat_solav">av</b>,<b name="data/work/plumed_ex3.dat_solav2">av2</b> <span class="plumedtooltip">FUNC<span class="right">the function you wish to evaluate<i></i></span></span>=y-x*x <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="color:blue" class="comment"># Print the variance</span>
<span style="display:none;" id="data/work/plumed_ex3.dat_solvar">The CUSTOM action with label <b>var</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">var.value</td><td>an arbitrary function</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/work/plumed_ex3.dat_solvar">var</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
</pre></div>

 {% endraw %} 

*Copy this input to a file called plumed.dat, fill in the blanks and run the calculation by executing the following command:*

````
> plumed driver --noatoms
````
Once you have run this calculation, you should be able to draw a graph showing how the estimate of $\sigma$ changes as a function of the number of CVs used in its calculation.  As you can 
see from the graph below, $\sigma$ quantity behaves similarly to the mean that we studied in exercise 1 

![Estimate of the standard deviation for the CV as a function of the number of samples it is computed from](figures/masterclass-21-2-var.png)

*Truncation the Taylor series of the free energy at second order as we have done in this section is equivalent to assuming that a [Harmonic Oscillator](https://www.notion.so/Harmonic-Oscillator-92855b39d13945dabb73cb831dc1234e) 
can be used to describe the fluctuations along our CV. 
The [partition function](https://www.notion.so/Generalised-partition-function-10ed8ca2b3c943aa82dff2116ae955e5), ensemble average and distribution for such systems can be calculated exactly, and there is no need for simulation. 
Even when the system is not harmonic, calculating the quantity we have called* $\sigma^2$ *in this section is still useful as this quantity is an estimator for the [variance](https://www.notion.so/Variance-3688f3132bd64d3fbc2f022d7ee17e88) 
of the distribution.  For anharmonic systems, there is not a simple 
closed-form expression between the variance* ( $\sigma^2$ ) *and the second derivative of the free energy at* $\mu$ *though.* 

### Exercise 4: Calculating block averages

The following PLUMED input splits the CV values into blocks and calculates [an average](https://www.notion.so/Sample-mean-583d58d7001343c68a7956a1b9f19f4b) from each block of data separately.  We can thus use it to get information on 
[the distribution](https://www.notion.so/The-cumulative-probability-distribution-function-dc346bc8b4f1440b8d075f8c8d2b0f53) that is being 
sampled when we calculate an average from sets of 500 random variables using the ideas discussed in exercise 1.  

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/work/plumed_ex4.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="plumed_ex4.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="plumed_ex4.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
<div class="headerBadge"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/work/plumed_ex4.dat")' onmousedown='toggleDisplay("data/work/plumed_ex4.dat")'/></div>
</div>
</div>
<div id="data/work/plumed_ex4.dat_short">
<pre class="plumedlisting">
<b name="data/work/plumed_ex4.datdata" onclick='showPath("data/work/plumed_ex4.dat","data/work/plumed_ex4.datdata","data/work/plumed_ex4.datdata","brown")'>data</b>: <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
<span style="display:none;" id="data/work/plumed_ex4.datdata">The READ action with label <b>data</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">data..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/work/plumed_ex4.datav" onclick='showPath("data/work/plumed_ex4.dat","data/work/plumed_ex4.datav","data/work/plumed_ex4.datav","brown")'>av</b>: <span class="plumedtooltip" style="color:green">AVERAGE<span class="right">Calculate the ensemble average of a collective variable <a href="https://www.plumed.org/doc-master/user-doc/html/AVERAGE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantity that is being averaged<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1 <span class="plumedtooltip">CLEAR<span class="right"> the frequency with whihc to clear the data that is being averaged<i></i></span></span>=500
<span style="display:none;" id="data/work/plumed_ex4.datav">The AVERAGE action with label <b>av</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">av.value</td><td>the value of the average</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
</pre></div>
<div style="display:none;" id="data/work/plumed_ex4.dat_long"><pre class="plumedlisting">
<b name="data/work/plumed_ex4.dat_soldata" onclick='showPath("data/work/plumed_ex4.dat","data/work/plumed_ex4.dat_soldata","data/work/plumed_ex4.dat_soldata","brown")'>data</b>: <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=../data/uncorrelated_data <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=rand
<span style="display:none;" id="data/work/plumed_ex4.dat_soldata">The READ action with label <b>data</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">data..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/work/plumed_ex4.dat_solav" onclick='showPath("data/work/plumed_ex4.dat","data/work/plumed_ex4.dat_solav","data/work/plumed_ex4.dat_solav","brown")'>av</b>: <span class="plumedtooltip" style="color:green">AVERAGE<span class="right">Calculate the ensemble average of a collective variable <a href="https://www.plumed.org/doc-master/user-doc/html/AVERAGE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantity that is being averaged<i></i></span></span>=<b name="data/work/plumed_ex4.dat_soldata">data</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1 <span class="plumedtooltip">CLEAR<span class="right"> the frequency with whihc to clear the data that is being averaged<i></i></span></span>=500
<span style="display:none;" id="data/work/plumed_ex4.dat_solav">The AVERAGE action with label <b>av</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">av.value</td><td>the value of the average</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/work/plumed_ex4.dat_solav">av</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=500 <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
</pre></div>

 {% endraw %} 

*Copy this input to a file called plumed.dat, fill in the blanks and run the calculation by executing the following command:*

````
> plumed driver --noatoms
````

Plot a graph showing the original data from `uncorrelated_data` and the averages in the `colvar` file.  You should be able to see something similar to this graph. 

![The yellow points are block averages computed from the data points shown in black](figures/masterclass-21-2-block-average.png)

Notice how the distribution for both the black (original data) and yellow points (averages) in this graph are centred on the same quantity.  Both of these quantities are thus 
[accurate estimators](https://www.notion.so/Point-estimation-d4225267e03e4539a2e85d08b9e9efad) for the expectation of the distribution.  However, the block average that is shown in yellow is a more 
[precise estimator](https://www.notion.so/Point-estimation-d4225267e03e4539a2e85d08b9e9efad) for this quantity.  

The reason the block average is a more precise estimator is connected to a well known result in statistics.  If we compute a mean as follows:

$$
\overline{X} = \frac{1}{N} \sum_{i=1}^N X_i
$$

where the $X_i$ are all [independent](https://www.notion.so/Independence-00fd3064fd3e4aa3b677d7fec6ecedcd) and [identical](https://www.notion.so/Random-variables-8aad5b4c3453423da3069168228fe890) 
random variables it is [straghtforward to show](https://www.notion.so/Sample-mean-583d58d7001343c68a7956a1b9f19f4b) that the expectation and variance of this random quantity are given by:

$$
\mathbb{E}(\overline{X}) = \mathbb{E}(X) \qquad \textrm{and} \qquad \textrm{var}(\overline{X}) = \frac{\textrm{var}(X)}{N}
$$

where $\mathbb{E}(X)$ and $\textrm{var}(X)$ are the expectation and variance of the random variable $X_i$ from which the mean was computed.

### Exercise 5: Free energy from block averages

We can use the block averaging method introduced in exercise 4 to calculate error bars on the estimates of free energy.  To generate 10 histograms
from the data in `uncorrelated_data` with 100 bins starting at -4 and finishing at +4 using PLUMED we can use the input file:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/work/plumed_ex5.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="plumed_ex5.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="plumed_ex5.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
<div class="headerBadge"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/work/plumed_ex5.dat")' onmousedown='toggleDisplay("data/work/plumed_ex5.dat")'/></div>
</div>
</div>
<div id="data/work/plumed_ex5.dat_short">
<pre class="plumedlisting">
<span class="plumedtooltip" style="color:green">UNITS<span class="right">This command sets the internal units for the code. <a href="https://www.plumed.org/doc-master/user-doc/html/UNITS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NATURAL<span class="right"> use natural units<i></i></span></span>
<span style="display:none;" id="data/work/plumed_ex5.dat">The UNITS action with label <b></b> calculates something</span><b name="data/work/plumed_ex5.datdata" onclick='showPath("data/work/plumed_ex5.dat","data/work/plumed_ex5.datdata","data/work/plumed_ex5.datdata","brown")'>data</b>: <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=<span style="background-color:yellow">__FILL__</span>
<span style="display:none;" id="data/work/plumed_ex5.datdata">The READ action with label <b>data</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">data..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/work/plumed_ex5.dathhh" onclick='showPath("data/work/plumed_ex5.dat","data/work/plumed_ex5.dathhh","data/work/plumed_ex5.dathhh","brown")'>hhh</b>: <span class="plumedtooltip" style="color:green">HISTOGRAM<span class="right">Accumulate the average probability density along a few CVs from a trajectory. <a href="https://www.plumed.org/doc-master/user-doc/html/HISTOGRAM" style="color:green">More details</a><i></i></span></span> ... 
   <span class="plumedtooltip">ARG<span class="right">the quantities that are being used to construct the histogram<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1 
   <span style="background-color:yellow">__FILL__</span>=-4.5 <span style="background-color:yellow">__FILL__</span>=4.5 <span style="background-color:yellow">__FILL__</span>=100 
   <span class="plumedtooltip">CLEAR<span class="right"> the frequency with whihc to clear the data that is being averaged<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span style="background-color:yellow">__FILL__</span>=DISCRETE
...
<span style="display:none;" id="data/work/plumed_ex5.dathhh">The HISTOGRAM action with label <b>hhh</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">hhh.value</td><td>the estimate of the histogram as a function of the argument that was obtained</td></tr></table></span><span class="plumedtooltip" style="color:green">DUMPGRID<span class="right">Output the function on the grid to a file with the PLUMED grid format. <a href="https://www.plumed.org/doc-master/user-doc/html/DUMPGRID" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">the grid you would like to print (can also use ARG for specifying what is being printed)<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">FILE<span class="right"> the file on which to write the grid<i></i></span></span>=hist.dat <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the grid should be output to the file<i></i></span></span>=1000
</pre></div>
<div style="display:none;" id="data/work/plumed_ex5.dat_long"><pre class="plumedlisting">
<span class="plumedtooltip" style="color:green">UNITS<span class="right">This command sets the internal units for the code. <a href="https://www.plumed.org/doc-master/user-doc/html/UNITS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NATURAL<span class="right"> use natural units<i></i></span></span>
<span style="display:none;" id="data/work/plumed_ex5.dat_sol">The UNITS action with label <b></b> calculates something</span><b name="data/work/plumed_ex5.dat_soldata" onclick='showPath("data/work/plumed_ex5.dat","data/work/plumed_ex5.dat_soldata","data/work/plumed_ex5.dat_soldata","brown")'>data</b>: <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=<b name="data/work/plumed_ex5.dat_sol">../data/uncorrelated_data</b> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=rand
<span style="display:none;" id="data/work/plumed_ex5.dat_soldata">The READ action with label <b>data</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">data..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/work/plumed_ex5.dat_solhhh" onclick='showPath("data/work/plumed_ex5.dat","data/work/plumed_ex5.dat_solhhh","data/work/plumed_ex5.dat_solhhh","brown")'>hhh</b>: <span class="plumedtooltip" style="color:green">HISTOGRAM<span class="right">Accumulate the average probability density along a few CVs from a trajectory. <a href="https://www.plumed.org/doc-master/user-doc/html/HISTOGRAM" style="color:green">More details</a><i></i></span></span> ... 
   <span class="plumedtooltip">ARG<span class="right">the quantities that are being used to construct the histogram<i></i></span></span>=<b name="data/work/plumed_ex5.dat_soldata">data</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1 
   <span class="plumedtooltip">GRID_MIN<span class="right"> the lower bounds for the grid<i></i></span></span>=-4.5 <span class="plumedtooltip">GRID_MAX<span class="right"> the upper bounds for the grid<i></i></span></span>=4.5 <span class="plumedtooltip">GRID_BIN<span class="right">the number of bins for the grid<i></i></span></span>=100 
   <span class="plumedtooltip">CLEAR<span class="right"> the frequency with whihc to clear the data that is being averaged<i></i></span></span>=1000 <span class="plumedtooltip">KERNEL<span class="right"> the kernel function you are using<i></i></span></span>=DISCRETE
...
<span style="display:none;" id="data/work/plumed_ex5.dat_solhhh">The HISTOGRAM action with label <b>hhh</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">hhh.value</td><td>the estimate of the histogram as a function of the argument that was obtained</td></tr></table></span><span class="plumedtooltip" style="color:green">DUMPGRID<span class="right">Output the function on the grid to a file with the PLUMED grid format. <a href="https://www.plumed.org/doc-master/user-doc/html/DUMPGRID" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">the grid you would like to print (can also use ARG for specifying what is being printed)<i></i></span></span>=<b name="data/work/plumed_ex5.dat_solhhh">hhh</b> <span class="plumedtooltip">FILE<span class="right"> the file on which to write the grid<i></i></span></span>=hist.dat <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the grid should be output to the file<i></i></span></span>=1000
</pre></div>

 {% endraw %} 

<b>Copy this input to a file called plumed.dat, fill in the blanks and run the calculation by executing the following command:</b>

````
> plumed driver --noatoms
````

Running this command should generate several files containing histograms that will be called: analysis.0.hist.dat,
analysis.1.hist.dat etc.  These files contain the histograms constructed from each of the blocks of data in your trajectory.  You can merge
them all to get the final free energy surface, which can be calculated using the well-known relation between the histogram, $P(s)$, and the
free energy surface, $F(s)$, by using the following python script:

```python
import matplotlib.pyplot as plt
import numpy as np
import glob

hist1 = np.loadtxt("../Exercises/Exercise_5/hist.dat")
N, average, average2 = 1, hist1[:,1], hist1[:,1]*hist1[:,1]
for filen in glob.glob( "../Exercises/Exercise_5/analysis.*.hist.dat") : 
    histn = np.loadtxt(filen)
    N, average, average2 = N + 1, average + histn[:,1], average2 + histn[:,1]*histn[:,1]
    
# Final averages 
average = average / N
# Final variances
var = (N/(N-1))*( average2 / N - average*average ) 
# Errors
error = np.sqrt( var / N )

# Convert to free energy 
fes = -np.log( average )
# Convert to error in fes
ferr = error / average 

# And draw graph of free energy surface
plt.fill_between( hist1[:,0], fes-ferr, fes+ferr )
plt.xlabel("CV value")
plt.ylabel('Free energy')
plt.show()
```

Copy this script to a cell in a python notebook and then run it on your data. You may need to adjust the names of the files that are being read to suit your machine's setup.
The graph shown in the figure below shows the free energy surface generated from the python script.  

![The free energy as a function of the CV for the data in uncorrelated_data.  The shaded region shows the errors on this estimate.  These errors were computed using block averaging](figures/masterclass-21-2-fes2.png) 

The value of the free energy in the $i$th bin is calculated using:

$$
F_i = -k_B T \ln \left( \frac{1}{N} \sum_{j=1}^N H_i^{(j)} \right)
$$

The sum here runs over the $N$ histograms and $H_i^{(j)}$ is the value of ith bin in the jth estimate of the histogram.
The above expression is thus calculating the logarithm of the histogram's average value in bin $i$.

The error on the free energy, which is illustrated using the shaded region in the figure above, is calculated using:

$$
\sigma_{F_i} = \frac{k_B T}{\frac{1}{N} \sum_{j=1}^N H_i^{(j)}} \sqrt{\frac{1}{N-1} \left[ \frac{1}{N}\sum_{j=1}^N (H_i^{(j)})^2 - \left( \frac{1}{N}\sum_{j=1}^N H_i^{(j)} \right)^2 \right] } 
$$ 

The term in the square root here is the error on the average value of the histogram in bin $i$.  The error on this [average](https://www.notion.so/Sample-mean-583d58d7001343c68a7956a1b9f19f4b) can be 
calculated using the formulas that were discussed in exercise 4.  To get the error on the free energy, we then have to propagate the errors through the
expression:

$$
F(s) = - k_B T \ln\left( P(s) \right)
$$

to get the expression above.

Lastly, notice that it is often useful to average the error over the grid using:

$$
\sigma = \frac{1}{M} \sum_{i=1}^M F_i
$$

where the sum runs over the $M$ bins in the histogram.

### Exercise 6: Calculating bootstrap averages

Exercise 4 demonstrated one way of sampling the mean's distribution.  We assumed that the $M$ estimates of the mean were all normal random variables in the 
previous section but we did not need to do that.  We could instead have used a non-parametric method.  When using such methods we have to generate more data, which we can either do by running longer simulations, 
which is expensive, or by bootstrapping, which is cheaper.  

We can demonstrate how bootstrapping works in practice by using the following script, which works with the first 500 points in `uncorrelated_data`.  As you can see, we first calculate the average from all the data points.  We then take new means by repeatedly sampling sets of 500 points with replacement from the data and calculating new means.  

```python
import numpy as np

ddd = np.loadtxt("../data/uncorrelated_data")
data = ddd[0:500,1]

bootstraps = np.zeros(200)
for i in range(200) : 
    av = 0
    for j in range(500) : av = av + data[np.random.randint(0,500)]
    bootstraps[i] = av / 500 

f = open("bootstraps", "w")
f.write("#! FIELDS time boot \n")
for i in range(0,200):
    f.write(str(i) + " "  + str(bootstraps[i) + "\n" )
f.close()
```

When you run the script above, it generates a file called `bootstraps` containing the averages that have been calculated by bootstrapping. If you now calculate the variance from all your bootstrapped averages you should see that it close to the value you got from the expression below which was introduced in exercise 4: 

$$
\textrm{var}(\overline{X}) = \frac{\textrm{var}(X)}{N}
$$ 

To use this expression you can insert the value of $\textrm{var}(X)$ you computed in exercise 3 with $N=500$.  

<em>You can also use bootstrapping to estimate the errors in the free energy surface.  As an additional exercise, you can try to do this form of analysis on the data in `uncorrelated_data` You should get 
a result that is similar to the result you got in exercise 5</em>

### Exercise 7: Dealing with correlated data

In this exercise, you will review everything you have done in the previous two exercises.  <b>You should</b>:

- Calculate block averages for the data in `correlated_data`.  Calculate the error on the average of the block average.  
- Calculate bootstrap averages for the data in `correlated_data`.  Calculate the error from the bootstrap averages.

You will see that the variance you obtain from the bootstrap averages is less than the variance you get by block averaging.

These variances are different because there are correlations between the data points in `correlated_data`. Such correlations were not present in the data set
you have examined in all the exercises that appeared previously to this one.  The reason this matters is that the expression:

$$
\textrm{var}(\overline{X}) = \frac{\textrm{var}(X)}{N}
$$ 

is only valid if the random variables that $\overline{X}$ is computed from are both [identical](https://www.notion.so/Random-variables-8aad5b4c3453423da3069168228fe890) and [<b>independent</b>](https://www.notion.so/Independence-00fd3064fd3e4aa3b677d7fec6ecedcd).   This expression is thus not valid for 
correlated data.  To be clear, however, we can still write:

$$
\mathbb{E}(\overline{X}) = \mathbb{E}(X)
$$ 

as this expression holds as long as the random variables from which $\overline{X}$ are [identical](https://www.notion.so/Random-variables-8aad5b4c3453423da3069168228fe890).  When we use this expression, the random variables only need to be 
independent and can be correlated.

<b>Any data we get by computing CVs from a molecular dynamics trajectory is almost certain to contain correlations.</b>  It is thus essential to know how to handle correlated
data.  The block averaging technique that was introduced in exercise 4 resolves this problem.  You can show that if the blocks are long enough, the averages you obtain are uncorrelated.

For the remainder of this exercise, you should use the data in `correlated_data` and what you have learned in the previous exercises to calculate block averages for different block sizes.  
For each block size 

- Estimate the mean and variance for your $N$ block averages (the $X_i$) using $\mu = \frac{1}{N} \sum X_i$ and $\sigma^2 = \frac{N}{N-1} \left[ \frac{1}{N} \sum_{i=1}^N X_i^2 - \left( \frac{1}{N}\sum_{i=1}^N X_i \right)^2 \right] $  
- Insert your estimate of the variance into the following expression for the error bar on your estimate for $\mu$: $\epsilon = \sqrt{\frac{\sigma^2}{N}}$

You should be able to use your data to draw a graph showing the value of the average and the associated error barm $\epsilon$, as a function of the size of the blocks similar to the one shown below:

![Average of blocks as a function of the blocks' size for the correlated data.  The bar shows the size of the error on the estimate of the average](figures/masterclass-21-2-corr-baverage.png)

This graph shows that, when the data is correlated, the error bar is underestimated if each block average is computed from a small number of data points.
When sufficient data points are used to calculate each block average, however, the error bar settles on a constant value that is independent of the block size.  When this has happened you 
can be confident that your block averages are no longer correlated and the expression $\textrm{var}(\overline{X}) = \frac{\textrm{var}(X)}{N}$ is thus valid.

<em>Notice that you can also calculate the error bar using bootstrapping by selecting samples from your block averages.  If you have time, you should try this. You should try to confirm that this method gives similar estimates for the error.</em>

### Exercise 8: Weighted averages

PLUMED is routinely used to run simulations using methods such as umbrella sampling and metadynamics.  In these methods, a bias potential, $V(x)$, is added to the Hamiltonian to enhance the sampling of phase space. 
CVs calculated from the frames of such biased MD simulations thus samples from the following distribution:

$$
P(s') = \frac{ \int \textrm{d}x \textrm{d}p \delta( s(x) - s') e^{-\frac{H(x,p)}{k_B T}} e^{-\frac{V(x)}{k_B T}} }{ \int \textrm{d}x\textrm{d}p e^{-\frac{H(x,p)}{k_B T}}e^{-\frac{V(x)}{k_B T}} }
$$

To get information on the unbiased distribution:

$$
P(s') = \frac{ \int \textrm{d}x \textrm{d}p \delta( s(x) - s') e^{-\frac{H(x,p)}{k_B T}} }{ \int \textrm{d}x\textrm{d}p e^{-\frac{H(x,p)}{k_B T}} }
$$

from such simulations we thus have to calculate [weighted averages](https://www.notion.so/Weighted-averages-81a28555cc3149f78047f80bb9dbba91) using:

$$
\overline{X}_w = \frac{\sum_{i=1}^N w_i X_i }{\sum_{i=1}^N w_i}
$$

where the $w_i$ are (random) weights that counteract the effect of the bias. The way the weights are calculated is described in other lessons)

In this exercise we are going to reweight the data in `weighted_data`, which consists  of samples from the following distribution:

$$
P(x) = \frac{1}{\sqrt{2\pi}\sigma} \exp\left( -\frac{(x-\mu)^2}{2\sigma^2} \right)
$$

with $\mu=0.6$ and $\sigma=0.5$ with and additional constrant that $ x $ is between 0 and 1.  Given this information the following weighted average:

$$
\overline{X}_w = \frac{\sum_{i=1}^N w_i X_i }{\sum_{i=1}^N w_i} \qquad \textrm{where} \qquad w_i = \frac{1}{P(X_i)}
$$

should be an estimator for the expectation of a uniform random variable between 0 and 1.  Furthermore, the expression below:

$$
\sigma^2_{X} = \frac{V_1}{V_1-1} \sum_{i=1}^N \frac{w_i}{V_1} (x_i - \overline{X}_w)^2 \qquad \textrm{where} \qquad V_1 = \sum_{i=1}^N w_i
$$  

gives an estimate for the variance of <b>the distribution</b> after reweighting (i.e. the variance of the uniform random variable).

Notice, finally, that the tools of statistics gives us expressions for the [expectation and variance of the <b>weighted average</b>](https://www.notion.so/Weighted-averages-81a28555cc3149f78047f80bb9dbba91):

$$
\mathbb{E}(\overline{X}_w) = \overline{X} \qquad \textrm{and} \qquad \textrm{var}(\overline{X}_w) = \frac{\sum_{i=1}^N w_i^2 (X_i - \overline{X}_w)^2 }{(\sum_{i=1}^N w_i)^2} 
$$

These expressions hold if all the $X_i$ from which the weighted average is computed are independent and identically distributed random variables. Notice, furthermore, how the expression above for the 
the variance of the weighted average <b>is not</b> a function of the variance for the variable as was the case for the unweighted averages in exercise 4.

In what follows we are thus going to try to extract the average and the fluctuations for the CV in the unbiased (in this case uniform) distribution as well as the 
unbiased free energy.  We will calculate these quantities by computing weighted averages and [weighted histograms](https://www.notion.so/Weighted-histograms-546d0b3837ce43a3b9de0dcf7a741353) from our simulation data.  For the histogram we 
are also going to extract error bars by reweighting.  To calculate these quantities using PLUMED we will use an input like this:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/work/plumed_ex6.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="plumed_ex6.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="plumed_ex6.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
<div class="headerBadge"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/work/plumed_ex6.dat")' onmousedown='toggleDisplay("data/work/plumed_ex6.dat")'/></div>
</div>
</div>
<div id="data/work/plumed_ex6.dat_short">
<pre class="plumedlisting">
<span class="plumedtooltip" style="color:green">UNITS<span class="right">This command sets the internal units for the code. <a href="https://www.plumed.org/doc-master/user-doc/html/UNITS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NATURAL<span class="right"> use natural units<i></i></span></span> <span style="color:blue" class="comment"># This ensures that Boltzmann&#x27;s constant is one </span>
<span style="display:none;" id="data/work/plumed_ex6.dat">The UNITS action with label <b></b> calculates something</span><b name="data/work/plumed_ex6.datdata" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.datdata","data/work/plumed_ex6.datdata","brown")'>data</b>: <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
<span style="color:blue" class="comment"># This restraint and the REWEIGHT_BIAS command after computes the weights in the formulas above.</span>
<span style="display:none;" id="data/work/plumed_ex6.datdata">The READ action with label <b>data</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">data..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/work/plumed_ex6.datmm" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.datmm","data/work/plumed_ex6.datmm","brown")'>mm</b>: <span class="plumedtooltip" style="color:green">RESTRAINT<span class="right">Adds harmonic and/or linear restraints on one or more variables. <a href="https://www.plumed.org/doc-master/user-doc/html/RESTRAINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values the harmonic restraint acts upon<i></i></span></span>=<b name="data/work/plumed_ex6.datdata">data</b> <span class="plumedtooltip">AT<span class="right">the position of the restraint<i></i></span></span>=0.6 <span class="plumedtooltip">KAPPA<span class="right"> specifies that the restraint is harmonic and what the values of the force constants on each of the variables are<i></i></span></span>=4 
<span style="display:none;" id="data/work/plumed_ex6.datmm">The RESTRAINT action with label <b>mm</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">mm.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">mm.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span><b name="data/work/plumed_ex6.datrw" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.datrw","data/work/plumed_ex6.datrw","brown")'>rw</b>: <span class="plumedtooltip" style="color:green">REWEIGHT_BIAS<span class="right">Calculate weights for ensemble averages that negate the effect the bias has on the region of phase space explored <a href="https://www.plumed.org/doc-master/user-doc/html/REWEIGHT_BIAS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">TEMP<span class="right">the system temperature<i></i></span></span>=1 
<span style="display:none;" id="data/work/plumed_ex6.datrw">The REWEIGHT_BIAS action with label <b>rw</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">rw.value</td><td>the weight to use for this frame to negate the effect the bias</td></tr></table></span><b name="data/work/plumed_ex6.datwav" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.datwav","data/work/plumed_ex6.datwav","brown")'>wav</b>: <span class="plumedtooltip" style="color:green">AVERAGE<span class="right">Calculate the ensemble average of a collective variable <a href="https://www.plumed.org/doc-master/user-doc/html/AVERAGE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantity that is being averaged<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1 <span class="plumedtooltip">LOGWEIGHTS<span class="right">the logarithm of the quantity to use as the weights when calculating averages<i></i></span></span>=<span style="background-color:yellow">__FILL__</span>
<span style="color:blue" class="comment"># These lines compute the variance of the random variable</span>
<span style="display:none;" id="data/work/plumed_ex6.datwav">The AVERAGE action with label <b>wav</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">wav.value</td><td>the value of the average</td></tr></table></span><b name="data/work/plumed_ex6.datdd" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.datdd","data/work/plumed_ex6.datdd","brown")'>dd</b>: <span class="plumedtooltip" style="color:green">CUSTOM<span class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/CUSTOM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<b name="data/work/plumed_ex6.datdata">data</b>,<b name="data/work/plumed_ex6.datwav">wav</b> <span class="plumedtooltip">FUNC<span class="right">the function you wish to evaluate<i></i></span></span>=(x-y)(x-y) <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="display:none;" id="data/work/plumed_ex6.datdd">The CUSTOM action with label <b>dd</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dd.value</td><td>an arbitrary function</td></tr></table></span><b name="data/work/plumed_ex6.datuvar" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.datuvar","data/work/plumed_ex6.datuvar","brown")'>uvar</b>: <span class="plumedtooltip" style="color:green">AVERAGE<span class="right">Calculate the ensemble average of a collective variable <a href="https://www.plumed.org/doc-master/user-doc/html/AVERAGE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantity that is being averaged<i></i></span></span>=<b name="data/work/plumed_ex6.datdd">dd</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1 <span class="plumedtooltip">LOGWEIGHTS<span class="right">the logarithm of the quantity to use as the weights when calculating averages<i></i></span></span>=<b name="data/work/plumed_ex6.datrw">rw</b> <span class="plumedtooltip">NORMALIZATION<span class="right">Including this keyword in the input to this action makes no difference to the calculation performed it was used in older versions of PLUMED and is provided here for back compatibility only<i></i></span></span>=false
<span style="display:none;" id="data/work/plumed_ex6.datuvar">The AVERAGE action with label <b>uvar</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">uvar.value</td><td>the value of the average</td></tr></table></span><b name="data/work/plumed_ex6.datone" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.datone","data/work/plumed_ex6.datone","brown")'>one</b>: <span class="plumedtooltip" style="color:green">CONSTANT<span class="right">Create a constant value that can be passed to actions <a href="https://www.plumed.org/doc-master/user-doc/html/CONSTANT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">VALUE<span class="right">the single number that you would like to store<i></i></span></span>=1
<span style="display:none;" id="data/work/plumed_ex6.datone">The CONSTANT action with label <b>one</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">one.value</td><td>the constant value that was read from the plumed input</td></tr></table></span><b name="data/work/plumed_ex6.datwsum" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.datwsum","data/work/plumed_ex6.datwsum","brown")'>wsum</b>: <span class="plumedtooltip" style="color:green">AVERAGE<span class="right">Calculate the ensemble average of a collective variable <a href="https://www.plumed.org/doc-master/user-doc/html/AVERAGE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantity that is being averaged<i></i></span></span>=<b name="data/work/plumed_ex6.datone">one</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1 <span class="plumedtooltip">LOGWEIGHTS<span class="right">the logarithm of the quantity to use as the weights when calculating averages<i></i></span></span>=<b name="data/work/plumed_ex6.datrw">rw</b> <span class="plumedtooltip">NORMALIZATION<span class="right">Including this keyword in the input to this action makes no difference to the calculation performed it was used in older versions of PLUMED and is provided here for back compatibility only<i></i></span></span>=false
<span style="display:none;" id="data/work/plumed_ex6.datwsum">The AVERAGE action with label <b>wsum</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">wsum.value</td><td>the value of the average</td></tr></table></span><b name="data/work/plumed_ex6.datvar" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.datvar","data/work/plumed_ex6.datvar","brown")'>var</b>: <span class="plumedtooltip" style="color:green">CUSTOM<span class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/CUSTOM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<b name="data/work/plumed_ex6.datuvar">uvar</b>,<b name="data/work/plumed_ex6.datwsum">wsum</b> <span class="plumedtooltip">FUNC<span class="right">the function you wish to evaluate<i></i></span></span>=x/(y-1) <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="color:blue" class="comment"># Print out the average and variance of the uniform random variable</span>
<span style="display:none;" id="data/work/plumed_ex6.datvar">The CUSTOM action with label <b>var</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">var.value</td><td>an arbitrary function</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=1 <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
<span style="color:blue" class="comment"># Construct the histogram</span>
<b name="data/work/plumed_ex6.dathhh" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.dathhh","data/work/plumed_ex6.dathhh","brown")'>hhh</b>: <span class="plumedtooltip" style="color:green">HISTOGRAM<span class="right">Accumulate the average probability density along a few CVs from a trajectory. <a href="https://www.plumed.org/doc-master/user-doc/html/HISTOGRAM" style="color:green">More details</a><i></i></span></span> ... 
   <span class="plumedtooltip">ARG<span class="right">the quantities that are being used to construct the histogram<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">LOGWEIGHTS<span class="right">the logarithm of the quantity to use as the weights when calculating averages<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
   <span style="background-color:yellow">__FILL__</span>=0 <span style="background-color:yellow">__FILL__</span>=1 <span style="background-color:yellow">__FILL__</span>=20 
   <span class="plumedtooltip">CLEAR<span class="right"> the frequency with whihc to clear the data that is being averaged<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">NORMALIZATION<span class="right"> This controls how the data is normalized it can be set equal to true, false or ndata<i></i></span></span>=true <span style="background-color:yellow">__FILL__</span>=DISCRETE
...
<span style="display:none;" id="data/work/plumed_ex6.dathhh">The HISTOGRAM action with label <b>hhh</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">hhh.value</td><td>the estimate of the histogram as a function of the argument that was obtained</td></tr></table></span><span class="plumedtooltip" style="color:green">DUMPGRID<span class="right">Output the function on the grid to a file with the PLUMED grid format. <a href="https://www.plumed.org/doc-master/user-doc/html/DUMPGRID" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">the grid you would like to print (can also use ARG for specifying what is being printed)<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">FILE<span class="right"> the file on which to write the grid<i></i></span></span>=hist.dat <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the grid should be output to the file<i></i></span></span>=1000
</pre></div>
<div style="display:none;" id="data/work/plumed_ex6.dat_long"><pre class="plumedlisting">
<span class="plumedtooltip" style="color:green">UNITS<span class="right">This command sets the internal units for the code. <a href="https://www.plumed.org/doc-master/user-doc/html/UNITS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NATURAL<span class="right"> use natural units<i></i></span></span> <span style="color:blue" class="comment"># This ensures that Boltzmann&#x27;s constant is one </span>
<span style="display:none;" id="data/work/plumed_ex6.dat_sol">The UNITS action with label <b></b> calculates something</span><b name="data/work/plumed_ex6.dat_soldata" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.dat_soldata","data/work/plumed_ex6.dat_soldata","brown")'>data</b>: <span class="plumedtooltip" style="color:green">READ<span class="right">Read quantities from a colvar file. <a href="https://www.plumed.org/doc-master/user-doc/html/READ" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file from which to read these quantities<i></i></span></span>=<b name="data/work/plumed_ex6.dat_sol">../data/weighted_data</b> <span class="plumedtooltip">VALUES<span class="right">the values to read from the file<i></i></span></span>=rand <span class="plumedtooltip">IGNORE_FORCES<span class="right"> use this flag if the forces added by any bias can be safely ignored<i></i></span></span> 
<span style="color:blue" class="comment"># This restraint and the REWEIGHT_BIAS command after computes the weights in the formulas above.</span>
<span style="display:none;" id="data/work/plumed_ex6.dat_soldata">The READ action with label <b>data</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">data..#!custom</td><td>the names of the output components for this action depend on the actions input file see the example inputs below for details</td></tr></table></span><b name="data/work/plumed_ex6.dat_solmm" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.dat_solmm","data/work/plumed_ex6.dat_solmm","brown")'>mm</b>: <span class="plumedtooltip" style="color:green">RESTRAINT<span class="right">Adds harmonic and/or linear restraints on one or more variables. <a href="https://www.plumed.org/doc-master/user-doc/html/RESTRAINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values the harmonic restraint acts upon<i></i></span></span>=<b name="data/work/plumed_ex6.dat_soldata">data</b> <span class="plumedtooltip">AT<span class="right">the position of the restraint<i></i></span></span>=0.6 <span class="plumedtooltip">KAPPA<span class="right"> specifies that the restraint is harmonic and what the values of the force constants on each of the variables are<i></i></span></span>=4 
<span style="display:none;" id="data/work/plumed_ex6.dat_solmm">The RESTRAINT action with label <b>mm</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">mm.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">mm.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span><b name="data/work/plumed_ex6.dat_solrw" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.dat_solrw","data/work/plumed_ex6.dat_solrw","brown")'>rw</b>: <span class="plumedtooltip" style="color:green">REWEIGHT_BIAS<span class="right">Calculate weights for ensemble averages that negate the effect the bias has on the region of phase space explored <a href="https://www.plumed.org/doc-master/user-doc/html/REWEIGHT_BIAS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">TEMP<span class="right">the system temperature<i></i></span></span>=1 
<span style="display:none;" id="data/work/plumed_ex6.dat_solrw">The REWEIGHT_BIAS action with label <b>rw</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">rw.value</td><td>the weight to use for this frame to negate the effect the bias</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/work/plumed_ex6.dat_soldata">data</b>,<b name="data/work/plumed_ex6.dat_solrw">rw</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=reweight
<b name="data/work/plumed_ex6.dat_solwav" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.dat_solwav","data/work/plumed_ex6.dat_solwav","brown")'>wav</b>: <span class="plumedtooltip" style="color:green">AVERAGE<span class="right">Calculate the ensemble average of a collective variable <a href="https://www.plumed.org/doc-master/user-doc/html/AVERAGE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantity that is being averaged<i></i></span></span>=<b name="data/work/plumed_ex6.dat_soldata">data</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1 <span class="plumedtooltip">LOGWEIGHTS<span class="right">the logarithm of the quantity to use as the weights when calculating averages<i></i></span></span>=<b name="data/work/plumed_ex6.dat_solrw">rw</b>
<span style="color:blue" class="comment"># These lines compute the variance of the random variable</span>
<span style="display:none;" id="data/work/plumed_ex6.dat_solwav">The AVERAGE action with label <b>wav</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">wav.value</td><td>the value of the average</td></tr></table></span><b name="data/work/plumed_ex6.dat_soldd" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.dat_soldd","data/work/plumed_ex6.dat_soldd","brown")'>dd</b>: <span class="plumedtooltip" style="color:green">CUSTOM<span class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/CUSTOM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<b name="data/work/plumed_ex6.dat_soldata">data</b>,<b name="data/work/plumed_ex6.dat_solwav">wav</b> <span class="plumedtooltip">FUNC<span class="right">the function you wish to evaluate<i></i></span></span>=(x-y)*(x-y) <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="display:none;" id="data/work/plumed_ex6.dat_soldd">The CUSTOM action with label <b>dd</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">dd.value</td><td>an arbitrary function</td></tr></table></span><b name="data/work/plumed_ex6.dat_soluvar" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.dat_soluvar","data/work/plumed_ex6.dat_soluvar","brown")'>uvar</b>: <span class="plumedtooltip" style="color:green">AVERAGE<span class="right">Calculate the ensemble average of a collective variable <a href="https://www.plumed.org/doc-master/user-doc/html/AVERAGE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantity that is being averaged<i></i></span></span>=<b name="data/work/plumed_ex6.dat_soldd">dd</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1 <span class="plumedtooltip">LOGWEIGHTS<span class="right">the logarithm of the quantity to use as the weights when calculating averages<i></i></span></span>=<b name="data/work/plumed_ex6.dat_solrw">rw</b> <span class="plumedtooltip">NORMALIZATION<span class="right">Including this keyword in the input to this action makes no difference to the calculation performed it was used in older versions of PLUMED and is provided here for back compatibility only<i></i></span></span>=false
<span style="display:none;" id="data/work/plumed_ex6.dat_soluvar">The AVERAGE action with label <b>uvar</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">uvar.value</td><td>the value of the average</td></tr></table></span><b name="data/work/plumed_ex6.dat_solone" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.dat_solone","data/work/plumed_ex6.dat_solone","brown")'>one</b>: <span class="plumedtooltip" style="color:green">CONSTANT<span class="right">Create a constant value that can be passed to actions <a href="https://www.plumed.org/doc-master/user-doc/html/CONSTANT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">VALUE<span class="right">the single number that you would like to store<i></i></span></span>=1
<span style="display:none;" id="data/work/plumed_ex6.dat_solone">The CONSTANT action with label <b>one</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">one.value</td><td>the constant value that was read from the plumed input</td></tr></table></span><b name="data/work/plumed_ex6.dat_solwsum" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.dat_solwsum","data/work/plumed_ex6.dat_solwsum","brown")'>wsum</b>: <span class="plumedtooltip" style="color:green">AVERAGE<span class="right">Calculate the ensemble average of a collective variable <a href="https://www.plumed.org/doc-master/user-doc/html/AVERAGE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the quantity that is being averaged<i></i></span></span>=<b name="data/work/plumed_ex6.dat_solone">one</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which to store data for averaging<i></i></span></span>=1 <span class="plumedtooltip">LOGWEIGHTS<span class="right">the logarithm of the quantity to use as the weights when calculating averages<i></i></span></span>=<b name="data/work/plumed_ex6.dat_solrw">rw</b> <span class="plumedtooltip">NORMALIZATION<span class="right">Including this keyword in the input to this action makes no difference to the calculation performed it was used in older versions of PLUMED and is provided here for back compatibility only<i></i></span></span>=false
<span style="display:none;" id="data/work/plumed_ex6.dat_solwsum">The AVERAGE action with label <b>wsum</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">wsum.value</td><td>the value of the average</td></tr></table></span><b name="data/work/plumed_ex6.dat_solvar" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.dat_solvar","data/work/plumed_ex6.dat_solvar","brown")'>var</b>: <span class="plumedtooltip" style="color:green">CUSTOM<span class="right">Calculate a combination of variables using a custom expression. <a href="https://www.plumed.org/doc-master/user-doc/html/CUSTOM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the values input to this function<i></i></span></span>=<b name="data/work/plumed_ex6.dat_soluvar">uvar</b>,<b name="data/work/plumed_ex6.dat_solwsum">wsum</b> <span class="plumedtooltip">FUNC<span class="right">the function you wish to evaluate<i></i></span></span>=x/(y-1) <span class="plumedtooltip">PERIODIC<span class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></span></span>=NO
<span style="color:blue" class="comment"># Print out the average and variance of the uniform random variable</span>
<span style="display:none;" id="data/work/plumed_ex6.dat_solvar">The CUSTOM action with label <b>var</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">var.value</td><td>an arbitrary function</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/work/plumed_ex6.dat_solwav">wav</b>,<b name="data/work/plumed_ex6.dat_solvar">var</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=1 <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
<span style="color:blue" class="comment"># Construct the histogram</span>
<b name="data/work/plumed_ex6.dat_solhhh" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.dat_solhhh","data/work/plumed_ex6.dat_solhhh","brown")'>hhh</b>: <span class="plumedtooltip" style="color:green">HISTOGRAM<span class="right">Accumulate the average probability density along a few CVs from a trajectory. <a href="https://www.plumed.org/doc-master/user-doc/html/HISTOGRAM" style="color:green">More details</a><i></i></span></span> ... 
   <span class="plumedtooltip">ARG<span class="right">the quantities that are being used to construct the histogram<i></i></span></span>=<b name="data/work/plumed_ex6.dat_soldata">data</b> <span class="plumedtooltip">LOGWEIGHTS<span class="right">the logarithm of the quantity to use as the weights when calculating averages<i></i></span></span>=<b name="data/work/plumed_ex6.dat_solrw">rw</b> 
   <span class="plumedtooltip">GRID_MIN<span class="right"> the lower bounds for the grid<i></i></span></span>=0 <span class="plumedtooltip">GRID_MAX<span class="right"> the upper bounds for the grid<i></i></span></span>=1 <span class="plumedtooltip">GRID_BIN<span class="right">the number of bins for the grid<i></i></span></span>=20 
   <span class="plumedtooltip">CLEAR<span class="right"> the frequency with whihc to clear the data that is being averaged<i></i></span></span>=1000 <span class="plumedtooltip">NORMALIZATION<span class="right"> This controls how the data is normalized it can be set equal to true, false or ndata<i></i></span></span>=true <span class="plumedtooltip">KERNEL<span class="right"> the kernel function you are using<i></i></span></span>=DISCRETE
...
<span style="display:none;" id="data/work/plumed_ex6.dat_solhhh">The HISTOGRAM action with label <b>hhh</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">hhh.value</td><td>the estimate of the histogram as a function of the argument that was obtained</td></tr></table></span><span class="plumedtooltip" style="color:green">DUMPGRID<span class="right">Output the function on the grid to a file with the PLUMED grid format. <a href="https://www.plumed.org/doc-master/user-doc/html/DUMPGRID" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">the grid you would like to print (can also use ARG for specifying what is being printed)<i></i></span></span>=<b name="data/work/plumed_ex6.dat_solhhh">hhh</b> <span class="plumedtooltip">FILE<span class="right"> the file on which to write the grid<i></i></span></span>=hist.dat <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the grid should be output to the file<i></i></span></span>=1000
</pre></div>

 {% endraw %} 

<b>Copy this input to a file called plumed.dat, fill in the blanks and run the calculation by executing the following command:</b>

````
> plumed driver --noatoms
````

I obtained the following graphs showing how the mean and variance change with sample size.  

![Average value of the random variable and the fluctuations as a function of sample size](figures/masterclass-21-2-average8.png)

The free energy with errors from this data looks like this:

![Free energy (with errors) as a function of the CV computed by reweighting](figures/masterclass-21-2-fes8.png) 

<b>It is up to you to work out how to adapt the script given in exercise 5, so it works here.  The script above works for unweighted means. 
Here, however, you have to calculate weighted means using the formulas above.</b>

### Exercise 9: The free energy from a biased simulation

We can now bring all this together by running a metadynamics simulation and extracting the free energy surface by reweighting.  The other exercises in this tutorial have shown us that when we do this, it is essential to:

- Quote error bars on the estimates of the free energy we obtain as the values we get from our simulation will be random variables.  Quoting error bars is thus essential in terms of making our results reproducible.
- Calculate weighted averages using the ideas discussed in exercise 8 as we need to account for the effect the bias has on the sampling of phase space.
- Use the block averaging method discussed in exercise 4 to obtain multiple estimates for the free energy.  Notice that we need to use block averaging because, as discussed in exercise 7, there are correlations between the CV values the system visits during the trajectory.

As these three issues have been the focus of this tutorial, we focus on them in the exercise that follows.  The theory behind the metadynamics method that we are using is discussed in detail in 
other lessons if you are interested.  

We will study a system of 7 Lennard Jones atoms in two dimensions in what follows using the MD code <b>simplemd</b> that is part of PLUMED.  You can run this code by issuing the command:

````
plumed simplemd < in
````

where <b>in</b> here is the input file from the GitHub repository for this tutorial.  This input file instructs PLUMED to perform 200000 steps of MD at a temperature of $k_B T = 0.1 \epsilon$ starting from the configuration in input.xyz.  

The timestep in this simulation is 0.005 $\sqrt{\epsilon}{m\sigma^2}$ and the temperature is kept fixed using a Langevin thermostat with a relaxation time of $0.1 \sqrt{\epsilon}{m\sigma^2}$.  Trajectory frames
are output every 1000 MD steps to a file called trajectory.xyz.  Notice also that to run the calculation above you need to provide a PLUMED input file called plumed.dat.  

We want to investigate transitions between the four structures of Lennard Jones 7 that are shown below using metadynamics.

![The four energetic minima in the energy landscape for two-dimensional Lennard Jones 7](figures/lyon-lj7-minima.png)

However, when we run the metadynamics, we will often find that the cluster evaporates and the seven atoms separate.  To prevent this, we will thus add restraints to prevent the cluster from evaporating.  The particular restraint we are going to use will 
prevent all the atoms from moving more than $2\sigma$ from the centre of mass of the cluster.  As the masses of all the atoms in the cluster are the same, we can compute the position of the centre of mass using:

$$
\mathbf{x}_\textrm{com} = \frac{1}{N} \sum_{i=1}^N \mathbf{x}_i
$$

where $\mathbf{x}_i$ is the position of the atom with index i.   The distance between the atom with index i and the position of this centre of mass, $d_i$, can be computed using Pythagoras' theorem.  These distances
are then restrained by using the following potential:

$$
V(d_i) = \begin{cases}
          100*(d_i-2.0)^2 & \textrm{if} \quad d_i < 2 \\
          0 & \textrm{otherwise}
\end{cases}
$$

as you can see, this potential does not affect the dynamics when these distances are less than 2 $\epsilon$.  If an atom is more than 2 $\epsilon$ from the centre of mass, however, this potential will drive it back
towards the centre of mass. 

A metadynamics bias will be used to force the system to move between the four configurations shown in the figure of the four minima above. This bias will act on the second and third central moments of the distribution of coordination numbers.
The nth central moment of a set of numbers, $\{X_i\}$ can be calculated using:

$$
\mu^n = \frac{1}{N} \sum_{i=1}^N ( X_i - \langle X \rangle )^n \qquad \textrm{where} \qquad \langle X \rangle = \frac{1}{N} \sum_{i=1}^N X_i
$$

Furthermore, we can compute the coordination number of our Lennard Jones atoms using:

$$
c_i = \sum_{i \ne j } \frac{1 - \left(\frac{r_{ij}}{1.5}\right)^8}{1 - \left(\frac{r_{ij}}{1.5}\right)^{16} }
$$

where $r_{ij}$ is the distance between atom $i$ and atom $j$.   With all this information in mind the following cell contains a skeleton input file for PLUMED that gets it to perform metadynamics using the second and third central
moments of the distribution of coordination numbers as a CV.

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/work/plumed_ex7.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="plumed_ex7.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="plumed_ex7.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
<div class="headerBadge"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/work/plumed_ex7.dat")' onmousedown='toggleDisplay("data/work/plumed_ex7.dat")'/></div>
</div>
</div>
<div id="data/work/plumed_ex7.dat_short">
<pre class="plumedlisting">
<span style="color:blue" class="comment"># this optional command tells VIM that this is a PLUMED file and to colour the text accordingly</span>
<span class="plumedtooltip" style="color:blue"># vim: ft=plumed<span class="right">Enables syntax highlighting for PLUMED files in vim. See <a href="https://www.plumed.org/doc-master/user-doc/html/vim">here for more details. </a><i></i></span></span>
<br/><span style="color:blue" class="comment"># This tells PLUMED we are using Lennard Jones units</span>
<span class="plumedtooltip" style="color:green">UNITS<span class="right">This command sets the internal units for the code. <a href="https://www.plumed.org/doc-master/user-doc/html/UNITS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NATURAL<span class="right"> use natural units<i></i></span></span>
<br/><span style="color:blue" class="comment"># Calculate the position of the centre of mass.  We can then refer to this position later in the input using the label com.</span>
<span style="display:none;" id="data/work/plumed_ex7.dat">The UNITS action with label <b></b> calculates something</span><b name="data/work/plumed_ex7.datcom" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.datcom","data/work/plumed_ex7.datcom","brown")'>com</b>: <span class="plumedtooltip" style="color:green">COM<span class="right">Calculate the center of mass for a group of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/COM" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<br/><span style="color:blue" class="comment"># Add the restraint on the distance between com and the first atom</span>
<span style="display:none;" id="data/work/plumed_ex7.datcom">The COM action with label <b>com</b> calculates something</span><b name="data/work/plumed_ex7.datd1" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.datd1","data/work/plumed_ex7.datd1","brown")'>d1</b>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<span style="display:none;" id="data/work/plumed_ex7.datd1">The DISTANCE action with label <b>d1</b> calculates the DISTANCE between this pair of atoms</span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=<b name="data/work/plumed_ex7.datd1">d1</b> <span style="background-color:yellow">__FILL__</span>
<br/><span style="color:blue" class="comment"># Add the restraint on the distance between com and the second atom</span>
<b name="data/work/plumed_ex7.datd2" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.datd2","data/work/plumed_ex7.datd2","brown")'>d2</b>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<span style="display:none;" id="data/work/plumed_ex7.datd2">The DISTANCE action with label <b>d2</b> calculates the DISTANCE between this pair of atoms</span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span>  <span style="background-color:yellow">__FILL__</span>
<br/><span style="color:blue" class="comment"># Add the restraint on the distance between com and the third atom</span>
<b name="data/work/plumed_ex7.datd3" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.datd3","data/work/plumed_ex7.datd3","brown")'>d3</b>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<span style="display:none;" id="data/work/plumed_ex7.datd3">The DISTANCE action with label <b>d3</b> calculates the DISTANCE between this pair of atoms</span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<br/><span style="color:blue" class="comment"># Add the restraint on the distance between com and the fourth atom</span>
<b name="data/work/plumed_ex7.datd4" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.datd4","data/work/plumed_ex7.datd4","brown")'>d4</b>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<span style="display:none;" id="data/work/plumed_ex7.datd4">The DISTANCE action with label <b>d4</b> calculates the DISTANCE between this pair of atoms</span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<br/><span style="color:blue" class="comment"># Add the restraint on the distance between com and the fifth atom</span>
<b name="data/work/plumed_ex7.datd5" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.datd5","data/work/plumed_ex7.datd5","brown")'>d5</b>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<span style="display:none;" id="data/work/plumed_ex7.datd5">The DISTANCE action with label <b>d5</b> calculates the DISTANCE between this pair of atoms</span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<br/><span style="color:blue" class="comment"># Add the restraint on the distance between com and the sixth atom</span>
<b name="data/work/plumed_ex7.datd6" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.datd6","data/work/plumed_ex7.datd6","brown")'>d6</b>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<span style="display:none;" id="data/work/plumed_ex7.datd6">The DISTANCE action with label <b>d6</b> calculates the DISTANCE between this pair of atoms</span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<br/><span style="color:blue" class="comment"># Add the restraint on the distance between com and the seventh atom</span>
<b name="data/work/plumed_ex7.datd7" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.datd7","data/work/plumed_ex7.datd7","brown")'>d7</b>: <span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<span style="display:none;" id="data/work/plumed_ex7.datd7">The DISTANCE action with label <b>d7</b> calculates the DISTANCE between this pair of atoms</span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>
<br/><span style="color:blue" class="comment"># Calculate the collective variables</span>
<b name="data/work/plumed_ex7.datc1" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.datc1","data/work/plumed_ex7.datc1","brown")'>c1</b>: <span class="plumedtooltip" style="color:green">COORDINATIONNUMBER<span class="right">Calculate the coordination numbers of atoms so that you can then calculate functions of the distribution of <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATIONNUMBER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">SPECIES<span class="right">the list of atoms for which the symmetry function is being calculated and the atoms that can be in the environments<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">MOMENTS<span class="right">the list of moments that you would like to calculate<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">SWITCH<span class="right">the switching function that it used in the construction of the contact matrix. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL __FILL__ }
<br/><span style="color:blue" class="comment"># Do metadynamics</span>
<span style="display:none;" id="data/work/plumed_ex7.datc1">The COORDINATIONNUMBER action with label <b>c1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c1.moment</td><td>the moments of the distribution</td></tr><tr><td width="5%">c1.value</td><td>the coordination numbers of the specified atoms</td></tr></table></span><span class="plumedtooltip" style="color:green">METAD<span class="right">Used to performed metadynamics on one or more collective variables. <a href="https://www.plumed.org/doc-master/user-doc/html/METAD" style="color:green">More details</a><i></i></span></span> ... 
   <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">HEIGHT<span class="right">the heights of the Gaussian hills<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">PACE<span class="right">the frequency for hill addition<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">SIGMA<span class="right">the widths of the Gaussian hills<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
   <span class="plumedtooltip">GRID_MIN<span class="right">the lower bounds for the grid<i></i></span></span>=-1.5,-1.5 <span class="plumedtooltip">GRID_MAX<span class="right">the upper bounds for the grid<i></i></span></span>=2.5,2.5 <span class="plumedtooltip">GRID_BIN<span class="right">the number of bins for the grid<i></i></span></span>=500,500 <span class="plumedtooltip">BIASFACTOR<span class="right">use well tempered metadynamics and use this bias factor<i></i></span></span>=5
...
</pre></div>
<div style="display:none;" id="data/work/plumed_ex7.dat_long"><pre class="plumedlisting">
<span style="color:blue" class="comment"># this optional command tells VIM that this is a PLUMED file and to colour the text accordingly</span>
<span class="plumedtooltip" style="color:blue"># vim: ft=plumed<span class="right">Enables syntax highlighting for PLUMED files in vim. See <a href="https://www.plumed.org/doc-master/user-doc/html/vim">here for more details. </a><i></i></span></span>
<br/><span style="color:blue" class="comment"># This tells PLUMED we are using Lennard Jones units</span>
<span class="plumedtooltip" style="color:green">UNITS<span class="right">This command sets the internal units for the code. <a href="https://www.plumed.org/doc-master/user-doc/html/UNITS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NATURAL<span class="right"> use natural units<i></i></span></span>
<br/><span style="color:blue" class="comment"># Calculate the position of the centre of mass.  We can then refer to this position later in the input using the label com.</span>
<span style="display:none;" id="data/work/plumed_ex7.dat_sol">The UNITS action with label <b></b> calculates something</span><span class="plumedtooltip" style="color:green">COM<span class="right">Calculate the center of mass for a group of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/COM" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the list of atoms which are involved the virtual atom's definition<i></i></span></span>=1-7 <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/work/plumed_ex7.dat_solcom" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.dat_solcom","data/work/plumed_ex7.dat_solcom","brown")'>com</b>
<br/><span style="color:blue" class="comment"># Add the restraint on the distance between com and the first atom</span>
<span style="display:none;" id="data/work/plumed_ex7.dat_solcom">The COM action with label <b>com</b> calculates something</span><span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=1,<b name="data/work/plumed_ex7.dat_solcom">com</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/work/plumed_ex7.dat_sold1" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.dat_sold1","data/work/plumed_ex7.dat_sold1","brown")'>d1</b>
<span style="display:none;" id="data/work/plumed_ex7.dat_sold1">The DISTANCE action with label <b>d1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d1.value</td><td>the DISTANCE between this pair of atoms</td></tr></table></span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=<b name="data/work/plumed_ex7.dat_sold1">d1</b> <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=2.0 <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=100.

<span style="color:blue" class="comment"># Add the restraint on the distance between com and the second atom</span>
<span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=2,<b name="data/work/plumed_ex7.dat_solcom">com</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/work/plumed_ex7.dat_sold2" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.dat_sold2","data/work/plumed_ex7.dat_sold2","brown")'>d2</b>
<span style="display:none;" id="data/work/plumed_ex7.dat_sold2">The DISTANCE action with label <b>d2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d2.value</td><td>the DISTANCE between this pair of atoms</td></tr></table></span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=<b name="data/work/plumed_ex7.dat_sold2">d2</b> <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=2.0 <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=100.

<span style="color:blue" class="comment"># Add the restraint on the distance between com and the third atom</span>
<span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=3,<b name="data/work/plumed_ex7.dat_solcom">com</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/work/plumed_ex7.dat_sold3" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.dat_sold3","data/work/plumed_ex7.dat_sold3","brown")'>d3</b>
<span style="display:none;" id="data/work/plumed_ex7.dat_sold3">The DISTANCE action with label <b>d3</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d3.value</td><td>the DISTANCE between this pair of atoms</td></tr></table></span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=<b name="data/work/plumed_ex7.dat_sold3">d3</b> <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=2.0 <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=100.

<span style="color:blue" class="comment"># Add the restraint on the distance between com and the fourth atom</span>
<span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=4,<b name="data/work/plumed_ex7.dat_solcom">com</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/work/plumed_ex7.dat_sold4" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.dat_sold4","data/work/plumed_ex7.dat_sold4","brown")'>d4</b>
<span style="display:none;" id="data/work/plumed_ex7.dat_sold4">The DISTANCE action with label <b>d4</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d4.value</td><td>the DISTANCE between this pair of atoms</td></tr></table></span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=<b name="data/work/plumed_ex7.dat_sold4">d4</b> <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=2.0 <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=100.

<span style="color:blue" class="comment"># Add the restraint on the distance between com and the fifth atom</span>
<span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=5,<b name="data/work/plumed_ex7.dat_solcom">com</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/work/plumed_ex7.dat_sold5" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.dat_sold5","data/work/plumed_ex7.dat_sold5","brown")'>d5</b>
<span style="display:none;" id="data/work/plumed_ex7.dat_sold5">The DISTANCE action with label <b>d5</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d5.value</td><td>the DISTANCE between this pair of atoms</td></tr></table></span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=<b name="data/work/plumed_ex7.dat_sold5">d5</b> <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=2.0 <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=100.

<span style="color:blue" class="comment"># Add the restraint on the distance between com and the sixth atom</span>
<span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=6,<b name="data/work/plumed_ex7.dat_solcom">com</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/work/plumed_ex7.dat_sold6" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.dat_sold6","data/work/plumed_ex7.dat_sold6","brown")'>d6</b>
<span style="display:none;" id="data/work/plumed_ex7.dat_sold6">The DISTANCE action with label <b>d6</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d6.value</td><td>the DISTANCE between this pair of atoms</td></tr></table></span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=<b name="data/work/plumed_ex7.dat_sold6">d6</b> <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=2.0 <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=100.

<span style="color:blue" class="comment"># Add the restraint on the distance between com and the seventh atom</span>
<span class="plumedtooltip" style="color:green">DISTANCE<span class="right">Calculate the distance/s between pairs of atoms. <a href="https://www.plumed.org/doc-master/user-doc/html/DISTANCE" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the pair of atom that we are calculating the distance between<i></i></span></span>=7,<b name="data/work/plumed_ex7.dat_solcom">com</b> <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/work/plumed_ex7.dat_sold7" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.dat_sold7","data/work/plumed_ex7.dat_sold7","brown")'>d7</b>
<span style="display:none;" id="data/work/plumed_ex7.dat_sold7">The DISTANCE action with label <b>d7</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">d7.value</td><td>the DISTANCE between this pair of atoms</td></tr></table></span><span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=<b name="data/work/plumed_ex7.dat_sold7">d7</b> <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=2.0 <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=100.

<span style="color:blue" class="comment"># Calculate the collective variables</span>
<b name="data/work/plumed_ex7.dat_solc1" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.dat_solc1","data/work/plumed_ex7.dat_solc1","brown")'>c1</b>: <span class="plumedtooltip" style="color:green">COORDINATIONNUMBER<span class="right">Calculate the coordination numbers of atoms so that you can then calculate functions of the distribution of <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATIONNUMBER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">SPECIES<span class="right">the list of atoms for which the symmetry function is being calculated and the atoms that can be in the environments<i></i></span></span>=1-7 <span class="plumedtooltip">MOMENTS<span class="right">the list of moments that you would like to calculate<i></i></span></span>=2-3 <span class="plumedtooltip">SWITCH<span class="right">the switching function that it used in the construction of the contact matrix. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=1.5 NN=8 MM=16}
<br/><span style="color:blue" class="comment"># Do metadynamics</span>
<span style="display:none;" id="data/work/plumed_ex7.dat_solc1">The COORDINATIONNUMBER action with label <b>c1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c1.moment</td><td>the moments of the distribution</td></tr><tr><td width="5%">c1.value</td><td>the coordination numbers of the specified atoms</td></tr></table></span><span class="plumedtooltip" style="color:green">METAD<span class="right">Used to performed metadynamics on one or more collective variables. <a href="https://www.plumed.org/doc-master/user-doc/html/METAD" style="color:green">More details</a><i></i></span></span> ... 
   <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<b name="data/work/plumed_ex7.dat_solc1">c1.*</b> <span class="plumedtooltip">HEIGHT<span class="right">the heights of the Gaussian hills<i></i></span></span>=0.05 <span class="plumedtooltip">PACE<span class="right">the frequency for hill addition<i></i></span></span>=500 <span class="plumedtooltip">SIGMA<span class="right">the widths of the Gaussian hills<i></i></span></span>=0.1,0.1 
   <span class="plumedtooltip">GRID_MIN<span class="right">the lower bounds for the grid<i></i></span></span>=-1.5,-1.5 <span class="plumedtooltip">GRID_MAX<span class="right">the upper bounds for the grid<i></i></span></span>=2.5,2.5 <span class="plumedtooltip">GRID_BIN<span class="right">the number of bins for the grid<i></i></span></span>=500,500 <span class="plumedtooltip">BIASFACTOR<span class="right">use well tempered metadynamics and use this bias factor<i></i></span></span>=5
...
</pre></div>

 {% endraw %} 
 
*Copy this input to file called plumed.dat and modify it so that it instructs PLUMED to add Gaussian kernels with a bandwidth of 0.1 in both the second and third moment of the distribution of coordination numbers and a height of 0.05* $\epsilon$ *every 
500 MD steps.  You can then use this input together with the input.xyz, and in files, you obtained from the GitHub repository to generate a metadynamics trajectory at* $k_B T = 0.1 \epsilon$ *by running the command:*

````
plumed simplemd < in
````

Once you have run the metadynamics calculations, you can post-process the output trajectory using <b> driver </b> to extract the free energy by [reweighting](https://www.notion.so/Weighted-histograms-546d0b3837ce43a3b9de0dcf7a741353).  Notice that to do block averaging, you will need to extract multiple estimates for the (weighted) histogram.  You should thus use the following input file to extract estimates of the histogram:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/work/plumed_ex8.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="plumed_ex8.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="plumed_ex8.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
<div class="headerBadge"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/work/plumed_ex8.dat")' onmousedown='toggleDisplay("data/work/plumed_ex8.dat")'/></div>
</div>
</div>
<div id="data/work/plumed_ex8.dat_short">
<pre class="plumedlisting">
<span style="color:blue" class="comment"># this optional command tells VIM that this is a PLUMED file and to colour the text accordingly</span>
<span class="plumedtooltip" style="color:blue"># vim: ft=plumed<span class="right">Enables syntax highlighting for PLUMED files in vim. See <a href="https://www.plumed.org/doc-master/user-doc/html/vim">here for more details. </a><i></i></span></span>
<br/><span class="plumedtooltip" style="color:green">UNITS<span class="right">This command sets the internal units for the code. <a href="https://www.plumed.org/doc-master/user-doc/html/UNITS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NATURAL<span class="right"> use natural units<i></i></span></span>
<br/><span style="color:blue" class="comment"># We can delete the parts of the input that specified the walls and disregard these in our </span>
<span style="color:blue" class="comment"># analysis. It is OK to do this as we are only interested in the value of the free energy </span>
<span style="color:blue" class="comment"># in parts of phase space where the bias due to these walls are not acting.</span>
<br/><span style="display:none;" id="data/work/plumed_ex8.dat">The UNITS action with label <b></b> calculates something</span><b name="data/work/plumed_ex8.datc1" onclick='showPath("data/work/plumed_ex8.dat","data/work/plumed_ex8.datc1","data/work/plumed_ex8.datc1","brown")'>c1</b>: <span class="plumedtooltip" style="color:green">COORDINATIONNUMBER<span class="right">Calculate the coordination numbers of atoms so that you can then calculate functions of the distribution of <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATIONNUMBER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">SPECIES<span class="right">the list of atoms for which the symmetry function is being calculated and the atoms that can be in the environments<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">MOMENTS<span class="right">the list of moments that you would like to calculate<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">SWITCH<span class="right">the switching function that it used in the construction of the contact matrix. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL __FILL__}
<br/><span style="color:blue" class="comment"># The metadynamics bias is restarted here so we consider the final bias as a static bias </span>
<span style="color:blue" class="comment"># in our calculations</span>
<span style="display:none;" id="data/work/plumed_ex8.datc1">The COORDINATIONNUMBER action with label <b>c1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c1.moment</td><td>the moments of the distribution</td></tr><tr><td width="5%">c1.value</td><td>the coordination numbers of the specified atoms</td></tr></table></span><span class="plumedtooltip" style="color:green">METAD<span class="right">Used to performed metadynamics on one or more collective variables. <a href="https://www.plumed.org/doc-master/user-doc/html/METAD" style="color:green">More details</a><i></i></span></span> ...
   <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">HEIGHT<span class="right">the heights of the Gaussian hills<i></i></span></span>=0.05 <span class="plumedtooltip">PACE<span class="right">the frequency for hill addition<i></i></span></span>=50000000 <span class="plumedtooltip">SIGMA<span class="right">the widths of the Gaussian hills<i></i></span></span>=0.1,0.1 
   <span class="plumedtooltip">GRID_MIN<span class="right">the lower bounds for the grid<i></i></span></span>=-1.5,-1.5 <span class="plumedtooltip">GRID_MAX<span class="right">the upper bounds for the grid<i></i></span></span>=2.5,2.5 <span class="plumedtooltip">GRID_BIN<span class="right">the number of bins for the grid<i></i></span></span>=500,500 
   <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is only needed if you are doing well-tempered metadynamics<i></i></span></span>=0.1 <span class="plumedtooltip">BIASFACTOR<span class="right">use well tempered metadynamics and use this bias factor<i></i></span></span>=5 <span class="plumedtooltip">RESTART<span class="right">allows per-action setting of restart (YES/NO/AUTO)<i></i></span></span>=YES
...
<br/><span style="color:blue" class="comment"># This adjusts the weights of the sampled configurations and thereby accounts for the </span>
<span style="color:blue" class="comment"># effect of the bias potential</span>
<b name="data/work/plumed_ex8.datrw" onclick='showPath("data/work/plumed_ex8.dat","data/work/plumed_ex8.datrw","data/work/plumed_ex8.datrw","brown")'>rw</b>: <span class="plumedtooltip" style="color:green">REWEIGHT_BIAS<span class="right">Calculate weights for ensemble averages that negate the effect the bias has on the region of phase space explored <a href="https://www.plumed.org/doc-master/user-doc/html/REWEIGHT_BIAS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">TEMP<span class="right">the system temperature<i></i></span></span>=0.1

<span style="color:blue" class="comment"># Calculate the histogram and output it to a file</span>
<span style="display:none;" id="data/work/plumed_ex8.datrw">The REWEIGHT_BIAS action with label <b>rw</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">rw.value</td><td>the weight to use for this frame to negate the effect the bias</td></tr></table></span><b name="data/work/plumed_ex8.dathh" onclick='showPath("data/work/plumed_ex8.dat","data/work/plumed_ex8.dathh","data/work/plumed_ex8.dathh","brown")'>hh</b>: <span class="plumedtooltip" style="color:green">HISTOGRAM<span class="right">Accumulate the average probability density along a few CVs from a trajectory. <a href="https://www.plumed.org/doc-master/user-doc/html/HISTOGRAM" style="color:green">More details</a><i></i></span></span> ...
   <span class="plumedtooltip">ARG<span class="right">the quantities that are being used to construct the histogram<i></i></span></span>=<b name="data/work/plumed_ex8.datc1">c1.*</b> <span class="plumedtooltip">GRID_MIN<span class="right"> the lower bounds for the grid<i></i></span></span>=-1.5,-1.5 
   <span class="plumedtooltip">GRID_MAX<span class="right"> the upper bounds for the grid<i></i></span></span>=2.5,2.5 <span class="plumedtooltip">GRID_BIN<span class="right">the number of bins for the grid<i></i></span></span>=200,200 <span class="plumedtooltip">BANDWIDTH<span class="right">the bandwidths for kernel density esimtation<i></i></span></span>=0.02,0.02 
   <span class="plumedtooltip">LOGWEIGHTS<span class="right">the logarithm of the quantity to use as the weights when calculating averages<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">CLEAR<span class="right"> the frequency with whihc to clear the data that is being averaged<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">NORMALIZATION<span class="right"> This controls how the data is normalized it can be set equal to true, false or ndata<i></i></span></span>=true
...
<span style="display:none;" id="data/work/plumed_ex8.dathh">The HISTOGRAM action with label <b>hh</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">hh.value</td><td>the estimate of the histogram as a function of the argument that was obtained</td></tr></table></span><span class="plumedtooltip" style="color:green">DUMPGRID<span class="right">Output the function on the grid to a file with the PLUMED grid format. <a href="https://www.plumed.org/doc-master/user-doc/html/DUMPGRID" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">the grid you would like to print (can also use ARG for specifying what is being printed)<i></i></span></span>=<b name="data/work/plumed_ex8.dathh">hh</b> <span class="plumedtooltip">FILE<span class="right"> the file on which to write the grid<i></i></span></span>=my_histogram.dat <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the grid should be output to the file<i></i></span></span>=2500
</pre></div>
<div style="display:none;" id="data/work/plumed_ex8.dat_long"><pre class="plumedlisting">
<span style="color:blue" class="comment"># this optional command tells VIM that this is a PLUMED file and to colour the text accordingly</span>
<span class="plumedtooltip" style="color:blue"># vim: ft=plumed<span class="right">Enables syntax highlighting for PLUMED files in vim. See <a href="https://www.plumed.org/doc-master/user-doc/html/vim">here for more details. </a><i></i></span></span>
<br/><span class="plumedtooltip" style="color:green">UNITS<span class="right">This command sets the internal units for the code. <a href="https://www.plumed.org/doc-master/user-doc/html/UNITS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">NATURAL<span class="right"> use natural units<i></i></span></span>
<br/><span style="color:blue" class="comment"># We can delete the parts of the input that specified the walls and disregard these in our </span>
<span style="color:blue" class="comment"># analysis. It is OK to do this as we are only interested in the value of the free energy </span>
<span style="color:blue" class="comment"># in parts of phase space where the bias due to these walls are not acting.</span>
<br/><span style="display:none;" id="data/work/plumed_ex8.dat_sol">The UNITS action with label <b></b> calculates something</span><b name="data/work/plumed_ex8.dat_solc1" onclick='showPath("data/work/plumed_ex8.dat","data/work/plumed_ex8.dat_solc1","data/work/plumed_ex8.dat_solc1","brown")'>c1</b>: <span class="plumedtooltip" style="color:green">COORDINATIONNUMBER<span class="right">Calculate the coordination numbers of atoms so that you can then calculate functions of the distribution of <a href="https://www.plumed.org/doc-master/user-doc/html/COORDINATIONNUMBER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">SPECIES<span class="right">the list of atoms for which the symmetry function is being calculated and the atoms that can be in the environments<i></i></span></span>=1-7 <span class="plumedtooltip">MOMENTS<span class="right">the list of moments that you would like to calculate<i></i></span></span>=2-3 <span class="plumedtooltip">SWITCH<span class="right">the switching function that it used in the construction of the contact matrix. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={RATIONAL R_0=1.5 NN=8 MM=16}
<br/><span style="color:blue" class="comment"># The metadynamics bias is restarted here so we consider the final bias as a static bias </span>
<span style="color:blue" class="comment"># in our calculations</span>
<span style="display:none;" id="data/work/plumed_ex8.dat_solc1">The COORDINATIONNUMBER action with label <b>c1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c1.moment</td><td>the moments of the distribution</td></tr><tr><td width="5%">c1.value</td><td>the coordination numbers of the specified atoms</td></tr></table></span><span class="plumedtooltip" style="color:green">METAD<span class="right">Used to performed metadynamics on one or more collective variables. <a href="https://www.plumed.org/doc-master/user-doc/html/METAD" style="color:green">More details</a><i></i></span></span> ...
   <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<b name="data/work/plumed_ex8.dat_solc1">c1.*</b> <span class="plumedtooltip">HEIGHT<span class="right">the heights of the Gaussian hills<i></i></span></span>=0.05 <span class="plumedtooltip">PACE<span class="right">the frequency for hill addition<i></i></span></span>=50000000 <span class="plumedtooltip">SIGMA<span class="right">the widths of the Gaussian hills<i></i></span></span>=0.1,0.1 
   <span class="plumedtooltip">GRID_MIN<span class="right">the lower bounds for the grid<i></i></span></span>=-1.5,-1.5 <span class="plumedtooltip">GRID_MAX<span class="right">the upper bounds for the grid<i></i></span></span>=2.5,2.5 <span class="plumedtooltip">GRID_BIN<span class="right">the number of bins for the grid<i></i></span></span>=500,500 
   <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is only needed if you are doing well-tempered metadynamics<i></i></span></span>=0.1 <span class="plumedtooltip">BIASFACTOR<span class="right">use well tempered metadynamics and use this bias factor<i></i></span></span>=5 <span class="plumedtooltip">RESTART<span class="right">allows per-action setting of restart (YES/NO/AUTO)<i></i></span></span>=YES
...
<br/><span style="color:blue" class="comment"># This adjusts the weights of the sampled configurations and thereby accounts for the </span>
<span style="color:blue" class="comment"># effect of the bias potential</span>
<b name="data/work/plumed_ex8.dat_solrw" onclick='showPath("data/work/plumed_ex8.dat","data/work/plumed_ex8.dat_solrw","data/work/plumed_ex8.dat_solrw","brown")'>rw</b>: <span class="plumedtooltip" style="color:green">REWEIGHT_BIAS<span class="right">Calculate weights for ensemble averages that negate the effect the bias has on the region of phase space explored <a href="https://www.plumed.org/doc-master/user-doc/html/REWEIGHT_BIAS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">TEMP<span class="right">the system temperature<i></i></span></span>=0.1

<span style="color:blue" class="comment"># Calculate the histogram and output it to a file</span>
<span style="display:none;" id="data/work/plumed_ex8.dat_solrw">The REWEIGHT_BIAS action with label <b>rw</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">rw.value</td><td>the weight to use for this frame to negate the effect the bias</td></tr></table></span><b name="data/work/plumed_ex8.dat_solhh" onclick='showPath("data/work/plumed_ex8.dat","data/work/plumed_ex8.dat_solhh","data/work/plumed_ex8.dat_solhh","brown")'>hh</b>: <span class="plumedtooltip" style="color:green">HISTOGRAM<span class="right">Accumulate the average probability density along a few CVs from a trajectory. <a href="https://www.plumed.org/doc-master/user-doc/html/HISTOGRAM" style="color:green">More details</a><i></i></span></span> ...
   <span class="plumedtooltip">ARG<span class="right">the quantities that are being used to construct the histogram<i></i></span></span>=<b name="data/work/plumed_ex8.dat_solc1">c1.*</b> <span class="plumedtooltip">GRID_MIN<span class="right"> the lower bounds for the grid<i></i></span></span>=-1.5,-1.5 
   <span class="plumedtooltip">GRID_MAX<span class="right"> the upper bounds for the grid<i></i></span></span>=2.5,2.5 <span class="plumedtooltip">GRID_BIN<span class="right">the number of bins for the grid<i></i></span></span>=200,200 <span class="plumedtooltip">BANDWIDTH<span class="right">the bandwidths for kernel density esimtation<i></i></span></span>=0.02,0.02 
   <span class="plumedtooltip">LOGWEIGHTS<span class="right">the logarithm of the quantity to use as the weights when calculating averages<i></i></span></span>=<b name="data/work/plumed_ex8.dat_solrw">rw</b> <span class="plumedtooltip">CLEAR<span class="right"> the frequency with whihc to clear the data that is being averaged<i></i></span></span>=2500 <span class="plumedtooltip">NORMALIZATION<span class="right"> This controls how the data is normalized it can be set equal to true, false or ndata<i></i></span></span>=true
...
<span style="display:none;" id="data/work/plumed_ex8.dat_solhh">The HISTOGRAM action with label <b>hh</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">hh.value</td><td>the estimate of the histogram as a function of the argument that was obtained</td></tr></table></span><span class="plumedtooltip" style="color:green">DUMPGRID<span class="right">Output the function on the grid to a file with the PLUMED grid format. <a href="https://www.plumed.org/doc-master/user-doc/html/DUMPGRID" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">GRID<span class="right">the grid you would like to print (can also use ARG for specifying what is being printed)<i></i></span></span>=<b name="data/work/plumed_ex8.dat_solhh">hh</b> <span class="plumedtooltip">FILE<span class="right"> the file on which to write the grid<i></i></span></span>=my_histogram.dat <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the grid should be output to the file<i></i></span></span>=2500
</pre></div>

 {% endraw %} 

Once you have filled in the blanks in this input, you can then run the calculation by using the command:

````
> plumed driver --ixyz trajectory.xyz  --initial-step 1
````

You must make sure that the HILLS file that was output by your metadynamics simulation is available in the directory where you run the above command.

For the rest of the exercise, you are on your own.  You must use what you have learned in the other parts of the tutorial to generate plots similar to those shown below.  The leftmost plot here is the 
free energy surface computed by taking the (weighted) average of the blocks, the right panel shows the size of the error bar on the free energy at each point of the free energy surface.  


![The estimate of the free energy for the Lennard Jones system (left panel) and the errors on these estimate of the free energy](figures/masterclass-21-2-fes_errors.png)

Notice that the data is correlated here so you should investigate how the error size depends on the lengths of the blocks as was discussed in exercise 7.  When I did this analysis 
I found that the error does not have a strong dependence on the size of the blocks.

![The dependence of the average error in the free energy on the size of the blocks used for the block averaging](figures/masterclass-21-2-fes_error_blocks.png) 

Finally, if you are struggling to plot the 2D free energy surface, you can generate free energy as a function of one CV only using the ideas from earlier exercises.

<em> Hint: You are now calculating weighted averages so you will need to use the code you wrote for exercise 8 to merge the histograms </em>

## Further reading

If you want to know more about good practise using PLUMED you can read [this paper](https://arxiv.org/abs/1812.08213).  We would also recommend learning about 
[kernel density estimation](https://en.wikipedia.org/wiki/Kernel_density_estimation), which will often give you smoother histograms. My full sets of notes are available here:

- [Probability theory notes](https://www.notion.so/940bd09c5be343888244beb21ed4a166?v=6bb0bd98d8fc47a081164069121ee396) 
- [Thermodynamics notes](https://www.notion.so/365db6742a81483ba82d27a3c9133eba?v=7859a0ae344042eab8ff6dab16533224)
- [Statistical Mechanics notes](https://www.notion.so/4bc79cd418674ffcb90b6730dbf94b22?v=c6499c1314624bb38869504d0111a024)
