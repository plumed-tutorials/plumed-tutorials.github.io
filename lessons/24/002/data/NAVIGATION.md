# PLUMED Tutorial on Trans-Cis isomerization in the ground and excited states

This lesson intends to show ho to combine PLUMED with your MD code to simulate dihedral angle isomerization in ground and excited states using FEP and Hamiltonian Replica exchange.

In this tutorial you will find:

* The reference paper.
* The slides of the simulation workflow.
* The instructions on how to setup the simulations.
* The plumed input file.
* A python notebook with a solution useful to complete the exercise.

The flow chart shown below indicates the order in which you should consult the resources.
You can click on the nodes to access the various resources.


```mermaid
flowchart LR
A[The method intro] ==> B[Lecture I]
B ==> C[Instructions]
C ==> D[An example of plumed file]
D ==> E[solution]
click A "https://pubs.aip.org/aip/jcp/article-abstract/154/17/174108/200045/Multi-replica-biased-sampling-for-photoswitchable?redirectedFrom=fulltext" "The paper related to the Multi-replica biased sampling for Trans-cis isomerization in the ground and excited states using PLUMED"
click B "https://static1.squarespace.com/static/5fe9a1f019bc26003ee2f585/t/66bf0a3059d1da25c8693695/1723796018487/Slide.pdf" "The lecture slides"
click C "GAT_SAFE_README.html" "The instructions for the masterclass"
click D "plumedfile.html" "The example plumed input file"
click E "notebook.html" "The notebook file"
```
