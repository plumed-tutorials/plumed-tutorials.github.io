## The serial code

```c++
void MyCoordination::calculate() {
  double ncoord = 0.;
  auto pos = getPositions();
  const unsigned nn = pos.size();
  Vector distance;
  for (unsigned int i0 = 0; i0 < nn; ++i0) {
    for (unsigned int i1 = 0; i1 < nn; ++i1) {
      if (i0 == i1) {continue;}
      distance = delta(getPosition(i0), getPosition(i1));
      ncoord += (distance.modulo() < R_0) ? 1 : 0;
    }
  }
  setValue(ncoord);
}
```
the workflow is:
- get the positions
- initialize `ncoord` to zero
- do a double loop calculating the distance between each possible couple of atoms
and increment `ncoord` each time the distance is less than `R_0`
(avoid calculating the distance from self)

[back](Readme.md)

See also:
[serial](Readme_Serial.md) [openMP](Readme_OMP.md) [MPI](Readme_MPI.md) [Cuda](Readme_CUDA.md)
