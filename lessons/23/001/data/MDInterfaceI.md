# Passing data to/from PLUMED

Data is passed to/from PLUMED from/to MD codes in void pointers. Given that, as discussed in [this article](Passing.md), data is passed between PLMD::Action 
objects in PLMD::Value objects, it stands to reason that there must be a PLMD::Action object that transfers the data in a PLMD::Value to a void pointer. Similarly,
there must also be some PLMD::Action that converts the data in void pointer into a PLMD::Value. These two PLMD::Actions are called GET and PUT. This article 
gives a brief introduction to these Actions.

## GET

The PLMD::Action GET inherits from PLMD::ActionWithArguments. This command takes in a single PLMD::Value and transfers the contents of the `data` vector for the 
PLMD::Value to a void pointer that is accessible in the code that called PLUMED. As the calling code does not know the shape of the PLMD::Value in advance, 
we provide the functionality to get the data rank and shape. The following Python snippet illustrates how this works in practice:

```python
import plumed

# Create a PLUMED object
p = plumed.Plumed()
# Setup PLUMED 
num_atoms = 10
p.cmd("setNatoms",num_atoms)
p.cmd("setLogFile","test.log")
p.cmd("init")
# Tell PLUMED to calculate the distance between two atoms
p.cmd("readInputLine", "d1: DISTANCE ATOMS=1,2")
# Get the rank of the PLMD::Value that holds the distance
# This command sets up the GET object
rank = np.zeros( 1, dtype=np.int_ )
p.cmd("getDataRank d1", rank )
# Now get the shape of the PLMD::Value d1 that we are asking for in the 
# GET object
shape = np.zeros( rank, dtype=np.int_ )
p.cmd("getDataShape d1", shape )
# And now set the void pointer that the data in PLMD::Value d1 should be 
# transferred to so it can be accessed in our python script when asking PLMD to do a calculation 
d1 = np.zeros( shape )
p.cmd("setMemoryForData d1", data ) 
```

Notice that you can have as many GET actions as you need. The data is transferred from the PLMD::Value to the void pointer when the `calculate` method of GET is called.  
Transferring variables is thus seamlessly integrated into the PLUMED calculation cycle. This simple mechanism for transferring variables replaces a mechanism that used a class called
PLMD::DataFetchingObject that did not inherit from PLMD::Action. Using this (old) mechanism means that additional lines in PLMD::PlumedMain were required to fetch variables. These additional 
lines are no longer needed.

## PUT

The PLMD::Action PUT inherits from PLMD::ActionWithValue. PUT transfers the data from a void pointer passed to PLMD from the calling code to a PLMD::Value. The calling
object knows the shapes of the variables it is passing, so if you want to pass a 3x3 matrix from the MD code to PLUMED, you create the space to do so as follows:

```c++
plumed.cmd("readInputLine n: PUT SHAPE=3,3 UNIT=length PERIODIC=NO");
``` 

This command then creates a PLMD::Value called `n` that you can refer to later in your PLUMED input file. To transfer data from the void pointer called val into the PLMD::Value 
called `n`, you would then use the following command:

```c++
plumed.cmd("setValue n", val);  
``` 

Notice also that if you expect PLUMED to try to apply forces on `n`, you can pass a void pointer called `force` to get the forces that PLUMED has applied on the elements of n as follows:

```c++
plumed.cmd("setValueForces n", force); 
```

Within the PLMD::Value `n`, the forces that PLUMED wishes to apply on the components of the input object are stored in the std::vector called `inputForce`. Furthermore, whenever a PLMD::Value
is created from a PUT action `storedata` is set to true. PUT also has a CONSTANT flag that allows you to transfer variables such as the value of the timestep that is set only once during the 
simulation (i.e. during startup).  

Data is transferred from the input void pointers to the PLMD value when the `share` and `wait` methods are called. Vectors, e.g. positions, that are split between the domains 
are transferred when the share and wait methods of the DOMAIN_DECOMPOSITION action are called. However, I will write more about that in another post.
