# Passing data between Actions

Each line in a PLUMED input file creates a PLMD::Action. Many of these PLMD::Action commands
calculate some quantity or some small set of quantities. These quantities are stored in PLMD::Value
objects. PLMD::Action commands that calculate quantities thus inherit from the base class PLMD::ActionWithValue.
If a second PLMD::Action uses the PLMD::Value that is calculated earlier in the input, then this section action
will inherit from PLMD::ActionWithArgument. To summarise:

* PLMD::Value holds the quantities that can be passed between PLMD::Action objects.
* PLMD::ActionWithValue objects are used to set PLMD::Value objects.
* PLMD::ActionWithArguments objects are used to get PLMD::Value objects.
 
So does all the data that passes between PLMD::Action objects do so in PLMD::Value objects? No.   

Why not? PLMD::Value objects can only be used to pass scalars between PLMD::Action objects. If one wishes to pass something  
more complicated (e.g. an atomic position), some alternative mechanism must be developed.

I have been interested in extending this mechanism for passing data between Actions over the past few years. I wanted to 
develop a new version of the PLMD::Value class that also allows one to pass vectors, matrices and functions on grids between
PLMD::Action objects. My interest in doing so came initially from a desire to make it easy to pass all these quantities from PLUMED
to Python. I quickly realised, however, that the greater flexibility this offers makes PLUMED more powerful.

## Anatomy of PLMD::Value

The four most important variables in a PLUMED 2.9 PLMD::Value object are:

* `value` = the value of the scalar
* `hasDeriv`= bool that is true if the action that calculates scalar also calculates the derivatives of the value with respect to the input quantities for the PLMD::Action that calculates it
* `derivatives` = the derivatives of the input quantity with respect to the input quantities for the PLMD::Action that calculates it
* `inputForce` = the force that acts upon this scalar. In calculating the forces on the atoms using the chain rule, this inputForce is multiplied by the derivatives in `derivatives.`

In the new version of PLUMED that allows one to pass scalars, vectors, matrices and grids, these four variables are replaced by:

* `data` = a std::vector that contains all the data that is to be passed between actions
* `shape` = a std::vector with 0 components if PLMD::Value is a scalar, 1 component if PLMD::Value is a vector/1D grid, 2 components if PLMD::Value is a matrix/2D grid.
* `hasDeriv` = if shape.size()==0 this bool is true if the action that calculates scalar also calculates the derivatives of the value with respect to the input quantities for the PLMD::Action that calculates it. If shape.size()>0, this bool is true if the PLMD::Value holds a function computed on a grid.
* `storedata` = a bool that is set true if hasDeriv is false, shape.size()>0, and we need to store the values of the vector/matrix to calculate forces using the chain rule.
* `inputForce` = a std::vector that contains the forces that should be applied on each component of the input object.

In future articles, I will write much more about the `storedata` variable and how we can calculate forces __without__ storing derivatives with respect to all the components. For now, though, I will explain 
the organisation of the information in `data` the three most basic data types:

* __scalars without derivatives__ - the data vector has only one component, which holds the scalar.
* __scalar with derivatives__   - the data vector has 1 + number of derivatives components. data[0] holds the value of the scalar. Every other component holds a derivative of the scalar.
* __vector__ - the data vector has `shape[0]` commponents. This is the number of components in the vector.
* __matrix__ - the data vector has `shape[0]*shape[1]` components. This is the number of components in the matrix.

I will expand on what is done for matrices, and grids will be provided in future articles as it is a little more complicated.

## Why/why not just scalars?

Systems in biochemistry, unlike those in condensed matter, do not have atom-interchange symmetry. When designing CVs, there is thus no reason to say that a quantity calculated for two different 
sets of atoms is interchangeable. Therefore, in biochemistry (as opposed to materials science), CVs are not often designed by calculating a vector of symmetrically equivalent quantities 
and then performing some operation on this vector (e.g. taking the average of all the quantities within it). Simulators of biomolecules, for instance, would also rarely calculate a radial distribution
function, which is a ubiquitous operation among researchers who simulate materials.

The majority of the simulations that are done with PLUMED are on systems of biomolecules. For these simulations having fine-grained control over the individual scalars 
passed in the input file makes sense, as these scalars are not all symmetrically equivalent. You thus rarely encounter situations, as you would in materials science, where the same operations 
should be done for every scalar in a vector. 

The introduction of methods such as parallel bias metadynamics suggests that it is worth trying to change the way we introduce methods such as metadynamics. This method was developed
in 2018, 16 years after the introduction of metadynamics. Given the time this development took, is it worth doing more to raise awareness that averaging over symmetrically-equivalent CVs is acceptable 
when using enhanced sampling methods?
