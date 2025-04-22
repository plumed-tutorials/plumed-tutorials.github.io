# Dealing with virtual atoms

Virtual atoms are used to refer to the positions used in calculating CVs but where no atoms 
can be found. The most commonly used example of a virtual atom is a centre of mass.  

In older versions of PLUMED, these virtual atom positions were passed back to the Atoms class. Consequently, if the 
MD code passed $n$ atoms to PLUMED, and PLUMED went on to define $k$ virtual atom positions; you could choose
from amongst $n+k$ positions when deciding how to calculate your CVs.

You can do the same in newer versions of PLUMED. Now, however, the virtual atom positions are stored in three
PLMD::Value objects so the passing is consistent with the ideas discussed [here](Passing.md). To make this possible
PLMD::ActionWithValue contains the following code in its constructor:

```c++
std::vector<ActionWithValue*> vatoms = plumed.getActionSet().select<ActionWithValue*>();
for(const auto & vv : vatoms ) {
  ActionToPutData* ap = dynamic_cast<ActionToPutData*>(vv);
  if( ap ) {
    if( ap->getRole()=="x" ) xpos.push_back( ap->copyOutput(0) );
    if( ap->getRole()=="y" ) ypos.push_back( ap->copyOutput(0) );
    if( ap->getRole()=="z" ) zpos.push_back( ap->copyOutput(0) );
    if( ap->getRole()=="m" ) masv.push_back( ap->copyOutput(0) );
    if( ap->getRole()=="q" ) chargev.push_back( ap->copyOutput(0) );
  }
  ActionWithVirtualAtom* av = dynamic_cast<ActionWithVirtualAtom*>(vv);
  if( av || vv->getName()=="ARGS2VATOM" ) {
    xpos.push_back( vv->copyOutput( vv->getLabel() + ".x") );
    ypos.push_back( vv->copyOutput( vv->getLabel() + ".y") );
    zpos.push_back( vv->copyOutput( vv->getLabel() + ".z") );
    masv.push_back( vv->copyOutput( vv->getLabel() + ".mass") );
    chargev.push_back( vv->copyOutput( vv->getLabel() + ".charge") );
  }
}
if( xpos.size()!=ypos.size() || xpos.size()!=zpos.size() || xpos.size()!=masv.size() || xpos.size()!=chargev.size() )
  error("mismatch between value arrays");
```

This code ensures that every Action that inherits from ActionAtomistic has five std::vector objects of pointers to PLMD::Value objects called
`xpos`, `ypos`, `zpos`, `masv` and `chargev`. These std::vector objects contain pointers to the PLMD::Value objects that contain information about 
the atoms passed from the MD code and the positions of the virtual atoms.

PLUMED works out the dependencies for this new ActionAtomistic object in `requestAtoms` by using the following code:

```c++
if(clearDep) clearDependencies();
unique.clear(); std::vector<bool> requirements( xpos.size(), false );
if( boxValue ) addDependency( boxValue->getPntrToAction() );
for(unsigned i=0; i<indexes.size(); i++) {
  if(indexes[i].index()>=n) { std::string num; Tools::convert( indexes[i].serial(),num ); error("atom " + num + " out of range"); }
  unsigned value, k; getValueIndices( indexes[i], valno, k ); requirements[valno] = true;
  if( valno==0 ) unique.push_back(indexes[i]);
  else if( k>0 ) error("action atomistic is not set up to deal with multiple vectors in position input");
}
// Add the dependencies to the actions that we require
Tools::removeDuplicates(unique);
for(unsigned i=0; i<requirements.size(); ++i ) {
  if( !requirements[i] ) continue;
  addDependency( xpos[i]->getPntrToAction() );
  addDependency( ypos[i]->getPntrToAction() );
  addDependency( zpos[i]->getPntrToAction() );
  addDependency( masv[i]->getPntrToAction() );
  addDependency( chargev[i]->getPntrToAction() );
}
```

The advantage of this new arrangement over the old one is that the code for applying forces on virtual atom positions is the same as the code for applying forces
on CVs.  
