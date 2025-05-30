# Part 3: Use the bias on a system with multiple ions

Now that our bias is tested for a single Mg<sup>2+</sup>–phosphate pair, we can use it on a larger RNA system with multiple binding sites and ions in solution.

We will directly use the accelerating stategy to sample the Mg-binding features of a short RNA duplex, G<sub>3</sub>·C<sub>3</sub>.
## Implementation

### Simulation set-up

<center><img src="duplex/duplex.png" alt="Rendering of the duplex system" width="40%"/></center>

We provide as input files:
- `input.gro`: equilibrated simulation box with the G<sub>3</sub>·C<sub>3</sub> duplex solvated with MgCl<sub>2</sub> (8 Mg<sup>2+</sup> and 10 Cl<sup>−</sup> ions in total)
- `run.mdp`: GROMACS MD parameter file
- `topol.top`: Standalone GROMACS topology file

[They can be downloaded here.](duplex/duplex.zip)


### Instructions

1) Write a PLUMED input file `plumed_duplex.dat`. You will need to declare two coordination CVs and one bias for every Mg atom.

> [!TIP]
> This is probably better done with a script. One way of doing this in a bash script is to first get a list of indices for all MG atoms, for example using [AWK](https://www.gnu.org/software/gawk/manual/gawk.html):
> ```bash
> mg_inds=$(awk '$2 ~ /^MG/ { print NR-2 }' input.gro)
> ```
> and then generate the PLUMED code in a `for` loop
> ```bash
> for img in ${mg_inds}; do
>    cat >> plumed_duplex.dat << EOF
> # ... Multiline PLUMED syntax ...
> # ... something that depends on $img ...
> EOF
> done

