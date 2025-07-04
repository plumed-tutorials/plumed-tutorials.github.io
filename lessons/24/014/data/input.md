__Note:__ The following code can be run in google colab or jupyter notebook. [This](https://colab.research.google.com/github/vendruscolo-lab/AlphaFold-MetaInference-Tutorial/blob/main/AF-IDP_colab.ipynb) google colab provides with the full AF-MI protocol, i.e software installation, CALVADOS, PLUMED input preparation, running AF-MI, and analysis. Lets break it down and explain each part. 

## Software installation



The code below needs to run in colab. We first install condacolab which is essential in running conda google colab. This step is not necessary if one runs just in a jupyter-notebook locally. 


```python
#Install collab
!pip install -q condacolab
import condacolab
condacolab.install()
```
The code below installs various necessary packages such as PLUMED, mpi, OPENMM, pandas, gromacs, biopython, pulchra. Moreover it builds the OPENMM-PLUMED-MPI patch which is necessary for running metainference in OPENMM.  

```python
import os
home=os.getcwd()
os.chdir(home)

#Download OpenMM-Plumed-MPI patch
!conda install -y -c conda-forge mpich mpi4py openmm=8.0 plumed=2.8.2=mpi_mpich_h7ded119_0 py-plumed cmake swig pandas mdtraj biopython matplotlib gromacs
!conda install -y -c anaconda ipykernel
!conda install -y -c bioconda pulchra

!git clone https://github.com/vendruscolo-lab/OpenMM-Plumed-MPI

os.chdir(home+'/OpenMM-Plumed-MPI')

#Build openmm-plumed-mpi
!mkdir build install openmm -p plumed/include -p plumed/lib
!unzip openmm.zip -d openmm
!unzip plumed_lib.zip -d plumed/lib
!unzip plumed_include.zip -d plumed/include
os.chdir(os.getcwd()+'/build')
!cmake ..
!make
!make install
!make PythonInstall
os.chdir(os.getcwd()+'/../install/lib')
!cp -r * /usr/local/lib/
```

## Run Alpha-Fold distance map prediction


__For this example (TDP-43 WtoA):__

The AF distance map has already been calculated and it is loaded below. We here show the AF prediction for the a) Inter-residue distances, b)PLDDT score and c)PAE per residue pair. 

<p align="center">
  <img src="https://github.com/vendruscolo-lab/AlphaFold-MetaInference-Tutorial/blob/main/images/alphafold2_ptm_model_3_seed_000_distmat.png?raw=true" alt="Alt text" width="50%">
    <img src="https://github.com/vendruscolo-lab/AlphaFold-MetaInference-Tutorial/blob/main/images/tdp43_WtoA_bf4cc_plddt.png?raw=true" alt="Alt text" width="50%">
    <img src="https://github.com/vendruscolo-lab/AlphaFold-MetaInference-Tutorial/blob/main/images/tdp43_WtoA_bf4cc_pae.png?raw=true" alt="Alt text" width="50%">
  <br> a) Inter-residue distances, b)PLDDT score and c)PAE per residue pair. 
  <em> </em>
</p>



__For arbitrary protein sequences:__

*   Open [this](https://github.com/zshengyu14/ColabFold_distmats/blob/main/AlphaFold2.ipynb) link and choose colab.
*   Input the protein sequence  as query sequence.
*   The rest of the options remain default and cells are run until the end.
*   Download the link with the AF data and upload it as AF_data in AlphaFold-IDP folder

## Setup protein system in CALVADOS2 and OPENMM

```python
os.chdir(home)
!git clone https://github.com/vendruscolo-lab/AlphaFold-IDP
os.chdir(home+'/AlphaFold-IDP/prep_run')
```
In the following step we need to define ```python fasta_sequence, pH, temp, ionic, PAE_cut, NR, ordered_domains, disordered_domains, pdb_af,json_af,npy_af, mean_af```. These variables respectively stand for the protein sequence to be simulated in AF-MI, the simulation pH, the simulation temperature (in K), the ionic strength of the solution, the highest AF predicted alighment error the considered inter-residue distances will have (residue distances with higher PAE are not considered in restraints), the number of replicas, the regions of the ordered domains (regions of more than 3 residues with PLDDT>0.75) where RMSD walls wil be used, the disordered regions (usually regions of more than 3 residues with PLDDT<0.75), AF predicted pdb file, AF predicted json containing the PAE per residue pair file, per residue pair probability distribution AF prediction file, mean AF inter-residue distance map prediction file  

```python
import shutil
import csv
dir=os.getcwd()
###################### The entries below need to be adapted in each simulation ######################
#TDP-43 sequence
fasta_sequence="MSEYIRVTEDENDEPIEIPSEDDGTVLLSTVTAQFPGACGLRYRNPVSQCMRGVRLVEGILHAPDAGAGNLVYVVNYPKDNKRKMDETDASSAVKVKRAVQKTSDLIVLGLPAKTTEQDLKEYFSTFGEVLMVQVKKDLKTGHSKGFGFVRFTEYETQVKVMSQRHMIDGRACDCKLPNSKQSQDEPLRSRKVFVGRCTEDMTEDELREFFSQYGDVMDVFIPKPFRAFAFVTFADDQIAQSLCGEDLIIKGISVHISNAEPKHNSNRQLERSGRFGGNPGGFGNQGGFGNSRGGGAGLGNNQGSNMGGGMNFGAFSINPAMMAAAQAALQSSAGMMGMLASQQNQSGPSGNNQNQGNMQREPNQAFGSGNNSYSGSNSGAAIGAGSASNAGSGSGFNGGFGSSMDSKSSGAGM"
#Conditions
pH=7.4
temp=298
ionic=0.2
PAE_cut=5
NR=2
#Decide the plddt based ordered (od) and disordered (dd) regions
ordered_domains = {'od1': [3, 79], 'od2': [104,178],'od3':[191,260]}
disordered_domains={'dd1': [1,2],'dd2':[80,103],'dd3':[179,190],'dd4':[261,414]}

#AF input created in AF-distance map prediction and used in AF-MI
pdb_af='tdp43_WtoA_bf4cc_unrelaxed_rank_001_alphafold2_ptm_model_3_seed_000.pdb'
json_af='tdp43_WtoA_bf4cc_predicted_aligned_error_v1.json'
npy_af='alphafold2_ptm_model_3_seed_000_prob_distributions.npy'
mean_af='alphafold2_ptm_model_3_seed_000_mean.csv'
#Copy AF data
shutil.copy2(dir+"/../AF_DATA/"+pdb_af, dir+"/pdb_af.pdb")
shutil.copy2(dir+"/../AF_DATA/"+json_af, dir+"/pae.json")
shutil.copy2(dir+"/../AF_DATA/tdp43_WtoA_bf4cc_distmat/"+mean_af, dir+"/mean_af.csv")
shutil.copy2(dir+"/../AF_DATA/tdp43_WtoA_bf4cc_distmat/"+npy_af, dir+"/prob.npy")
####################################################################################################
```

In the following step we create the OPENMM CALVADOS2 .xml files

```python 
f = open("sequence.dat", "w")
f.write(fasta_sequence)
f.close()
#Write the csv files
with open('ordered_domains.csv', 'w') as f:  # You will need 'wb' mode in Python 2.x
    w = csv.DictWriter(f, ordered_domains.keys())
    w.writeheader()
    w.writerow(ordered_domains)
with open('disordered_domains.csv', 'w') as f:  # You will need 'wb' mode in Python 2.x
    w = csv.DictWriter(f, disordered_domains.keys())
    w.writeheader()
    w.writerow(disordered_domains)

#Copy OPENMM calvados forcefield files
shutil.copy2(dir+"/../scripts_prep/gen_xml_and_constraints.py", dir)
shutil.copy2(dir+"/../scripts_prep/residues.csv", dir)

path_gen_xml = dir+'/gen_xml_and_constraints.py sequence.dat '+str(pH)+' '+str(temp)+' '+str(ionic)
print(path_gen_xml)
os.system(f'python {path_gen_xml}')
```
Make the AF-MI PLUMED ``` plumed.dat``` input file 
```python
#Make plumed files.
#Copy and run the prep script that makes the plumed file.
#The Collective variables (CVs) in these case are chosen to be the torsion angles between structured domains.
import subprocess
shutil.copy2(dir+"/../scripts_prep/make_plumed_distmat.py", dir)
subprocess.run(['python', str(dir)+'/make_plumed_distmat.py', 'sequence.dat',str(PAE_cut), '0.2'], capture_output=True, text=True)
```
The plumed.dat file can be seen below. The ```distance_rest_domains``` are the af-distances do be restrained. For TDP-43 WtoA, the three ordered domains are RMSD restrained with RMSD1,RMSD2,RMSD3. 
Note the __FILL__ entries the user should specify for the specific system at hand. This includes the CV definition, biasfactor, sigma, number of bins in the grid for saving the FES along the PB MetaD simulation. More info on PB-MetaD can be found [here](https://www.plumed.org/doc-v2.9/user-doc/html/_p_b_m_e_t_a_d.html). A usual rule of thumb for the ```biasfactor``` value is ```10*sqrt(number of biased CVs)```. 
{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/plumed_TDP-43.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="plumed_TDP-43.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="plumed_TDP-43.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></div>
<div class="headerBadge"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/plumed_TDP-43.dat")' onmousedown='toggleDisplay("data/plumed_TDP-43.dat")'/></div>
</div>
</div>
<div id="data/plumed_TDP-43.dat_short">
<pre class="plumedlisting">
<span class="plumedtooltip" style="color:green">MOLINFO<span class="right">This command is used to provide information on the molecules that are present in your system. <a href="https://www.plumed.org/doc-master/user-doc/html/MOLINFO" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">MOLTYPE<span class="right"> what kind of molecule is contained in the pdb file - usually not needed since protein/RNA/DNA are compatible<i></i></span></span>=protein <span class="plumedtooltip">STRUCTURE<span class="right">a file in pdb format containing a reference structure<i></i></span></span>=input_af.pdb
<span style="display:none;" id="data/plumed_TDP-43.dat">The MOLINFO action with label <b></b> calculates something</span><span class="plumedtooltip" style="color:green">WHOLEMOLECULES<span class="right">This action is used to rebuild molecules that can become split by the periodic boundary conditions. <a href="https://www.plumed.org/doc-master/user-doc/html/WHOLEMOLECULES" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ENTITY0<span class="right">the atoms that make up a molecule that you wish to align<i></i></span></span>=1-414
    
<b name="data/plumed_TDP-43.datdistance_rest_domains" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.datdistance_rest_domains","data/plumed_TDP-43.datdistance_rest_domains","brown")'>distance_rest_domains</b>:  <span class="plumedtooltip" style="color:green">CONTACTMAP<span class="right">Calculate the distances between a number of pairs of atoms and transform each distance by a switching function. <a href="https://www.plumed.org/doc-master/user-doc/html/CONTACTMAP" style="color:green">More details</a><i></i></span></span> ...
<span class="plumedtooltip">ATOMS1<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=1,4
<span class="plumedtooltip">ATOMS2<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=2,5
<span class="plumedtooltip">ATOMS3<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=2,20
<span class="plumedtooltip">ATOMS4<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=28,79
<span class="plumedtooltip">ATOMS5<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=31,79
<span class="plumedtooltip">ATOMS6<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=35,79
<span class="plumedtooltip">ATOMS7<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=37,79
<span class="plumedtooltip">ATOMS8<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=38,79
<span class="plumedtooltip">ATOMS9<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=39,79
<span class="plumedtooltip">ATOMS10<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=40,79
<span class="plumedtooltip">ATOMS11<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=41,79
<span class="plumedtooltip">ATOMS12<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=42,79
<span class="plumedtooltip">ATOMS13<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=74,79
<span class="plumedtooltip">ATOMS14<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=75,79
<span class="plumedtooltip">ATOMS15<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=76,79
<span class="plumedtooltip">ATOMS16<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,105
<span class="plumedtooltip">ATOMS17<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,106
<span class="plumedtooltip">ATOMS18<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,150
<span class="plumedtooltip">ATOMS19<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,151
<span class="plumedtooltip">ATOMS20<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,152
<span class="plumedtooltip">ATOMS21<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,155
<span class="plumedtooltip">ATOMS22<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,158
<span class="plumedtooltip">ATOMS23<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,159
<span class="plumedtooltip">ATOMS24<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,161
<span class="plumedtooltip">ATOMS25<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,106
<span class="plumedtooltip">ATOMS26<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,107
<span class="plumedtooltip">ATOMS27<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,108
<span class="plumedtooltip">ATOMS28<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,120
<span class="plumedtooltip">ATOMS29<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,121
<span class="plumedtooltip">ATOMS30<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,124
<span class="plumedtooltip">ATOMS31<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,130
<span class="plumedtooltip">ATOMS32<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,131
<span class="plumedtooltip">ATOMS33<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,132
<span class="plumedtooltip">ATOMS34<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,133
<span class="plumedtooltip">ATOMS35<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,134
<span class="plumedtooltip">ATOMS36<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,135
<span class="plumedtooltip">ATOMS37<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,147
<span class="plumedtooltip">ATOMS38<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,148
<span class="plumedtooltip">ATOMS39<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,149
<span class="plumedtooltip">ATOMS40<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,150
<span class="plumedtooltip">ATOMS41<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,151
<span class="plumedtooltip">ATOMS42<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,152
<span class="plumedtooltip">ATOMS43<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,153
<span class="plumedtooltip">ATOMS44<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,154
<span class="plumedtooltip">ATOMS45<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,155
<span class="plumedtooltip">ATOMS46<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,156
<span class="plumedtooltip">ATOMS47<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,157
<span class="plumedtooltip">ATOMS48<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,158
<span class="plumedtooltip">ATOMS49<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,159
<span class="plumedtooltip">ATOMS50<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,160
<span class="plumedtooltip">ATOMS51<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,161
<span class="plumedtooltip">ATOMS52<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,162
<span class="plumedtooltip">ATOMS53<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,175
<span class="plumedtooltip">ATOMS54<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,176
<span class="plumedtooltip">ATOMS55<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,177
<span class="plumedtooltip">ATOMS56<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,178
<span class="plumedtooltip">ATOMS57<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=104,178
<span class="plumedtooltip">ATOMS58<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=105,178
<span class="plumedtooltip">ATOMS59<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=105,179
<span class="plumedtooltip">ATOMS60<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=106,178
<span class="plumedtooltip">ATOMS61<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=106,179
<span class="plumedtooltip">ATOMS62<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=107,178
<span class="plumedtooltip">ATOMS63<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=107,179
<span class="plumedtooltip">ATOMS64<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=108,178
<span class="plumedtooltip">ATOMS65<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=108,179
<span class="plumedtooltip">ATOMS66<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=109,178
<span class="plumedtooltip">ATOMS67<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=109,179
<span class="plumedtooltip">ATOMS68<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=110,178
<span class="plumedtooltip">ATOMS69<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=111,178
<span class="plumedtooltip">ATOMS70<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=120,178
<span class="plumedtooltip">ATOMS71<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=124,178
<span class="plumedtooltip">ATOMS72<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=131,178
<span class="plumedtooltip">ATOMS73<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=132,178
<span class="plumedtooltip">ATOMS74<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=133,178
<span class="plumedtooltip">ATOMS75<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=134,178
<span class="plumedtooltip">ATOMS76<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=135,178
<span class="plumedtooltip">ATOMS77<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=136,178
<span class="plumedtooltip">ATOMS78<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=137,178
<span class="plumedtooltip">ATOMS79<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=145,178
<span class="plumedtooltip">ATOMS80<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=146,178
<span class="plumedtooltip">ATOMS81<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=147,178
<span class="plumedtooltip">ATOMS82<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=147,179
<span class="plumedtooltip">ATOMS83<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=148,178
<span class="plumedtooltip">ATOMS84<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=148,179
<span class="plumedtooltip">ATOMS85<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=149,178
<span class="plumedtooltip">ATOMS86<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=149,179
<span class="plumedtooltip">ATOMS87<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=150,178
<span class="plumedtooltip">ATOMS88<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=150,179
<span class="plumedtooltip">ATOMS89<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=151,178
<span class="plumedtooltip">ATOMS90<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=151,179
<span class="plumedtooltip">ATOMS91<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=152,178
<span class="plumedtooltip">ATOMS92<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=155,178
<span class="plumedtooltip">ATOMS93<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=158,178
<span class="plumedtooltip">ATOMS94<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=159,178
<span class="plumedtooltip">ATOMS95<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=159,179
<span class="plumedtooltip">ATOMS96<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=161,178
<span class="plumedtooltip">ATOMS97<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=161,179
<span class="plumedtooltip">ATOMS98<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=162,178
<span class="plumedtooltip">ATOMS99<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=162,179
<span class="plumedtooltip">ATOMS100<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=163,178
<span class="plumedtooltip">ATOMS101<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=164,178
<span class="plumedtooltip">ATOMS102<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=165,178
<span class="plumedtooltip">ATOMS103<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=166,178
<span class="plumedtooltip">ATOMS104<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=173,178
<span class="plumedtooltip">ATOMS105<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=174,178
<span class="plumedtooltip">ATOMS106<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=174,179
<span class="plumedtooltip">ATOMS107<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=175,178
<span class="plumedtooltip">ATOMS108<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=175,179
<span class="plumedtooltip">ATOMS109<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=176,179
<span class="plumedtooltip">ATOMS110<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=189,192
<span class="plumedtooltip">ATOMS111<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=189,233
<span class="plumedtooltip">ATOMS112<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=189,240
<span class="plumedtooltip">ATOMS113<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,193
<span class="plumedtooltip">ATOMS114<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,194
<span class="plumedtooltip">ATOMS115<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,195
<span class="plumedtooltip">ATOMS116<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,209
<span class="plumedtooltip">ATOMS117<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,210
<span class="plumedtooltip">ATOMS118<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,211
<span class="plumedtooltip">ATOMS119<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,212
<span class="plumedtooltip">ATOMS120<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,213
<span class="plumedtooltip">ATOMS121<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,214
<span class="plumedtooltip">ATOMS122<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,216
<span class="plumedtooltip">ATOMS123<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,217
<span class="plumedtooltip">ATOMS124<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,218
<span class="plumedtooltip">ATOMS125<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,219
<span class="plumedtooltip">ATOMS126<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,220
<span class="plumedtooltip">ATOMS127<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,230
<span class="plumedtooltip">ATOMS128<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,231
<span class="plumedtooltip">ATOMS129<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,232
<span class="plumedtooltip">ATOMS130<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,233
<span class="plumedtooltip">ATOMS131<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,234
<span class="plumedtooltip">ATOMS132<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,235
<span class="plumedtooltip">ATOMS133<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,236
<span class="plumedtooltip">ATOMS134<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,237
<span class="plumedtooltip">ATOMS135<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,238
<span class="plumedtooltip">ATOMS136<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,239
<span class="plumedtooltip">ATOMS137<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,240
<span class="plumedtooltip">ATOMS138<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,241
<span class="plumedtooltip">ATOMS139<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,242
<span class="plumedtooltip">ATOMS140<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,243
<span class="plumedtooltip">ATOMS141<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,244
<span class="plumedtooltip">ATOMS142<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,257
<span class="plumedtooltip">ATOMS143<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,258
<span class="plumedtooltip">ATOMS144<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=191,260
<span class="plumedtooltip">ATOMS145<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=192,260
<span class="plumedtooltip">ATOMS146<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=192,261
<span class="plumedtooltip">ATOMS147<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=193,260
<span class="plumedtooltip">ATOMS148<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=193,261
<span class="plumedtooltip">ATOMS149<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=193,262
<span class="plumedtooltip">ATOMS150<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=194,260
<span class="plumedtooltip">ATOMS151<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=194,261
<span class="plumedtooltip">ATOMS152<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=194,262
<span class="plumedtooltip">ATOMS153<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=195,260
<span class="plumedtooltip">ATOMS154<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=195,261
<span class="plumedtooltip">ATOMS155<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=196,260
<span class="plumedtooltip">ATOMS156<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=197,260
<span class="plumedtooltip">ATOMS157<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=211,260
<span class="plumedtooltip">ATOMS158<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=219,260
<span class="plumedtooltip">ATOMS159<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=221,260
<span class="plumedtooltip">ATOMS160<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=222,260
<span class="plumedtooltip">ATOMS161<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=223,260
<span class="plumedtooltip">ATOMS162<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=229,260
<span class="plumedtooltip">ATOMS163<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=229,261
<span class="plumedtooltip">ATOMS164<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=230,260
<span class="plumedtooltip">ATOMS165<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=230,261
<span class="plumedtooltip">ATOMS166<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=231,260
<span class="plumedtooltip">ATOMS167<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=231,261
<span class="plumedtooltip">ATOMS168<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=232,260
<span class="plumedtooltip">ATOMS169<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=232,261
<span class="plumedtooltip">ATOMS170<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=233,260
<span class="plumedtooltip">ATOMS171<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=234,260
<span class="plumedtooltip">ATOMS172<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=234,261
<span class="plumedtooltip">ATOMS173<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=236,260
<span class="plumedtooltip">ATOMS174<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=237,260
<span class="plumedtooltip">ATOMS175<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=238,260
<span class="plumedtooltip">ATOMS176<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=239,260
<span class="plumedtooltip">ATOMS177<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=240,260
<span class="plumedtooltip">ATOMS178<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=241,260
<span class="plumedtooltip">ATOMS179<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=241,261
<span class="plumedtooltip">ATOMS180<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=242,260
<span class="plumedtooltip">ATOMS181<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=243,260
<span class="plumedtooltip">ATOMS182<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=243,261
<span class="plumedtooltip">ATOMS183<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=244,260
<span class="plumedtooltip">ATOMS184<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=245,260
<span class="plumedtooltip">ATOMS185<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=246,260
<span class="plumedtooltip">ATOMS186<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=247,260
<span class="plumedtooltip">ATOMS187<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=248,260
<span class="plumedtooltip">ATOMS188<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=255,260
<span class="plumedtooltip">ATOMS189<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=256,260
<span class="plumedtooltip">ATOMS190<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=256,261
<span class="plumedtooltip">ATOMS191<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=257,260
<span class="plumedtooltip">ATOMS192<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=257,261
<span class="plumedtooltip">ATOMS193<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=258,261
<span class="plumedtooltip">ATOMS194<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=258,262
<span class="plumedtooltip">ATOMS195<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=259,262
<span class="plumedtooltip">ATOMS196<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=298,301
<span class="plumedtooltip">ATOMS197<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=300,303
<span class="plumedtooltip">ATOMS198<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=304,307
<span class="plumedtooltip">ATOMS199<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=318,321
<span class="plumedtooltip">ATOMS200<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=321,324
<span class="plumedtooltip">ATOMS201<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=321,325
<span class="plumedtooltip">ATOMS202<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=321,326
<span class="plumedtooltip">ATOMS203<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=322,325
<span class="plumedtooltip">ATOMS204<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=322,326
<span class="plumedtooltip">ATOMS205<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=323,326
<span class="plumedtooltip">ATOMS206<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=323,327
<span class="plumedtooltip">ATOMS207<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=324,327
<span class="plumedtooltip">ATOMS208<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=325,328
<span class="plumedtooltip">ATOMS209<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=326,329
<span class="plumedtooltip">ATOMS210<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=348,351
<span class="plumedtooltip">ATOMS211<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=350,353
<span class="plumedtooltip">ATOMS212<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=351,354
<span class="plumedtooltip">ATOMS213<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=352,355
<span class="plumedtooltip">ATOMS214<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=357,360
<span class="plumedtooltip">ATOMS215<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=360,363
<span class="plumedtooltip">ATOMS216<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=371,374
<span class="plumedtooltip">ATOMS217<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=376,379
<span class="plumedtooltip">ATOMS218<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=386,389
<span class="plumedtooltip">ATOMS219<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=392,395
<span class="plumedtooltip">ATOMS220<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=394,397
<span class="plumedtooltip">ATOMS221<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=396,399
<span class="plumedtooltip">ATOMS222<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=399,402
<span class="plumedtooltip">ATOMS223<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=400,403
<span class="plumedtooltip">ATOMS224<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=402,405
<span class="plumedtooltip">ATOMS225<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=402,406
<span class="plumedtooltip">ATOMS226<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=407,411
<span class="plumedtooltip">ATOMS227<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=408,411
<span class="plumedtooltip">SWITCH<span class="right">The switching functions to use for each of the contacts in your map. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={CUSTOM FUNC=x R_0=1}
...
<br/><span style="display:none;" id="data/plumed_TDP-43.datdistance_rest_domains">The CONTACTMAP action with label <b>distance_rest_domains</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">distance_rest_domains.contact</td><td>By not using SUM or CMDIST each contact will be stored in a component</td></tr><tr><td width="5%">distance_rest_domains.value</td><td>the sum of all the switching function on all the distances</td></tr></table></span><b name="data/plumed_TDP-43.dataf_dist_rest" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dataf_dist_rest","data/plumed_TDP-43.dataf_dist_rest","brown")'>af_dist_rest</b>: <span class="plumedtooltip" style="color:green">CONSTANT<span class="right">Create a constant value that can be passed to actions <a href="https://www.plumed.org/doc-master/user-doc/html/CONSTANT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">VALUES<span class="right">the numbers that are in your constant value<i></i></span></span>=1.0032847926020623,1.0311901761218905,0.7455537494271994,1.7088723132386805,1.713635583035648,1.5095473634079102,1.1722138326615095,1.2549746362492442,0.9444370301440359,1.2123430594801905,1.5226123476400972,1.3369803665205837,1.4350552991032601,1.271596952714026,0.8981292195618154,1.084396699629724,1.2897209025919436,1.5121250515803697,1.0559752460569143,1.0836912801489234,0.707867799885571,0.9799594385549426,1.2259459158405663,1.5500808618962765,0.9052655544131994,1.3762398231774569,1.5152623694390062,1.68192987870425,1.6158358810469509,1.3273277390748264,1.1055688032880424,0.7953455133363603,1.0522321155294776,1.3843332368880512,1.5040866650640965,1.9200282409787175,1.9061048422008757,1.6269824001938105,1.2354281768202782,1.0676583984866739,0.6573523612692953,0.6149551127105952,0.7450687747448683,0.7618590366095304,0.5613296514376999,1.0004315715283156,0.8841317959129811,0.5908093221485615,0.9980626434087752,1.263882938399911,1.1281702172011137,1.1415027465671301,1.3193011650815607,1.4435925820842384,1.1070262966677549,1.31037020906806,0.8523610839620233,0.6740215603262186,1.1396584818139672,0.7467208079993726,1.1898928672075273,0.4552792670205237,0.8395836766809226,1.017876618169248,1.3974865483120085,1.0051763331517576,1.1795675404369834,1.4049736192449929,1.459107712842524,1.5650913815945389,1.59471937045455,1.5574198851361871,1.3527641544118525,1.4486837401986123,1.1706370314583183,1.4376086220145226,1.1653784492984414,1.7256552413105966,1.4055226838216186,1.427379228360951,0.9732663879171014,1.2228183863684539,0.9791120953857901,1.3816555082798005,0.7472525445744396,1.2260105818510056,1.0942220810800791,1.5762166528031232,1.1099413389340045,1.5934589028358461,1.434581000171602,1.630307266302407,1.2566113555803897,1.5485478518530726,1.81100521478802,1.3977122131735087,1.7663343697786331,1.162875016592443,1.430508084408939,1.6525550663471222,1.7831156572327018,1.785999870300293,1.6451806398108602,1.4654783833771945,1.2249537132680417,1.3939366523176433,1.0378110969439147,1.3681153113022448,0.9096965923905374,1.0000388860702516,1.2344506287947297,0.8380141992121936,0.8398237504065037,1.0381346080452205,1.4053251046687365,2.167353528179228,1.9828473469242454,1.528205112926662,1.8880876734852792,2.016520819067955,1.5591710267588497,1.5430319080129267,1.4479076098650694,1.236793963611126,1.3141041703522205,1.5537533987313508,1.5692297449335457,1.121472422592342,1.1581335106864572,0.91726502366364,0.9532682375982404,1.2505696462467313,1.1205617936328052,0.6651569686830044,1.0967526400461791,1.140981236472726,0.6660797173157335,0.8100334141403437,1.2571399945765735,1.1800085892900825,0.9563456442207099,1.2749242424964906,1.1340990519151093,0.9276029605418444,0.5047679111361504,0.9407211143523457,0.6309511506929995,1.074688763730228,1.2769522689282895,0.5026340553537011,0.7528656773269176,1.0695354964584112,0.9779949204996229,1.300148520246148,1.1204699540510774,1.5327852481976152,1.4124552657827738,1.2289950992912055,1.0769147641956807,1.4084996918216348,1.2656738823279738,1.0495817463845016,1.1779037110507489,1.095422700792551,1.3921284958720208,0.6597456347197295,1.0181769583374263,0.9364564327523113,1.3884215405210854,0.9055566122755409,1.1202643141150477,1.596531630679965,1.518569000810385,1.201885962113738,1.5418776268139482,1.3921274995431305,0.8939561096951366,1.1407407995313406,1.4240611214190722,1.4680646168068052,1.164111346192658,1.5423512058332562,0.9587342431768777,1.234714117459953,1.4588959828019143,1.6841880340129138,1.6086150078102948,1.4471713358536364,1.2795427026227117,1.444847053103149,1.002940315194428,1.3102364122867585,0.9022639036178589,1.2806951073929669,0.989768156595528,0.9441032137721775,0.9244450947269796,0.9194099459797145,0.9374097302556038,0.7403792202472688,0.8557088484987617,1.1484702169895173,0.7273479776456953,0.8502402873709798,0.6981262018904091,0.8579837949946523,0.7507739521563054,0.7508660649880767,0.7793322708457708,0.9225482998415828,0.9773600473999976,0.9583356784656645,0.9616499662399293,0.9474486894905567,1.0015693807974457,0.9874830450862646,0.9377102639526129,0.9753739142790437,0.9764441156759859,0.973571441695094,0.950638056918979,0.9416109262034296,0.9724794756621122,0.966675561480224,1.2231912130489944,1.235738294199109,0.9654571769759062 NODERIV
  
<span style="display:none;" id="data/plumed_TDP-43.dataf_dist_rest">The CONSTANT action with label <b>af_dist_rest</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">af_dist_rest.value</td><td>the constant value that was read from the plumed input</td></tr></table></span><b name="data/plumed_TDP-43.dataf_dist2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dataf_dist2","data/plumed_TDP-43.dataf_dist2","brown")'>af_dist2</b>: <span class="plumedtooltip" style="color:green">CONSTANT<span class="right">Create a constant value that can be passed to actions <a href="https://www.plumed.org/doc-master/user-doc/html/CONSTANT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">VALUES<span class="right">the numbers that are in your constant value<i></i></span></span>=0 NODERIV
<span style="display:none;" id="data/plumed_TDP-43.dataf_dist2">The CONSTANT action with label <b>af_dist2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">af_dist2.value</td><td>the constant value that was read from the plumed input</td></tr></table></span><b name="data/plumed_TDP-43.datRg" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.datRg","data/plumed_TDP-43.datRg","brown")'>Rg</b>: <span class="plumedtooltip" style="color:green">GYRATION<span class="right">Calculate the radius of gyration, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/GYRATION" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">TYPE<span class="right"> The type of calculation relative to the Gyration Tensor you want to perform<i></i></span></span>=RADIUS <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></span></span>=1-414
<span style="display:none;" id="data/plumed_TDP-43.datRg">The GYRATION action with label <b>Rg</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">Rg.value</td><td>the radius that was computed from the weights</td></tr></table></span><b name="data/plumed_TDP-43.datRMSD1" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.datRMSD1","data/plumed_TDP-43.datRMSD1","brown")'>RMSD1</b>: <span class="plumedtooltip" style="color:green">RMSD<span class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/RMSD" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">REFERENCE<span class="right">a file in pdb format containing the reference structure and the atoms involved in the CV<i></i></span></span>=struct1.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which RMSD alignment is performed<i></i></span></span>=OPTIMAL
<span style="display:none;" id="data/plumed_TDP-43.datRMSD1">The RMSD action with label <b>RMSD1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">RMSD1.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><b name="data/plumed_TDP-43.datRMSD2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.datRMSD2","data/plumed_TDP-43.datRMSD2","brown")'>RMSD2</b>: <span class="plumedtooltip" style="color:green">RMSD<span class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/RMSD" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">REFERENCE<span class="right">a file in pdb format containing the reference structure and the atoms involved in the CV<i></i></span></span>=struct2.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which RMSD alignment is performed<i></i></span></span>=OPTIMAL
<span style="display:none;" id="data/plumed_TDP-43.datRMSD2">The RMSD action with label <b>RMSD2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">RMSD2.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><b name="data/plumed_TDP-43.datRMSD3" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.datRMSD3","data/plumed_TDP-43.datRMSD3","brown")'>RMSD3</b>: <span class="plumedtooltip" style="color:green">RMSD<span class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/RMSD" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">REFERENCE<span class="right">a file in pdb format containing the reference structure and the atoms involved in the CV<i></i></span></span>=struct3.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which RMSD alignment is performed<i></i></span></span>=OPTIMAL
<span style="display:none;" id="data/plumed_TDP-43.datRMSD3">The RMSD action with label <b>RMSD3</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">RMSD3.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><b name="data/plumed_TDP-43.datuwall" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.datuwall","data/plumed_TDP-43.datuwall","brown")'>uwall</b>: <span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=<b name="data/plumed_TDP-43.datRMSD1">RMSD1</b>,<b name="data/plumed_TDP-43.datRMSD2">RMSD2</b>,<b name="data/plumed_TDP-43.datRMSD3">RMSD3</b> <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=0.02,0.02,0.02 <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=100000,100000,100000 <span class="plumedtooltip">EXP<span class="right"> the powers for the walls<i></i></span></span>=2,2,2 <span class="plumedtooltip">EPS<span class="right"> the values for s_i in the expression for a wall<i></i></span></span>=1,1,1 <span class="plumedtooltip">OFFSET<span class="right"> the offset for the start of the wall<i></i></span></span>=0,0,0
<span style="display:none;" id="data/plumed_TDP-43.datuwall">The UPPER_WALLS action with label <b>uwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">uwall.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">uwall.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=DISTANCE_MAP_REST <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/plumed_TDP-43.datdistance_rest_domains">distance_rest_domains.*</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=200
<span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=COLVAR <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=200
<span class="plumedtooltip" style="color:green">PBMETAD<span class="right">Used to performed Parallel Bias metadynamics. <a href="https://www.plumed.org/doc-master/user-doc/html/PBMETAD" style="color:green">More details</a><i></i></span></span> ...
    <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/plumed_TDP-43.datpb" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.datpb","data/plumed_TDP-43.datpb","brown")'>pb</b>
    <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<span style="background-color:yellow">__FILL__</span>
    <span class="plumedtooltip">SIGMA<span class="right">the widths of the Gaussian hills<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
    <span class="plumedtooltip">SIGMA_MIN<span class="right">the lower bounds for the sigmas (in CV units) when using adaptive hills<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
    <span class="plumedtooltip">SIGMA_MAX<span class="right">the upper bounds for the sigmas (in CV units) when using adaptive hills<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
    <span class="plumedtooltip">ADAPTIVE<span class="right">use a geometric (=GEOM) or diffusion (=DIFF) based hills width scheme<i></i></span></span>=DIFF
    <span class="plumedtooltip">HEIGHT<span class="right">the height of the Gaussian hills, one for all biases<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
    <span class="plumedtooltip">PACE<span class="right">the frequency for hill addition, one for all biases<i></i></span></span>=200
    <span class="plumedtooltip">BIASFACTOR<span class="right">use well tempered metadynamics with this bias factor, one for all biases<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
    <span class="plumedtooltip">GRID_MIN<span class="right">the lower bounds for the grid<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
    <span class="plumedtooltip">GRID_MAX<span class="right">the upper bounds for the grid<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
    <span class="plumedtooltip">GRID_WSTRIDE<span class="right">frequency for dumping the grid<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
    <span class="plumedtooltip">WALKERS_MPI<span class="right"> Switch on MPI version of multiple walkers - not compatible with WALKERS_* options other than WALKERS_DIR<i></i></span></span>
    <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is only needed if you are doing well-tempered metadynamics<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
... PBMETAD
<span style="display:none;" id="data/plumed_TDP-43.datpb">The PBMETAD action with label <b>pb</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">pb.bias</td><td>the instantaneous value of the bias potential</td></tr></table></span><span class="plumedtooltip" style="color:green">METAINFERENCE<span class="right">Calculates the Metainference energy for a set of experimental data. <a href="https://www.plumed.org/doc-master/user-doc/html/METAINFERENCE" style="color:green">More details</a><i></i></span></span> ...
    <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=(distance_rest_domains.*),<b name="data/plumed_TDP-43.datpb">pb.bias</b> <span class="plumedtooltip">REWEIGHT<span class="right"> simple REWEIGHT using the latest ARG as energy<i></i></span></span>
    <span class="plumedtooltip">PARARG<span class="right">reference values for the experimental data, these can be provided as arguments without derivatives<i></i></span></span>=(af_dist_rest.*)
    <span class="plumedtooltip">SIGMA_MEAN0<span class="right">starting value for the uncertainty in the mean estimate<i></i></span></span>=1
    <span class="plumedtooltip">NOISETYPE<span class="right"> functional form of the noise (GAUSS,MGAUSS,OUTLIERS,MOUTLIERS,GENERIC)<i></i></span></span>=MGAUSS  <span class="plumedtooltip">OPTSIGMAMEAN<span class="right"> Set to NONE/SEM to manually set sigma mean, or to estimate it on the fly<i></i></span></span>=SEM <span class="plumedtooltip">AVERAGING<span class="right">Stride for calculation of averaged weights and sigma_mean<i></i></span></span>=200
    <span class="plumedtooltip">SIGMA0<span class="right"> initial value of the uncertainty parameter<i></i></span></span>=10.0 <span class="plumedtooltip">SIGMA_MIN<span class="right"> minimum value of the uncertainty parameter<i></i></span></span>=0.0001 <span class="plumedtooltip">SIGMA_MAX<span class="right"> maximum value of the uncertainty parameter<i></i></span></span>=10.0 <span class="plumedtooltip">DSIGMA<span class="right">maximum MC move of the uncertainty parameter<i></i></span></span>=0.1
    <span class="plumedtooltip">MC_STEPS<span class="right">number of MC steps<i></i></span></span>=10
    <span class="plumedtooltip">MC_CHUNKSIZE<span class="right">MC chunksize<i></i></span></span>=23
    <span class="plumedtooltip">WRITE_STRIDE<span class="right"> write the status to a file every N steps, this can be used for restart/continuation<i></i></span></span>=10000
    <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is only needed if code doesn't pass the temperature to plumed<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
    <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/plumed_TDP-43.dataf_mi_rest_domains" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dataf_mi_rest_domains","data/plumed_TDP-43.dataf_mi_rest_domains","brown")'>af_mi_rest_domains</b>
... METAINFERENCE
<span style="display:none;" id="data/plumed_TDP-43.dataf_mi_rest_domains">The METAINFERENCE action with label <b>af_mi_rest_domains</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">af_mi_rest_domains.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">af_mi_rest_domains.sigma</td><td>uncertainty parameter</td></tr><tr><td width="5%">af_mi_rest_domains.sigmaMean</td><td>uncertainty in the mean estimate</td></tr><tr><td width="5%">af_mi_rest_domains.neff</td><td>effective number of replicas</td></tr><tr><td width="5%">af_mi_rest_domains.acceptSigma</td><td>MC acceptance for sigma values</td></tr><tr><td width="5%">af_mi_rest_domains.weight</td><td>weights of the weighted average</td></tr><tr><td width="5%">af_mi_rest_domains.biasDer</td><td>derivatives with respect to the bias</td></tr></table></span><span class="plumedtooltip" style="color:green">FLUSH<span class="right">This command instructs plumed to flush all the open files with a user specified frequency. <a href="https://www.plumed.org/doc-master/user-doc/html/FLUSH" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">STRIDE<span class="right">the frequency with which all the open files should be flushed<i></i></span></span>=200
<span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=ENERGY <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/plumed_TDP-43.datpb">pb.bias</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=200
<span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/plumed_TDP-43.dataf_mi_rest_domains">af_mi_rest_domains.*</b>   <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=200 <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=BAYES_rest_domains
<span class="plumedtooltip" style="color:green">ENDPLUMED<span class="right">Terminate plumed input. <a href="https://www.plumed.org/doc-master/user-doc/html/ENDPLUMED" style="color:green">More details</a><i></i></span></span><span style="color:blue" class="comment">
</span></pre></div>
<div style="display:none;" id="data/plumed_TDP-43.dat_long"><pre class="plumedlisting">
<span class="plumedtooltip" style="color:green">MOLINFO<span class="right">This command is used to provide information on the molecules that are present in your system. <a href="https://www.plumed.org/doc-master/user-doc/html/MOLINFO" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">MOLTYPE<span class="right"> what kind of molecule is contained in the pdb file - usually not needed since protein/RNA/DNA are compatible<i></i></span></span>=protein <span class="plumedtooltip">STRUCTURE<span class="right">a file in pdb format containing a reference structure<i></i></span></span>=input_af.pdb
<span style="display:none;" id="data/plumed_TDP-43.dat_sol">The MOLINFO action with label <b></b> calculates something</span><span class="plumedtooltip" style="color:green">WHOLEMOLECULES<span class="right">This action is used to rebuild molecules that can become split by the periodic boundary conditions. <a href="https://www.plumed.org/doc-master/user-doc/html/WHOLEMOLECULES" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ENTITY0<span class="right">the atoms that make up a molecule that you wish to align<i></i></span></span>=1-414

<b name="data/plumed_TDP-43.dat_soldistance_rest_domains" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soldistance_rest_domains","data/plumed_TDP-43.dat_soldistance_rest_domains","brown")'>distance_rest_domains</b>:  <span class="plumedtooltip" style="color:green">CONTACTMAP<span class="right">Calculate the distances between a number of pairs of atoms and transform each distance by a switching function. <a href="https://www.plumed.org/doc-master/user-doc/html/CONTACTMAP" style="color:green">More details</a><i></i></span></span> ...
<span class="plumedtooltip">ATOMS1<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=1,4
<span class="plumedtooltip">ATOMS2<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=2,5
<span class="plumedtooltip">ATOMS3<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=2,20
<span class="plumedtooltip">ATOMS4<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=28,79
<span class="plumedtooltip">ATOMS5<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=31,79
<span class="plumedtooltip">ATOMS6<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=35,79
<span class="plumedtooltip">ATOMS7<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=37,79
<span class="plumedtooltip">ATOMS8<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=38,79
<span class="plumedtooltip">ATOMS9<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=39,79
<span class="plumedtooltip">ATOMS10<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=40,79
<span class="plumedtooltip">ATOMS11<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=41,79
<span class="plumedtooltip">ATOMS12<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=42,79
<span class="plumedtooltip">ATOMS13<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=74,79
<span class="plumedtooltip">ATOMS14<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=75,79
<span class="plumedtooltip">ATOMS15<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=76,79
<span class="plumedtooltip">ATOMS16<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,105
<span class="plumedtooltip">ATOMS17<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,106
<span class="plumedtooltip">ATOMS18<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,150
<span class="plumedtooltip">ATOMS19<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,151
<span class="plumedtooltip">ATOMS20<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,152
<span class="plumedtooltip">ATOMS21<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,155
<span class="plumedtooltip">ATOMS22<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,158
<span class="plumedtooltip">ATOMS23<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,159
<span class="plumedtooltip">ATOMS24<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=102,161
<span class="plumedtooltip">ATOMS25<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,106
<span class="plumedtooltip">ATOMS26<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,107
<span class="plumedtooltip">ATOMS27<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,108
<span class="plumedtooltip">ATOMS28<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,120
<span class="plumedtooltip">ATOMS29<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,121
<span class="plumedtooltip">ATOMS30<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,124
<span class="plumedtooltip">ATOMS31<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,130
<span class="plumedtooltip">ATOMS32<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,131
<span class="plumedtooltip">ATOMS33<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,132
<span class="plumedtooltip">ATOMS34<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,133
<span class="plumedtooltip">ATOMS35<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,134
<span class="plumedtooltip">ATOMS36<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,135
<span class="plumedtooltip">ATOMS37<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,147
<span class="plumedtooltip">ATOMS38<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,148
<span class="plumedtooltip">ATOMS39<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,149
<span class="plumedtooltip">ATOMS40<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,150
<span class="plumedtooltip">ATOMS41<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,151
<span class="plumedtooltip">ATOMS42<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,152
<span class="plumedtooltip">ATOMS43<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,153
<span class="plumedtooltip">ATOMS44<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,154
<span class="plumedtooltip">ATOMS45<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,155
<span class="plumedtooltip">ATOMS46<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,156
<span class="plumedtooltip">ATOMS47<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,157
<span class="plumedtooltip">ATOMS48<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,158
<span class="plumedtooltip">ATOMS49<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,159
<span class="plumedtooltip">ATOMS50<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,160
<span class="plumedtooltip">ATOMS51<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,161
<span class="plumedtooltip">ATOMS52<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,162
<span class="plumedtooltip">ATOMS53<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,175
<span class="plumedtooltip">ATOMS54<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,176
<span class="plumedtooltip">ATOMS55<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,177
<span class="plumedtooltip">ATOMS56<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=103,178
<span class="plumedtooltip">ATOMS57<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=104,178
<span class="plumedtooltip">ATOMS58<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=105,178
<span class="plumedtooltip">ATOMS59<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=105,179
<span class="plumedtooltip">ATOMS60<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=106,178
<span class="plumedtooltip">ATOMS61<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=106,179
<span class="plumedtooltip">ATOMS62<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=107,178
<span class="plumedtooltip">ATOMS63<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=107,179
<span class="plumedtooltip">ATOMS64<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=108,178
<span class="plumedtooltip">ATOMS65<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=108,179
<span class="plumedtooltip">ATOMS66<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=109,178
<span class="plumedtooltip">ATOMS67<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=109,179
<span class="plumedtooltip">ATOMS68<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=110,178
<span class="plumedtooltip">ATOMS69<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=111,178
<span class="plumedtooltip">ATOMS70<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=120,178
<span class="plumedtooltip">ATOMS71<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=124,178
<span class="plumedtooltip">ATOMS72<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=131,178
<span class="plumedtooltip">ATOMS73<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=132,178
<span class="plumedtooltip">ATOMS74<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=133,178
<span class="plumedtooltip">ATOMS75<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=134,178
<span class="plumedtooltip">ATOMS76<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=135,178
<span class="plumedtooltip">ATOMS77<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=136,178
<span class="plumedtooltip">ATOMS78<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=137,178
<span class="plumedtooltip">ATOMS79<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=145,178
<span class="plumedtooltip">ATOMS80<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=146,178
<span class="plumedtooltip">ATOMS81<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=147,178
<span class="plumedtooltip">ATOMS82<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=147,179
<span class="plumedtooltip">ATOMS83<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=148,178
<span class="plumedtooltip">ATOMS84<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=148,179
<span class="plumedtooltip">ATOMS85<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=149,178
<span class="plumedtooltip">ATOMS86<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=149,179
<span class="plumedtooltip">ATOMS87<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=150,178
<span class="plumedtooltip">ATOMS88<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=150,179
<span class="plumedtooltip">ATOMS89<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=151,178
<span class="plumedtooltip">ATOMS90<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=151,179
<span class="plumedtooltip">ATOMS91<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=152,178
<span class="plumedtooltip">ATOMS92<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=155,178
<span class="plumedtooltip">ATOMS93<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=158,178
<span class="plumedtooltip">ATOMS94<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=159,178
<span class="plumedtooltip">ATOMS95<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=159,179
<span class="plumedtooltip">ATOMS96<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=161,178
<span class="plumedtooltip">ATOMS97<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=161,179
<span class="plumedtooltip">ATOMS98<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=162,178
<span class="plumedtooltip">ATOMS99<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=162,179
<span class="plumedtooltip">ATOMS100<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=163,178
<span class="plumedtooltip">ATOMS101<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=164,178
<span class="plumedtooltip">ATOMS102<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=165,178
<span class="plumedtooltip">ATOMS103<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=166,178
<span class="plumedtooltip">ATOMS104<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=173,178
<span class="plumedtooltip">ATOMS105<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=174,178
<span class="plumedtooltip">ATOMS106<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=174,179
<span class="plumedtooltip">ATOMS107<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=175,178
<span class="plumedtooltip">ATOMS108<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=175,179
<span class="plumedtooltip">ATOMS109<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=176,179
<span class="plumedtooltip">ATOMS110<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=189,192
<span class="plumedtooltip">ATOMS111<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=189,233
<span class="plumedtooltip">ATOMS112<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=189,240
<span class="plumedtooltip">ATOMS113<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,193
<span class="plumedtooltip">ATOMS114<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,194
<span class="plumedtooltip">ATOMS115<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,195
<span class="plumedtooltip">ATOMS116<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,209
<span class="plumedtooltip">ATOMS117<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,210
<span class="plumedtooltip">ATOMS118<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,211
<span class="plumedtooltip">ATOMS119<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,212
<span class="plumedtooltip">ATOMS120<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,213
<span class="plumedtooltip">ATOMS121<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,214
<span class="plumedtooltip">ATOMS122<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,216
<span class="plumedtooltip">ATOMS123<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,217
<span class="plumedtooltip">ATOMS124<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,218
<span class="plumedtooltip">ATOMS125<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,219
<span class="plumedtooltip">ATOMS126<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,220
<span class="plumedtooltip">ATOMS127<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,230
<span class="plumedtooltip">ATOMS128<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,231
<span class="plumedtooltip">ATOMS129<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,232
<span class="plumedtooltip">ATOMS130<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,233
<span class="plumedtooltip">ATOMS131<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,234
<span class="plumedtooltip">ATOMS132<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,235
<span class="plumedtooltip">ATOMS133<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,236
<span class="plumedtooltip">ATOMS134<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,237
<span class="plumedtooltip">ATOMS135<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,238
<span class="plumedtooltip">ATOMS136<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,239
<span class="plumedtooltip">ATOMS137<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,240
<span class="plumedtooltip">ATOMS138<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,241
<span class="plumedtooltip">ATOMS139<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,242
<span class="plumedtooltip">ATOMS140<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,243
<span class="plumedtooltip">ATOMS141<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,244
<span class="plumedtooltip">ATOMS142<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,257
<span class="plumedtooltip">ATOMS143<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=190,258
<span class="plumedtooltip">ATOMS144<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=191,260
<span class="plumedtooltip">ATOMS145<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=192,260
<span class="plumedtooltip">ATOMS146<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=192,261
<span class="plumedtooltip">ATOMS147<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=193,260
<span class="plumedtooltip">ATOMS148<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=193,261
<span class="plumedtooltip">ATOMS149<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=193,262
<span class="plumedtooltip">ATOMS150<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=194,260
<span class="plumedtooltip">ATOMS151<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=194,261
<span class="plumedtooltip">ATOMS152<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=194,262
<span class="plumedtooltip">ATOMS153<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=195,260
<span class="plumedtooltip">ATOMS154<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=195,261
<span class="plumedtooltip">ATOMS155<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=196,260
<span class="plumedtooltip">ATOMS156<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=197,260
<span class="plumedtooltip">ATOMS157<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=211,260
<span class="plumedtooltip">ATOMS158<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=219,260
<span class="plumedtooltip">ATOMS159<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=221,260
<span class="plumedtooltip">ATOMS160<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=222,260
<span class="plumedtooltip">ATOMS161<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=223,260
<span class="plumedtooltip">ATOMS162<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=229,260
<span class="plumedtooltip">ATOMS163<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=229,261
<span class="plumedtooltip">ATOMS164<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=230,260
<span class="plumedtooltip">ATOMS165<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=230,261
<span class="plumedtooltip">ATOMS166<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=231,260
<span class="plumedtooltip">ATOMS167<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=231,261
<span class="plumedtooltip">ATOMS168<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=232,260
<span class="plumedtooltip">ATOMS169<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=232,261
<span class="plumedtooltip">ATOMS170<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=233,260
<span class="plumedtooltip">ATOMS171<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=234,260
<span class="plumedtooltip">ATOMS172<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=234,261
<span class="plumedtooltip">ATOMS173<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=236,260
<span class="plumedtooltip">ATOMS174<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=237,260
<span class="plumedtooltip">ATOMS175<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=238,260
<span class="plumedtooltip">ATOMS176<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=239,260
<span class="plumedtooltip">ATOMS177<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=240,260
<span class="plumedtooltip">ATOMS178<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=241,260
<span class="plumedtooltip">ATOMS179<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=241,261
<span class="plumedtooltip">ATOMS180<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=242,260
<span class="plumedtooltip">ATOMS181<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=243,260
<span class="plumedtooltip">ATOMS182<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=243,261
<span class="plumedtooltip">ATOMS183<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=244,260
<span class="plumedtooltip">ATOMS184<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=245,260
<span class="plumedtooltip">ATOMS185<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=246,260
<span class="plumedtooltip">ATOMS186<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=247,260
<span class="plumedtooltip">ATOMS187<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=248,260
<span class="plumedtooltip">ATOMS188<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=255,260
<span class="plumedtooltip">ATOMS189<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=256,260
<span class="plumedtooltip">ATOMS190<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=256,261
<span class="plumedtooltip">ATOMS191<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=257,260
<span class="plumedtooltip">ATOMS192<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=257,261
<span class="plumedtooltip">ATOMS193<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=258,261
<span class="plumedtooltip">ATOMS194<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=258,262
<span class="plumedtooltip">ATOMS195<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=259,262
<span class="plumedtooltip">ATOMS196<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=298,301
<span class="plumedtooltip">ATOMS197<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=300,303
<span class="plumedtooltip">ATOMS198<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=304,307
<span class="plumedtooltip">ATOMS199<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=318,321
<span class="plumedtooltip">ATOMS200<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=321,324
<span class="plumedtooltip">ATOMS201<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=321,325
<span class="plumedtooltip">ATOMS202<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=321,326
<span class="plumedtooltip">ATOMS203<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=322,325
<span class="plumedtooltip">ATOMS204<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=322,326
<span class="plumedtooltip">ATOMS205<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=323,326
<span class="plumedtooltip">ATOMS206<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=323,327
<span class="plumedtooltip">ATOMS207<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=324,327
<span class="plumedtooltip">ATOMS208<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=325,328
<span class="plumedtooltip">ATOMS209<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=326,329
<span class="plumedtooltip">ATOMS210<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=348,351
<span class="plumedtooltip">ATOMS211<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=350,353
<span class="plumedtooltip">ATOMS212<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=351,354
<span class="plumedtooltip">ATOMS213<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=352,355
<span class="plumedtooltip">ATOMS214<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=357,360
<span class="plumedtooltip">ATOMS215<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=360,363
<span class="plumedtooltip">ATOMS216<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=371,374
<span class="plumedtooltip">ATOMS217<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=376,379
<span class="plumedtooltip">ATOMS218<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=386,389
<span class="plumedtooltip">ATOMS219<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=392,395
<span class="plumedtooltip">ATOMS220<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=394,397
<span class="plumedtooltip">ATOMS221<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=396,399
<span class="plumedtooltip">ATOMS222<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=399,402
<span class="plumedtooltip">ATOMS223<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=400,403
<span class="plumedtooltip">ATOMS224<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=402,405
<span class="plumedtooltip">ATOMS225<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=402,406
<span class="plumedtooltip">ATOMS226<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=407,411
<span class="plumedtooltip">ATOMS227<span class="right">the atoms involved in each of the contacts you wish to calculate<i></i></span></span>=408,411
<span class="plumedtooltip">SWITCH<span class="right">The switching functions to use for each of the contacts in your map. Options for this keyword are explained in the documentation for <a href="https://www.plumed.org/doc-master/user-doc/html/LESS_THAN">LESS_THAN</a>.<i></i></span></span>={CUSTOM FUNC=x R_0=1}
...
<br/><span style="display:none;" id="data/plumed_TDP-43.dat_soldistance_rest_domains">The CONTACTMAP action with label <b>distance_rest_domains</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">distance_rest_domains.contact</td><td>By not using SUM or CMDIST each contact will be stored in a component</td></tr><tr><td width="5%">distance_rest_domains.value</td><td>the sum of all the switching function on all the distances</td></tr></table></span><b name="data/plumed_TDP-43.dat_solaf_dist_rest" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solaf_dist_rest","data/plumed_TDP-43.dat_solaf_dist_rest","brown")'>af_dist_rest</b>: <span class="plumedtooltip" style="color:green">CONSTANT<span class="right">Create a constant value that can be passed to actions <a href="https://www.plumed.org/doc-master/user-doc/html/CONSTANT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">VALUES<span class="right">the numbers that are in your constant value<i></i></span></span>=1.0032847926020623,1.0311901761218905,0.7455537494271994,1.7088723132386805,1.713635583035648,1.5095473634079102,1.1722138326615095,1.2549746362492442,0.9444370301440359,1.2123430594801905,1.5226123476400972,1.3369803665205837,1.4350552991032601,1.271596952714026,0.8981292195618154,1.084396699629724,1.2897209025919436,1.5121250515803697,1.0559752460569143,1.0836912801489234,0.707867799885571,0.9799594385549426,1.2259459158405663,1.5500808618962765,0.9052655544131994,1.3762398231774569,1.5152623694390062,1.68192987870425,1.6158358810469509,1.3273277390748264,1.1055688032880424,0.7953455133363603,1.0522321155294776,1.3843332368880512,1.5040866650640965,1.9200282409787175,1.9061048422008757,1.6269824001938105,1.2354281768202782,1.0676583984866739,0.6573523612692953,0.6149551127105952,0.7450687747448683,0.7618590366095304,0.5613296514376999,1.0004315715283156,0.8841317959129811,0.5908093221485615,0.9980626434087752,1.263882938399911,1.1281702172011137,1.1415027465671301,1.3193011650815607,1.4435925820842384,1.1070262966677549,1.31037020906806,0.8523610839620233,0.6740215603262186,1.1396584818139672,0.7467208079993726,1.1898928672075273,0.4552792670205237,0.8395836766809226,1.017876618169248,1.3974865483120085,1.0051763331517576,1.1795675404369834,1.4049736192449929,1.459107712842524,1.5650913815945389,1.59471937045455,1.5574198851361871,1.3527641544118525,1.4486837401986123,1.1706370314583183,1.4376086220145226,1.1653784492984414,1.7256552413105966,1.4055226838216186,1.427379228360951,0.9732663879171014,1.2228183863684539,0.9791120953857901,1.3816555082798005,0.7472525445744396,1.2260105818510056,1.0942220810800791,1.5762166528031232,1.1099413389340045,1.5934589028358461,1.434581000171602,1.630307266302407,1.2566113555803897,1.5485478518530726,1.81100521478802,1.3977122131735087,1.7663343697786331,1.162875016592443,1.430508084408939,1.6525550663471222,1.7831156572327018,1.785999870300293,1.6451806398108602,1.4654783833771945,1.2249537132680417,1.3939366523176433,1.0378110969439147,1.3681153113022448,0.9096965923905374,1.0000388860702516,1.2344506287947297,0.8380141992121936,0.8398237504065037,1.0381346080452205,1.4053251046687365,2.167353528179228,1.9828473469242454,1.528205112926662,1.8880876734852792,2.016520819067955,1.5591710267588497,1.5430319080129267,1.4479076098650694,1.236793963611126,1.3141041703522205,1.5537533987313508,1.5692297449335457,1.121472422592342,1.1581335106864572,0.91726502366364,0.9532682375982404,1.2505696462467313,1.1205617936328052,0.6651569686830044,1.0967526400461791,1.140981236472726,0.6660797173157335,0.8100334141403437,1.2571399945765735,1.1800085892900825,0.9563456442207099,1.2749242424964906,1.1340990519151093,0.9276029605418444,0.5047679111361504,0.9407211143523457,0.6309511506929995,1.074688763730228,1.2769522689282895,0.5026340553537011,0.7528656773269176,1.0695354964584112,0.9779949204996229,1.300148520246148,1.1204699540510774,1.5327852481976152,1.4124552657827738,1.2289950992912055,1.0769147641956807,1.4084996918216348,1.2656738823279738,1.0495817463845016,1.1779037110507489,1.095422700792551,1.3921284958720208,0.6597456347197295,1.0181769583374263,0.9364564327523113,1.3884215405210854,0.9055566122755409,1.1202643141150477,1.596531630679965,1.518569000810385,1.201885962113738,1.5418776268139482,1.3921274995431305,0.8939561096951366,1.1407407995313406,1.4240611214190722,1.4680646168068052,1.164111346192658,1.5423512058332562,0.9587342431768777,1.234714117459953,1.4588959828019143,1.6841880340129138,1.6086150078102948,1.4471713358536364,1.2795427026227117,1.444847053103149,1.002940315194428,1.3102364122867585,0.9022639036178589,1.2806951073929669,0.989768156595528,0.9441032137721775,0.9244450947269796,0.9194099459797145,0.9374097302556038,0.7403792202472688,0.8557088484987617,1.1484702169895173,0.7273479776456953,0.8502402873709798,0.6981262018904091,0.8579837949946523,0.7507739521563054,0.7508660649880767,0.7793322708457708,0.9225482998415828,0.9773600473999976,0.9583356784656645,0.9616499662399293,0.9474486894905567,1.0015693807974457,0.9874830450862646,0.9377102639526129,0.9753739142790437,0.9764441156759859,0.973571441695094,0.950638056918979,0.9416109262034296,0.9724794756621122,0.966675561480224,1.2231912130489944,1.235738294199109,0.9654571769759062 NODERIV
<br/><span style="display:none;" id="data/plumed_TDP-43.dat_solaf_dist_rest">The CONSTANT action with label <b>af_dist_rest</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">af_dist_rest.value</td><td>the constant value that was read from the plumed input</td></tr></table></span><b name="data/plumed_TDP-43.dat_solaf_dist2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solaf_dist2","data/plumed_TDP-43.dat_solaf_dist2","brown")'>af_dist2</b>: <span class="plumedtooltip" style="color:green">CONSTANT<span class="right">Create a constant value that can be passed to actions <a href="https://www.plumed.org/doc-master/user-doc/html/CONSTANT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">VALUES<span class="right">the numbers that are in your constant value<i></i></span></span>=0 NODERIV
<span style="display:none;" id="data/plumed_TDP-43.dat_solaf_dist2">The CONSTANT action with label <b>af_dist2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">af_dist2.value</td><td>the constant value that was read from the plumed input</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRg" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRg","data/plumed_TDP-43.dat_solRg","brown")'>Rg</b>: <span class="plumedtooltip" style="color:green">GYRATION<span class="right">Calculate the radius of gyration, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/GYRATION" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">TYPE<span class="right"> The type of calculation relative to the Gyration Tensor you want to perform<i></i></span></span>=RADIUS <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></span></span>=1-414
<span style="display:none;" id="data/plumed_TDP-43.dat_solRg">The GYRATION action with label <b>Rg</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">Rg.value</td><td>the radius that was computed from the weights</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRMSD1" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRMSD1","data/plumed_TDP-43.dat_solRMSD1","brown")'>RMSD1</b>: <span class="plumedtooltip" style="color:green">RMSD<span class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/RMSD" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">REFERENCE<span class="right">a file in pdb format containing the reference structure and the atoms involved in the CV<i></i></span></span>=struct1.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which RMSD alignment is performed<i></i></span></span>=OPTIMAL
<span style="display:none;" id="data/plumed_TDP-43.dat_solRMSD1">The RMSD action with label <b>RMSD1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">RMSD1.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRMSD2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRMSD2","data/plumed_TDP-43.dat_solRMSD2","brown")'>RMSD2</b>: <span class="plumedtooltip" style="color:green">RMSD<span class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/RMSD" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">REFERENCE<span class="right">a file in pdb format containing the reference structure and the atoms involved in the CV<i></i></span></span>=struct2.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which RMSD alignment is performed<i></i></span></span>=OPTIMAL
<span style="display:none;" id="data/plumed_TDP-43.dat_solRMSD2">The RMSD action with label <b>RMSD2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">RMSD2.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRMSD3" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRMSD3","data/plumed_TDP-43.dat_solRMSD3","brown")'>RMSD3</b>: <span class="plumedtooltip" style="color:green">RMSD<span class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/RMSD" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">REFERENCE<span class="right">a file in pdb format containing the reference structure and the atoms involved in the CV<i></i></span></span>=struct3.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which RMSD alignment is performed<i></i></span></span>=OPTIMAL

<span style="display:none;" id="data/plumed_TDP-43.dat_solRMSD3">The RMSD action with label <b>RMSD3</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">RMSD3.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><b name="data/plumed_TDP-43.dat_soluwall" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soluwall","data/plumed_TDP-43.dat_soluwall","brown")'>uwall</b>: <span class="plumedtooltip" style="color:green">UPPER_WALLS<span class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/UPPER_WALLS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the arguments on which the bias is acting<i></i></span></span>=<b name="data/plumed_TDP-43.dat_solRMSD1">RMSD1</b>,<b name="data/plumed_TDP-43.dat_solRMSD2">RMSD2</b>,<b name="data/plumed_TDP-43.dat_solRMSD3">RMSD3</b> <span class="plumedtooltip">AT<span class="right">the positions of the wall<i></i></span></span>=0.02,0.02,0.02 <span class="plumedtooltip">KAPPA<span class="right">the force constant for the wall<i></i></span></span>=100000,100000,100000 <span class="plumedtooltip">EXP<span class="right"> the powers for the walls<i></i></span></span>=2,2,2 <span class="plumedtooltip">EPS<span class="right"> the values for s_i in the expression for a wall<i></i></span></span>=1,1,1 <span class="plumedtooltip">OFFSET<span class="right"> the offset for the start of the wall<i></i></span></span>=0,0,0
<span style="display:none;" id="data/plumed_TDP-43.dat_soluwall">The UPPER_WALLS action with label <b>uwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">uwall.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">uwall.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRg1" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRg1","data/plumed_TDP-43.dat_solRg1","brown")'>Rg1</b>: <span class="plumedtooltip" style="color:green">GYRATION<span class="right">Calculate the radius of gyration, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/GYRATION" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">TYPE<span class="right"> The type of calculation relative to the Gyration Tensor you want to perform<i></i></span></span>=RADIUS <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></span></span>=1-2
<span style="display:none;" id="data/plumed_TDP-43.dat_solRg1">The GYRATION action with label <b>Rg1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">Rg1.value</td><td>the radius that was computed from the weights</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRg2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRg2","data/plumed_TDP-43.dat_solRg2","brown")'>Rg2</b>: <span class="plumedtooltip" style="color:green">GYRATION<span class="right">Calculate the radius of gyration, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/GYRATION" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">TYPE<span class="right"> The type of calculation relative to the Gyration Tensor you want to perform<i></i></span></span>=RADIUS <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></span></span>=80-103
<span style="display:none;" id="data/plumed_TDP-43.dat_solRg2">The GYRATION action with label <b>Rg2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">Rg2.value</td><td>the radius that was computed from the weights</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRg3" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRg3","data/plumed_TDP-43.dat_solRg3","brown")'>Rg3</b>: <span class="plumedtooltip" style="color:green">GYRATION<span class="right">Calculate the radius of gyration, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/GYRATION" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">TYPE<span class="right"> The type of calculation relative to the Gyration Tensor you want to perform<i></i></span></span>=RADIUS <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></span></span>=179-190
<span style="display:none;" id="data/plumed_TDP-43.dat_solRg3">The GYRATION action with label <b>Rg3</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">Rg3.value</td><td>the radius that was computed from the weights</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRg4" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRg4","data/plumed_TDP-43.dat_solRg4","brown")'>Rg4</b>: <span class="plumedtooltip" style="color:green">GYRATION<span class="right">Calculate the radius of gyration, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/GYRATION" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">TYPE<span class="right"> The type of calculation relative to the Gyration Tensor you want to perform<i></i></span></span>=RADIUS <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></span></span>=261-414
<span style="display:none;" id="data/plumed_TDP-43.dat_solRg4">The GYRATION action with label <b>Rg4</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">Rg4.value</td><td>the radius that was computed from the weights</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=COLVAR <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/plumed_TDP-43.dat_solRg">Rg</b>,<b name="data/plumed_TDP-43.dat_solRMSD1">RMSD1</b>,<b name="data/plumed_TDP-43.dat_solRMSD2">RMSD2</b>,<b name="data/plumed_TDP-43.dat_solRMSD3">RMSD3</b>,<b name="data/plumed_TDP-43.dat_solRg1">Rg1</b>,<b name="data/plumed_TDP-43.dat_solRg2">Rg2</b>,<b name="data/plumed_TDP-43.dat_solRg3">Rg3</b>,<b name="data/plumed_TDP-43.dat_solRg4">Rg4</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=200
<span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=DISTANCE_MAP_REST <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/plumed_TDP-43.dat_soldistance_rest_domains">distance_rest_domains.*</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=200

<b name="data/plumed_TDP-43.dat_solt1" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solt1","data/plumed_TDP-43.dat_solt1","brown")'>t1</b>: <span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=3-40
<span style="display:none;" id="data/plumed_TDP-43.dat_solt1">The CENTER action with label <b>t1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">t1.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_solt2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solt2","data/plumed_TDP-43.dat_solt2","brown")'>t2</b>: <span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=41-79
<span style="display:none;" id="data/plumed_TDP-43.dat_solt2">The CENTER action with label <b>t2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">t2.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_solt3" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solt3","data/plumed_TDP-43.dat_solt3","brown")'>t3</b>: <span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=104-140
<span style="display:none;" id="data/plumed_TDP-43.dat_solt3">The CENTER action with label <b>t3</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">t3.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_solt4" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solt4","data/plumed_TDP-43.dat_solt4","brown")'>t4</b>: <span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=141-178

<span style="display:none;" id="data/plumed_TDP-43.dat_solt4">The CENTER action with label <b>t4</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">t4.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_soltorsion1" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soltorsion1","data/plumed_TDP-43.dat_soltorsion1","brown")'>torsion1</b>: <span class="plumedtooltip" style="color:green">TORSION<span class="right">Calculate one or multiple torsional angles. <a href="https://www.plumed.org/doc-master/user-doc/html/TORSION" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the four atoms involved in the torsional angle<i></i></span></span>=<b name="data/plumed_TDP-43.dat_solt1">t1</b>,<b name="data/plumed_TDP-43.dat_solt2">t2</b>,<b name="data/plumed_TDP-43.dat_solt3">t3</b>,<b name="data/plumed_TDP-43.dat_solt4">t4</b>

<span style="display:none;" id="data/plumed_TDP-43.dat_soltorsion1">The TORSION action with label <b>torsion1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">torsion1.value</td><td>the TORSION involving these atoms</td></tr></table></span><b name="data/plumed_TDP-43.dat_soltt1" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soltt1","data/plumed_TDP-43.dat_soltt1","brown")'>tt1</b>: <span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=104-140
<span style="display:none;" id="data/plumed_TDP-43.dat_soltt1">The CENTER action with label <b>tt1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">tt1.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_soltt2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soltt2","data/plumed_TDP-43.dat_soltt2","brown")'>tt2</b>: <span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=141-178
<span style="display:none;" id="data/plumed_TDP-43.dat_soltt2">The CENTER action with label <b>tt2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">tt2.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_soltt3" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soltt3","data/plumed_TDP-43.dat_soltt3","brown")'>tt3</b>: <span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=191-225
<span style="display:none;" id="data/plumed_TDP-43.dat_soltt3">The CENTER action with label <b>tt3</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">tt3.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_soltt4" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soltt4","data/plumed_TDP-43.dat_soltt4","brown")'>tt4</b>: <span class="plumedtooltip" style="color:green">CENTER<span class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/CENTER" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the group of atoms that appear in the definition of this center<i></i></span></span>=226-260

<span style="display:none;" id="data/plumed_TDP-43.dat_soltt4">The CENTER action with label <b>tt4</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">tt4.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_soltorsion2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soltorsion2","data/plumed_TDP-43.dat_soltorsion2","brown")'>torsion2</b>: <span class="plumedtooltip" style="color:green">TORSION<span class="right">Calculate one or multiple torsional angles. <a href="https://www.plumed.org/doc-master/user-doc/html/TORSION" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the four atoms involved in the torsional angle<i></i></span></span>=<b name="data/plumed_TDP-43.dat_soltt1">tt1</b>,<b name="data/plumed_TDP-43.dat_soltt2">tt2</b>,<b name="data/plumed_TDP-43.dat_soltt3">tt3</b>,<b name="data/plumed_TDP-43.dat_soltt4">tt4</b>


<span style="color:blue" class="comment"># PBMetaD</span>
<span style="display:none;" id="data/plumed_TDP-43.dat_soltorsion2">The TORSION action with label <b>torsion2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">torsion2.value</td><td>the TORSION involving these atoms</td></tr></table></span><span class="plumedtooltip" style="color:green">PBMETAD<span class="right">Used to performed Parallel Bias metadynamics. <a href="https://www.plumed.org/doc-master/user-doc/html/PBMETAD" style="color:green">More details</a><i></i></span></span> ...
    <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/plumed_TDP-43.dat_solpb" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solpb","data/plumed_TDP-43.dat_solpb","brown")'>pb</b>
    <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=<b name="data/plumed_TDP-43.dat_soltorsion1">torsion1</b>,<b name="data/plumed_TDP-43.dat_soltorsion2">torsion2</b>
    <span class="plumedtooltip">SIGMA<span class="right">the widths of the Gaussian hills<i></i></span></span>=1000
    <span class="plumedtooltip">SIGMA_MIN<span class="right">the lower bounds for the sigmas (in CV units) when using adaptive hills<i></i></span></span>=0.05,0.05
    <span class="plumedtooltip">SIGMA_MAX<span class="right">the upper bounds for the sigmas (in CV units) when using adaptive hills<i></i></span></span>=0.1,0.1
    <span class="plumedtooltip">ADAPTIVE<span class="right">use a geometric (=GEOM) or diffusion (=DIFF) based hills width scheme<i></i></span></span>=DIFF
    <span class="plumedtooltip">HEIGHT<span class="right">the height of the Gaussian hills, one for all biases<i></i></span></span>=0.5
    <span class="plumedtooltip">PACE<span class="right">the frequency for hill addition, one for all biases<i></i></span></span>=200
    <span class="plumedtooltip">BIASFACTOR<span class="right">use well tempered metadynamics with this bias factor, one for all biases<i></i></span></span>=35
    <span class="plumedtooltip">GRID_MIN<span class="right">the lower bounds for the grid<i></i></span></span>=-pi,-pi
    <span class="plumedtooltip">GRID_MAX<span class="right">the upper bounds for the grid<i></i></span></span>=pi,pi
    <span class="plumedtooltip">GRID_WSTRIDE<span class="right">frequency for dumping the grid<i></i></span></span>=5000
    <span class="plumedtooltip">WALKERS_MPI<span class="right"> Switch on MPI version of multiple walkers - not compatible with WALKERS_* options other than WALKERS_DIR<i></i></span></span>
    <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is only needed if you are doing well-tempered metadynamics<i></i></span></span>=298
... PBMETAD
<br/><span style="display:none;" id="data/plumed_TDP-43.dat_solpb">The PBMETAD action with label <b>pb</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">pb.bias</td><td>the instantaneous value of the bias potential</td></tr></table></span><span class="plumedtooltip" style="color:green">METAINFERENCE<span class="right">Calculates the Metainference energy for a set of experimental data. <a href="https://www.plumed.org/doc-master/user-doc/html/METAINFERENCE" style="color:green">More details</a><i></i></span></span> ...
    <span class="plumedtooltip">ARG<span class="right">the labels of the scalars on which the bias will act<i></i></span></span>=(distance_rest_domains.*),<b name="data/plumed_TDP-43.dat_solpb">pb.bias</b> <span class="plumedtooltip">REWEIGHT<span class="right"> simple REWEIGHT using the latest ARG as energy<i></i></span></span>
    <span class="plumedtooltip">PARARG<span class="right">reference values for the experimental data, these can be provided as arguments without derivatives<i></i></span></span>=(af_dist_rest.*)
    <span class="plumedtooltip">SIGMA_MEAN0<span class="right">starting value for the uncertainty in the mean estimate<i></i></span></span>=1
    <span class="plumedtooltip">NOISETYPE<span class="right"> functional form of the noise (GAUSS,MGAUSS,OUTLIERS,MOUTLIERS,GENERIC)<i></i></span></span>=MGAUSS  <span class="plumedtooltip">OPTSIGMAMEAN<span class="right"> Set to NONE/SEM to manually set sigma mean, or to estimate it on the fly<i></i></span></span>=SEM <span class="plumedtooltip">AVERAGING<span class="right">Stride for calculation of averaged weights and sigma_mean<i></i></span></span>=200
    <span class="plumedtooltip">SIGMA0<span class="right"> initial value of the uncertainty parameter<i></i></span></span>=10.0 <span class="plumedtooltip">SIGMA_MIN<span class="right"> minimum value of the uncertainty parameter<i></i></span></span>=0.0001 <span class="plumedtooltip">SIGMA_MAX<span class="right"> maximum value of the uncertainty parameter<i></i></span></span>=10.0 <span class="plumedtooltip">DSIGMA<span class="right">maximum MC move of the uncertainty parameter<i></i></span></span>=0.1
    <span class="plumedtooltip">MC_STEPS<span class="right">number of MC steps<i></i></span></span>=10
    <span class="plumedtooltip">MC_CHUNKSIZE<span class="right">MC chunksize<i></i></span></span>=20
    <span class="plumedtooltip">WRITE_STRIDE<span class="right"> write the status to a file every N steps, this can be used for restart/continuation<i></i></span></span>=10000
    <span class="plumedtooltip">TEMP<span class="right">the system temperature - this is only needed if code doesn't pass the temperature to plumed<i></i></span></span>=298
    <span class="plumedtooltip">LABEL<span class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></span></span>=<b name="data/plumed_TDP-43.dat_solaf_mi_rest_domains" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solaf_mi_rest_domains","data/plumed_TDP-43.dat_solaf_mi_rest_domains","brown")'>af_mi_rest_domains</b>
... METAINFERENCE
<br/><span style="display:none;" id="data/plumed_TDP-43.dat_solaf_mi_rest_domains">The METAINFERENCE action with label <b>af_mi_rest_domains</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">af_mi_rest_domains.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">af_mi_rest_domains.sigma</td><td>uncertainty parameter</td></tr><tr><td width="5%">af_mi_rest_domains.sigmaMean</td><td>uncertainty in the mean estimate</td></tr><tr><td width="5%">af_mi_rest_domains.neff</td><td>effective number of replicas</td></tr><tr><td width="5%">af_mi_rest_domains.acceptSigma</td><td>MC acceptance for sigma values</td></tr><tr><td width="5%">af_mi_rest_domains.weight</td><td>weights of the weighted average</td></tr><tr><td width="5%">af_mi_rest_domains.biasDer</td><td>derivatives with respect to the bias</td></tr></table></span><span class="plumedtooltip" style="color:green">FLUSH<span class="right">This command instructs plumed to flush all the open files with a user specified frequency. <a href="https://www.plumed.org/doc-master/user-doc/html/FLUSH" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">STRIDE<span class="right">the frequency with which all the open files should be flushed<i></i></span></span>=200
<span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=ENERGY <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/plumed_TDP-43.dat_solpb">pb.bias</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=200
<span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/plumed_TDP-43.dat_solaf_mi_rest_domains">af_mi_rest_domains.*</b>   <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=200 <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=BAYES_rest_domains
<span class="plumedtooltip" style="color:green">ENDPLUMED<span class="right">Terminate plumed input. <a href="https://www.plumed.org/doc-master/user-doc/html/ENDPLUMED" style="color:green">More details</a><i></i></span></span><span style="color:blue" class="comment">
</span></pre></div>

 {% endraw %} 

Make the PLUMED analysis file ```python plumed_analysis.dat```

```python
#Make the plumed_analysis.dat file
shutil.copy2(dir+"/../scripts_prep/make_plumed_analysis.py", dir)
path_gen_analysis = dir+'/make_plumed_analysis.py sequence.dat'
os.system(f'python {path_gen_analysis}')

```
Similarly the plumed_analysis file is used to calculate the weights using the Torrie valeau weights as done [here](https://link.springer.com/protocol/10.1007/978-1-4939-9608-7_13). For TDP-43 WtoA, the plumed_analysis.dat can be found [here](https://github.com/vendruscolo-lab/AlphaFold-IDP/blob/main/scripts_prep/plumed_analysis_TDP-43.dat)

__Note:__ This tutorial assumes that you know [Parallel Bias Metadynamics](https://www.plumed.org/doc-v2.9/user-doc/html/_p_b_m_e_t_a_d.html) and Metainference [theory](https://link.springer.com/content/pdf/10.1007/978-1-4939-9608-7_13.pdf) and [practice](https://www.plumed.org/doc-v2.9/user-doc/html/_m_e_t_a_i_n_f_e_r_e_n_c_e.html).

### In case you are running the TDP-43 WtoA example:

You can directly use the PBMetaD and Metainference parameters just as copied below by executing the next shell. Otherwise you need to define your system specific parameters.


```python
shutil.copy2(dir+"/../scripts_prep/plumed_TDP-43.dat", dir+'/plumed.dat')
shutil.copy2(dir+"/../scripts_prep/plumed_analysis_TDP-43.dat", dir+'/plumed_analysis.dat')
```

## Short energy minimization using OPENMM and CALVADOS2
```python
shutil.copy2(dir+"/../scripts_prep/simulate_em.py", dir)
simulate_em = dir+'/simulate_em.py '+str(pH)+' '+str(temp)
os.system(f'python {simulate_em}')
```

## Run AF-MI

```python
shutil.copy2(dir+"/../scripts_prep/simulate.py", dir)
!mpirun -np {NR} python simulate.py {pH} {temp}
```
##### [Back to AlphaFold-Metainference home](NAVIGATION.md)
