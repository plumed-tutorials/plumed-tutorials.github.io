# Community and hierarchy

When a developer writes a new PLUMED action, they are forced to decide where the documentation
for that action should appear in the manual. Should their new PLMD::Action be listed as a collective variable, function, bias, or something else? 

I increasingly feel that these somewhat arbitrary and abstract categorisations are not that useful. They force developers to think 
in terms of a particular application domain. As the code grows, this limitation makes less and less sense.

Providing tools to document what can be done with the tools they implemented in PLUMED is more beneficial. They can do this
by submitting tutorials and, if they so wish, they can even come up with their own categorisations for the PLMD::Action objects
in the code. 

In other words, different developers working in different application domains should have the flexibility to document 
and categorise actions in a way that makes sense for the particular application domain they are working within. PLUMED is a 
community-developed code. If different people in the community think differently about the code's functionalities, then the documentation should be flexible enough to incorporate these different views.

Rather than thinking the code must have one manual, we should move to a model of having many manuals. These manuals can 
then explain how the code is used in practice.
