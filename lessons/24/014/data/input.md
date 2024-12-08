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

* Open [this](https://github.com/zshengyu14/ColabFold_distmats/blob/main/AlphaFold2.ipynb) link and choose colab. 
* Input the protein sequence as query sequence. 
* The rest of the options remain default and cells are run until the end. 
* Download the link with the AF data and upload it as AF_data in AlphaFold-IDP folder 

## Setup protein system in CALVADOS2 and OPENMM 

```python 
os.chdir(home) 
!git clone https://github.com/vendruscolo-lab/AlphaFold-IDP 
os.chdir(home+'/AlphaFold-IDP/prep_run') 
``` 
In the following step we need to define ```python fasta_sequence, pH, temp, ionic, PAE_cut, NR, ordered_domains, disordered_domains, pdb_af,json_af,npy_af, mean_af```. These variables respectively stand for the protein sequence to be simulated in AF-MI, the simulation pH, the simulation temperature (in K), the ionic strength of the solution, the highest AF predicted alighment error the considered inter-residue distances will have (residue distances with higher PAE are not considered in restraints), the number of replicas, the regions of the ordered domains (regions of more than 3 residues with PLDDT>0.75) where [RMSD](https://www.plumed.org/doc-master/user-doc/html/_r_m_s_d.html) walls wil be used, the disordered regions (usually regions of more than 3 residues with PLDDT<0.75), AF predicted pdb file, AF predicted json containing the PAE per residue pair file, per residue pair probability distribution AF prediction file, mean AF inter-residue distance map prediction file 

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
with open('ordered_domains.csv', 'w') as f: # You will need 'wb' mode in Python 2.x 
w = csv.DictWriter(f, ordered_domains.keys()) 
w.writeheader() 
w.writerow(ordered_domains) 
with open('disordered_domains.csv', 'w') as f: # You will need 'wb' mode in Python 2.x 
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
<div style="width: 100%; float:left">
<div style="width: 90%; float:left" id="value_details_data/plumed_TDP-43.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div style="width: 10%; float:left"><table><tr><td style="padding:1px"><a href="plumed_TDP-43.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested onv2.9" /></a></td></tr><tr><td style="padding:1px"><a href="plumed_TDP-43.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-failed-red.svg" alt="tested onmaster" /></a></td></tr><tr><td style="padding:0px"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/plumed_TDP-43.dat")' onmousedown='toggleDisplay("data/plumed_TDP-43.dat")'/></td></tr>
</table></div></div>
<div id="data/plumed_TDP-43.dat_short">
<pre style="width=97%;">
<div class="tooltip" style="color:green">MOLINFO<div class="right">This command is used to provide information on the molecules that are present in your system. <a href="https://www.plumed.org/doc-master/user-doc/html/_m_o_l_i_n_f_o.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">MOLTYPE<div class="right"> what kind of molecule is contained in the pdb file - usually not needed since protein/RNA/DNA are compatible<i></i></div></div>=protein <div class="tooltip">STRUCTURE<div class="right">a file in pdb format containing a reference structure<i></i></div></div>=input_af.pdb
<span style="display:none;" id="data/plumed_TDP-43.dat">The MOLINFO action with label <b></b> calculates something</span><div class="tooltip" style="color:green">WHOLEMOLECULES<div class="right">This action is used to rebuild molecules that can become split by the periodic boundary conditions. <a href="https://www.plumed.org/doc-master/user-doc/html/_w_h_o_l_e_m_o_l_e_c_u_l_e_s.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ENTITY0<div class="right">the atoms that make up a molecule that you wish to align<i></i></div></div>=1-414
    
<b name="data/plumed_TDP-43.datdistance_rest_domains" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.datdistance_rest_domains","data/plumed_TDP-43.datdistance_rest_domains","brown")'>distance_rest_domains</b>:  <div class="tooltip" style="color:green">CONTACTMAP<div class="right">Calculate the distances between a number of pairs of atoms and transform each distance by a switching function. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_n_t_a_c_t_m_a_p.html" style="color:green">More details</a><i></i></div></div> ...
<div class="tooltip">ATOMS1<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=1,4
<div class="tooltip">ATOMS2<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=2,5
<div class="tooltip">ATOMS3<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=2,20
<div class="tooltip">ATOMS4<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=28,79
<div class="tooltip">ATOMS5<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=31,79
<div class="tooltip">ATOMS6<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=35,79
<div class="tooltip">ATOMS7<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=37,79
<div class="tooltip">ATOMS8<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=38,79
<div class="tooltip">ATOMS9<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=39,79
<div class="tooltip">ATOMS10<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=40,79
<div class="tooltip">ATOMS11<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=41,79
<div class="tooltip">ATOMS12<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=42,79
<div class="tooltip">ATOMS13<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=74,79
<div class="tooltip">ATOMS14<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=75,79
<div class="tooltip">ATOMS15<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=76,79
<div class="tooltip">ATOMS16<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,105
<div class="tooltip">ATOMS17<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,106
<div class="tooltip">ATOMS18<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,150
<div class="tooltip">ATOMS19<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,151
<div class="tooltip">ATOMS20<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,152
<div class="tooltip">ATOMS21<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,155
<div class="tooltip">ATOMS22<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,158
<div class="tooltip">ATOMS23<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,159
<div class="tooltip">ATOMS24<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,161
<div class="tooltip">ATOMS25<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,106
<div class="tooltip">ATOMS26<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,107
<div class="tooltip">ATOMS27<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,108
<div class="tooltip">ATOMS28<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,120
<div class="tooltip">ATOMS29<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,121
<div class="tooltip">ATOMS30<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,124
<div class="tooltip">ATOMS31<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,130
<div class="tooltip">ATOMS32<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,131
<div class="tooltip">ATOMS33<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,132
<div class="tooltip">ATOMS34<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,133
<div class="tooltip">ATOMS35<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,134
<div class="tooltip">ATOMS36<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,135
<div class="tooltip">ATOMS37<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,147
<div class="tooltip">ATOMS38<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,148
<div class="tooltip">ATOMS39<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,149
<div class="tooltip">ATOMS40<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,150
<div class="tooltip">ATOMS41<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,151
<div class="tooltip">ATOMS42<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,152
<div class="tooltip">ATOMS43<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,153
<div class="tooltip">ATOMS44<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,154
<div class="tooltip">ATOMS45<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,155
<div class="tooltip">ATOMS46<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,156
<div class="tooltip">ATOMS47<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,157
<div class="tooltip">ATOMS48<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,158
<div class="tooltip">ATOMS49<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,159
<div class="tooltip">ATOMS50<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,160
<div class="tooltip">ATOMS51<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,161
<div class="tooltip">ATOMS52<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,162
<div class="tooltip">ATOMS53<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,175
<div class="tooltip">ATOMS54<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,176
<div class="tooltip">ATOMS55<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,177
<div class="tooltip">ATOMS56<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,178
<div class="tooltip">ATOMS57<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=104,178
<div class="tooltip">ATOMS58<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=105,178
<div class="tooltip">ATOMS59<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=105,179
<div class="tooltip">ATOMS60<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=106,178
<div class="tooltip">ATOMS61<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=106,179
<div class="tooltip">ATOMS62<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=107,178
<div class="tooltip">ATOMS63<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=107,179
<div class="tooltip">ATOMS64<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=108,178
<div class="tooltip">ATOMS65<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=108,179
<div class="tooltip">ATOMS66<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=109,178
<div class="tooltip">ATOMS67<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=109,179
<div class="tooltip">ATOMS68<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=110,178
<div class="tooltip">ATOMS69<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=111,178
<div class="tooltip">ATOMS70<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=120,178
<div class="tooltip">ATOMS71<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=124,178
<div class="tooltip">ATOMS72<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=131,178
<div class="tooltip">ATOMS73<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=132,178
<div class="tooltip">ATOMS74<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=133,178
<div class="tooltip">ATOMS75<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=134,178
<div class="tooltip">ATOMS76<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=135,178
<div class="tooltip">ATOMS77<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=136,178
<div class="tooltip">ATOMS78<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=137,178
<div class="tooltip">ATOMS79<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=145,178
<div class="tooltip">ATOMS80<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=146,178
<div class="tooltip">ATOMS81<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=147,178
<div class="tooltip">ATOMS82<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=147,179
<div class="tooltip">ATOMS83<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=148,178
<div class="tooltip">ATOMS84<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=148,179
<div class="tooltip">ATOMS85<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=149,178
<div class="tooltip">ATOMS86<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=149,179
<div class="tooltip">ATOMS87<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=150,178
<div class="tooltip">ATOMS88<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=150,179
<div class="tooltip">ATOMS89<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=151,178
<div class="tooltip">ATOMS90<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=151,179
<div class="tooltip">ATOMS91<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=152,178
<div class="tooltip">ATOMS92<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=155,178
<div class="tooltip">ATOMS93<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=158,178
<div class="tooltip">ATOMS94<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=159,178
<div class="tooltip">ATOMS95<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=159,179
<div class="tooltip">ATOMS96<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=161,178
<div class="tooltip">ATOMS97<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=161,179
<div class="tooltip">ATOMS98<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=162,178
<div class="tooltip">ATOMS99<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=162,179
<div class="tooltip">ATOMS100<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=163,178
<div class="tooltip">ATOMS101<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=164,178
<div class="tooltip">ATOMS102<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=165,178
<div class="tooltip">ATOMS103<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=166,178
<div class="tooltip">ATOMS104<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=173,178
<div class="tooltip">ATOMS105<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=174,178
<div class="tooltip">ATOMS106<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=174,179
<div class="tooltip">ATOMS107<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=175,178
<div class="tooltip">ATOMS108<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=175,179
<div class="tooltip">ATOMS109<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=176,179
<div class="tooltip">ATOMS110<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=189,192
<div class="tooltip">ATOMS111<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=189,233
<div class="tooltip">ATOMS112<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=189,240
<div class="tooltip">ATOMS113<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,193
<div class="tooltip">ATOMS114<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,194
<div class="tooltip">ATOMS115<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,195
<div class="tooltip">ATOMS116<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,209
<div class="tooltip">ATOMS117<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,210
<div class="tooltip">ATOMS118<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,211
<div class="tooltip">ATOMS119<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,212
<div class="tooltip">ATOMS120<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,213
<div class="tooltip">ATOMS121<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,214
<div class="tooltip">ATOMS122<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,216
<div class="tooltip">ATOMS123<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,217
<div class="tooltip">ATOMS124<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,218
<div class="tooltip">ATOMS125<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,219
<div class="tooltip">ATOMS126<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,220
<div class="tooltip">ATOMS127<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,230
<div class="tooltip">ATOMS128<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,231
<div class="tooltip">ATOMS129<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,232
<div class="tooltip">ATOMS130<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,233
<div class="tooltip">ATOMS131<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,234
<div class="tooltip">ATOMS132<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,235
<div class="tooltip">ATOMS133<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,236
<div class="tooltip">ATOMS134<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,237
<div class="tooltip">ATOMS135<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,238
<div class="tooltip">ATOMS136<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,239
<div class="tooltip">ATOMS137<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,240
<div class="tooltip">ATOMS138<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,241
<div class="tooltip">ATOMS139<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,242
<div class="tooltip">ATOMS140<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,243
<div class="tooltip">ATOMS141<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,244
<div class="tooltip">ATOMS142<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,257
<div class="tooltip">ATOMS143<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,258
<div class="tooltip">ATOMS144<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=191,260
<div class="tooltip">ATOMS145<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=192,260
<div class="tooltip">ATOMS146<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=192,261
<div class="tooltip">ATOMS147<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=193,260
<div class="tooltip">ATOMS148<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=193,261
<div class="tooltip">ATOMS149<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=193,262
<div class="tooltip">ATOMS150<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=194,260
<div class="tooltip">ATOMS151<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=194,261
<div class="tooltip">ATOMS152<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=194,262
<div class="tooltip">ATOMS153<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=195,260
<div class="tooltip">ATOMS154<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=195,261
<div class="tooltip">ATOMS155<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=196,260
<div class="tooltip">ATOMS156<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=197,260
<div class="tooltip">ATOMS157<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=211,260
<div class="tooltip">ATOMS158<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=219,260
<div class="tooltip">ATOMS159<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=221,260
<div class="tooltip">ATOMS160<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=222,260
<div class="tooltip">ATOMS161<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=223,260
<div class="tooltip">ATOMS162<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=229,260
<div class="tooltip">ATOMS163<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=229,261
<div class="tooltip">ATOMS164<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=230,260
<div class="tooltip">ATOMS165<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=230,261
<div class="tooltip">ATOMS166<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=231,260
<div class="tooltip">ATOMS167<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=231,261
<div class="tooltip">ATOMS168<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=232,260
<div class="tooltip">ATOMS169<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=232,261
<div class="tooltip">ATOMS170<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=233,260
<div class="tooltip">ATOMS171<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=234,260
<div class="tooltip">ATOMS172<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=234,261
<div class="tooltip">ATOMS173<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=236,260
<div class="tooltip">ATOMS174<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=237,260
<div class="tooltip">ATOMS175<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=238,260
<div class="tooltip">ATOMS176<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=239,260
<div class="tooltip">ATOMS177<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=240,260
<div class="tooltip">ATOMS178<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=241,260
<div class="tooltip">ATOMS179<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=241,261
<div class="tooltip">ATOMS180<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=242,260
<div class="tooltip">ATOMS181<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=243,260
<div class="tooltip">ATOMS182<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=243,261
<div class="tooltip">ATOMS183<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=244,260
<div class="tooltip">ATOMS184<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=245,260
<div class="tooltip">ATOMS185<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=246,260
<div class="tooltip">ATOMS186<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=247,260
<div class="tooltip">ATOMS187<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=248,260
<div class="tooltip">ATOMS188<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=255,260
<div class="tooltip">ATOMS189<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=256,260
<div class="tooltip">ATOMS190<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=256,261
<div class="tooltip">ATOMS191<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=257,260
<div class="tooltip">ATOMS192<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=257,261
<div class="tooltip">ATOMS193<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=258,261
<div class="tooltip">ATOMS194<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=258,262
<div class="tooltip">ATOMS195<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=259,262
<div class="tooltip">ATOMS196<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=298,301
<div class="tooltip">ATOMS197<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=300,303
<div class="tooltip">ATOMS198<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=304,307
<div class="tooltip">ATOMS199<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=318,321
<div class="tooltip">ATOMS200<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=321,324
<div class="tooltip">ATOMS201<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=321,325
<div class="tooltip">ATOMS202<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=321,326
<div class="tooltip">ATOMS203<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=322,325
<div class="tooltip">ATOMS204<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=322,326
<div class="tooltip">ATOMS205<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=323,326
<div class="tooltip">ATOMS206<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=323,327
<div class="tooltip">ATOMS207<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=324,327
<div class="tooltip">ATOMS208<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=325,328
<div class="tooltip">ATOMS209<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=326,329
<div class="tooltip">ATOMS210<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=348,351
<div class="tooltip">ATOMS211<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=350,353
<div class="tooltip">ATOMS212<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=351,354
<div class="tooltip">ATOMS213<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=352,355
<div class="tooltip">ATOMS214<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=357,360
<div class="tooltip">ATOMS215<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=360,363
<div class="tooltip">ATOMS216<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=371,374
<div class="tooltip">ATOMS217<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=376,379
<div class="tooltip">ATOMS218<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=386,389
<div class="tooltip">ATOMS219<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=392,395
<div class="tooltip">ATOMS220<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=394,397
<div class="tooltip">ATOMS221<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=396,399
<div class="tooltip">ATOMS222<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=399,402
<div class="tooltip">ATOMS223<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=400,403
<div class="tooltip">ATOMS224<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=402,405
<div class="tooltip">ATOMS225<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=402,406
<div class="tooltip">ATOMS226<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=407,411
<div class="tooltip">ATOMS227<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=408,411
<div class="tooltip">SWITCH<div class="right">The switching functions to use for each of the contacts in your map<i></i></div></div>={CUSTOM FUNC=x R_0=1}
...
<br/><span style="display:none;" id="data/plumed_TDP-43.datdistance_rest_domains">The CONTACTMAP action with label <b>distance_rest_domains</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">distance_rest_domains.contact</td><td>By not using SUM or CMDIST each contact will be stored in a component</td></tr><tr><td width="5%">distance_rest_domains.value</td><td>the sum of all the switching function on all the distances</td></tr></table></span><b name="data/plumed_TDP-43.dataf_dist_rest" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dataf_dist_rest","data/plumed_TDP-43.dataf_dist_rest","brown")'>af_dist_rest</b>: <div class="tooltip" style="color:green">CONSTANT<div class="right">Create a constant value that can be passed to actions <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_n_s_t_a_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">VALUES<div class="right">the numbers that are in your constant value<i></i></div></div>=1.0032847926020623,1.0311901761218905,0.7455537494271994,1.7088723132386805,1.713635583035648,1.5095473634079102,1.1722138326615095,1.2549746362492442,0.9444370301440359,1.2123430594801905,1.5226123476400972,1.3369803665205837,1.4350552991032601,1.271596952714026,0.8981292195618154,1.084396699629724,1.2897209025919436,1.5121250515803697,1.0559752460569143,1.0836912801489234,0.707867799885571,0.9799594385549426,1.2259459158405663,1.5500808618962765,0.9052655544131994,1.3762398231774569,1.5152623694390062,1.68192987870425,1.6158358810469509,1.3273277390748264,1.1055688032880424,0.7953455133363603,1.0522321155294776,1.3843332368880512,1.5040866650640965,1.9200282409787175,1.9061048422008757,1.6269824001938105,1.2354281768202782,1.0676583984866739,0.6573523612692953,0.6149551127105952,0.7450687747448683,0.7618590366095304,0.5613296514376999,1.0004315715283156,0.8841317959129811,0.5908093221485615,0.9980626434087752,1.263882938399911,1.1281702172011137,1.1415027465671301,1.3193011650815607,1.4435925820842384,1.1070262966677549,1.31037020906806,0.8523610839620233,0.6740215603262186,1.1396584818139672,0.7467208079993726,1.1898928672075273,0.4552792670205237,0.8395836766809226,1.017876618169248,1.3974865483120085,1.0051763331517576,1.1795675404369834,1.4049736192449929,1.459107712842524,1.5650913815945389,1.59471937045455,1.5574198851361871,1.3527641544118525,1.4486837401986123,1.1706370314583183,1.4376086220145226,1.1653784492984414,1.7256552413105966,1.4055226838216186,1.427379228360951,0.9732663879171014,1.2228183863684539,0.9791120953857901,1.3816555082798005,0.7472525445744396,1.2260105818510056,1.0942220810800791,1.5762166528031232,1.1099413389340045,1.5934589028358461,1.434581000171602,1.630307266302407,1.2566113555803897,1.5485478518530726,1.81100521478802,1.3977122131735087,1.7663343697786331,1.162875016592443,1.430508084408939,1.6525550663471222,1.7831156572327018,1.785999870300293,1.6451806398108602,1.4654783833771945,1.2249537132680417,1.3939366523176433,1.0378110969439147,1.3681153113022448,0.9096965923905374,1.0000388860702516,1.2344506287947297,0.8380141992121936,0.8398237504065037,1.0381346080452205,1.4053251046687365,2.167353528179228,1.9828473469242454,1.528205112926662,1.8880876734852792,2.016520819067955,1.5591710267588497,1.5430319080129267,1.4479076098650694,1.236793963611126,1.3141041703522205,1.5537533987313508,1.5692297449335457,1.121472422592342,1.1581335106864572,0.91726502366364,0.9532682375982404,1.2505696462467313,1.1205617936328052,0.6651569686830044,1.0967526400461791,1.140981236472726,0.6660797173157335,0.8100334141403437,1.2571399945765735,1.1800085892900825,0.9563456442207099,1.2749242424964906,1.1340990519151093,0.9276029605418444,0.5047679111361504,0.9407211143523457,0.6309511506929995,1.074688763730228,1.2769522689282895,0.5026340553537011,0.7528656773269176,1.0695354964584112,0.9779949204996229,1.300148520246148,1.1204699540510774,1.5327852481976152,1.4124552657827738,1.2289950992912055,1.0769147641956807,1.4084996918216348,1.2656738823279738,1.0495817463845016,1.1779037110507489,1.095422700792551,1.3921284958720208,0.6597456347197295,1.0181769583374263,0.9364564327523113,1.3884215405210854,0.9055566122755409,1.1202643141150477,1.596531630679965,1.518569000810385,1.201885962113738,1.5418776268139482,1.3921274995431305,0.8939561096951366,1.1407407995313406,1.4240611214190722,1.4680646168068052,1.164111346192658,1.5423512058332562,0.9587342431768777,1.234714117459953,1.4588959828019143,1.6841880340129138,1.6086150078102948,1.4471713358536364,1.2795427026227117,1.444847053103149,1.002940315194428,1.3102364122867585,0.9022639036178589,1.2806951073929669,0.989768156595528,0.9441032137721775,0.9244450947269796,0.9194099459797145,0.9374097302556038,0.7403792202472688,0.8557088484987617,1.1484702169895173,0.7273479776456953,0.8502402873709798,0.6981262018904091,0.8579837949946523,0.7507739521563054,0.7508660649880767,0.7793322708457708,0.9225482998415828,0.9773600473999976,0.9583356784656645,0.9616499662399293,0.9474486894905567,1.0015693807974457,0.9874830450862646,0.9377102639526129,0.9753739142790437,0.9764441156759859,0.973571441695094,0.950638056918979,0.9416109262034296,0.9724794756621122,0.966675561480224,1.2231912130489944,1.235738294199109,0.9654571769759062 NODERIV
  
<span style="display:none;" id="data/plumed_TDP-43.dataf_dist_rest">The CONSTANT action with label <b>af_dist_rest</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">af_dist_rest.value</td><td>the constant value that was read from the plumed input</td></tr></table></span><b name="data/plumed_TDP-43.dataf_dist2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dataf_dist2","data/plumed_TDP-43.dataf_dist2","brown")'>af_dist2</b>: <div class="tooltip" style="color:green">CONSTANT<div class="right">Create a constant value that can be passed to actions <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_n_s_t_a_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">VALUES<div class="right">the numbers that are in your constant value<i></i></div></div>=0 NODERIV
<span style="display:none;" id="data/plumed_TDP-43.dataf_dist2">The CONSTANT action with label <b>af_dist2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">af_dist2.value</td><td>the constant value that was read from the plumed input</td></tr></table></span><b name="data/plumed_TDP-43.datRg" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.datRg","data/plumed_TDP-43.datRg","brown")'>Rg</b>: <div class="tooltip" style="color:green">GYRATION<div class="right">Calculate the radius of gyration, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/_g_y_r_a_t_i_o_n.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">TYPE<div class="right"> The type of calculation relative to the Gyration Tensor you want to perform<i></i></div></div>=RADIUS <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=1-414
<span style="display:none;" id="data/plumed_TDP-43.datRg">The GYRATION action with label <b>Rg</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">Rg.value</td><td>the radius that was computed from the weights</td></tr></table></span><b name="data/plumed_TDP-43.datRMSD1" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.datRMSD1","data/plumed_TDP-43.datRMSD1","brown")'>RMSD1</b>: <div class="tooltip" style="color:green">RMSD<div class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/_r_m_s_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">REFERENCE<div class="right">a file in pdb format containing the reference structure and the atoms involved in the CV<i></i></div></div>=struct1.pdb <div class="tooltip">TYPE<div class="right"> the manner in which RMSD alignment is performed<i></i></div></div>=OPTIMAL
<span style="display:none;" id="data/plumed_TDP-43.datRMSD1">The RMSD action with label <b>RMSD1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">RMSD1.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><b name="data/plumed_TDP-43.datRMSD2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.datRMSD2","data/plumed_TDP-43.datRMSD2","brown")'>RMSD2</b>: <div class="tooltip" style="color:green">RMSD<div class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/_r_m_s_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">REFERENCE<div class="right">a file in pdb format containing the reference structure and the atoms involved in the CV<i></i></div></div>=struct2.pdb <div class="tooltip">TYPE<div class="right"> the manner in which RMSD alignment is performed<i></i></div></div>=OPTIMAL
<span style="display:none;" id="data/plumed_TDP-43.datRMSD2">The RMSD action with label <b>RMSD2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">RMSD2.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><b name="data/plumed_TDP-43.datRMSD3" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.datRMSD3","data/plumed_TDP-43.datRMSD3","brown")'>RMSD3</b>: <div class="tooltip" style="color:green">RMSD<div class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/_r_m_s_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">REFERENCE<div class="right">a file in pdb format containing the reference structure and the atoms involved in the CV<i></i></div></div>=struct3.pdb <div class="tooltip">TYPE<div class="right"> the manner in which RMSD alignment is performed<i></i></div></div>=OPTIMAL
<span style="display:none;" id="data/plumed_TDP-43.datRMSD3">The RMSD action with label <b>RMSD3</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">RMSD3.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><b name="data/plumed_TDP-43.datuwall" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.datuwall","data/plumed_TDP-43.datuwall","brown")'>uwall</b>: <div class="tooltip" style="color:green">UPPER_WALLS<div class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/_u_p_p_e_r__w_a_l_l_s.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the arguments on which the bias is acting<i></i></div></div>=<b name="data/plumed_TDP-43.datRMSD1">RMSD1</b>,<b name="data/plumed_TDP-43.datRMSD2">RMSD2</b>,<b name="data/plumed_TDP-43.datRMSD3">RMSD3</b> <div class="tooltip">AT<div class="right">the positions of the wall<i></i></div></div>=0.02,0.02,0.02 <div class="tooltip">KAPPA<div class="right">the force constant for the wall<i></i></div></div>=100000,100000,100000 <div class="tooltip">EXP<div class="right"> the powers for the walls<i></i></div></div>=2,2,2 <div class="tooltip">EPS<div class="right"> the values for s_i in the expression for a wall<i></i></div></div>=1,1,1 <div class="tooltip">OFFSET<div class="right"> the offset for the start of the wall<i></i></div></div>=0,0,0
<span style="display:none;" id="data/plumed_TDP-43.datuwall">The UPPER_WALLS action with label <b>uwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">uwall.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">uwall.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span><div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=DISTANCE_MAP_REST <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/plumed_TDP-43.datdistance_rest_domains">distance_rest_domains</b> <div class="tooltip">STRIDE<div class="right"> the frequency with which the quantities of interest should be output<i></i></div></div>=200
<div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=COLVAR <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<span style="background-color:yellow">__FILL__</span> <div class="tooltip">STRIDE<div class="right"> the frequency with which the quantities of interest should be output<i></i></div></div>=200
<div class="tooltip" style="color:green">PBMETAD<div class="right">Used to performed Parallel Bias metadynamics. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_b_m_e_t_a_d.html" style="color:green">More details</a><i></i></div></div> ...
    <div class="tooltip">LABEL<div class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></div></div>=<b name="data/plumed_TDP-43.datpb" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.datpb","data/plumed_TDP-43.datpb","brown")'>pb</b>
    <div class="tooltip">ARG<div class="right">the labels of the scalars on which the bias will act<i></i></div></div>=<span style="background-color:yellow">__FILL__</span>
    <div class="tooltip">SIGMA<div class="right">the widths of the Gaussian hills<i></i></div></div>=<span style="background-color:yellow">__FILL__</span> 
    <div class="tooltip">SIGMA_MIN<div class="right">the lower bounds for the sigmas (in CV units) when using adaptive hills<i></i></div></div>=<span style="background-color:yellow">__FILL__</span> 
    <div class="tooltip">SIGMA_MAX<div class="right">the upper bounds for the sigmas (in CV units) when using adaptive hills<i></i></div></div>=<span style="background-color:yellow">__FILL__</span> 
    <div class="tooltip">ADAPTIVE<div class="right">use a geometric (=GEOM) or diffusion (=DIFF) based hills width scheme<i></i></div></div>=DIFF
    <div class="tooltip">HEIGHT<div class="right">the height of the Gaussian hills, one for all biases<i></i></div></div>=<span style="background-color:yellow">__FILL__</span> 
    <div class="tooltip">PACE<div class="right">the frequency for hill addition, one for all biases<i></i></div></div>=200
    <div class="tooltip">BIASFACTOR<div class="right">use well tempered metadynamics with this bias factor, one for all biases<i></i></div></div>=<span style="background-color:yellow">__FILL__</span> 
    <div class="tooltip">GRID_MIN<div class="right">the lower bounds for the grid<i></i></div></div>=<span style="background-color:yellow">__FILL__</span> 
    <div class="tooltip">GRID_MAX<div class="right">the upper bounds for the grid<i></i></div></div>=<span style="background-color:yellow">__FILL__</span> 
    <div class="tooltip">GRID_WSTRIDE<div class="right">frequency for dumping the grid<i></i></div></div>=<span style="background-color:yellow">__FILL__</span> 
    <div class="tooltip">WALKERS_MPI<div class="right"> Switch on MPI version of multiple walkers - not compatible with WALKERS_* options other than WALKERS_DIR<i></i></div></div>
    <div class="tooltip">TEMP<div class="right">the system temperature - this is only needed if you are doing well-tempered metadynamics<i></i></div></div>=<span style="background-color:yellow">__FILL__</span> 
... PBMETAD
<span style="display:none;" id="data/plumed_TDP-43.datpb">The PBMETAD action with label <b>pb</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">pb.bias</td><td>the instantaneous value of the bias potential</td></tr></table></span><div class="tooltip" style="color:green">METAINFERENCE<div class="right">Calculates the Metainference energy for a set of experimental data. <a href="https://www.plumed.org/doc-master/user-doc/html/_m_e_t_a_i_n_f_e_r_e_n_c_e.html" style="color:green">More details</a><i></i></div></div> ...
    <div class="tooltip">ARG<div class="right">the labels of the scalars on which the bias will act<i></i></div></div>=(distance_rest_domains.*),<b name="data/plumed_TDP-43.datpb">pb.bias</b> <div class="tooltip">REWEIGHT<div class="right"> simple REWEIGHT using the latest ARG as energy<i></i></div></div>
    <div class="tooltip">PARARG<div class="right">reference values for the experimental data, these can be provided as arguments without derivatives<i></i></div></div>=(af_dist_rest
    <div class="tooltip">SIGMA_MEAN0<div class="right">starting value for the uncertainty in the mean estimate<i></i></div></div>=1
    <div class="tooltip">NOISETYPE<div class="right"> functional form of the noise (GAUSS,MGAUSS,OUTLIERS,MOUTLIERS,GENERIC)<i></i></div></div>=MGAUSS  <div class="tooltip">OPTSIGMAMEAN<div class="right"> Set to NONE/SEM to manually set sigma mean, or to estimate it on the fly<i></i></div></div>=SEM <div class="tooltip">AVERAGING<div class="right">Stride for calculation of averaged weights and sigma_mean<i></i></div></div>=200
    <div class="tooltip">SIGMA0<div class="right"> initial value of the uncertainty parameter<i></i></div></div>=10.0 <div class="tooltip">SIGMA_MIN<div class="right"> minimum value of the uncertainty parameter<i></i></div></div>=0.0001 <div class="tooltip">SIGMA_MAX<div class="right"> maximum value of the uncertainty parameter<i></i></div></div>=10.0 <div class="tooltip">DSIGMA<div class="right">maximum MC move of the uncertainty parameter<i></i></div></div>=0.1
    <div class="tooltip">MC_STEPS<div class="right">number of MC steps<i></i></div></div>=10
    <div class="tooltip">MC_CHUNKSIZE<div class="right">MC chunksize<i></i></div></div>=23
    <div class="tooltip">WRITE_STRIDE<div class="right"> write the status to a file every N steps, this can be used for restart/continuation<i></i></div></div>=10000
    <div class="tooltip">TEMP<div class="right">the system temperature - this is only needed if code doesn't pass the temperature to plumed<i></i></div></div>=<span style="background-color:yellow">__FILL__</span> 
    <div class="tooltip">LABEL<div class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></div></div>=<b name="data/plumed_TDP-43.dataf_mi_rest_domains" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dataf_mi_rest_domains","data/plumed_TDP-43.dataf_mi_rest_domains","brown")'>af_mi_rest_domains</b>
... METAINFERENCE
<span style="display:none;" id="data/plumed_TDP-43.dataf_mi_rest_domains">The METAINFERENCE action with label <b>af_mi_rest_domains</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">af_mi_rest_domains.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">af_mi_rest_domains.sigma</td><td>uncertainty parameter</td></tr><tr><td width="5%">af_mi_rest_domains.sigmaMean</td><td>uncertainty in the mean estimate</td></tr><tr><td width="5%">af_mi_rest_domains.neff</td><td>effective number of replicas</td></tr><tr><td width="5%">af_mi_rest_domains.acceptSigma</td><td>MC acceptance for sigma values</td></tr><tr><td width="5%">af_mi_rest_domains.weight</td><td>weights of the weighted average</td></tr><tr><td width="5%">af_mi_rest_domains.biasDer</td><td>derivatives with respect to the bias</td></tr></table></span><div class="tooltip" style="color:green">FLUSH<div class="right">This command instructs plumed to flush all the open files with a user specified frequency. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_l_u_s_h.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">STRIDE<div class="right">the frequency with which all the open files should be flushed<i></i></div></div>=200
<div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=ENERGY <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/plumed_TDP-43.datpb">pb.bias</b> <div class="tooltip">STRIDE<div class="right"> the frequency with which the quantities of interest should be output<i></i></div></div>=200
<div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/plumed_TDP-43.dataf_mi_rest_domains">af_mi_rest_domains</b>   <div class="tooltip">STRIDE<div class="right"> the frequency with which the quantities of interest should be output<i></i></div></div>=200 <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=BAYES_rest_domains
<div class="tooltip" style="color:green">ENDPLUMED<div class="right">Terminate plumed input. <a href="https://www.plumed.org/doc-master/user-doc/html/_e_n_d_p_l_u_m_e_d.html" style="color:green">More details</a><i></i></div></div><span style="color:blue" class="comment">
</span></pre></div>
<div style="display:none;" id="data/plumed_TDP-43.dat_long"><pre style="width=97%;">
<div class="tooltip" style="color:green">MOLINFO<div class="right">This command is used to provide information on the molecules that are present in your system. <a href="https://www.plumed.org/doc-master/user-doc/html/_m_o_l_i_n_f_o.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">MOLTYPE<div class="right"> what kind of molecule is contained in the pdb file - usually not needed since protein/RNA/DNA are compatible<i></i></div></div>=protein <div class="tooltip">STRUCTURE<div class="right">a file in pdb format containing a reference structure<i></i></div></div>=input_af.pdb
<span style="display:none;" id="data/plumed_TDP-43.dat_sol">The MOLINFO action with label <b></b> calculates something</span><div class="tooltip" style="color:green">WHOLEMOLECULES<div class="right">This action is used to rebuild molecules that can become split by the periodic boundary conditions. <a href="https://www.plumed.org/doc-master/user-doc/html/_w_h_o_l_e_m_o_l_e_c_u_l_e_s.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ENTITY0<div class="right">the atoms that make up a molecule that you wish to align<i></i></div></div>=1-414
<br/><b name="data/plumed_TDP-43.dat_soldistance_rest_domains" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soldistance_rest_domains","data/plumed_TDP-43.dat_soldistance_rest_domains","brown")'>distance_rest_domains</b>:  <div class="tooltip" style="color:green">CONTACTMAP<div class="right">Calculate the distances between a number of pairs of atoms and transform each distance by a switching function. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_n_t_a_c_t_m_a_p.html" style="color:green">More details</a><i></i></div></div> ...
<div class="tooltip">ATOMS1<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=1,4
<div class="tooltip">ATOMS2<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=2,5
<div class="tooltip">ATOMS3<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=2,20
<div class="tooltip">ATOMS4<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=28,79
<div class="tooltip">ATOMS5<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=31,79
<div class="tooltip">ATOMS6<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=35,79
<div class="tooltip">ATOMS7<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=37,79
<div class="tooltip">ATOMS8<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=38,79
<div class="tooltip">ATOMS9<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=39,79
<div class="tooltip">ATOMS10<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=40,79
<div class="tooltip">ATOMS11<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=41,79
<div class="tooltip">ATOMS12<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=42,79
<div class="tooltip">ATOMS13<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=74,79
<div class="tooltip">ATOMS14<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=75,79
<div class="tooltip">ATOMS15<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=76,79
<div class="tooltip">ATOMS16<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,105
<div class="tooltip">ATOMS17<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,106
<div class="tooltip">ATOMS18<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,150
<div class="tooltip">ATOMS19<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,151
<div class="tooltip">ATOMS20<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,152
<div class="tooltip">ATOMS21<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,155
<div class="tooltip">ATOMS22<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,158
<div class="tooltip">ATOMS23<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,159
<div class="tooltip">ATOMS24<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=102,161
<div class="tooltip">ATOMS25<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,106
<div class="tooltip">ATOMS26<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,107
<div class="tooltip">ATOMS27<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,108
<div class="tooltip">ATOMS28<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,120
<div class="tooltip">ATOMS29<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,121
<div class="tooltip">ATOMS30<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,124
<div class="tooltip">ATOMS31<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,130
<div class="tooltip">ATOMS32<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,131
<div class="tooltip">ATOMS33<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,132
<div class="tooltip">ATOMS34<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,133
<div class="tooltip">ATOMS35<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,134
<div class="tooltip">ATOMS36<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,135
<div class="tooltip">ATOMS37<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,147
<div class="tooltip">ATOMS38<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,148
<div class="tooltip">ATOMS39<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,149
<div class="tooltip">ATOMS40<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,150
<div class="tooltip">ATOMS41<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,151
<div class="tooltip">ATOMS42<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,152
<div class="tooltip">ATOMS43<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,153
<div class="tooltip">ATOMS44<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,154
<div class="tooltip">ATOMS45<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,155
<div class="tooltip">ATOMS46<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,156
<div class="tooltip">ATOMS47<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,157
<div class="tooltip">ATOMS48<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,158
<div class="tooltip">ATOMS49<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,159
<div class="tooltip">ATOMS50<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,160
<div class="tooltip">ATOMS51<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,161
<div class="tooltip">ATOMS52<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,162
<div class="tooltip">ATOMS53<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,175
<div class="tooltip">ATOMS54<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,176
<div class="tooltip">ATOMS55<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,177
<div class="tooltip">ATOMS56<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=103,178
<div class="tooltip">ATOMS57<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=104,178
<div class="tooltip">ATOMS58<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=105,178
<div class="tooltip">ATOMS59<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=105,179
<div class="tooltip">ATOMS60<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=106,178
<div class="tooltip">ATOMS61<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=106,179
<div class="tooltip">ATOMS62<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=107,178
<div class="tooltip">ATOMS63<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=107,179
<div class="tooltip">ATOMS64<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=108,178
<div class="tooltip">ATOMS65<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=108,179
<div class="tooltip">ATOMS66<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=109,178
<div class="tooltip">ATOMS67<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=109,179
<div class="tooltip">ATOMS68<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=110,178
<div class="tooltip">ATOMS69<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=111,178
<div class="tooltip">ATOMS70<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=120,178
<div class="tooltip">ATOMS71<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=124,178
<div class="tooltip">ATOMS72<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=131,178
<div class="tooltip">ATOMS73<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=132,178
<div class="tooltip">ATOMS74<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=133,178
<div class="tooltip">ATOMS75<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=134,178
<div class="tooltip">ATOMS76<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=135,178
<div class="tooltip">ATOMS77<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=136,178
<div class="tooltip">ATOMS78<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=137,178
<div class="tooltip">ATOMS79<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=145,178
<div class="tooltip">ATOMS80<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=146,178
<div class="tooltip">ATOMS81<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=147,178
<div class="tooltip">ATOMS82<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=147,179
<div class="tooltip">ATOMS83<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=148,178
<div class="tooltip">ATOMS84<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=148,179
<div class="tooltip">ATOMS85<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=149,178
<div class="tooltip">ATOMS86<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=149,179
<div class="tooltip">ATOMS87<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=150,178
<div class="tooltip">ATOMS88<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=150,179
<div class="tooltip">ATOMS89<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=151,178
<div class="tooltip">ATOMS90<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=151,179
<div class="tooltip">ATOMS91<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=152,178
<div class="tooltip">ATOMS92<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=155,178
<div class="tooltip">ATOMS93<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=158,178
<div class="tooltip">ATOMS94<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=159,178
<div class="tooltip">ATOMS95<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=159,179
<div class="tooltip">ATOMS96<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=161,178
<div class="tooltip">ATOMS97<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=161,179
<div class="tooltip">ATOMS98<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=162,178
<div class="tooltip">ATOMS99<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=162,179
<div class="tooltip">ATOMS100<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=163,178
<div class="tooltip">ATOMS101<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=164,178
<div class="tooltip">ATOMS102<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=165,178
<div class="tooltip">ATOMS103<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=166,178
<div class="tooltip">ATOMS104<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=173,178
<div class="tooltip">ATOMS105<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=174,178
<div class="tooltip">ATOMS106<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=174,179
<div class="tooltip">ATOMS107<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=175,178
<div class="tooltip">ATOMS108<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=175,179
<div class="tooltip">ATOMS109<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=176,179
<div class="tooltip">ATOMS110<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=189,192
<div class="tooltip">ATOMS111<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=189,233
<div class="tooltip">ATOMS112<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=189,240
<div class="tooltip">ATOMS113<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,193
<div class="tooltip">ATOMS114<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,194
<div class="tooltip">ATOMS115<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,195
<div class="tooltip">ATOMS116<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,209
<div class="tooltip">ATOMS117<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,210
<div class="tooltip">ATOMS118<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,211
<div class="tooltip">ATOMS119<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,212
<div class="tooltip">ATOMS120<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,213
<div class="tooltip">ATOMS121<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,214
<div class="tooltip">ATOMS122<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,216
<div class="tooltip">ATOMS123<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,217
<div class="tooltip">ATOMS124<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,218
<div class="tooltip">ATOMS125<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,219
<div class="tooltip">ATOMS126<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,220
<div class="tooltip">ATOMS127<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,230
<div class="tooltip">ATOMS128<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,231
<div class="tooltip">ATOMS129<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,232
<div class="tooltip">ATOMS130<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,233
<div class="tooltip">ATOMS131<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,234
<div class="tooltip">ATOMS132<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,235
<div class="tooltip">ATOMS133<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,236
<div class="tooltip">ATOMS134<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,237
<div class="tooltip">ATOMS135<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,238
<div class="tooltip">ATOMS136<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,239
<div class="tooltip">ATOMS137<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,240
<div class="tooltip">ATOMS138<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,241
<div class="tooltip">ATOMS139<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,242
<div class="tooltip">ATOMS140<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,243
<div class="tooltip">ATOMS141<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,244
<div class="tooltip">ATOMS142<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,257
<div class="tooltip">ATOMS143<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=190,258
<div class="tooltip">ATOMS144<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=191,260
<div class="tooltip">ATOMS145<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=192,260
<div class="tooltip">ATOMS146<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=192,261
<div class="tooltip">ATOMS147<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=193,260
<div class="tooltip">ATOMS148<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=193,261
<div class="tooltip">ATOMS149<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=193,262
<div class="tooltip">ATOMS150<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=194,260
<div class="tooltip">ATOMS151<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=194,261
<div class="tooltip">ATOMS152<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=194,262
<div class="tooltip">ATOMS153<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=195,260
<div class="tooltip">ATOMS154<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=195,261
<div class="tooltip">ATOMS155<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=196,260
<div class="tooltip">ATOMS156<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=197,260
<div class="tooltip">ATOMS157<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=211,260
<div class="tooltip">ATOMS158<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=219,260
<div class="tooltip">ATOMS159<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=221,260
<div class="tooltip">ATOMS160<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=222,260
<div class="tooltip">ATOMS161<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=223,260
<div class="tooltip">ATOMS162<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=229,260
<div class="tooltip">ATOMS163<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=229,261
<div class="tooltip">ATOMS164<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=230,260
<div class="tooltip">ATOMS165<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=230,261
<div class="tooltip">ATOMS166<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=231,260
<div class="tooltip">ATOMS167<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=231,261
<div class="tooltip">ATOMS168<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=232,260
<div class="tooltip">ATOMS169<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=232,261
<div class="tooltip">ATOMS170<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=233,260
<div class="tooltip">ATOMS171<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=234,260
<div class="tooltip">ATOMS172<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=234,261
<div class="tooltip">ATOMS173<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=236,260
<div class="tooltip">ATOMS174<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=237,260
<div class="tooltip">ATOMS175<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=238,260
<div class="tooltip">ATOMS176<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=239,260
<div class="tooltip">ATOMS177<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=240,260
<div class="tooltip">ATOMS178<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=241,260
<div class="tooltip">ATOMS179<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=241,261
<div class="tooltip">ATOMS180<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=242,260
<div class="tooltip">ATOMS181<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=243,260
<div class="tooltip">ATOMS182<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=243,261
<div class="tooltip">ATOMS183<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=244,260
<div class="tooltip">ATOMS184<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=245,260
<div class="tooltip">ATOMS185<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=246,260
<div class="tooltip">ATOMS186<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=247,260
<div class="tooltip">ATOMS187<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=248,260
<div class="tooltip">ATOMS188<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=255,260
<div class="tooltip">ATOMS189<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=256,260
<div class="tooltip">ATOMS190<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=256,261
<div class="tooltip">ATOMS191<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=257,260
<div class="tooltip">ATOMS192<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=257,261
<div class="tooltip">ATOMS193<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=258,261
<div class="tooltip">ATOMS194<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=258,262
<div class="tooltip">ATOMS195<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=259,262
<div class="tooltip">ATOMS196<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=298,301
<div class="tooltip">ATOMS197<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=300,303
<div class="tooltip">ATOMS198<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=304,307
<div class="tooltip">ATOMS199<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=318,321
<div class="tooltip">ATOMS200<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=321,324
<div class="tooltip">ATOMS201<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=321,325
<div class="tooltip">ATOMS202<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=321,326
<div class="tooltip">ATOMS203<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=322,325
<div class="tooltip">ATOMS204<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=322,326
<div class="tooltip">ATOMS205<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=323,326
<div class="tooltip">ATOMS206<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=323,327
<div class="tooltip">ATOMS207<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=324,327
<div class="tooltip">ATOMS208<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=325,328
<div class="tooltip">ATOMS209<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=326,329
<div class="tooltip">ATOMS210<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=348,351
<div class="tooltip">ATOMS211<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=350,353
<div class="tooltip">ATOMS212<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=351,354
<div class="tooltip">ATOMS213<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=352,355
<div class="tooltip">ATOMS214<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=357,360
<div class="tooltip">ATOMS215<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=360,363
<div class="tooltip">ATOMS216<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=371,374
<div class="tooltip">ATOMS217<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=376,379
<div class="tooltip">ATOMS218<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=386,389
<div class="tooltip">ATOMS219<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=392,395
<div class="tooltip">ATOMS220<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=394,397
<div class="tooltip">ATOMS221<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=396,399
<div class="tooltip">ATOMS222<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=399,402
<div class="tooltip">ATOMS223<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=400,403
<div class="tooltip">ATOMS224<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=402,405
<div class="tooltip">ATOMS225<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=402,406
<div class="tooltip">ATOMS226<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=407,411
<div class="tooltip">ATOMS227<div class="right">the atoms involved in each of the contacts you wish to calculate<i></i></div></div>=408,411
<div class="tooltip">SWITCH<div class="right">The switching functions to use for each of the contacts in your map<i></i></div></div>={CUSTOM FUNC=x R_0=1}
...
<br/><span style="display:none;" id="data/plumed_TDP-43.dat_soldistance_rest_domains">The CONTACTMAP action with label <b>distance_rest_domains</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">distance_rest_domains.contact</td><td>By not using SUM or CMDIST each contact will be stored in a component</td></tr><tr><td width="5%">distance_rest_domains.value</td><td>the sum of all the switching function on all the distances</td></tr></table></span><b name="data/plumed_TDP-43.dat_solaf_dist_rest" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solaf_dist_rest","data/plumed_TDP-43.dat_solaf_dist_rest","brown")'>af_dist_rest</b>: <div class="tooltip" style="color:green">CONSTANT<div class="right">Create a constant value that can be passed to actions <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_n_s_t_a_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">VALUES<div class="right">the numbers that are in your constant value<i></i></div></div>=1.0032847926020623,1.0311901761218905,0.7455537494271994,1.7088723132386805,1.713635583035648,1.5095473634079102,1.1722138326615095,1.2549746362492442,0.9444370301440359,1.2123430594801905,1.5226123476400972,1.3369803665205837,1.4350552991032601,1.271596952714026,0.8981292195618154,1.084396699629724,1.2897209025919436,1.5121250515803697,1.0559752460569143,1.0836912801489234,0.707867799885571,0.9799594385549426,1.2259459158405663,1.5500808618962765,0.9052655544131994,1.3762398231774569,1.5152623694390062,1.68192987870425,1.6158358810469509,1.3273277390748264,1.1055688032880424,0.7953455133363603,1.0522321155294776,1.3843332368880512,1.5040866650640965,1.9200282409787175,1.9061048422008757,1.6269824001938105,1.2354281768202782,1.0676583984866739,0.6573523612692953,0.6149551127105952,0.7450687747448683,0.7618590366095304,0.5613296514376999,1.0004315715283156,0.8841317959129811,0.5908093221485615,0.9980626434087752,1.263882938399911,1.1281702172011137,1.1415027465671301,1.3193011650815607,1.4435925820842384,1.1070262966677549,1.31037020906806,0.8523610839620233,0.6740215603262186,1.1396584818139672,0.7467208079993726,1.1898928672075273,0.4552792670205237,0.8395836766809226,1.017876618169248,1.3974865483120085,1.0051763331517576,1.1795675404369834,1.4049736192449929,1.459107712842524,1.5650913815945389,1.59471937045455,1.5574198851361871,1.3527641544118525,1.4486837401986123,1.1706370314583183,1.4376086220145226,1.1653784492984414,1.7256552413105966,1.4055226838216186,1.427379228360951,0.9732663879171014,1.2228183863684539,0.9791120953857901,1.3816555082798005,0.7472525445744396,1.2260105818510056,1.0942220810800791,1.5762166528031232,1.1099413389340045,1.5934589028358461,1.434581000171602,1.630307266302407,1.2566113555803897,1.5485478518530726,1.81100521478802,1.3977122131735087,1.7663343697786331,1.162875016592443,1.430508084408939,1.6525550663471222,1.7831156572327018,1.785999870300293,1.6451806398108602,1.4654783833771945,1.2249537132680417,1.3939366523176433,1.0378110969439147,1.3681153113022448,0.9096965923905374,1.0000388860702516,1.2344506287947297,0.8380141992121936,0.8398237504065037,1.0381346080452205,1.4053251046687365,2.167353528179228,1.9828473469242454,1.528205112926662,1.8880876734852792,2.016520819067955,1.5591710267588497,1.5430319080129267,1.4479076098650694,1.236793963611126,1.3141041703522205,1.5537533987313508,1.5692297449335457,1.121472422592342,1.1581335106864572,0.91726502366364,0.9532682375982404,1.2505696462467313,1.1205617936328052,0.6651569686830044,1.0967526400461791,1.140981236472726,0.6660797173157335,0.8100334141403437,1.2571399945765735,1.1800085892900825,0.9563456442207099,1.2749242424964906,1.1340990519151093,0.9276029605418444,0.5047679111361504,0.9407211143523457,0.6309511506929995,1.074688763730228,1.2769522689282895,0.5026340553537011,0.7528656773269176,1.0695354964584112,0.9779949204996229,1.300148520246148,1.1204699540510774,1.5327852481976152,1.4124552657827738,1.2289950992912055,1.0769147641956807,1.4084996918216348,1.2656738823279738,1.0495817463845016,1.1779037110507489,1.095422700792551,1.3921284958720208,0.6597456347197295,1.0181769583374263,0.9364564327523113,1.3884215405210854,0.9055566122755409,1.1202643141150477,1.596531630679965,1.518569000810385,1.201885962113738,1.5418776268139482,1.3921274995431305,0.8939561096951366,1.1407407995313406,1.4240611214190722,1.4680646168068052,1.164111346192658,1.5423512058332562,0.9587342431768777,1.234714117459953,1.4588959828019143,1.6841880340129138,1.6086150078102948,1.4471713358536364,1.2795427026227117,1.444847053103149,1.002940315194428,1.3102364122867585,0.9022639036178589,1.2806951073929669,0.989768156595528,0.9441032137721775,0.9244450947269796,0.9194099459797145,0.9374097302556038,0.7403792202472688,0.8557088484987617,1.1484702169895173,0.7273479776456953,0.8502402873709798,0.6981262018904091,0.8579837949946523,0.7507739521563054,0.7508660649880767,0.7793322708457708,0.9225482998415828,0.9773600473999976,0.9583356784656645,0.9616499662399293,0.9474486894905567,1.0015693807974457,0.9874830450862646,0.9377102639526129,0.9753739142790437,0.9764441156759859,0.973571441695094,0.950638056918979,0.9416109262034296,0.9724794756621122,0.966675561480224,1.2231912130489944,1.235738294199109,0.9654571769759062 NODERIV
<br/><span style="display:none;" id="data/plumed_TDP-43.dat_solaf_dist_rest">The CONSTANT action with label <b>af_dist_rest</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">af_dist_rest.value</td><td>the constant value that was read from the plumed input</td></tr></table></span><b name="data/plumed_TDP-43.dat_solaf_dist2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solaf_dist2","data/plumed_TDP-43.dat_solaf_dist2","brown")'>af_dist2</b>: <div class="tooltip" style="color:green">CONSTANT<div class="right">Create a constant value that can be passed to actions <a href="https://www.plumed.org/doc-master/user-doc/html/_c_o_n_s_t_a_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">VALUES<div class="right">the numbers that are in your constant value<i></i></div></div>=0 NODERIV
<span style="display:none;" id="data/plumed_TDP-43.dat_solaf_dist2">The CONSTANT action with label <b>af_dist2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">af_dist2.value</td><td>the constant value that was read from the plumed input</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRg" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRg","data/plumed_TDP-43.dat_solRg","brown")'>Rg</b>: <div class="tooltip" style="color:green">GYRATION<div class="right">Calculate the radius of gyration, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/_g_y_r_a_t_i_o_n.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">TYPE<div class="right"> The type of calculation relative to the Gyration Tensor you want to perform<i></i></div></div>=RADIUS <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=1-414
<span style="display:none;" id="data/plumed_TDP-43.dat_solRg">The GYRATION action with label <b>Rg</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">Rg.value</td><td>the radius that was computed from the weights</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRMSD1" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRMSD1","data/plumed_TDP-43.dat_solRMSD1","brown")'>RMSD1</b>: <div class="tooltip" style="color:green">RMSD<div class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/_r_m_s_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">REFERENCE<div class="right">a file in pdb format containing the reference structure and the atoms involved in the CV<i></i></div></div>=struct1.pdb <div class="tooltip">TYPE<div class="right"> the manner in which RMSD alignment is performed<i></i></div></div>=OPTIMAL
<span style="display:none;" id="data/plumed_TDP-43.dat_solRMSD1">The RMSD action with label <b>RMSD1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">RMSD1.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRMSD2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRMSD2","data/plumed_TDP-43.dat_solRMSD2","brown")'>RMSD2</b>: <div class="tooltip" style="color:green">RMSD<div class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/_r_m_s_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">REFERENCE<div class="right">a file in pdb format containing the reference structure and the atoms involved in the CV<i></i></div></div>=struct2.pdb <div class="tooltip">TYPE<div class="right"> the manner in which RMSD alignment is performed<i></i></div></div>=OPTIMAL
<span style="display:none;" id="data/plumed_TDP-43.dat_solRMSD2">The RMSD action with label <b>RMSD2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">RMSD2.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRMSD3" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRMSD3","data/plumed_TDP-43.dat_solRMSD3","brown")'>RMSD3</b>: <div class="tooltip" style="color:green">RMSD<div class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/_r_m_s_d.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">REFERENCE<div class="right">a file in pdb format containing the reference structure and the atoms involved in the CV<i></i></div></div>=struct3.pdb <div class="tooltip">TYPE<div class="right"> the manner in which RMSD alignment is performed<i></i></div></div>=OPTIMAL
<br/><span style="display:none;" id="data/plumed_TDP-43.dat_solRMSD3">The RMSD action with label <b>RMSD3</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">RMSD3.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><b name="data/plumed_TDP-43.dat_soluwall" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soluwall","data/plumed_TDP-43.dat_soluwall","brown")'>uwall</b>: <div class="tooltip" style="color:green">UPPER_WALLS<div class="right">Defines a wall for the value of one or more collective variables, <a href="https://www.plumed.org/doc-master/user-doc/html/_u_p_p_e_r__w_a_l_l_s.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the arguments on which the bias is acting<i></i></div></div>=<b name="data/plumed_TDP-43.dat_solRMSD1">RMSD1</b>,<b name="data/plumed_TDP-43.dat_solRMSD2">RMSD2</b>,<b name="data/plumed_TDP-43.dat_solRMSD3">RMSD3</b> <div class="tooltip">AT<div class="right">the positions of the wall<i></i></div></div>=0.02,0.02,0.02 <div class="tooltip">KAPPA<div class="right">the force constant for the wall<i></i></div></div>=100000,100000,100000 <div class="tooltip">EXP<div class="right"> the powers for the walls<i></i></div></div>=2,2,2 <div class="tooltip">EPS<div class="right"> the values for s_i in the expression for a wall<i></i></div></div>=1,1,1 <div class="tooltip">OFFSET<div class="right"> the offset for the start of the wall<i></i></div></div>=0,0,0
<span style="display:none;" id="data/plumed_TDP-43.dat_soluwall">The UPPER_WALLS action with label <b>uwall</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">uwall.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">uwall.force2</td><td>the instantaneous value of the squared force due to this bias potential</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRg1" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRg1","data/plumed_TDP-43.dat_solRg1","brown")'>Rg1</b>: <div class="tooltip" style="color:green">GYRATION<div class="right">Calculate the radius of gyration, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/_g_y_r_a_t_i_o_n.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">TYPE<div class="right"> The type of calculation relative to the Gyration Tensor you want to perform<i></i></div></div>=RADIUS <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=1-2
<span style="display:none;" id="data/plumed_TDP-43.dat_solRg1">The GYRATION action with label <b>Rg1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">Rg1.value</td><td>the radius that was computed from the weights</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRg2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRg2","data/plumed_TDP-43.dat_solRg2","brown")'>Rg2</b>: <div class="tooltip" style="color:green">GYRATION<div class="right">Calculate the radius of gyration, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/_g_y_r_a_t_i_o_n.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">TYPE<div class="right"> The type of calculation relative to the Gyration Tensor you want to perform<i></i></div></div>=RADIUS <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=80-103
<span style="display:none;" id="data/plumed_TDP-43.dat_solRg2">The GYRATION action with label <b>Rg2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">Rg2.value</td><td>the radius that was computed from the weights</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRg3" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRg3","data/plumed_TDP-43.dat_solRg3","brown")'>Rg3</b>: <div class="tooltip" style="color:green">GYRATION<div class="right">Calculate the radius of gyration, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/_g_y_r_a_t_i_o_n.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">TYPE<div class="right"> The type of calculation relative to the Gyration Tensor you want to perform<i></i></div></div>=RADIUS <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=179-190
<span style="display:none;" id="data/plumed_TDP-43.dat_solRg3">The GYRATION action with label <b>Rg3</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">Rg3.value</td><td>the radius that was computed from the weights</td></tr></table></span><b name="data/plumed_TDP-43.dat_solRg4" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solRg4","data/plumed_TDP-43.dat_solRg4","brown")'>Rg4</b>: <div class="tooltip" style="color:green">GYRATION<div class="right">Calculate the radius of gyration, or other properties related to it. <a href="https://www.plumed.org/doc-master/user-doc/html/_g_y_r_a_t_i_o_n.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">TYPE<div class="right"> The type of calculation relative to the Gyration Tensor you want to perform<i></i></div></div>=RADIUS <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=261-414
<span style="display:none;" id="data/plumed_TDP-43.dat_solRg4">The GYRATION action with label <b>Rg4</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">Rg4.value</td><td>the radius that was computed from the weights</td></tr></table></span><div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=COLVAR <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/plumed_TDP-43.dat_solRg">Rg</b>,<b name="data/plumed_TDP-43.dat_solRMSD1">RMSD1</b>,<b name="data/plumed_TDP-43.dat_solRMSD2">RMSD2</b>,<b name="data/plumed_TDP-43.dat_solRMSD3">RMSD3</b>,<b name="data/plumed_TDP-43.dat_solRg1">Rg1</b>,<b name="data/plumed_TDP-43.dat_solRg2">Rg2</b>,<b name="data/plumed_TDP-43.dat_solRg3">Rg3</b>,<b name="data/plumed_TDP-43.dat_solRg4">Rg4</b> <div class="tooltip">STRIDE<div class="right"> the frequency with which the quantities of interest should be output<i></i></div></div>=200
<div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=DISTANCE_MAP_REST <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/plumed_TDP-43.dat_soldistance_rest_domains">distance_rest_domains</b> <div class="tooltip">STRIDE<div class="right"> the frequency with which the quantities of interest should be output<i></i></div></div>=200
<br/><b name="data/plumed_TDP-43.dat_solt1" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solt1","data/plumed_TDP-43.dat_solt1","brown")'>t1</b>: <div class="tooltip" style="color:green">CENTER<div class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_e_n_t_e_r.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=3-40
<span style="display:none;" id="data/plumed_TDP-43.dat_solt1">The CENTER action with label <b>t1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">t1.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_solt2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solt2","data/plumed_TDP-43.dat_solt2","brown")'>t2</b>: <div class="tooltip" style="color:green">CENTER<div class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_e_n_t_e_r.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=41-79
<span style="display:none;" id="data/plumed_TDP-43.dat_solt2">The CENTER action with label <b>t2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">t2.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_solt3" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solt3","data/plumed_TDP-43.dat_solt3","brown")'>t3</b>: <div class="tooltip" style="color:green">CENTER<div class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_e_n_t_e_r.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=104-140
<span style="display:none;" id="data/plumed_TDP-43.dat_solt3">The CENTER action with label <b>t3</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">t3.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_solt4" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solt4","data/plumed_TDP-43.dat_solt4","brown")'>t4</b>: <div class="tooltip" style="color:green">CENTER<div class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_e_n_t_e_r.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=141-178
<br/><span style="display:none;" id="data/plumed_TDP-43.dat_solt4">The CENTER action with label <b>t4</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">t4.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_soltorsion1" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soltorsion1","data/plumed_TDP-43.dat_soltorsion1","brown")'>torsion1</b>: <div class="tooltip" style="color:green">TORSION<div class="right">Calculate a torsional angle. <a href="https://www.plumed.org/doc-master/user-doc/html/_t_o_r_s_i_o_n.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the four atoms involved in the torsional angle<i></i></div></div>=<b name="data/plumed_TDP-43.dat_solt1">t1</b>,<b name="data/plumed_TDP-43.dat_solt2">t2</b>,<b name="data/plumed_TDP-43.dat_solt3">t3</b>,<b name="data/plumed_TDP-43.dat_solt4">t4</b>
<br/><span style="display:none;" id="data/plumed_TDP-43.dat_soltorsion1">The TORSION action with label <b>torsion1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">torsion1.value</td><td>the TORSION involving these atoms</td></tr></table></span><b name="data/plumed_TDP-43.dat_soltt1" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soltt1","data/plumed_TDP-43.dat_soltt1","brown")'>tt1</b>: <div class="tooltip" style="color:green">CENTER<div class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_e_n_t_e_r.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=104-140
<span style="display:none;" id="data/plumed_TDP-43.dat_soltt1">The CENTER action with label <b>tt1</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">tt1.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_soltt2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soltt2","data/plumed_TDP-43.dat_soltt2","brown")'>tt2</b>: <div class="tooltip" style="color:green">CENTER<div class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_e_n_t_e_r.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=141-178
<span style="display:none;" id="data/plumed_TDP-43.dat_soltt2">The CENTER action with label <b>tt2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">tt2.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_soltt3" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soltt3","data/plumed_TDP-43.dat_soltt3","brown")'>tt3</b>: <div class="tooltip" style="color:green">CENTER<div class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_e_n_t_e_r.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=191-225
<span style="display:none;" id="data/plumed_TDP-43.dat_soltt3">The CENTER action with label <b>tt3</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">tt3.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_soltt4" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soltt4","data/plumed_TDP-43.dat_soltt4","brown")'>tt4</b>: <div class="tooltip" style="color:green">CENTER<div class="right">Calculate the center for a group of atoms, with arbitrary weights. <a href="https://www.plumed.org/doc-master/user-doc/html/_c_e_n_t_e_r.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the group of atoms that you are calculating the Gyration Tensor for<i></i></div></div>=226-260
<br/><span style="display:none;" id="data/plumed_TDP-43.dat_soltt4">The CENTER action with label <b>tt4</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">tt4.value</td><td>the position of the center of mass</td></tr></table></span><b name="data/plumed_TDP-43.dat_soltorsion2" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_soltorsion2","data/plumed_TDP-43.dat_soltorsion2","brown")'>torsion2</b>: <div class="tooltip" style="color:green">TORSION<div class="right">Calculate a torsional angle. <a href="https://www.plumed.org/doc-master/user-doc/html/_t_o_r_s_i_o_n.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ATOMS<div class="right">the four atoms involved in the torsional angle<i></i></div></div>=<b name="data/plumed_TDP-43.dat_soltt1">tt1</b>,<b name="data/plumed_TDP-43.dat_soltt2">tt2</b>,<b name="data/plumed_TDP-43.dat_soltt3">tt3</b>,<b name="data/plumed_TDP-43.dat_soltt4">tt4</b>

<br/><span style="color:blue" class="comment"># PBMetaD</span>
<span style="display:none;" id="data/plumed_TDP-43.dat_soltorsion2">The TORSION action with label <b>torsion2</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">torsion2.value</td><td>the TORSION involving these atoms</td></tr></table></span><div class="tooltip" style="color:green">PBMETAD<div class="right">Used to performed Parallel Bias metadynamics. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_b_m_e_t_a_d.html" style="color:green">More details</a><i></i></div></div> ...
    <div class="tooltip">LABEL<div class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></div></div>=<b name="data/plumed_TDP-43.dat_solpb" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solpb","data/plumed_TDP-43.dat_solpb","brown")'>pb</b>
    <div class="tooltip">ARG<div class="right">the labels of the scalars on which the bias will act<i></i></div></div>=<b name="data/plumed_TDP-43.dat_soltorsion1">torsion1</b>,<b name="data/plumed_TDP-43.dat_soltorsion2">torsion2</b>
    <div class="tooltip">SIGMA<div class="right">the widths of the Gaussian hills<i></i></div></div>=1000
    <div class="tooltip">SIGMA_MIN<div class="right">the lower bounds for the sigmas (in CV units) when using adaptive hills<i></i></div></div>=0.05,0.05
    <div class="tooltip">SIGMA_MAX<div class="right">the upper bounds for the sigmas (in CV units) when using adaptive hills<i></i></div></div>=0.1,0.1
    <div class="tooltip">ADAPTIVE<div class="right">use a geometric (=GEOM) or diffusion (=DIFF) based hills width scheme<i></i></div></div>=DIFF
    <div class="tooltip">HEIGHT<div class="right">the height of the Gaussian hills, one for all biases<i></i></div></div>=0.5
    <div class="tooltip">PACE<div class="right">the frequency for hill addition, one for all biases<i></i></div></div>=200
    <div class="tooltip">BIASFACTOR<div class="right">use well tempered metadynamics with this bias factor, one for all biases<i></i></div></div>=35
    <div class="tooltip">GRID_MIN<div class="right">the lower bounds for the grid<i></i></div></div>=-pi,-pi
    <div class="tooltip">GRID_MAX<div class="right">the upper bounds for the grid<i></i></div></div>=pi,pi
    <div class="tooltip">GRID_WSTRIDE<div class="right">frequency for dumping the grid<i></i></div></div>=5000
    <div class="tooltip">WALKERS_MPI<div class="right"> Switch on MPI version of multiple walkers - not compatible with WALKERS_* options other than WALKERS_DIR<i></i></div></div>
    <div class="tooltip">TEMP<div class="right">the system temperature - this is only needed if you are doing well-tempered metadynamics<i></i></div></div>=298
... PBMETAD
<br/><span style="display:none;" id="data/plumed_TDP-43.dat_solpb">The PBMETAD action with label <b>pb</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">pb.bias</td><td>the instantaneous value of the bias potential</td></tr></table></span><div class="tooltip" style="color:green">METAINFERENCE<div class="right">Calculates the Metainference energy for a set of experimental data. <a href="https://www.plumed.org/doc-master/user-doc/html/_m_e_t_a_i_n_f_e_r_e_n_c_e.html" style="color:green">More details</a><i></i></div></div> ...
    <div class="tooltip">ARG<div class="right">the labels of the scalars on which the bias will act<i></i></div></div>=(distance_rest_domains.*),<b name="data/plumed_TDP-43.dat_solpb">pb.bias</b> <div class="tooltip">REWEIGHT<div class="right"> simple REWEIGHT using the latest ARG as energy<i></i></div></div>
    <div class="tooltip">PARARG<div class="right">reference values for the experimental data, these can be provided as arguments without derivatives<i></i></div></div>=(af_dist_rest
    <div class="tooltip">SIGMA_MEAN0<div class="right">starting value for the uncertainty in the mean estimate<i></i></div></div>=1
    <div class="tooltip">NOISETYPE<div class="right"> functional form of the noise (GAUSS,MGAUSS,OUTLIERS,MOUTLIERS,GENERIC)<i></i></div></div>=MGAUSS  <div class="tooltip">OPTSIGMAMEAN<div class="right"> Set to NONE/SEM to manually set sigma mean, or to estimate it on the fly<i></i></div></div>=SEM <div class="tooltip">AVERAGING<div class="right">Stride for calculation of averaged weights and sigma_mean<i></i></div></div>=200
    <div class="tooltip">SIGMA0<div class="right"> initial value of the uncertainty parameter<i></i></div></div>=10.0 <div class="tooltip">SIGMA_MIN<div class="right"> minimum value of the uncertainty parameter<i></i></div></div>=0.0001 <div class="tooltip">SIGMA_MAX<div class="right"> maximum value of the uncertainty parameter<i></i></div></div>=10.0 <div class="tooltip">DSIGMA<div class="right">maximum MC move of the uncertainty parameter<i></i></div></div>=0.1
    <div class="tooltip">MC_STEPS<div class="right">number of MC steps<i></i></div></div>=10
    <div class="tooltip">MC_CHUNKSIZE<div class="right">MC chunksize<i></i></div></div>=20
    <div class="tooltip">WRITE_STRIDE<div class="right"> write the status to a file every N steps, this can be used for restart/continuation<i></i></div></div>=10000
    <div class="tooltip">TEMP<div class="right">the system temperature - this is only needed if code doesn't pass the temperature to plumed<i></i></div></div>=298
    <div class="tooltip">LABEL<div class="right">a label for the action so that its output can be referenced in the input to other actions<i></i></div></div>=<b name="data/plumed_TDP-43.dat_solaf_mi_rest_domains" onclick='showPath("data/plumed_TDP-43.dat","data/plumed_TDP-43.dat_solaf_mi_rest_domains","data/plumed_TDP-43.dat_solaf_mi_rest_domains","brown")'>af_mi_rest_domains</b>
... METAINFERENCE
<br/><span style="display:none;" id="data/plumed_TDP-43.dat_solaf_mi_rest_domains">The METAINFERENCE action with label <b>af_mi_rest_domains</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">af_mi_rest_domains.bias</td><td>the instantaneous value of the bias potential</td></tr><tr><td width="5%">af_mi_rest_domains.sigma</td><td>uncertainty parameter</td></tr><tr><td width="5%">af_mi_rest_domains.sigmaMean</td><td>uncertainty in the mean estimate</td></tr><tr><td width="5%">af_mi_rest_domains.neff</td><td>effective number of replicas</td></tr><tr><td width="5%">af_mi_rest_domains.acceptSigma</td><td>MC acceptance for sigma values</td></tr><tr><td width="5%">af_mi_rest_domains.weight</td><td>weights of the weighted average</td></tr><tr><td width="5%">af_mi_rest_domains.biasDer</td><td>derivatives with respect to the bias</td></tr></table></span><div class="tooltip" style="color:green">FLUSH<div class="right">This command instructs plumed to flush all the open files with a user specified frequency. <a href="https://www.plumed.org/doc-master/user-doc/html/_f_l_u_s_h.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">STRIDE<div class="right">the frequency with which all the open files should be flushed<i></i></div></div>=200
<div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=ENERGY <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/plumed_TDP-43.dat_solpb">pb.bias</b> <div class="tooltip">STRIDE<div class="right"> the frequency with which the quantities of interest should be output<i></i></div></div>=200
<div class="tooltip" style="color:green">PRINT<div class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/_p_r_i_n_t.html" style="color:green">More details</a><i></i></div></div> <div class="tooltip">ARG<div class="right">the labels of the values that you would like to print to the file<i></i></div></div>=<b name="data/plumed_TDP-43.dat_solaf_mi_rest_domains">af_mi_rest_domains</b>   <div class="tooltip">STRIDE<div class="right"> the frequency with which the quantities of interest should be output<i></i></div></div>=200 <div class="tooltip">FILE<div class="right">the name of the file on which to output these quantities<i></i></div></div>=BAYES_rest_domains
<div class="tooltip" style="color:green">ENDPLUMED<div class="right">Terminate plumed input. <a href="https://www.plumed.org/doc-master/user-doc/html/_e_n_d_p_l_u_m_e_d.html" style="color:green">More details</a><i></i></div></div><span style="color:blue" class="comment">
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
