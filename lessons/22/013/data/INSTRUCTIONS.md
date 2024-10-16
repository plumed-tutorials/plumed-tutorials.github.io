# PLUMED Masterclass 22.13: SASA module and the application of PLUMED for implicit solvent simulations 

## Origin 

This masterclass was authored by Andrea Arsiccio on September 12, 2022 

## Aims 

This Masterclass is an introduction to the use of the SASA module of Plumed for the execution of implicit solvent simulations. 

## Objectives 

The objectives of this Masterclass are: 
- Learn how the SASA module of PLUMED works 
- Learn how to run an implicit solvent simulation of a protein using PLUMED 
- Learn how to introduce the effect of temperature, pressure and osmolytes on protein stability in implicit solvent simulations 
- Understand the advantages and limitations of implicit solvent simulations using PLUMED 

## Prerequisites 

We assume that the person that will follow this tutorial is familiar with the Linux terminal, AMBER and basic functionality of PLUMED. 
Knowledge of the metadynamics enhanced sampling technique is recommended. 
Familiarity with gnuplot and xmgrace (or python with matplotlib) is recommended. 

## Setting up PLUMED 

We will use AMBER and PLUMED to perform the calculations. 
Conda packages with the software required for this class have been prepared and you can install them following the instructions in [this link](https://github.com/plumed/masterclass-2022). 
Make sure to install the conda package for AMBER. 

If you are compiling PLUMED on your own, you will need to install the SASA module manually by adding '--enable-modules=sasa' to your './configure' command when building PLUMED. 

The data needed to run the exercises of this Masterclass can be found on [GitHub](https://github.com/andrea-arsiccio/masterclass-22-13). 
You can clone this repository locally on your machine using the following command: 

```` 
git clone https://github.com/andrea-arsiccio/masterclass-22-13 
```` 

You will also need a python script for the calculation of free energies of transfer, available on [GitHub] (https://github.com/andrea-arsiccio/DeltaG-calculation). 

## Summary of theory 

The SASA module contains methods for the calculation of the solvent accessible surface area (SASA) of proteins. 
It can be used to include the SASA as a collective variable in metadynamics simulations, and for implicit solvent simulations. 

There are two SASA functions that could be used: 

SASA_HASEL: computates the SASA using the algorithm described [here](https://www.sciencedirect.com/science/article/abs/pii/0898552988900152) 

SASA_LCPO: computes the SASA using the algorithm described [here](https://onlinelibrary.wiley.com/doi/10.1002/%28SICI%291096-987X%2819990130%2920%3A2%3C217%3A%3AAID-JCC4%3E3.0.CO%3B2-A) 

The algorithm by Hasel et al. is about 2 to 3 times faster than the LCPO (linear combination of pairwise overlaps) algorithm, but slightly less accurate. Both algorithms have the advantage that apply simple analytical functions for the computation of the SASA, and because of this it is easy to compute their derivative, which is a necessary step to apply a bias based on the SASA to a molecular dynamics simulation. 

The atoms for which the SASA is desired should be indicated with the keyword ATOMS, and a pdb file of the protein must be provided in input with the [MOLINFO](https://www.plumed.org/doc-master/user-doc/html/_m_o_l_i_n_f_o.html) keyword. Two types of calculations are possible: 

TOTAL: the total SASA is computed, which is the desired type of calculation if one wants to use the SASA as a CV in metadynamics simulations. 

TRANSFER: in this case the free energy of transfer for the protein is computed according to the transfer model (TRANSFER). This keyword can be used, for instance, to compute: 

1. The transfer of a protein to different temperatures as in [this paper](https://pubs.acs.org/doi/abs/10.1021/acs.jpcb.1c01694) 
2. The transfer of a protein to different pressures as in [this paper](https://pubs.acs.org/doi/abs/10.1021/acs.jpcb.1c04398) 
3. The transfer of a protein to different osmolyte solutions as in [this paper](https://pubs.acs.org/doi/abs/10.1021/acs.jpcb.2c00889) 

Using the protein SASA as a CV in metadynamics simulations, or monitoring the SASA on the fly during the simulation or while postprocessing a trajectory, is straightforward. The user, after having enabled the SASA module, can use the SASA functions mentioned above similarly to any other CV in PLUMED. 

For instance, the following input tells plumed to print the total SASA for atoms 10 to 20 in a protein chain: 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/INSTRUCTIONS.md_working_1.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="INSTRUCTIONS.md_working_1.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="INSTRUCTIONS.md_working_1.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">SASA_HASEL<div class="right">Calculates the solvent accessible surface area (SASA) of a protein molecule, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/_s_a_s_a__h_a_s_e_l.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">TYPE<div class="right"> The type of calculation you want to perform<i></i></div></div>=TOTAL <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the SASA for<i></i></div></div>=10-20 <div class="tooltip">NL_STRIDE<div class="right">The frequency with which the neighbor list for the calculation of SASA is updated<i></i></div></div>=10 <div class="tooltip">LABEL<div class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_1.datsasa" onclick='showPath("data/INSTRUCTIONS.md_working_1.dat","data/INSTRUCTIONS.md_working_1.datsasa","data/INSTRUCTIONS.md_working_1.datsasa","black")'>sasa</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_1.datsasa">The SASA_HASEL action with label <b>sasa</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">sasa</td><td width="5%"><font color="black">scalar</font></td><td>the solvent accessible surface area (SASA) of the molecule</td></tr></table></span>
<div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_1.datsasa">sasa</b> <div class="tooltip">STRIDE<div class="right"> the frequency with which the quantities of interest should be output<i></i></div></div>=1 <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=colvar
</pre>
 {% endraw %} 

This tutorial will focus on the use of the SASA module for running implicit solvent simulations with PLUMED. 
In implicit solvent simulations, the solvent is not any more described at atomistic/coarse-grained level, but is instead treated as a continuum and described as a mean field. The advantages are that the absence of the solvent degrees of freedom alleviates the computational cost, and the absence of viscous friction accelerates the exploration of the protein conformational space. However, the solvent effects are described less accurately. 
The degree of accuracy can be improved by using the concept of free energy of transfer, which is at the basis of the SASA module. 

The common implementation of implicit solvent simulations relies on the computation of the free energy of a protein as the sum of three contributions: 

$$ 
G^{tot}= E^{vac}+G^{np}+G^{el} 
$$ 

where $E^{vac}$ is the molecule's energy in vacuum, which is the sum of internal contributions (bond and angle stretching, dihedral angles interactions) and van der Waals energy terms. $G^{np}$ is the non-polar solvation contribution, i.e., the free energy of solvation for a molecule from which all charges have been removed. $G^{el}$ is the electrostatic part, calculated as the free energy for turning on the partial charges in solution. This approach has been developed to describe (implicitly) the solvation of a protein in pure water, at ambient temperature (298 K) and pressure (1 atm). 

The idea behind the SASA module is the addition of a free energy of transfer term $G^{tr}(T,P,c)$: 

$$ 
G^{tot}= E^{vac}+G^{np}+G^{el}+G^{tr}(T,P,c) 
$$ 

that describes the transfer of the protein to any given temperature $T$, pressure $P$ and concentration $c$ of an osmolyte. 

The free energy of transfer term has the following functional form: 

$$ 
G^{tr} = \sum_{j=1}^{n} g^{tr}_{j,sc} \alpha_{j,sc} +g^{tr}_{bb}\sum_{j=1}^{n} \alpha_{j, bb} 
$$ 

where $n$ is the number of residues in the protein and the global transfer free energy is obtained by summing the contributions ($g^{tr}$) given by the amino acid side chains (subscript sc) and by the peptide backbone (subscript bb). 

Each contribution is weighed by the fractional solvent accessible surface area $SASA_{j}$ of residue $j$, 

$$ 
\alpha_{j}=\frac{SASA_{j}}{SASA_{j, Gly-X-Gly}} 
$$ 

where $SASA_{j, Gly-X-Gly}$ is the solvent accessibility of amino acid X in the tripeptide Gly-X-Gly, and X is the amino acid residue type $j$. 

The amino acid side chains and peptide backbone contributions to the transfer free energy are computed according to the mathematical derivation described in the papers above. 

Briefly, the tranfer free energy contributions describing the effect of temperatures have been derived by downloading a large set of Protein Data Bank (pdb) files resolved by nuclear magnetic resonance at different temperatures, and by computing the probability of different side chains/backbone groups to be surface exposed at different temperatures. 
The relation between energy and probability has then been exploited to compute the free energy of transfer contributions as a function of temperature. 

The transfer free energy terms describing the effect of pressure have been obtained by computing three different contributions for each side chain/backbone group: 1) the elimination of a consistent fraction of the void volumes that are present within the native state upon unfolding, 2) the volume reduction of bound water molecules due to the increased SASA of a protein upon unfolding, and 3) the stabilizing excluded volume effect of a denser solvent. 

Finally, the transfer free energy contributions as function of osmolyte type/concentrations have been obtained from experimental works, where solubility measurements of protein amino acids/peptide backbone models have been conducted in different osmolyte solutions and exploited to extract the difference in chemical potential between water and the osmolyte solution itself. 

The interested user is invited to read the original works on this topic, which are included in the graph illustrating this tutorial, for a better understanding of the theory behind the free energy of transfer contributions. 

When the TRANSFER keyword is used, a file with the free energy of transfer values ($g^{tr}$) for the sidechains and backbone atoms should be provided (using the keyword DELTAGFILE). Such file should have the following format: 

``` 

----------------Sample DeltaG.dat file--------------------- 
ALA 0.711019999999962 
ARG -2.24832799999996 
ASN -2.74838799999999 
ASP -2.5626376 
CYS 3.89864000000006 
GLN -1.76192 
GLU -2.38664400000002 
GLY 0 
HIS -3.58152799999999 
ILE 2.42634399999986 
LEU 1.77233599999988 
LYS -1.92576400000002 
MET -0.262827999999956 
PHE 1.62028800000007 
PRO -2.15598800000001 
SER -1.60934800000004 
THR -0.591559999999987 
TRP 1.22936000000027 
TYR 0.775547999999958 
VAL 2.12779200000011 
BACKBONE 1.00066920000002 
----------------------------------------------------------- 
```` 

where the second column is the free energy of transfer for each sidechain/backbone, in kJ/mol. 

A Python script for the computation of free energy of transfer values to describe the effect of osmolyte concentration, temperature and pressure (using ideas from the papers that are cited above) is freely available on [GitHub](https://github.com/andrea-arsiccio/DeltaG-calculation). The script automatically outputs a DeltaG.dat file compatible with the SASA module. Please have a look at the README file of this script to better understand its usage. 

For instance, the following input tells plumed to compute the transfer free energy for the protein chain containing atoms 10 to 20. Such transfer free energy is then used as a bias in the simulation (e.g., implicit solvent simulations). The free energy of transfer values are read from a file called DeltaG.dat: 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/INSTRUCTIONS.md_working_2.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="INSTRUCTIONS.md_working_2.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="INSTRUCTIONS.md_working_2.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">SASA_HASEL<div class="right">Calculates the solvent accessible surface area (SASA) of a protein molecule, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/_s_a_s_a__h_a_s_e_l.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">TYPE<div class="right"> The type of calculation you want to perform<i></i></div></div>=TRANSFER <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the SASA for<i></i></div></div>=10-20 <div class="tooltip">NL_STRIDE<div class="right">The frequency with which the neighbor list for the calculation of SASA is updated<i></i></div></div>=10 <div class="tooltip">DELTAGFILE<div class="right">a file containing the free energy of transfer values for backbone and sidechains atoms<i></i></div></div>=DeltaG.dat <div class="tooltip">LABEL<div class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_2.datsasa" onclick='showPath("data/INSTRUCTIONS.md_working_2.dat","data/INSTRUCTIONS.md_working_2.datsasa","data/INSTRUCTIONS.md_working_2.datsasa","black")'>sasa</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_2.datsasa">The SASA_HASEL action with label <b>sasa</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">sasa</td><td width="5%"><font color="black">scalar</font></td><td>the solvent accessible surface area (SASA) of the molecule</td></tr></table></span>
<br/><b name="data/INSTRUCTIONS.md_working_2.datbias" onclick='showPath("data/INSTRUCTIONS.md_working_2.dat","data/INSTRUCTIONS.md_working_2.datbias","data/INSTRUCTIONS.md_working_2.datbias","black")'>bias</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_2.datbias">The BIASVALUE action with label <b>bias</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">bias.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">bias.sasa_bias</td><td width="5%"><font color="black">scalar</font></td><td>one or multiple instances of this quantity can be referenced elsewhere in the input file. these quantities will named with  the arguments of the bias followed by the character string _bias. These quantities tell the user how much the bias is due to each of the colvars. This particular component measures this quantity for the input CV named sasa</td></tr></table></span>: <div class="tooltip" style="color:green">BIASVALUE<div class="right">Takes the value of one variable and use it as a bias <a href="https://www.plumed.org/doc-master/user-doc/html/_b_i_a_s_v_a_l_u_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the scalar/vector arguments whose values will be used as a bias on the system<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_2.datsasa">sasa</b>
<br/><div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_2.datsasa">sasa</b>,<b name="data/INSTRUCTIONS.md_working_2.datbias">bias</b> <div class="tooltip">STRIDE<div class="right"> the frequency with which the quantities of interest should be output<i></i></div></div>=1 <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=colvar
</pre>
 {% endraw %} 

If the DELTAGFILE is not provided, the SASA module computes the free energy of transfer values as if they had to take into account the effect of temperature according to approaches 2 or 3 (they differ in the mathematical model employed to extract free energies of transfer) in the paper about using SASA with temperature. Please read and cite this paper if using the transfer model for computing the effect of temperature in implicit solvent simulations. For this purpose, the keyword APPROACH should be added, and set to either 2 or 3, as exemplified in the following input: 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/INSTRUCTIONS.md_working_3.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="INSTRUCTIONS.md_working_3.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="INSTRUCTIONS.md_working_3.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">SASA_HASEL<div class="right">Calculates the solvent accessible surface area (SASA) of a protein molecule, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/_s_a_s_a__h_a_s_e_l.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">TYPE<div class="right"> The type of calculation you want to perform<i></i></div></div>=TRANSFER <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the SASA for<i></i></div></div>=10-20 <div class="tooltip">NL_STRIDE<div class="right">The frequency with which the neighbor list for the calculation of SASA is updated<i></i></div></div>=10 <div class="tooltip">APPROACH<div class="right">either approach 2 or 3<i></i></div></div>=2 <div class="tooltip">LABEL<div class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_3.datsasa" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datsasa","data/INSTRUCTIONS.md_working_3.datsasa","black")'>sasa</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datsasa">The SASA_HASEL action with label <b>sasa</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">sasa</td><td width="5%"><font color="black">scalar</font></td><td>the solvent accessible surface area (SASA) of the molecule</td></tr></table></span>
<br/><b name="data/INSTRUCTIONS.md_working_3.datbias" onclick='showPath("data/INSTRUCTIONS.md_working_3.dat","data/INSTRUCTIONS.md_working_3.datbias","data/INSTRUCTIONS.md_working_3.datbias","black")'>bias</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_3.datbias">The BIASVALUE action with label <b>bias</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">bias.bias</td><td width="5%"><font color="black">scalar</font></td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">bias.sasa_bias</td><td width="5%"><font color="black">scalar</font></td><td>one or multiple instances of this quantity can be referenced elsewhere in the input file. these quantities will named with  the arguments of the bias followed by the character string _bias. These quantities tell the user how much the bias is due to each of the colvars. This particular component measures this quantity for the input CV named sasa</td></tr></table></span>: <div class="tooltip" style="color:green">BIASVALUE<div class="right">Takes the value of one variable and use it as a bias <a href="https://www.plumed.org/doc-master/user-doc/html/_b_i_a_s_v_a_l_u_e.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the scalar/vector arguments whose values will be used as a bias on the system<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_3.datsasa">sasa</b>
<br/><div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_3.datsasa">sasa</b>,<b name="data/INSTRUCTIONS.md_working_3.datbias">bias</b> <div class="tooltip">STRIDE<div class="right"> the frequency with which the quantities of interest should be output<i></i></div></div>=1 <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=colvar
</pre>
 {% endraw %} 

## The system: Refolding of a model peptide 

For this tutorial we will work on a model peptide called $(AAQAA)\_3$. $(AAQAA)\_3$ is a short peptide with known $\alpha$-helix structure. 
We will simulate this peptide starting from an unfolded conformation, and we will see in which conditions (of temperature, pressure, and solution composition) it folds back to a $\alpha$-helix, and which conditions promote instead an unfolded conformation. 

[Starting (unfolded) conformation of the model peptide used for the simulations](figs/masterclass-22-13-aaqaa_min.png) 

We will perform the simulations in implicit solvent, using the AMBER ff03 force field. 

For this tutorial, the following conditions will be explored: 

1. 298 K, 1 bar, 0 M 
2. 228 K (approach 2 in [this paper](https://pubs.acs.org/doi/abs/10.1021/acs.jpcb.1c01694)), 1 bar, 0 M 
3. 348 K (approach 2 in [this paper](https://pubs.acs.org/doi/abs/10.1021/acs.jpcb.1c01694)), 1 bar, 0 M 
4. 298 K, 1 bar, 10 M urea 
5. 298 K, 3 kbar, 0 M 

Each simulation will be performed for 5 ns. 

## Exercise 1: Simulation 1 at 298 K, 1 bar and 0 M osmolyte concentration 

For the exercises, we will need PLUMED and AMBER. For this purpose, you should first proceed to their installation using the provided conda packages: 

```` 
#install the PLUMED environment 
conda create --name plumed-masterclass-2022 
conda activate plumed-masterclass-2022 
conda install -c conda-forge plumed py-plumed numpy pandas matplotlib notebook mdtraj mdanalysis git 


#install the AMBER environment 
conda create --name plumed-masterclass-2022-amber 
conda activate plumed-masterclass-2022-amber 
conda install -c conda-forge ambertools 


#stack the two environments together 
conda activate plumed-masterclass-2022 
conda activate --stack plumed-masterclass-2022-amber 
export PLUMED_KERNEL=/your_path_here/plumed-masterclass-2022/lib/libplumedKernel.so 
```` 

Then, you should download the folder with the input files for the exercises using the following command: 

```` 
git clone https://github.com/andrea-arsiccio/masterclass-22-13 
```` 

In order to perform exercise 1, cd to the folder SASA_module/01_298K. There you will find a number of files: 

-aaqaa.prmtop: a topology file of the protein, described according to the AMBER ff03 force field. 

-AAQAA_298.in: an input file for running the simulation through AMBER. I will go more in detail over this file in the following. 

-aaqaa_min.ncrst/aaqaa_min.pdb: configuration files for the (unfolded) protein, which we will use as starting point for our simulations. 

-histograms.py/picture_rg_alpha.gnu/script_rg_alpha.bash: files that we will use for the analyses and postprocessing of our trajectories. 

-plumed.dat: PLUMED input file. I will go more in detail over this in the following. 

The AAQAA_298.in file is an input AMBER file for carrying out our implicit solvent simulation, and it has the following aspect: 

```` 
MD Generalise Born, no cut off 
&cntrl 
imin = 0, 
igb = 5, gbsa = 1, extdiel = 78.4, ntpr = 1000, ntwx = 1000, ntwr = 1000, 
ntt = 3, gamma_ln = 1.0, ig = -1, nscm = 500, 
tempi = 298.0, temp0 = 298.0, 
nstlim = 2500000, dt = 0.002, ntc = 2, ntf = 2, 
cut = 9999.0, plumed = 1, plumedfile = 'plumed.dat' 
/ 
```` 

where the different commands have the following meaning: 

- imin = 0: we are running an MD simulation without performing energy minimization 
- igb = 5: we are using the model described [here](https://doi.org/10.1002/prot.20033) for computing the electrostatic interactions $G^{el}$ 
- gbsa = 1: the $G^{np}$ term is also computed 
- extdiel = 78.4: the dielectric constant of the solvent 
- ntpr = 1000: we print energy info every 1000 steps 
- ntwx = 1000: we print coordinates every 1000 steps 
- ntwr = 1000: we print the restart file every 1000 steps 
- ntt = 3: we apply Langevin dynamics 
- gamma_ln = 1.0: we set the collision frequency for Langevin dynamics 
- ig = -1: seed for pseudo-random number generator. -1 means that the random seed will be based on the current date and time 
- nscm = 500: translational/rotational [COM](https://www.plumed.org/doc-master/user-doc/html/_c_o_m.html) motions will be removed every 500 steps 
- tempi = 298.0: initial temperature 
- temp0 = 298.0: reference temperature at which the system is to be kept 
- nstlim = 2500000: we will run the system for 2500000 steps 
- dt = 0.002: we will apply a 2 fs time step 
- ntc = 2: we will constrain bonds linking to a hydrogen 
- ntf = 2: bond interactions involving H-atoms will be omitted in force evaluations 
- cut = 9999.0: no cut off will be applied for nonbonded interactions 
- plumed = 1: we will run PLUMED together with AMBER 
- plumedfile = 'plumed.dat': the PLUMED file to read is called plumed.dat 

The PLUMED input file plumed.dat has, instead, the following aspect: 

{% raw %}
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/INSTRUCTIONS.md_working_4.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="INSTRUCTIONS.md_working_4.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="INSTRUCTIONS.md_working_4.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></td></tr></table></div></div>
<pre style="width=97%;">
<div class="tooltip" style="color:green">MOLINFO<div class="right">This command is used to provide information on the molecules that are present in your system. <a href="https://www.plumed.org/doc-master/user-doc/html/_m_o_l_i_n_f_o.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">MOLTYPE<div class="right"> what kind of molecule is contained in the pdb file - usually not needed since protein/RNA/DNA are compatible<i></i></div></div>=protein <div class="tooltip">STRUCTURE<div class="right">a file in pdb format containing a reference structure<i></i></div></div>=aaqaa_min.pdb
<br/><span style="color:blue" class="comment"># radius of gyration</span>
<span style="display:none;" id="data/INSTRUCTIONS.md_working_4.dat">The MOLINFO action with label <b></b> calculates something</span><b name="data/INSTRUCTIONS.md_working_4.datrgyr" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datrgyr","data/INSTRUCTIONS.md_working_4.datrgyr","black")'>rgyr</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datrgyr">The GYRATION action with label <b>rgyr</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">rgyr</td><td width="5%"><font color="black">scalar</font></td><td>the radius of gyration</td></tr></table></span>: <div class="tooltip" style="color:green">GYRATION<div class="right">Calculate the radius of gyration, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/_g_y_r_a_t_i_o_n.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">TYPE<div class="right"> The type of calculation relative to the Gyration Tensor you want to perform<i></i></div></div>=RADIUS <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=1-174
<br/><span style="color:blue" class="comment"># antiparallel beta</span>
<span id="data/INSTRUCTIONS.md_working_4.datab_short"><span id="data/INSTRUCTIONS.md_working_4.datdefab_short"><b name="data/INSTRUCTIONS.md_working_4.datab" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datab","data/INSTRUCTIONS.md_working_4.datab_shortcut","blue")'>ab</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datab_shortcut">The ANTIBETARMSD action with label <b>ab</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">ab</td><td width="5%"><font color="blue">vector</font></td><td>if LESS_THAN is present the RMSD distance between each residue and the ideal antiparallel beta sheet.  If LESS_THAN is not present the number of residue segments where the structure is similar to an anti parallel beta sheet</td></tr><tr><td width="5%">ab_lessthan</td><td width="5%"><font color="black">scalar</font></td><td>the number blocks of residues that have an RMSD from the secondary structure that is less than the threshold</td></tr></table></span>: <div class="tooltip" style="color:green">ANTIBETARMSD<div class="right">Probe the antiparallel beta sheet content of your protein structure. This action is <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datab");'>a shortcut</a> and it has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datdefab");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_a_n_t_i_b_e_t_a_r_m_s_d.html">More details</a><i></i></div></div> <div class="tooltip">RESIDUES<div class="right">this command is used to specify the set of residues that could conceivably form part of the secondary structure<i></i></div></div>=all <div class="tooltip">LESS_THAN<div class="right">calculate the number of a residue segments that are within a certain target distance of this secondary structure type<i></i></div></div>={RATIONAL R_0=0.08 NN=8 MM=12} <div class="tooltip">STRANDS_CUTOFF<div class="right">If in a segment of protein the two strands are further apart then the calculation of the actual RMSD is skipped as the structure is very far from being beta-sheet like<i></i></div></div>=1
</span><span id="data/INSTRUCTIONS.md_working_4.datdefab_long" style="display:none;"><b name="data/INSTRUCTIONS.md_working_4.datab" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datab","data/INSTRUCTIONS.md_working_4.datab_shortcut","blue")'>ab</b>: <div class="tooltip" style="color:green">ANTIBETARMSD<div class="right">Probe the antiparallel beta sheet content of your protein structure. This action is <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datab");'>a shortcut</a> and uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datdefab");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_a_n_t_i_b_e_t_a_r_m_s_d.html">More details</a><i></i></div></div> <div class="tooltip">RESIDUES<div class="right">this command is used to specify the set of residues that could conceivably form part of the secondary structure<i></i></div></div>=all <div class="tooltip">LESS_THAN<div class="right">calculate the number of a residue segments that are within a certain target distance of this secondary structure type<i></i></div></div>={RATIONAL R_0=0.08 NN=8 MM=12} <div class="tooltip">STRANDS_CUTOFF<div class="right">If in a segment of protein the two strands are further apart then the calculation of the actual RMSD is skipped as the structure is very far from being beta-sheet like<i></i></div></div>=1  <div class="tooltip">STYLE<div class="right"> Antiparallel beta sheets can either form in a single chain or from a pair of chains<i></i></div></div>=all <div class="tooltip">TYPE<div class="right"> the manner in which RMSD alignment is performed<i></i></div></div>=DRMSD
</span></span><span id="data/INSTRUCTIONS.md_working_4.datab_long" style="display:none;"><span style="color:blue" class="comment"># PLUMED interprets the command:
</span><span class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datab")'># ab: ANTIBETARMSD RESIDUES=all LESS_THAN={RATIONAL R_0=0.08 NN=8 MM=12} STRANDS_CUTOFF=1</span>
<span style="color:blue" class="comment"># as follows (Click the red comment above to revert to the short version of the input):</span>
<b name="data/INSTRUCTIONS.md_working_4.datab" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datab","data/INSTRUCTIONS.md_working_4.datab","blue")'>ab</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datab">The SECONDARY_STRUCTURE_RMSD action with label <b>ab</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">ab</td><td width="5%"><font color="blue">vector</font></td><td>a vector containing the rmsd distance between each of the residue segments and the reference structure</td></tr></table></span>: <div class="tooltip" style="color:green">SECONDARY_STRUCTURE_RMSD<div class="right">Calclulate the distance between segments of a protein and a reference structure of interest <a href="https://www.plumed.org/doc-master/user-doc/html/_s_e_c_o_n_d_a_r_y__s_t_r_u_c_t_u_r_e__r_m_s_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">BONDLENGTH<div class="right">the length to use for bonds<i></i></div></div>=0.17 <div class="tooltip">ATOMS<div class="right">this is the full list of atoms that we are investigating<i></i></div></div>=1,5,7,11,12,13,15,17,21,22,23,25,27,38,39,40,42,44,48,49,50,52,54,58,59,60,62,64,68,69,70,72,74,78,79,80,82,84,95,96,97,99,101,105,106,107,109,111,115,116,117,119,121,125,126,127,129,131,135,136,137,139,141,152,153,154,156,158,162,163,164,166,168,172,173 <div class="tooltip">TYPE<div class="right"> the manner in which RMSD alignment is performed<i></i></div></div>=DRMSD <div class="tooltip">STRANDS_CUTOFF<div class="right">If in a segment of protein the two strands are further apart then the calculation of the actual RMSD is skipped as the structure is very far from being beta-sheet like<i></i></div></div>=1 <div class="tooltip">SEGMENT1<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39 <div class="tooltip">SEGMENT2<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44 <div class="tooltip">SEGMENT3<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49 <div class="tooltip">SEGMENT4<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54 <div class="tooltip">SEGMENT5<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59 <div class="tooltip">STRUCTURE1<div class="right">the reference structure<i></i></div></div>=2.263,-3.795,1.722,2.493,-2.426,2.263,3.847,-1.838,1.761,1.301,-1.517,1.921,0.852,-1.504,0.739,0.818,-0.738,2.917,-0.299,0.243,2.748,-1.421,-0.076,3.757,0.273,1.68,2.854,0.902,1.993,3.888,0.119,2.532,1.813,0.683,3.916,1.68,1.58,3.94,0.395,-0.394,5.011,1.63,-1.459,4.814,0.982,-2.962,3.559,-1.359,-2.439,2.526,-2.287,-1.189,3.006,-3.087,-2.081,1.231,-1.52,-1.524,1.324,-0.409,-2.326,0.037,-2.095,-1.858,-1.269,-1.554,-3.053,-2.199,-1.291,-0.869,-1.949,-2.512,-1.255,-2.07,-3.71,0.326,-2.363,-2.072,1.405,-2.992,-2.872,2.699,-2.129,-2.917,1.745,-4.399,-2.33,1.899,-4.545,-1.102     <span style="color:blue" class="comment"># Action input conctinues with 31 further SEGMENTn keywords, </span>
<b name="data/INSTRUCTIONS.md_working_4.datab_lt" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datab_lt","data/INSTRUCTIONS.md_working_4.datab_lt","blue")'>ab_lt</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datab_lt">The LESS_THAN action with label <b>ab_lt</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">ab_lt</td><td width="5%"><font color="blue">vector</font></td><td>the vector obtained by doing an element-wise application of a function that is one if the input is less than a threshold to the input vectors</td></tr></table></span>: <div class="tooltip" style="color:green">LESS_THAN<div class="right">Use a switching function to determine how many of the input variables are less than a certain cutoff. <a href="https://www.plumed.org/doc-master/user-doc/html/_l_e_s_s__t_h_a_n.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_4.datab">ab</b> <div class="tooltip">SWITCH<div class="right">This keyword is used if you want to employ an alternative to the continuous swiching function defined above<i></i></div></div>={RATIONAL R_0=0.08 NN=8 MM=12}
<b name="data/INSTRUCTIONS.md_working_4.datab_lessthan" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datab_lessthan","data/INSTRUCTIONS.md_working_4.datab_lessthan","black")'>ab_lessthan</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datab_lessthan">The SUM action with label <b>ab_lessthan</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">ab_lessthan</td><td width="5%"><font color="black">scalar</font></td><td>the sum of all the elements in the input vector</td></tr></table></span>: <div class="tooltip" style="color:green">SUM<div class="right">Calculate the sum of the arguments <a href="https://www.plumed.org/doc-master/user-doc/html/_s_u_m.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_4.datab_lt">ab_lt</b> <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
<span style="color:blue"># --- End of included input --- </span></span><br/><span style="color:blue" class="comment"># parallel beta</span>
<span id="data/INSTRUCTIONS.md_working_4.datpb_short"><span id="data/INSTRUCTIONS.md_working_4.datdefpb_short"><b name="data/INSTRUCTIONS.md_working_4.datpb" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datpb","data/INSTRUCTIONS.md_working_4.datpb_shortcut","blue")'>pb</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datpb_shortcut">The PARABETARMSD action with label <b>pb</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">pb</td><td width="5%"><font color="blue">vector</font></td><td>if LESS_THAN is present the RMSD distance between each residue and the ideal parallel beta sheet.  If LESS_THAN is not present the number of residue segments where the structure is similar to a parallel beta sheet</td></tr><tr><td width="5%">pb_lessthan</td><td width="5%"><font color="black">scalar</font></td><td>the number blocks of residues that have an RMSD from the secondary structure that is less than the threshold</td></tr></table></span>: <div class="tooltip" style="color:green">PARABETARMSD<div class="right">Probe the parallel beta sheet content of your protein structure. This action is <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datpb");'>a shortcut</a> and it has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datdefpb");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_a_r_a_b_e_t_a_r_m_s_d.html">More details</a><i></i></div></div> <div class="tooltip">RESIDUES<div class="right">this command is used to specify the set of residues that could conceivably form part of the secondary structure<i></i></div></div>=all <div class="tooltip">LESS_THAN<div class="right">calculate the number of a residue segments that are within a certain target distance of this secondary structure type<i></i></div></div>={RATIONAL R_0=0.08 NN=8 MM=12} <div class="tooltip">STRANDS_CUTOFF<div class="right">If in a segment of protein the two strands are further apart then the calculation of the actual RMSD is skipped as the structure is very far from being beta-sheet like<i></i></div></div>=1
</span><span id="data/INSTRUCTIONS.md_working_4.datdefpb_long" style="display:none;"><b name="data/INSTRUCTIONS.md_working_4.datpb" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datpb","data/INSTRUCTIONS.md_working_4.datpb_shortcut","blue")'>pb</b>: <div class="tooltip" style="color:green">PARABETARMSD<div class="right">Probe the parallel beta sheet content of your protein structure. This action is <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datpb");'>a shortcut</a> and uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datdefpb");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_a_r_a_b_e_t_a_r_m_s_d.html">More details</a><i></i></div></div> <div class="tooltip">RESIDUES<div class="right">this command is used to specify the set of residues that could conceivably form part of the secondary structure<i></i></div></div>=all <div class="tooltip">LESS_THAN<div class="right">calculate the number of a residue segments that are within a certain target distance of this secondary structure type<i></i></div></div>={RATIONAL R_0=0.08 NN=8 MM=12} <div class="tooltip">STRANDS_CUTOFF<div class="right">If in a segment of protein the two strands are further apart then the calculation of the actual RMSD is skipped as the structure is very far from being beta-sheet like<i></i></div></div>=1  <div class="tooltip">STYLE<div class="right"> Parallel beta sheets can either form in a single chain or from a pair of chains<i></i></div></div>=all <div class="tooltip">TYPE<div class="right"> the manner in which RMSD alignment is performed<i></i></div></div>=DRMSD
</span></span><span id="data/INSTRUCTIONS.md_working_4.datpb_long" style="display:none;"><span style="color:blue" class="comment"># PLUMED interprets the command:
</span><span class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datpb")'># pb: PARABETARMSD RESIDUES=all LESS_THAN={RATIONAL R_0=0.08 NN=8 MM=12} STRANDS_CUTOFF=1</span>
<span style="color:blue" class="comment"># as follows (Click the red comment above to revert to the short version of the input):</span>
<b name="data/INSTRUCTIONS.md_working_4.datpb_both" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datpb_both","data/INSTRUCTIONS.md_working_4.datpb_both","blue")'>pb_both</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datpb_both">The SECONDARY_STRUCTURE_RMSD action with label <b>pb_both</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">pb_both.struct-1</td><td width="5%"><font color="blue">vector</font></td><td>the vectors containing the rmsd distances between the residues and each of the reference structures  This is the 1th of these quantities</td></tr><tr><td width="5%">pb_both.struct-2</td><td width="5%"><font color="blue">vector</font></td><td>the vectors containing the rmsd distances between the residues and each of the reference structures  This is the 2th of these quantities</td></tr></table></span>: <div class="tooltip" style="color:green">SECONDARY_STRUCTURE_RMSD<div class="right">Calclulate the distance between segments of a protein and a reference structure of interest <a href="https://www.plumed.org/doc-master/user-doc/html/_s_e_c_o_n_d_a_r_y__s_t_r_u_c_t_u_r_e__r_m_s_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">BONDLENGTH<div class="right">the length to use for bonds<i></i></div></div>=0.17 <div class="tooltip">ATOMS<div class="right">this is the full list of atoms that we are investigating<i></i></div></div>=1,5,7,11,12,13,15,17,21,22,23,25,27,38,39,40,42,44,48,49,50,52,54,58,59,60,62,64,68,69,70,72,74,78,79,80,82,84,95,96,97,99,101,105,106,107,109,111,115,116,117,119,121,125,126,127,129,131,135,136,137,139,141,152,153,154,156,158,162,163,164,166,168,172,173 <div class="tooltip">TYPE<div class="right"> the manner in which RMSD alignment is performed<i></i></div></div>=DRMSD <div class="tooltip">STRANDS_CUTOFF<div class="right">If in a segment of protein the two strands are further apart then the calculation of the actual RMSD is skipped as the structure is very far from being beta-sheet like<i></i></div></div>=1 <div class="tooltip">SEGMENT1<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44 <div class="tooltip">SEGMENT2<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49 <div class="tooltip">SEGMENT3<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54 <div class="tooltip">SEGMENT4<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59 <div class="tooltip">SEGMENT5<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64 <div class="tooltip">STRUCTURE1<div class="right">the reference structure<i></i></div></div>=1.244,-4.62,-2.127,-0.016,-4.5,-1.395,0.105,-5.089,0.024,-0.287,-3,-1.301,0.55,-2.245,-0.822,-1.445,-2.551,-1.779,-1.752,-1.13,-1.677,-2.113,-0.55,-3.059,-2.906,-0.961,-0.689,-3.867,-1.738,-0.695,-2.774,0.034,0.19,-3.788,0.331,1.201,-3.188,0.3,2.624,-4.294,1.743,0.937,-3.503,2.671,0.821,4.746,-2.363,0.188,3.427,-1.839,0.545,3.135,-1.958,2.074,3.346,-0.365,0.181,4.237,0.412,0.521,2.261,0.013,-0.487,2.024,1.401,-0.875,1.489,1.514,-2.313,0.914,1.902,0.044,-0.173,1.33,0.052,1.202,2.94,0.828,0.19,3.507,1.718,0.772,3.801,3.104,-0.229,4.791,1.038,0.523,5.771,0.996 <div class="tooltip">STRUCTURE2<div class="right">the reference structure<i></i></div></div>=-1.439,-5.122,-1.144,-0.816,-3.803,-1.013,0.099,-3.509,-2.206,-1.928,-2.77,-0.952,-2.991,-2.97,-1.551,-1.698,-1.687,-0.215,-2.681,-0.613,-0.143,-3.323,-0.477,1.267,-1.984,0.681,-0.574,-0.807,0.921,-0.273,-2.716,1.492,-1.329,-2.196,2.731,-1.883,-2.263,2.692,-3.418,-2.989,3.949,-1.433,-4.214,3.989,-1.583,2.464,-4.352,2.149,3.078,-3.17,1.541,3.398,-3.415,0.06,2.08,-2.021,1.639,0.938,-2.178,1.225,2.525,-0.886,2.183,1.692,0.303,2.346,1.541,0.665,3.842,2.42,1.41,1.608,3.567,1.733,1.937,1.758,1.976,0.6,2.373,2.987,-0.238,2.367,2.527,-1.72,1.684,4.331,-0.148,0.486,4.43,-0.415     <span style="color:blue" class="comment"># Action input conctinues with 23 further SEGMENTn keywords, </span>
<b name="data/INSTRUCTIONS.md_working_4.datpb" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datpb","data/INSTRUCTIONS.md_working_4.datpb","blue")'>pb</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datpb">The LOWEST action with label <b>pb</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">pb</td><td width="5%"><font color="blue">vector</font></td><td>the smallest element in the input vector if one vector specified.  If multiple vectors of the same size specified the largest elements of these vector computed elementwise.</td></tr></table></span>: <div class="tooltip" style="color:green">LOWEST<div class="right">This function can be used to find the lowest colvar by magnitude in a set. <a href="https://www.plumed.org/doc-master/user-doc/html/_l_o_w_e_s_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_4.datpb_both">pb_both.struct-1</b>,<b name="data/INSTRUCTIONS.md_working_4.datpb_both">pb_both.struct-2</b>
<b name="data/INSTRUCTIONS.md_working_4.datpb_lt" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datpb_lt","data/INSTRUCTIONS.md_working_4.datpb_lt","blue")'>pb_lt</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datpb_lt">The LESS_THAN action with label <b>pb_lt</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">pb_lt</td><td width="5%"><font color="blue">vector</font></td><td>the vector obtained by doing an element-wise application of a function that is one if the input is less than a threshold to the input vectors</td></tr></table></span>: <div class="tooltip" style="color:green">LESS_THAN<div class="right">Use a switching function to determine how many of the input variables are less than a certain cutoff. <a href="https://www.plumed.org/doc-master/user-doc/html/_l_e_s_s__t_h_a_n.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_4.datpb">pb</b> <div class="tooltip">SWITCH<div class="right">This keyword is used if you want to employ an alternative to the continuous swiching function defined above<i></i></div></div>={RATIONAL R_0=0.08 NN=8 MM=12}
<b name="data/INSTRUCTIONS.md_working_4.datpb_lessthan" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datpb_lessthan","data/INSTRUCTIONS.md_working_4.datpb_lessthan","black")'>pb_lessthan</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datpb_lessthan">The SUM action with label <b>pb_lessthan</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">pb_lessthan</td><td width="5%"><font color="black">scalar</font></td><td>the sum of all the elements in the input vector</td></tr></table></span>: <div class="tooltip" style="color:green">SUM<div class="right">Calculate the sum of the arguments <a href="https://www.plumed.org/doc-master/user-doc/html/_s_u_m.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_4.datpb_lt">pb_lt</b> <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
<span style="color:blue"># --- End of included input --- </span></span><br/><span style="color:blue" class="comment"># alpha helix</span>
<span id="data/INSTRUCTIONS.md_working_4.datalfa_short"><span id="data/INSTRUCTIONS.md_working_4.datdefalfa_short"><b name="data/INSTRUCTIONS.md_working_4.datalfa" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datalfa","data/INSTRUCTIONS.md_working_4.datalfa_shortcut","blue")'>alfa</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datalfa_shortcut">The ALPHARMSD action with label <b>alfa</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">alfa</td><td width="5%"><font color="blue">vector</font></td><td>if LESS_THAN is present the RMSD distance between each residue and the ideal alpha helix.  If LESS_THAN is not present the number of residue segments where the structure is similar to an alpha helix</td></tr><tr><td width="5%">alfa_lessthan</td><td width="5%"><font color="black">scalar</font></td><td>the number blocks of residues that have an RMSD from the secondary structure that is less than the threshold</td></tr></table></span>: <div class="tooltip" style="color:green">ALPHARMSD<div class="right">Probe the alpha helical content of a protein structure. This action is <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datalfa");'>a shortcut</a> and it has <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datdefalfa");'>hidden defaults</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_a_l_p_h_a_r_m_s_d.html">More details</a><i></i></div></div> <div class="tooltip">RESIDUES<div class="right">this command is used to specify the set of residues that could conceivably form part of the secondary structure<i></i></div></div>=all <div class="tooltip">LESS_THAN<div class="right">calculate the number of a residue segments that are within a certain target distance of this secondary structure type<i></i></div></div>={RATIONAL R_0=0.08 NN=8 MM=12}
</span><span id="data/INSTRUCTIONS.md_working_4.datdefalfa_long" style="display:none;"><b name="data/INSTRUCTIONS.md_working_4.datalfa" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datalfa","data/INSTRUCTIONS.md_working_4.datalfa_shortcut","blue")'>alfa</b>: <div class="tooltip" style="color:green">ALPHARMSD<div class="right">Probe the alpha helical content of a protein structure. This action is <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datalfa");'>a shortcut</a> and uses the <a class="toggler" href='javascript:;' onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datdefalfa");'>defaults shown here</a>. <a href="https://www.plumed.org/doc-master/user-doc/html/_a_l_p_h_a_r_m_s_d.html">More details</a><i></i></div></div> <div class="tooltip">RESIDUES<div class="right">this command is used to specify the set of residues that could conceivably form part of the secondary structure<i></i></div></div>=all <div class="tooltip">LESS_THAN<div class="right">calculate the number of a residue segments that are within a certain target distance of this secondary structure type<i></i></div></div>={RATIONAL R_0=0.08 NN=8 MM=12}  <div class="tooltip">TYPE<div class="right"> the manner in which RMSD alignment is performed<i></i></div></div>=DRMSD
</span></span><span id="data/INSTRUCTIONS.md_working_4.datalfa_long" style="display:none;"><span style="color:blue" class="comment"># PLUMED interprets the command:
</span><span class="toggler" style="color:red" onclick='toggleDisplay("data/INSTRUCTIONS.md_working_4.datalfa")'># alfa: ALPHARMSD RESIDUES=all LESS_THAN={RATIONAL R_0=0.08 NN=8 MM=12}</span>
<span style="color:blue" class="comment"># as follows (Click the red comment above to revert to the short version of the input):</span>
<b name="data/INSTRUCTIONS.md_working_4.datalfa" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datalfa","data/INSTRUCTIONS.md_working_4.datalfa","blue")'>alfa</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datalfa">The SECONDARY_STRUCTURE_RMSD action with label <b>alfa</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">alfa</td><td width="5%"><font color="blue">vector</font></td><td>a vector containing the rmsd distance between each of the residue segments and the reference structure</td></tr></table></span>: <div class="tooltip" style="color:green">SECONDARY_STRUCTURE_RMSD<div class="right">Calclulate the distance between segments of a protein and a reference structure of interest <a href="https://www.plumed.org/doc-master/user-doc/html/_s_e_c_o_n_d_a_r_y__s_t_r_u_c_t_u_r_e__r_m_s_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">BONDLENGTH<div class="right">the length to use for bonds<i></i></div></div>=0.17 <div class="tooltip">ATOMS<div class="right">this is the full list of atoms that we are investigating<i></i></div></div>=1,5,7,11,12,13,15,17,21,22,23,25,27,38,39,40,42,44,48,49,50,52,54,58,59,60,62,64,68,69,70,72,74,78,79,80,82,84,95,96,97,99,101,105,106,107,109,111,115,116,117,119,121,125,126,127,129,131,135,136,137,139,141,152,153,154,156,158,162,163,164,166,168,172,173 <div class="tooltip">TYPE<div class="right"> the manner in which RMSD alignment is performed<i></i></div></div>=DRMSD <div class="tooltip">SEGMENT1<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29 <div class="tooltip">SEGMENT2<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34 <div class="tooltip">SEGMENT3<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39 <div class="tooltip">SEGMENT4<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44 <div class="tooltip">SEGMENT5<div class="right">this is the lists of atoms in the segment that are being considered<i></i></div></div>=20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49 <div class="tooltip">STRUCTURE1<div class="right">the reference structure<i></i></div></div>=0.733,0.519,5.298,1.763,0.81,4.301,3.166,0.543,4.881,1.527,-0.045,3.053,1.646,0.436,1.928,1.18,-1.312,3.254,0.924,-2.203,2.126,0.65,-3.626,2.626,-0.239,-1.711,1.261,-0.19,-1.815,0.032,-1.28,-1.172,1.891,-2.416,-0.661,1.127,-3.548,-0.217,2.056,-1.964,0.529,0.276,-2.364,0.659,-0.88,-1.13,1.391,0.856,-0.62,2.565,0.148,0.228,3.439,1.077,0.231,2.129,-1.032,0.179,2.733,-2.099,1.028,1.084,-0.833,1.872,0.593,-1.919,2.85,-0.462,-1.397,1.02,0.02,-3.049,1.317,0.227,-4.224,-0.051,-0.684,-2.696,-0.927,-1.261,-3.713,-1.933,-2.219,-3.074,-1.663,-0.171,-4.475,-1.916,-0.296,-5.673     <span style="color:blue" class="comment"># Action input conctinues with 5 further SEGMENTn keywords, </span>
<b name="data/INSTRUCTIONS.md_working_4.datalfa_lt" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datalfa_lt","data/INSTRUCTIONS.md_working_4.datalfa_lt","blue")'>alfa_lt</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datalfa_lt">The LESS_THAN action with label <b>alfa_lt</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">alfa_lt</td><td width="5%"><font color="blue">vector</font></td><td>the vector obtained by doing an element-wise application of a function that is one if the input is less than a threshold to the input vectors</td></tr></table></span>: <div class="tooltip" style="color:green">LESS_THAN<div class="right">Use a switching function to determine how many of the input variables are less than a certain cutoff. <a href="https://www.plumed.org/doc-master/user-doc/html/_l_e_s_s__t_h_a_n.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_4.datalfa">alfa</b> <div class="tooltip">SWITCH<div class="right">This keyword is used if you want to employ an alternative to the continuous swiching function defined above<i></i></div></div>={RATIONAL R_0=0.08 NN=8 MM=12}
<b name="data/INSTRUCTIONS.md_working_4.datalfa_lessthan" onclick='showPath("data/INSTRUCTIONS.md_working_4.dat","data/INSTRUCTIONS.md_working_4.datalfa_lessthan","data/INSTRUCTIONS.md_working_4.datalfa_lessthan","black")'>alfa_lessthan</b><span style="display:none;" id="data/INSTRUCTIONS.md_working_4.datalfa_lessthan">The SUM action with label <b>alfa_lessthan</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td width="5%"><b> Type </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">alfa_lessthan</td><td width="5%"><font color="black">scalar</font></td><td>the sum of all the elements in the input vector</td></tr></table></span>: <div class="tooltip" style="color:green">SUM<div class="right">Calculate the sum of the arguments <a href="https://www.plumed.org/doc-master/user-doc/html/_s_u_m.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the values input to this function<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_4.datalfa_lt">alfa_lt</b> <div class="tooltip">PERIODIC<div class="right">if the output of your function is periodic then you should specify the periodicity of the function<i></i></div></div>=NO
<span style="color:blue"># --- End of included input --- </span></span><br/><br/><div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> ... 
 <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/INSTRUCTIONS.md_working_4.datrgyr">rgyr</b>,<b name="data/INSTRUCTIONS.md_working_4.datab">ab.lessthan</b>,<b name="data/INSTRUCTIONS.md_working_4.datpb">pb.lessthan</b>,<b name="data/INSTRUCTIONS.md_working_4.datalfa">alfa.lessthan</b>
 <div class="tooltip">STRIDE<div class="right"> the frequency with which the quantities of interest should be output<i></i></div></div>=1000
 <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=COLVAR
... PRINT
</pre>
 {% endraw %} 

We are providing PLUMED with a protein structure (aaqaa_min.pdb) in input using the [MOLINFO](https://www.plumed.org/doc-master/user-doc/html/_m_o_l_i_n_f_o.html) keyword. We are then computing the radius of gyration, parallel/antiparallel beta-sheet content and alpha-helix content of the protein, and we are printing this info to a file called COLVAR every 1000 integration steps. 
$(AAQAA)\_3$ should fold as a alpha-helix, but we are monitoring also the parallel/antiparallel beta-sheet content in order to identify potential cases of misfolding. 


In this first example, we are simulating $(AAQAA)\_3$ in pure water at 298 K and ambient pressure, so we do not need to add the free energy of transfer term $G^{tr}(T,P,c)$, and the SASA module is not even called in the PLUMED file. 
However, for exercises 2-5, you will need to use the SASA module to include the effect of temperature/pressure/urea concentration on protein stability. 

To run the simulation, just type the command: 

```` 
sander -O -i AAQAA_298.in -o aaqaa-MD.out -c aaqaa_min.ncrst -p aaqaa.prmtop -r aaqaa-MD.ncrst -x aaqaa-MD.nc >& logfile 
```` 

The simulation should take 1-2 hours on a common laptop, so you should not need a cluster for this masterclass. 

At the end of the simulation, you will have a COLVAR file that lists the evolution of radius of gyration and secondary structure content of the protein as function of time. Try to plot the columns of the COLVAR file versus time. 

Does the protein fold? If yes, how fast is the process? Do you think the process would be equally fast in explicit solvent? 

Here is the evolution of the helical content of $(AAQAA)\_3$ over time during the simulation: 

[Evolution of helical content over time during the simulation of exercise 1](figs/masterclass-22-13-tvsalpha.png) 

You can also use the script_rg_alpha.bash file provided to have a 2D representation of the conformational space explored by the protein during the simulation. Just type: 

```` 
chmod +x script_rg_alpha.bash 
./script_rg_alpha.bash COLVAR 
```` 

The script generates a file called normFEL.dat that can be visualized in gnuplot using the picture_rg_alpha.gnu script provided. You should obtain something similar to: 

[Free energy surface showing radius of gyration and helical content of the protein during the simulation of exercise 1](figs/masterclass-22-13-FES_rg_alpha.png) 

## Exercises 2-5: Introducing the free energy of transfer contribution to implicit solvent simulations 

Using the learnings from the theoretical part of this masterclass and exercise 1, you should now be able to autonomously run exercises 2-5. The difference now is that you need to employ free energy of transfer contributions to simulate the solution conditions of exercises 2-5. 
Exercises 2 and 3 explore extreme (cold and hot) values of temperature. Exercise 4 includes the presence of a potent denaturant (urea), and exercise 5 is performed at a high pressure value. 

This means that you will need to use the SASA module, as described in the thoretical summary, to introduce the effect of temperature, pressure and osmolyte concentration within the implicit solvent simulation. 

The folder that you downloaded from [GitHub](https://github.com/andrea-arsiccio/masterclass-22-13) contains 5 subfolders, one for each exercise. In each subfolder, every file is ready to use, with the only exception of the plumed.dat file, that you will need to write autonomously using the template employed in exercise 1. Specifically, please monitor for each exercise the radius of gyration and secondary structure content (alpha-helix, parallel and antiparalle beta-sheet) of the protein, and print this information to a file called COLVAR. 
You will also need to add a [SASA_HASEL](https://www.plumed.org/doc-master/user-doc/html/_s_a_s_a__h_a_s_e_l.html) (hint: use [SASA_HASEL](https://www.plumed.org/doc-master/user-doc/html/_s_a_s_a__h_a_s_e_l.html) instead of SASA_LCPO, as the algorithm by Hasel et al. is faster) and a [BIASVALUE](https://www.plumed.org/doc-master/user-doc/html/_b_i_a_s_v_a_l_u_e.html) section to the plumed.dat file, as discussed in the theoretical section. 

You will need to perform the following steps: 

- install the software (PLUMED, AMBER) 
- clone the GitHub folder with input files: git clone https://github.com/andrea-arsiccio/masterclass-22-13 
- write a PLUMED file in each subfolder according to the example of Exercise 1 (hint: use the DeltaG-calculation.py script if needed! The README for the script is available on [GitHub] (https://github.com/andrea-arsiccio/DeltaG-calculation), please have a look into it) 
- Run the simulations using the command: 

```` 
sander -O -i AAQAA_%%%.in -o aaqaa-MD.out -c aaqaa_min.ncrst -p aaqaa.prmtop -r aaqaa-MD.ncrst -x aaqaa-MD.nc >& logfile 
```` 

- Analyze the trajectories as already done during exercise 1 (plot the COLVAR columns versus time, and use the script_rg_alpha.bash file to get a representation of the conformational space explored) 

You should ask yourself the following questions: 

- what would you expect to occur at the protein structure at extreme values of temperature/pressure/urea concentration? Are your expections reflected in the simulation outputs? 
- would you observe similar phenomena also in 5-ns-long explicit solvent calculations? 

## Final thoughts 

Through this tutorial we have learnt that the SASA module of PLUMED implements two algorithms for the computation of the SASA (the faster algorithm by Hasel et al., and the more accurate LCPO algorithm). 

We have found out that the SASA module can be used for introducing the SASA as a collective variable or for monitoring the SASA, but it can furthermore be employed to perform implicit solvent MD simulations. 

Implicit solvent simulations with the SASA module are based on the concept of free energy of transfer (where the 'transfer' occurs from pure water at ambient temperature and pressure to an osmolyte solution at any desired value of temperature and pressure). 

Implicit solvent simulations have the advantage, compared to their explicit solvent counterpart, to speed up conformational transitions, and allow a faster exploration of conformational space. 

NOTE: The Masterclass files with the solutions to the exercises are also avilable on [GitHub](https://github.com/andrea-arsiccio/masterclass-22-13-results), but please do the exercises on your own before checking on the results! 
