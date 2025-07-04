# Installing PLUMED with MacPorts

If you are using a Mac, notice that you can take advantage of a MacPorts package.
Installing a working plumed should be as easy as:

- Install [MacPorts](https://www.macports.org/)
- Type `sudo port install plumed`

Notice that plumed comes with many variants that can be inspected with the command

```bash
sudo port info plumed
```

Plumed uses variants to support different compilers.
For instance, you can install plumed with mpich using

```bash
sudo port install plumed +mpich
```

Using more recent clang instead of native compilers is recommended so as to
take advantage of openMP

```bash
sudo port install plumed +mpich +clang50
```

Notice that support for c++17 with gcc compilers is someway problematic within MacPorts
due to impossibility to use the system c++ library. For this reason, only clang compilers are supported
(see also [this discussion](https://github.com/macports/macports-ports/pull/1252)).

Variants can be also used to compile with debug flags (`+debug`), to pick a linear algebra library 
(e.g. `+openblas`) and to enable all optional modules (`+allmodules`).
Notice that the default variant installed with `sudo port install plumed` is shipped as a compiled
binary, which is significantly faster to install.

In addition, we provide a developer version (typically: a later version not yet considered as stable)
under the subport `plumed-devel` that can be installed with

```bash
sudo port install plumed-devel
```

`plumed-devel` also supports the same variants as `plumed` in order to customize the compilation.
`plumed-devel` and `plumed` cannot be installed at the same time.

It is also possible to install a plumed-patched version of gromacs.
For instance, you can use the following command to install
gromacs patched with plumed with clang-5.0 compiler and mpich:

```bash
sudo port install plumed +mpich +clang50
sudo port install gromacs-plumed +mpich +clang50
```

In case you want to combine gromacs with the unstable version of plumed, use this instead:

```bash
sudo port install plumed-devel +mpich +clang50
sudo port install gromacs-plumed +mpich +clang50
```

Notice that gromacs should be compiled using the same compiler
variant as plumed (in this example `+mpich +clang50`). In case this is not
true, compilation will fail.

Also notice that gromacs is patched with plumed in runtime mode
but that the path of libplumedKernel.dylib in the MacPorts tree
is hard coded. As a consequence:

- If gromacs is run with `PLUMED_KERNEL` environment variable unset (or set to empty),
  then the MacPorts plumed is used.

- If gromacs is run with `PLUMED_KERNEL` environment variable pointing to another instance
  of the plumed library, the other instance is used.

This is especially useful if you are developing PLUMED since you will be able to install
gromacs once for all and combine it with your working version of PLUMED.
