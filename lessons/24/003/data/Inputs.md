Some other inputs that we have used when benchmarking plumed include:

The inputs below were all tested using the `--atom-distribution=sc` option.

## Coordination number using multicolvar

```plumed
c1: CONTACT_MATRIX GROUP=@mdatoms SWITCH={EXP D_0=1.0 R_0=0.1 D_MAX=2.0}
ones: ONES SIZE=8000
cc: MATRIX_VECTOR_PRODUCT ARG=c1,ones
mts: SUM ARG=cc PERIODIC=NO
PRINT ARG=mts FILE=colvar
BIASVALUE ARG=mts
```

## Steinhardt order parameters

```plumed
q6: Q6 SPECIES=@mdatoms SWITCH={EXP D_0=1.0 R_0=0.1 D_MAX=2.0} SUM
PRINT ARG=q6_sum FILE=colvar
BIASVALUE ARG=q6_sum
```

## Local Steinhard parameters

```plumed
q6: Q6 SPECIES=@mdatoms SWITCH={EXP D_0=1.0 R_0=0.1 D_MAX=2.0}
lq6: LOCAL_Q6 SPECIES=q6 SWITCH={EXP D_0=1.0 R_0=0.1 D_MAX=2.0} SUM

PRINT ARG=lq6_sum FILE=colvar
BIASVALUE ARG=lq6_sum
```
