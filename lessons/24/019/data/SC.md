# Ab-initio Metadynamics: Small Silver Cluster 

In the same way as we analyzed the toy model, we can also obtain the free energy profile using an Ab-initio calculator. In this part of the tutorial, we show how to find the free energy surface of an Ag-6 cluster presented in the paper [D. Sucerquia *et. al.*, JCP, 2022](https://doi.org/10.1063/5.0082332). There, we showed that this cluster is the smallest silver cluster where entropic effects at room temperature boost the non-planar isomer probability to a competing state. 

## Collective variables 

To obtain a proper exploration of the different states of the silver cluster, we can use the coordination number (C) and the radius of gyration (R) as collective variables. These Collective variables are defined as 

$$ 
C= \sum_{i=1}^{N_a} \sum_{j\ne i}\frac{1-(r_{ij}/d)^8}{1-(r_{ij}/d)^{16}}, 
$$ 

and 

$$ 
R= \left(\frac{\sum_i^N |{\color{black}{\bf r}}_i - {\color{black}{\bf r}}_{CM}|^2}{N_a}\right)^{1/2}, 
$$ 

where $r_i$ is the position of atom $i$, $r_{CM}$ is the center of mass of the cluster and $N_a$ is the number of atoms of the cluster. This CV gives information about how disperse the system is with respect to the center of mass. $C$ and $R$ enable extracting information about the shape of the cluster and permit differentiating the free-energy minima found by DFT optimization, which are expected to be metastable states in the free energy landscape. 

By performing short WT-MTD along these CVs, we noticed that there were isomers with broken bonds or that formed linear clusters, which are not of interest in the isomerisation process. Therefore, there are regions of the space that are thermodynamically insignificant. Considering how expensive Ab-initio calculations are, and to avoid enhancing the exploration toward these regions, we created a new set of CVs (CV1 and CV2) that are a rotation of C and R, which allow us to easily apply a constraint, as in the previous example. The rotated CVs are defined as 

$$ 
CV 1 = 0.99715 C − 0.07534Å^{−1} R 
$$ 

and 

$$ 
CV 2 = 0.07534 C + 0.99715Å^{−1} R 
$$ 

Using this CV setup for WT-MTD, we added walls using repulsive semi-harmonic potentials that act when CV1 is lower than 8 with harmonic constant 10 eV and values of CV2 greater than 3.3 with harmonic constant 50 eV. 

## Running the Simulation 

| **WARNING** | 
| --- | 
| The aim of this tutorial is to show an example of the capabilities of the ASE-PLUMED calculatory. To obtain a full reconstruction of the free energy surface, metadynamics must to run for a long time to reach convergence. This could take many hours (or even days) to be completed. The code presented here runs for 1000 time steps, which gives an estimate of the free energy surface, although real convergence cannot yet be guaranteed. For more details on how we achieved convergence in this case, check the paper [D. Sucerquia *et. al.*, JCP, 2022](https://doi.org/10.1063/5.0082332). For longer simulations, you have to change the argument of the function `run` in the last line, and you might need to use High Performance Computing in order to complete it in a feasible time.| 

You need to create a file called [`plumedSC.dat`](https://github.com/Sucerquia/ASE-PLUMED_tutorial/blob/master/files/plumedSC.dat) containing the lines, 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/SC.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="SC.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="SC.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">UNITS<div class="right">This command sets the internal units for the code. <a href="https://www.plumed.org/doc-master/user-doc/html/_u_n_i_t_s.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">LENGTH<div class="right">the units of lengths<i></i></div></div>=A <div class="tooltip">TIME<div class="right">the units of time<i></i></div></div>=0.0101805 <div class="tooltip">ENERGY<div class="right">the units of energy<i></i></div></div>=96.4853329
<span id="data/SC.md_working_1.datdefc_short"><span style="display:none;" id="data/SC.md_working_1.dat">The UNITS action with label <b></b> calculates something</span><b name="data/SC.md_working_1.datc" onclick='showPath("data/SC.md_working_1.dat","data/SC.md_working_1.datc","data/SC.md_working_1.datc","black")'>c</b><span style="display:none;" id="data/SC.md_working_1.datc">The COORDINATION action with label <b>c</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c</td><td width="5%"><font color="black">scalar</font></td><td>the value of the coordination</td></tr></table></span>: <div class="tooltip" style="color:green">COORDINATION<div class="right">Calculate coordination numbers. This action has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/SC.md_working_1.datdefc");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_o_r_d_i_n_a_t_i_o_n.html">More details</a><i></i></div></div> <div class="tooltip">GROUPA<div class="right">First list of atoms<i></i></div></div>=1-6 <div class="tooltip">GROUPB<div class="right">Second list of atoms (if empty, N*(N-1)/2 pairs in GROUPA are counted)<i></i></div></div>=1-6 <div class="tooltip">R_0<div class="right">The r_0 parameter of the switching function<i></i></div></div>=2.8
</span><span id="data/SC.md_working_1.datdefc_long" style="display:none;"><b name="data/SC.md_working_1.datc" onclick='showPath("data/SC.md_working_1.dat","data/SC.md_working_1.datc","data/SC.md_working_1.datc","black")'>c</b>: <div class="tooltip" style="color:green">COORDINATION<div class="right">Calculate coordination numbers. This action uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/SC.md_working_1.datdefc");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_o_r_d_i_n_a_t_i_o_n.html">More details</a><i></i></div></div> <div class="tooltip">GROUPA<div class="right">First list of atoms<i></i></div></div>=1-6 <div class="tooltip">GROUPB<div class="right">Second list of atoms (if empty, N*(N-1)/2 pairs in GROUPA are counted)<i></i></div></div>=1-6 <div class="tooltip">R_0<div class="right">The r_0 parameter of the switching function<i></i></div></div>=2.8  <div class="tooltip">D_0<div class="right"> The d_0 parameter of the switching function<i></i></div></div>=0.0 <div class="tooltip">NN<div class="right"> The n parameter of the switching function <i></i></div></div>=6 <div class="tooltip">MM<div class="right"> The m parameter of the switching function; 0 implies 2*NN<i></i></div></div>=0
</span><b name="data/SC.md_working_1.datr" onclick='showPath("data/SC.md_working_1.dat","data/SC.md_working_1.datr","data/SC.md_working_1.datr","black")'>r</b><span style="display:none;" id="data/SC.md_working_1.datr">The GYRATION action with label <b>r</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">r</td><td width="5%"><font color="black">scalar</font></td><td>the radius of gyration</td></tr></table></span>: <div class="tooltip" style="color:green">GYRATION<div class="right">Calculate the radius of gyration, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/_g_y_r_a_t_i_o_n.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=1-6
<b name="data/SC.md_working_1.datrrot" onclick='showPath("data/SC.md_working_1.dat","data/SC.md_working_1.datrrot","data/SC.md_working_1.datrrot","black")'>rrot</b><span style="display:none;" id="data/SC.md_working_1.datrrot">The COMBINE action with label <b>rrot</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">rrot</td><td width="5%"><font color="black">scalar</font></td><td>a linear compbination</td></tr></table></span>: <div class="tooltip" style="color:green">COMBINE<div class="right">Calculate a polynomial combination of a set of other variables. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_m_b_i_n_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/SC.md_working_1.datc">c</b>,<b name="data/SC.md_working_1.datr">r</b> <div class="tooltip">COEFFICIENTS<div class="right"> the coefficients of the arguments in your function<i></i></div></div>=0.07534,0.99715 <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
<b name="data/SC.md_working_1.datcrot" onclick='showPath("data/SC.md_working_1.dat","data/SC.md_working_1.datcrot","data/SC.md_working_1.datcrot","black")'>crot</b><span style="display:none;" id="data/SC.md_working_1.datcrot">The COMBINE action with label <b>crot</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">crot</td><td width="5%"><font color="black">scalar</font></td><td>a linear compbination</td></tr></table></span>: <div class="tooltip" style="color:green">COMBINE<div class="right">Calculate a polynomial combination of a set of other variables. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_m_b_i_n_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/SC.md_working_1.datc">c</b>,<b name="data/SC.md_working_1.datr">r</b> <div class="tooltip">COEFFICIENTS<div class="right"> the coefficients of the arguments in your function<i></i></div></div>=0.99715,-0.07534 <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
<div class="tooltip" style="color:green">UPPER_WALLS<div class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/_u_p_p_e_r__w_a_l_l_s.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the arguments on which the bias is acting<i></i></div></div>=<b name="data/SC.md_working_1.datrrot">rrot</b> <div class="tooltip">AT<div class="right">the positions of the wall<i></i></div></div>=3.3 <div class="tooltip">KAPPA<div class="right">the force constant for the wall<i></i></div></div>=50
<div class="tooltip" style="color:green">LOWER_WALLS<div class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/_l_o_w_e_r__w_a_l_l_s.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the arguments on which the bias is acting<i></i></div></div>=<b name="data/SC.md_working_1.datcrot">crot</b> <div class="tooltip">AT<div class="right">the positions of the wall<i></i></div></div>=8 <div class="tooltip">KAPPA<div class="right">the force constant for the wall<i></i></div></div>=10
<div class="tooltip" style="color:green">METAD<div class="right">Used to performed metadynamics on one or more collective variables. <a href="https://www.plumed.org/doc-master/user-doc/html/_m_e_t_a_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the scalars on which the bias will act<i></i></div></div>=<b name="data/SC.md_working_1.datcrot">crot</b>,<b name="data/SC.md_working_1.datrrot">rrot</b> <div class="tooltip">SIGMA<div class="right">the widths of the Gaussian hills<i></i></div></div>=0.3,0.03 <div class="tooltip">HEIGHT<div class="right">the heights of the Gaussian hills<i></i></div></div>=0.2 <div class="tooltip">PACE<div class="right">the frequency for hill addition<i></i></div></div>=100 <div class="tooltip">BIASFACTOR<div class="right">use well tempered metadynamics and use this bias factor<i></i></div></div>=100 <div class="tooltip">FILE<div class="right"> a file in which the list of added hills is stored<i></i></div></div>=HILLS
<div class="tooltip" style="color:green">FLUSH<div class="right">This command instructs plumed to flush all the open files with a user specified frequency. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_l_u_s_h.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">STRIDE<div class="right">the frequency with which all the open files should be flushed<i></i></div></div>=100
</pre>
 {% endraw %} 

Once this file is created, we can start the simulation from one of the DFT-optimized configurations, here called [isomerSC.xyz](https://github.com/Sucerquia/ASE-PLUMED_tutorial/blob/master/files/isomerSC.xyz). Note that for this part of the tutorial you need to set up [GPAW](https://gpaw.readthedocs.io/), which is a DFT code. You can choose the QM code that you prefer. This can be done as shown in the file [MTD-SC.py](https://github.com/Sucerquia/ASE-PLUMED_tutorial/blob/master/files/MTD-SC.py): 

``` python 
from ase.md.velocitydistribution import MaxwellBoltzmannDistribution 
from ase.md.nvtberendsen import NVTBerendsen 
from gpaw import MixerDif, FermiDirac, GPAW 
from ase.calculators.plumed import Plumed 
from ase.io import read 
from ase import Atoms 
from ase import units 


pos = read("isomerSC.xyz").get_positions() 

setup = open("plumedSC.dat", "r").read().splitlines() 

T = 100 
timestep = 5 * units.fs 
taut = 50 * units.fs 

atoms = Atoms('Ag6', pos) 

MaxwellBoltzmannDistribution(atoms, temperature_K=T) 

p = atoms.get_momenta() 
psum = p.sum(axis=0) / float(len(p)) 
p = p - psum 
atoms.set_momenta(p) 

a = 16 

atoms.set_cell([a, a, a]) 
atoms.set_pbc(True) 
atoms.center() 

atoms.calc = Plumed(GPAW(h=0.2, 
mode='lcao', 
basis='pvalence.dz', 
xc='PBE', 
spinpol=True, 
nbands=-4, 
occupations=FermiDirac(0.05), 
parallel=dict(augment_grids=True), 
mixer=MixerDif(beta=0.25, nmaxold=3, weight=50.0), 
symmetry='off'), 
input=setup, 
timestep=timestep, 
atoms=atoms, 
kT=units.kB*T) 

dyn = NVTBerendsen(atoms, timestep, temperature_K=T, taut=taut, fixcm=False, 
trajectory='trajectory.traj') 

dyn.run(1000) 
``` 

After running this same code but changing the temperature and the number of time steps, you can obtain the free energy surfaces shown in Figure 4. 

<div align="center"> 
<img src="./files/Ag6-FES.png" width="500"> 
</div> 

**Figure 4.** Free energy surface of a Ag6 cluster at three different temperatures. 