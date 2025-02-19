# Rewriting the coordination for plumed in Cuda

Here I am showing how to set up a plug-in that is compiled with the cuda compiler
and that can be LOADed in plumed.
The project consists in two parts: the actual
[coordination implementation](Implementation.md) and a [helper module](Helpers.md)
 with the reduction algorithm and a tool for easing memory management.


```mermaid
flowchart LR

Intro[Introduction]
Implementation
Helpers
AB[GROUPA,GROUPB]
Pair

Intro ==> Implementation
Implementation <==> Helpers
Intro ==> Helpers
Implementation <==> Pair
Implementation <==> AB


click Intro "NAVIGATION.html" "The introduction"
click Implementation "Implementation.html" "The coordination implementation"
click AB "ImplementationTwoGroups.html" "The coordination between two groups"
click Pair "ImplementationPair.html" "The coordination in pairs"
click Helpers "Helpers.html" "A simple manual with the helper library"
```
