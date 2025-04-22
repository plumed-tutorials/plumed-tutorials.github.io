# Passing energy to PLUMED

Several enhanced sampling methods apply a bias potential on the potential energy that is calculated by the MD code.  If the potential energy that is passed to 
PLUMED is $V$, and the force from the bias on the potential energy is $f_e$, then the corresponding forces on position component $j$ of atom $i$ can be calculated as:

$$
F_{ij}^{\textrm{bias}} = f_e \left(  \frac{\partial V}{\partial x_{ij} } \right)
$$

$\frac{\partial V}{\partial x_{ij} }$ is simply the negative of the force on position component $j$ of atom $i$ due to the potential $E$.  
We can thus calculate the total force on position component $j$ of atom $i$ from both the potential $E$ and the bias potential that is acting upon the potential energy as:

$$
F_{ij}^{\textrm{bias}+\textrm{potential}} = \left( 1 - f_e \right) \left( \frac{\partial V}{\partial x_{ij} } \right)
$$ 

In other words, we need to multiply the forces passed from the MD code to PLUMED by $\left( 1 - f_e \right)$ to calculate the total force on the atoms.

You can see how this mechanism for determining the total force due to the potential and a bias on the potential is used within `colvar/Energy.cpp.`  As I was writing this
Could similar code be employed elsewhere within the interface? For example, if you calculated some properties of each atom in the MD code and 
passed these properties through the DOMAIN_DECOMPOSITION, could you then use something like this to gather the forces on the sum of the individual atomic properties?

