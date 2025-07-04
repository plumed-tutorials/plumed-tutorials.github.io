# PLUMED Masterclass 21.6: Dimensionality reduction

## Aims

The primary aim of this Masterclass is to show you how you might use PLUMED in your work.
We will see how to call PLUMED from a python notebook and discuss some strategies for selecting
collective variables.

## Objectives

Once this Masterclass is completed, users will be able to:

- Use the projection of a vector as a CV.
- Use path collective variables.

## Resources

The data needed to complete this Masterclass can be found on [GitHub](https://github.com/plumed/masterclass-21-6).
You can clone this repository locally on your machine using the following command:

````
git clone https://github.com/plumed/masterclass-21-6.git
````

I recommend that you run each exercise in a separate sub-directory (i.e. Exercise-1, Exercise-2, ...), which you can create inside the root directory `masterclass-21-6`. Organizing your data this way will help you to keep things clean.

_All the exercises have been tested with PLUMED version 2.7.0._

## Acknowledgements

Throughout this exercise, we use the [atomistic simulation environment](https://wiki.fysik.dtu.dk/ase/) 
and [chemiscope](https://chemiscope.org/).  Please look at the information at the links I have provided here 
for more information about these codes.

## Exercises

In many papers in this area, you will hear people talk about the distinction between collective variables and the reaction coordinate.  The distinction these authors are trying emphasize when they use this language 
is between a descriptor that takes different values for the various important basins in the energy landscape (the collective variable) and the actual pathway the reaction proceeds along (the reaction coordinate).
Furthermore, the authors of such papers will often argue that the reaction coordinate is simply some linear/non-linear combination of collective variables.
In this exercise, we will study alanine dipeptide with path collective variables to show you one way of thinking about this distinction between collective variables and reaction coordinates.  
By studying a system that is this simple, you will also hopefully come to understand how we can interpret the coordinates that we extract using the dimensionality reduction algorithms that were discussed in the previous exercise.

To remind you, the free energy surface as a function of the $\phi$ and $\psi$ angles for alanine dipeptide is shown below:

![The Free energy landscape of alanine dipeptide in Ramachandran angles in the CHARMM27 force field](figures/belfast-2-rama.png)

In other masterclasses, we have discussed how there are two critical states in the above energy landscape.  These states are labelled C7eq and C7ax above.  The two Ramachandran angles plotted on the x and y axes of the free energy surface
above are examples of what we have called collective variables.  Both of these angles can be used to distinguish between C7eq and C7ax configurations.
The reaction coordinate is the path that the system actually takes as it moves from the C7ax to the C7eq configuration.  Based on the shape of the free
energy surface, we might suppose that this reaction  coordinate looks something like the black line shown below: 

![Paths that connect the C7eq and C7ax configuration](figures/belfast-2-good-bad-path.png) 

The file called alanine-transformation.pdb that you can find in the data directory of the GitHub repository contains a series of configurations that lie close to the transition path that is illustrated in black in the figure above.  Below are plots that show how 
$\phi$ and $\psi$ change as the system moves along this path.  __Try to see if you can use what you have learned in previous masterclasses to reproduce the figure above before continuing.__  

![Changes in the Ramachandran angles as the protein transitions from the C7ax to C7eq state](figures/masterclass-21-6-rama-transition.png)

### RMSD distances

We know what structures correspond to the various stable states of our system.  We might, therefore, be tempted to ask ourselves if we can not just use the RMSD distance from a structure as the reaction coordinate.
This approach will work if there is a single important configuration in the energy landscape.  We could use the RMSD distance from this lowest energy structure as a CV to extract this configuration's free energy
relative to everything else.  How well does this work if we have two distinct states, though, as we have for alanine dipeptide?  To investigate this question, fill in the PLUMED input below that calculates the RMSD distances 
from the C7ax and C7eq configurations:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/work/plumed_ex5.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="plumed_ex5.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="plumed_ex5.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
<div class="headerBadge"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/work/plumed_ex5.dat")' onmousedown='toggleDisplay("data/work/plumed_ex5.dat")'/></div>
</div>
</div>
<div id="data/work/plumed_ex5.dat_short">
<pre class="plumedlisting">
<b name="data/work/plumed_ex5.datc7ax" onclick='showPath("data/work/plumed_ex5.dat","data/work/plumed_ex5.datc7ax","data/work/plumed_ex5.datc7ax","brown")'>c7ax</b>: <span class="plumedtooltip" style="color:green">RMSD<span class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/RMSD" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>=../data/c7ax.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which RMSD alignment is performed<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> 
<span style="display:none;" id="data/work/plumed_ex5.datc7ax">The RMSD action with label <b>c7ax</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c7ax.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><b name="data/work/plumed_ex5.datc7eq" onclick='showPath("data/work/plumed_ex5.dat","data/work/plumed_ex5.datc7eq","data/work/plumed_ex5.datc7eq","brown")'>c7eq</b>: <span class="plumedtooltip" style="color:green">RMSD<span class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/RMSD" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>=../data/c7eq.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which RMSD alignment is performed<i></i></span></span>=<span style="background-color:yellow">__FILL__</span>
<span style="display:none;" id="data/work/plumed_ex5.datc7eq">The RMSD action with label <b>c7eq</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c7eq.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/work/plumed_ex5.datc7ax">c7ax</b>,<b name="data/work/plumed_ex5.datc7eq">c7eq</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=100
</pre></div>
<div style="display:none;" id="data/work/plumed_ex5.dat_long"><pre class="plumedlisting">
<b name="data/work/plumed_ex5.dat_solc7ax" onclick='showPath("data/work/plumed_ex5.dat","data/work/plumed_ex5.dat_solc7ax","data/work/plumed_ex5.dat_solc7ax","brown")'>c7ax</b>: <span class="plumedtooltip" style="color:green">RMSD<span class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/RMSD" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">REFERENCE<span class="right">a file in pdb format containing the reference structure and the atoms involved in the CV<i></i></span></span>=../data/c7ax.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which RMSD alignment is performed<i></i></span></span>=OPTIMAL 
<span style="display:none;" id="data/work/plumed_ex5.dat_solc7ax">The RMSD action with label <b>c7ax</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c7ax.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><b name="data/work/plumed_ex5.dat_solc7eq" onclick='showPath("data/work/plumed_ex5.dat","data/work/plumed_ex5.dat_solc7eq","data/work/plumed_ex5.dat_solc7eq","brown")'>c7eq</b>: <span class="plumedtooltip" style="color:green">RMSD<span class="right">Calculate the RMSD with respect to a reference structure. <a href="https://www.plumed.org/doc-master/user-doc/html/RMSD" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">REFERENCE<span class="right">a file in pdb format containing the reference structure and the atoms involved in the CV<i></i></span></span>=../data/c7eq.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which RMSD alignment is performed<i></i></span></span>=OPTIMAL 
<span style="display:none;" id="data/work/plumed_ex5.dat_solc7eq">The RMSD action with label <b>c7eq</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">c7eq.value</td><td>the RMSD distance between the instaneous structure and the reference structure/s that were input</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/work/plumed_ex5.dat_solc7ax">c7ax</b>,<b name="data/work/plumed_ex5.dat_solc7eq">c7eq</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=100
</pre></div>

 {% endraw %} 

You can run an MD simulation to monitor these distances using the python script below.

```python
def generate_gromacs_input( directory, plumed_input, nsteps, temp ) :
    # Setup the initial configuration by picking a frame at random from the startpoints file
    allc = io.read('../data/startpoints.pdb',':')
    nframes = len(allc)
    io.write( directory + '/conf.pdb', allc[int(np.random.randint(0,nframes))] )
    # Copy the topology to the appropriate directory
    shutil.copyfile("../data/topol.top", directory + "/topol.top")
    # Setup the mdp file
    mdp = open("../data/md.mdp","r")
    contents = mdp.read()
    mdp.close()
    new_content = contents.replace("SEED", str(np.random.randint(0,1000000))).replace("NSTEPS",str(nsteps)).replace("TEMP",str(temp))
    mdpout = open(directory + "/md.mdp", "w")
    mdpout.write(new_content)
    mdpout.close()
    # And write the plumed input
    pout = open(directory + "/plumed.dat", "w")
    pout.write( plumed_input )
    pout.close()
    return

plm = '''
INSERT PLUMED INNPUT HERE
'''
# Create a directory to run the calculation in
!rm -rf ../Unbiased_MD && mkdir ../Unbiased_MD
# Generate gromacs input for MD simulation at 1000 K
generate_gromacs_input( '../Unbiased_MD', plm, 500000, 1000 )
# Now run gromacs
!cd ../Unbiased_MD/ && gmx_mpi grompp -f md.mdp -c conf.pdb -p topol.top -maxwarn 2 &> /dev/null
!cd ../Unbiased_MD/ && gmx_mpi mdrun --plumed plumed.dat &> /dev/null
# And read in the colvar files
unbiased_data = np.loadtxt('../Unbiased_MD/colvar')
```

I ran simulations at 300K and 1000K using the above script.  When the simulations completed, I was able to construct the figures below:

![The black points are the configurations visited in MD simulations at 300K (left) and 1000K (right).  The top panel shows these trajectories in the Ramachandran plane.  In the lower panel, I have projected the trajectories on the RMSD distances from the two reference states.](figures/masterclass-21-6-rmsd-distances.png)

The black points above are the RMSD values for the trajectories.  I have also shown the RMSD values for the frames in
alanine-transformation in red.  Notice that all the configurations explored in the MD are very distant from the C7ax and C7eq states.
__Try now to reproduce the above figure yourself.__

You can see that at 300K, the simulation we ran did not visit the C7eq state.  Furthermore, you can also clearly see this from the 
projections of the trajectories on the RMSD distances from these two configurations.  Notice in these figures, however, that the distances
from these two reference configurations were often considerably larger than the distance between these reference configurations and the configurations on the reference path in alanine-transformation.pdb.

### Using dot products to calculate CVs

Instead of calculating two distances, we might ask ourselves if the linear combination of $\phi$ and $\psi$ that is illustrated in the figure below:

![An illustration showing how PCAVARS coordinates work.  The vector connecting some reference state to any state the system is in can be in (purple and orange points) can be projected onto the vector connecting the two states of interest (black arrow) by using the dot product of the vectors shown here.](figures/marvel-2-pca-coordinates.png)

gives a better description for the transition.  We can define this CV as follows:

$$
s = \frac{(\phi_2 - \phi_1).(\phi_3 - \phi_1) + (\psi_2 - \psi_1).(\psi_3 - \psi_1)}{ \sqrt{(\phi_2 - \phi_1)^2 + (\psi_2 - \psi_1)^2} }
$$

In this expression $(\phi_1,\psi_1)$ are the Ramachandran angles in the $C_7eq$ configuration and 
$(\phi_2,\psi_2)$ are the Ramachandran angles in the $C_7ax$.  $(\phi_3,\psi_3)$ is the 
instantaneous configuration.  You should thus be able to see that we have arrived at the above expression
by using our knowledge of the dot product between two vectors.

__See if you can write an input to re-analyse the data in alanine-transformation.pdb and the MD simulations from the previous section using this CV.__  You should be able to get plots of the value of this CV as a function of step number that looks like the ones shown below:

![The black points are the configurations visited in MD simulations at 300K (left) and 1000K (right).  The top panel shows these trajectories in the Ramachandran plane.  In the lower panel, I have projected the trajectories on vector in the Ramachandran plane shown above.](figures/masterclass-21-6-pcavars-transition.png)

I implemented this CV using a combination of TORSION and COMBINE.  I also ignored the fact that the torsions are periodic variables when calculating the linear combination. You can't use the sort of linear algebra above with periodic variables, but it is OK for these illustrative purposes.  

Notice that the first frame in alanine-transformation.pdb has the molecule in the $C_7ax$ configuration.  The last frame has the molecule in the $C_7eq$ state.  

### PCA Collective Variables

In a previous section we saw how we can construct a new collective variables by taking a linear combination of two other 
variables.  This idea can be extended to higher dimensions, however.  As long as we can find the vector that connectes the $C_7eq$ and 
$C_7ax$ states we can project our current coordinates on that particular vector.  We can even define this vector in the space of the 
coordinates of the atoms.  In other words, if the 3$N$ coordinate of atomic positions is $\mathbf{x}^{(1)}$ for the $C_7eq$ 
configuration and $\mathbf{x}^{(2)}$ for the $C_7ax$ configuration and if the instantaneous configuration of the atoms is $\mathbf{x}^{(3)}$ we 
can use the following as a CV:

$$
s = \frac{\sum_{i=1}^{3N} (x^{(2)}_i - x^{(1)}_i ) (x^{(3)}_i - x^{(1)}_i )}{ \sqrt{\sum_{i=1}^{3N} (x^{(2)}_i - x^{(1)}_i )^2} } 
$$

as long as rotational and translational movement is removed before calculating the two displacement vectors above. 

We can also get some sense of how far the system has moved from this vector by computing:

$$
z = \sqrt{ \sum_{i=1}^{3N} (x^{(3)}_i - x^{(1)}_i)^2 - s^2 }
$$

which follows by applying Pythagoras theorem.

You can calculate this collective variable using PLUMED by using the input below:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/work/plumed_ex6.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="plumed_ex6.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="plumed_ex6.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
<div class="headerBadge"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/work/plumed_ex6.dat")' onmousedown='toggleDisplay("data/work/plumed_ex6.dat")'/></div>
</div>
</div>
<div id="data/work/plumed_ex6.dat_short">
<pre class="plumedlisting">
<b name="data/work/plumed_ex6.datp" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.datp","data/work/plumed_ex6.datp","brown")'>p</b>: <span class="plumedtooltip" style="color:green">PCAVARS<span class="right">Projection on principal component eigenvectors or other high dimensional linear subspace <a href="https://www.plumed.org/doc-master/user-doc/html/PCAVARS" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>=pca-reference.pdb <span style="background-color:yellow">__FILL__</span>=OPTIMAL
<span style="display:none;" id="data/work/plumed_ex6.datp">The PCAVARS action with label <b>p</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">p.eig</td><td>the projections on the eigenvalues</td></tr><tr><td width="5%">p.residual</td><td>the residual distance that is not projected on any of the eigenvalues</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/work/plumed_ex6.datp">p.*</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
</pre></div>
<div style="display:none;" id="data/work/plumed_ex6.dat_long"><pre class="plumedlisting">
<b name="data/work/plumed_ex6.dat_solp" onclick='showPath("data/work/plumed_ex6.dat","data/work/plumed_ex6.dat_solp","data/work/plumed_ex6.dat_solp","brown")'>p</b>: <span class="plumedtooltip" style="color:green">PCAVARS<span class="right">Projection on principal component eigenvectors or other high dimensional linear subspace <a href="https://www.plumed.org/doc-master/user-doc/html/PCAVARS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">REFERENCE<span class="right">a pdb file containing the set of reference configurations<i></i></span></span>=../data/pca-reference.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which distances are calculated<i></i></span></span>=OPTIMAL
<span style="display:none;" id="data/work/plumed_ex6.dat_solp">The PCAVARS action with label <b>p</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">p.eig</td><td>the projections on the eigenvalues</td></tr><tr><td width="5%">p.residual</td><td>the residual distance that is not projected on any of the eigenvalues</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/work/plumed_ex6.dat_solp">p.*</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
</pre></div>

 {% endraw %} 

__Use this input to re-analyse the data in `alanine-transformation.pdb` and your MD simulations before continuing.__  The figure below shows the results that I obtained by analyzing the 
data using the PCAVARS command above.

![The black points are the configurations visited in MD simulations at 300K (left) and 1000K (right).  The top panel shows these trajectories in the Ramachandran plane.  The projection on the vector connecting the C7ax and C7eq states (left) and the perpendicular distance from this vector (right) and shown in the bottom panels.](figures/masterclass-21-6-pcavars.png)

The figure above shows that this coordinate is good.  We move quite far from this initial vector when we move to the C7ax state, however.

### Two PCA Collective variables

Instead of using a single PCA variable and calculating the projection on the vector connecting these two points, we can instead use the projection of the instantaneous coordinates 
in the plane that contains three reference configurations.  You can calculate these collective variables using PLUMED by using the input below:

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
<b name="data/work/plumed_ex7.datp" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.datp","data/work/plumed_ex7.datp","brown")'>p</b>: <span class="plumedtooltip" style="color:green">PCAVARS<span class="right">Projection on principal component eigenvectors or other high dimensional linear subspace <a href="https://www.plumed.org/doc-master/user-doc/html/PCAVARS" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>=../work/pca2-reference.pdb <span style="background-color:yellow">__FILL__</span>=OPTIMAL
<span style="display:none;" id="data/work/plumed_ex7.datp">The PCAVARS action with label <b>p</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">p.eig</td><td>the projections on the eigenvalues</td></tr><tr><td width="5%">p.residual</td><td>the residual distance that is not projected on any of the eigenvalues</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/work/plumed_ex7.datp">p.*</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
</pre></div>
<div style="display:none;" id="data/work/plumed_ex7.dat_long"><pre class="plumedlisting">
<b name="data/work/plumed_ex7.dat_solp" onclick='showPath("data/work/plumed_ex7.dat","data/work/plumed_ex7.dat_solp","data/work/plumed_ex7.dat_solp","brown")'>p</b>: <span class="plumedtooltip" style="color:green">PCAVARS<span class="right">Projection on principal component eigenvectors or other high dimensional linear subspace <a href="https://www.plumed.org/doc-master/user-doc/html/PCAVARS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">REFERENCE<span class="right">a pdb file containing the set of reference configurations<i></i></span></span>=../data/pca2-reference.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which distances are calculated<i></i></span></span>=OPTIMAL
<span style="display:none;" id="data/work/plumed_ex7.dat_solp">The PCAVARS action with label <b>p</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">p.eig</td><td>the projections on the eigenvalues</td></tr><tr><td width="5%">p.residual</td><td>the residual distance that is not projected on any of the eigenvalues</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/work/plumed_ex7.dat_solp">p.*</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
</pre></div>

 {% endraw %} 

Notice that there are now three structures within `pca2-reference.pdb`, and thus two vectors are defined.  __Use this input to re-analyse the data in `alanine-transformation.pdb` and your MD simulations before continuing.__  
The figure below shows the results that I obtained by analyzing the
data using the PCAVARS command above.

![The black points are the configurations visited in MD simulations at 300K (left) and 1000K (right).  The top panel shows these trajectories in the Ramachandran plane.   The projection on the vectors defined using the configurations in pca2-reference.pdb is shown in the bottom panel.  The green points in the top panel give the Ramachandran angles for the configurations used to define the reference configurations.](figures/masterclass-21-6-pcavars2.png)

### Path collective variables

Instead of using the projection on more than one vector, we can extend the ideas in the previous section and use curvilinear paths rather than linear paths.  This trick is what is done with the PATH CVs that are illustrated in the figure below:

![The S variable can be thought as the length of the red segment, while the Z variable is the length of the green one](figures/belfast-2-ab-sz.png)

As you can see, there are two path collective variables, $S(X)$ measures your position on a path and is calculated using:

$$
S(X)=\frac{\sum_{i=1}^{N} i\ \exp^{-\lambda \vert X-X_i \vert }}{ \sum_{i=1}^{N} \exp^{-\lambda \vert X-X_i \vert } }
$$

$Z(x)$, meanwhile, measures the distance from the path using:

$$
Z(X) = - \frac{1}{\lambda} \ln\left[ \sum_{i=1}^{N} \exp^{-\lambda \vert X-X_i \vert } \right]
$$

We can calculate these CVs using a filled-in version of the input that is shown below:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/work/plumed_ex8.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="plumed_ex8.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="plumed_ex8.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
<div class="headerBadge"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/work/plumed_ex8.dat")' onmousedown='toggleDisplay("data/work/plumed_ex8.dat")'/></div>
</div>
</div>
<div id="data/work/plumed_ex8.dat_short">
<pre class="plumedlisting">
<b name="data/work/plumed_ex8.datpath" onclick='showPath("data/work/plumed_ex8.dat","data/work/plumed_ex8.datpath","data/work/plumed_ex8.datpath","brown")'>path</b>: <span class="plumedtooltip" style="color:green">PATH<span class="right">Path collective variables with a more flexible framework for the distance metric being used. <a href="https://www.plumed.org/doc-master/user-doc/html/PATH" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>=../data/alanine-path.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which distances are calculated<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">LAMBDA<span class="right">the lambda parameter is needed for smoothing, is in the units of plumed<i></i></span></span>=15100.
<span style="display:none;" id="data/work/plumed_ex8.datpath">The PATH action with label <b>path</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">path.spath</td><td>the position along the path calculated</td></tr><tr><td width="5%">path.zpath</td><td>the distance from the path calculated</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=* <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
</pre></div>
<div style="display:none;" id="data/work/plumed_ex8.dat_long"><pre class="plumedlisting">
<b name="data/work/plumed_ex8.dat_solpath" onclick='showPath("data/work/plumed_ex8.dat","data/work/plumed_ex8.dat_solpath","data/work/plumed_ex8.dat_solpath","brown")'>path</b>: <span class="plumedtooltip" style="color:green">PATH<span class="right">Path collective variables with a more flexible framework for the distance metric being used. <a href="https://www.plumed.org/doc-master/user-doc/html/PATH" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">REFERENCE<span class="right">a pdb file containing the set of reference configurations<i></i></span></span>=../data/alanine-path.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which distances are calculated<i></i></span></span>=OPTIMAL <span class="plumedtooltip">LAMBDA<span class="right">the lambda parameter is needed for smoothing, is in the units of plumed<i></i></span></span>=15100.
<span style="display:none;" id="data/work/plumed_ex8.dat_solpath">The PATH action with label <b>path</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">path.spath</td><td>the position along the path calculated</td></tr><tr><td width="5%">path.zpath</td><td>the distance from the path calculated</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=* <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar
</pre></div>

 {% endraw %} 

The figure below shows the $\phi$ and $\psi$ angles for the configurations that define the path as red dots.  Meanwhile, the black dots are the 
$\phi$ and $\psi$ angles that are visited during a high temperature, unbiased MD trajectory.  The green dots are then the configurations in alanine-transformation.pdb 
You can clearly see that the red dots lie along the transition path that connects the C7eq and C7ax configurations and that the green dots follow this pathway: 

![The path that we have defined for our transition in the Ramachandran plane.  Black dots are the configurations visited at 300 K (left) and 1000 K (right)](figures/masterclass-21-6-path-angles.png)

When we calculate the path collective variables for the black and red data points in the above figure, we get the result shown on the right. The panel on the left shows the output from 
a 300 K simulation during which the C7eq configuration was not visited:

![An analysis of the path CV values visited during trajectories at 300 K and 1000 K.](figures/masterclass-21-6-path-path.png)

You can see that the majority of configurations have very small z values.  It would thus seem that we have identified our reaction coordinate.  We can use the S-path coordinate
to tell us where we are on the transition pathway between the two states.  Furthermore, in defining this coordinate, we have used the positions of all the heavy atoms in the protein.  

### The isocommittor

Notice that when we talk about the reaction coordinate, we are not talking about a single set of configurations that connect the two states.
The previous sections have shown that there are always multiple pathways that connect the two states.  The task of identifying a single reaction coordinate thus appears
impossible.  How, after all, can there be a single reaction path if we know that there are multiple pathways that connect the two states?  

One way of answering this question is to look at how far the transitions you observe deviate from the reference transition path using the Z-coordinate.  An
alternative answer can be found by considering so-called isocommittor surfaces.  When using this method, you suppose there is a
saddle point between the two states of interest (the $C_7ax$ and $C_7eq$ configurations in our alanine dipeptide example).  

Let's suppose that we now start a simulation with the system balanced precariously on this saddle point.  The system will, very-rapidly, fall off the maximum and move
towards either the left or the right basin.  If we are exactly at the saddle, 50% of the trajectories will fall to the right, and 50% will fall to the left. 

We can use the idea of the isocommittor to identify whether any collective variable is giving a good description of the transition state ensemble's location.
The idea in such simulations is to define regions of space that correspond to the various stable states in the free energy landscape.  We then launch lots of simulations
from configurations that are not within these basins and identify the basin that these calculations visit first.  We can then make graphs like those shown below. These graphs 
show the fraction of times a particular CV value was visited in a trajectory that visited the c7eq basin before it visited the c7ax basin. 

![Probabilities of visiting the C7eq basin before the C7ax basin if you are differents points on each of the CV ranges](figures/masterclass-21-6-committor.png)

The PLUMED input that I used when making the figure above is a filled in version of the following:

{% raw %}
<div class="plumedpreheader">
<div class="headerInfo" id="value_details_data/work/plumed_ex9.dat"> Click on the labels of the actions for more information on what each action computes </div>
<div class="containerBadge">
<div class="headerBadge"><a href="plumed_ex9.dat.plumed.stderr"><img src="https://img.shields.io/badge/v2.9-passing-green.svg" alt="tested onv2.9" /></a></div>
<div class="headerBadge"><a href="plumed_ex9.dat.plumed_master.stderr"><img src="https://img.shields.io/badge/master-passing-green.svg" alt="tested onmaster" /></a></div>
<div class="headerBadge"><img class="toggler" src="https://img.shields.io/badge/master-incomplete-yellow.svg" alt="tested on master" onmouseup='toggleDisplay("data/work/plumed_ex9.dat")' onmousedown='toggleDisplay("data/work/plumed_ex9.dat")'/></div>
</div>
</div>
<div id="data/work/plumed_ex9.dat_short">
<pre class="plumedlisting">
<b name="data/work/plumed_ex9.datphi" onclick='showPath("data/work/plumed_ex9.dat","data/work/plumed_ex9.datphi","data/work/plumed_ex9.datphi","brown")'>phi</b>: <span class="plumedtooltip" style="color:green">TORSION<span class="right">Calculate one or multiple torsional angles. <a href="https://www.plumed.org/doc-master/user-doc/html/TORSION" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>=5,7,9,15
<span style="display:none;" id="data/work/plumed_ex9.datphi">The TORSION action with label <b>phi</b> calculates the TORSION involving these atoms</span><b name="data/work/plumed_ex9.datpsi" onclick='showPath("data/work/plumed_ex9.dat","data/work/plumed_ex9.datpsi","data/work/plumed_ex9.datpsi","brown")'>psi</b>: <span class="plumedtooltip" style="color:green">TORSION<span class="right">Calculate one or multiple torsional angles. <a href="https://www.plumed.org/doc-master/user-doc/html/TORSION" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>=7,9,15,17
<span style="display:none;" id="data/work/plumed_ex9.datpsi">The TORSION action with label <b>psi</b> calculates the TORSION involving these atoms</span><b name="data/work/plumed_ex9.datpca" onclick='showPath("data/work/plumed_ex9.dat","data/work/plumed_ex9.datpca","data/work/plumed_ex9.datpca","brown")'>pca</b>: <span class="plumedtooltip" style="color:green">PCAVARS<span class="right">Projection on principal component eigenvectors or other high dimensional linear subspace <a href="https://www.plumed.org/doc-master/user-doc/html/PCAVARS" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>=../data/pca-reference.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which distances are calculated<i></i></span></span>=<span style="background-color:yellow">__FILL__</span>
<span style="display:none;" id="data/work/plumed_ex9.datpca">The PCAVARS action with label <b>pca</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">pca.eig</td><td>the projections on the eigenvalues</td></tr><tr><td width="5%">pca.residual</td><td>the residual distance that is not projected on any of the eigenvalues</td></tr></table></span><b name="data/work/plumed_ex9.datpath" onclick='showPath("data/work/plumed_ex9.dat","data/work/plumed_ex9.datpath","data/work/plumed_ex9.datpath","brown")'>path</b>: <span class="plumedtooltip" style="color:green">PATH<span class="right">Path collective variables with a more flexible framework for the distance metric being used. <a href="https://www.plumed.org/doc-master/user-doc/html/PATH" style="color:green">More details</a><i></i></span></span>  <span style="background-color:yellow">__FILL__</span>=../data/alanine-path.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which distances are calculated<i></i></span></span>=<span style="background-color:yellow">__FILL__</span> <span class="plumedtooltip">LAMBDA<span class="right">the lambda parameter is needed for smoothing, is in the units of plumed<i></i></span></span>=15100
<span style="display:none;" id="data/work/plumed_ex9.datpath">The PATH action with label <b>path</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">path.spath</td><td>the position along the path calculated</td></tr><tr><td width="5%">path.zpath</td><td>the distance from the path calculated</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span style="background-color:yellow">__FILL__</span>=<b name="data/work/plumed_ex9.datphi">phi</b>,<b name="data/work/plumed_ex9.datpsi">psi</b>,<b name="data/work/plumed_ex9.datpca">pca.eig-1</b>,<b name="data/work/plumed_ex9.datpath">path.spath</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=1
<span style="display:none;" id="data/work/plumed_ex9.dat">The PRINT action with label <b></b> calculates something</span><span class="plumedtooltip" style="color:green">COMMITTOR<span class="right">Does a committor analysis. <a href="https://www.plumed.org/doc-master/user-doc/html/COMMITTOR" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values which is being used to define the committor surface<i></i></span></span>=<b name="data/work/plumed_ex9.datphi">phi</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the CVs are analyzed<i></i></span></span>=1 <span class="plumedtooltip">BASIN_LL1<span class="right">List of lower limits for basin #<i></i></span></span>=-3 <span class="plumedtooltip">BASIN_UL1<span class="right">List of upper limits for basin #<i></i></span></span>=-1 <span class="plumedtooltip">BASIN_LL2<span class="right">List of lower limits for basin #<i></i></span></span>=1 <span class="plumedtooltip">BASIN_UL2<span class="right">List of upper limits for basin #<i></i></span></span>=2 <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output the reached basin<i></i></span></span>=basin
</pre></div>
<div style="display:none;" id="data/work/plumed_ex9.dat_long"><pre class="plumedlisting">
<b name="data/work/plumed_ex9.dat_solphi" onclick='showPath("data/work/plumed_ex9.dat","data/work/plumed_ex9.dat_solphi","data/work/plumed_ex9.dat_solphi","brown")'>phi</b>: <span class="plumedtooltip" style="color:green">TORSION<span class="right">Calculate one or multiple torsional angles. <a href="https://www.plumed.org/doc-master/user-doc/html/TORSION" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the four atoms involved in the torsional angle<i></i></span></span>=5,7,9,15
<span style="display:none;" id="data/work/plumed_ex9.dat_solphi">The TORSION action with label <b>phi</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">phi.value</td><td>the TORSION involving these atoms</td></tr></table></span><b name="data/work/plumed_ex9.dat_solpsi" onclick='showPath("data/work/plumed_ex9.dat","data/work/plumed_ex9.dat_solpsi","data/work/plumed_ex9.dat_solpsi","brown")'>psi</b>: <span class="plumedtooltip" style="color:green">TORSION<span class="right">Calculate one or multiple torsional angles. <a href="https://www.plumed.org/doc-master/user-doc/html/TORSION" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ATOMS<span class="right">the four atoms involved in the torsional angle<i></i></span></span>=7,9,15,17
<span style="display:none;" id="data/work/plumed_ex9.dat_solpsi">The TORSION action with label <b>psi</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">psi.value</td><td>the TORSION involving these atoms</td></tr></table></span><b name="data/work/plumed_ex9.dat_solpca" onclick='showPath("data/work/plumed_ex9.dat","data/work/plumed_ex9.dat_solpca","data/work/plumed_ex9.dat_solpca","brown")'>pca</b>: <span class="plumedtooltip" style="color:green">PCAVARS<span class="right">Projection on principal component eigenvectors or other high dimensional linear subspace <a href="https://www.plumed.org/doc-master/user-doc/html/PCAVARS" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">REFERENCE<span class="right">a pdb file containing the set of reference configurations<i></i></span></span>=../data/pca-reference.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which distances are calculated<i></i></span></span>=OPTIMAL
<span style="display:none;" id="data/work/plumed_ex9.dat_solpca">The PCAVARS action with label <b>pca</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">pca.eig</td><td>the projections on the eigenvalues</td></tr><tr><td width="5%">pca.residual</td><td>the residual distance that is not projected on any of the eigenvalues</td></tr></table></span><b name="data/work/plumed_ex9.dat_solpath" onclick='showPath("data/work/plumed_ex9.dat","data/work/plumed_ex9.dat_solpath","data/work/plumed_ex9.dat_solpath","brown")'>path</b>: <span class="plumedtooltip" style="color:green">PATH<span class="right">Path collective variables with a more flexible framework for the distance metric being used. <a href="https://www.plumed.org/doc-master/user-doc/html/PATH" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">REFERENCE<span class="right">a pdb file containing the set of reference configurations<i></i></span></span>=../data/alanine-path.pdb <span class="plumedtooltip">TYPE<span class="right"> the manner in which distances are calculated<i></i></span></span>=OPTIMAL <span class="plumedtooltip">LAMBDA<span class="right">the lambda parameter is needed for smoothing, is in the units of plumed<i></i></span></span>=15100.
<span style="display:none;" id="data/work/plumed_ex9.dat_solpath">The PATH action with label <b>path</b> calculates the following quantities:<table  align="center" frame="void" width="95%" cellpadding="5%"><tr><td width="5%"><b> Quantity </b>  </td><td><b> Description </b> </td></tr><tr><td width="5%">path.spath</td><td>the position along the path calculated</td></tr><tr><td width="5%">path.zpath</td><td>the distance from the path calculated</td></tr></table></span><span class="plumedtooltip" style="color:green">PRINT<span class="right">Print quantities to a file. <a href="https://www.plumed.org/doc-master/user-doc/html/PRINT" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values that you would like to print to the file<i></i></span></span>=<b name="data/work/plumed_ex9.dat_solphi">phi</b>,<b name="data/work/plumed_ex9.dat_solpsi">psi</b>,<b name="data/work/plumed_ex9.dat_solpca">pca.eig-1</b>,<b name="data/work/plumed_ex9.dat_solpath">path.spath</b> <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output these quantities<i></i></span></span>=colvar <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the quantities of interest should be output<i></i></span></span>=1
<span style="display:none;" id="data/work/plumed_ex9.dat_sol">The PRINT action with label <b></b> calculates something</span><span class="plumedtooltip" style="color:green">COMMITTOR<span class="right">Does a committor analysis. <a href="https://www.plumed.org/doc-master/user-doc/html/COMMITTOR" style="color:green">More details</a><i></i></span></span> <span class="plumedtooltip">ARG<span class="right">the labels of the values which is being used to define the committor surface<i></i></span></span>=<b name="data/work/plumed_ex9.dat_solphi">phi</b> <span class="plumedtooltip">STRIDE<span class="right"> the frequency with which the CVs are analyzed<i></i></span></span>=1 <span class="plumedtooltip">BASIN_LL1<span class="right">List of lower limits for basin #<i></i></span></span>=-3 <span class="plumedtooltip">BASIN_UL1<span class="right">List of upper limits for basin #<i></i></span></span>=-1 <span class="plumedtooltip">BASIN_LL2<span class="right">List of lower limits for basin #<i></i></span></span>=1 <span class="plumedtooltip">BASIN_UL2<span class="right">List of upper limits for basin #<i></i></span></span>=2 <span class="plumedtooltip">FILE<span class="right">the name of the file on which to output the reached basin<i></i></span></span>=basin
</pre></div>

 {% endraw %} 

I deployed the input above within the following python script that launches a large number of gromacs simulations:

```python
def gen_trajectories( ntraj, plm ) : 
    nc7eq, c7eq_colv, all_data = 0, np.zeros([0,5]), np.zeros([0,5])
    for i in range(ntraj) :
        !rm -rf ../Test && mkdir ../Test
        generate_gromacs_input( '../Test', plm, 10000000, 300 )
        !cd ../Test/ && gmx_mpi grompp -f md.mdp -c conf.pdb -p topol.top -maxwarn 2 &> /dev/null 
        !cd ../Test/ && gmx_mpi mdrun --plumed plumed.dat &> /dev/null
        bfile = open('../Test/basin','r')
        with open( '../Test/basin', "r" ) as myfile :
            for line in myfile :
                if line.startswith("#! SET COMMITTED TO BASIN") : basin = line.split()[5]
        colv_data = np.loadtxt("../Test/colvar")
        if len(colv_data.shape)==1 : colv_data = np.reshape( colv_data, (1,5) )
        all_data = np.concatenate( (all_data, colv_data), axis=0 )
        if basin=="1" : 
            c7eq_colv = np.concatenate( (c7eq_colv, colv_data), axis=0 )
            nc7eq = nc7eq + 1
    print( "NUMBER c7ax", ntraj-nc7eq, "c7eq", nc7eq )
    return c7eq_colv, all_data

p='''
YOUR PLUMED INPUT GOES HERE
'''
bas_data, all_data = gen_trajectories( ntraj, p )
```

Notice how the above script stores the CV values from trajectories that finished in the C7eq basin in the NumPy array called `bas_data`. 
We can use the data in this file to construct the (unnormalized) histograms of CV value that finished in C7eq and the total histogram. 
The script I used to construct these histograms is shown below.  This script also shows how we can arrive at the final conditional probability distributions from 
the figure above by dividing by the total number of configurations that moves to C7eq first by the total number of configuration that visited 
a point.

```python
def histo( data, nbins, xmin, xmax ) :
    delr = ( xmax - xmin ) / nbins 
    hist = np.zeros(nbins)
    for d in data : 
        xbin = int( np.floor( (d-xmin) / delr ) )
        hist[xbin] = hist[xbin] + 1
    return hist / delr 

def get_isocommitor( bas_data, full_data, nbins, xmin, xmax ) :
    bas_histo = histo( bas_data, nbins, xmin, xmax ) 
    full_histo = histo( full_data, nbins, xmin, xmax )
    for i in range(nbins) : 
        if np.abs(full_histo[i])<1E-4 : bas_histo[i] = 0 
        else : bas_histo[i] = bas_histo[i] / full_histo[i]
    return bas_histo 

# This makes the isocommittor as a function of \f$\phi\f$:
commit = get_isocommitor( bas_data[:,1],  all_data[:,1], 30, -np.pi, np.pi )
```

Notice that the script above does not compute the error bars I included in the figure.  __Your task in this exercise is to reproduce this 
figure with the error bars.__   I generated the error bars in my figure by running 10 sets of 500 simulations.  I constructed separate histograms
from each of these batches of simulations and calculated the mean and variance from these ten sets of samples. 

## Conclusions

The exercises in this section aimed to discuss the difference between collective variables and the reaction coordinate.  I have argued that collective variables are developed by researchers thinking about coordinates that can distinguish between the important states.  Reaction coordinates, meanwhile, are the actual pathways
that reactions proceed along.  These reaction coordinates are found by probing the data we get from simulations.    

I am not convinced that the distinction between reaction coordinates and collective variables is very important.  Every coordinate we have tried in the previous sections has allowed us to determine whether we are in the C7eq or the C7ax basin.   My view is that when we do science, we impose structure on our results by asking questions.  Our question has been
to determine the relative free energies of the C7ax and C7eq basins in this exercise.  To do this, we have to define what configurations are in the C7ax basin and what configurations are in the C7eq basin.  The distinction between these two structures is an arbitrary figment of our imagination.  If we use different variables, we might be defining these states differently, and we might get slightly different answers. 
We should not be surprised by the fact that we get different answers if we ask the question differently.  The important thing is to develop an interesting question and to tell a good story about whatever you find out. 
