# Lennard Jones: Possible project extensions

In the example project I studied how the heat capacity for a system of Lennard Jones particles depends on temperature.
The obvious extension for you to try is to investigate the heat capacity as a function of temperature for some other pair 
potential.  You can do something as simple as changing the powers of 6 and 12 in the Lennard Jones potential to different 
numbers. Alternatively, if you want to try something more challenging you can try to develop a completely different potential.
For example, you could try to investigate what happens if there are two minima in the potential energy as a function of distance.

The only limitations on the function that you choose are that:

1. The pair potential $V(r)$ should be a continuous and differentiable function of $r$.
2. The pair potential $V(r)$ should go to infinity as $r \rightarrow 0$ 
3. The pair potential $V(r)$ should go  to zero as $r \righarrow \infty$ 

One way to generate an interesting potential would be to give the values for $V(r) at a series of $r$ values and to then 
interpolate the function between these points.

Please include a figure in any report you write on this topic that shows the pair potential function that you have investigated.  
