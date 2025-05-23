# Preparing the input files
The hySAS ONEBEAD mapping (1 bead for 1 amino acid, 3 beads for 1 nucleodide) requires two PDBs, one for the MOLINFO and one for the TEMPLATE actions. This applies to both SAXS and SAS modules. The MOLINFO PDB may contain atoms, residues, chains, that are not included for the SAS signal calculation, while the TEMPLATE PDB must contain only the residues that are used for the ONEBEAD conversion. Some general rules:

#### 1. Consistency between MOLINFO and TEMPLATE PDBs
The numbering of atoms and residues must be consistent between the MOLINFO and TEMPLATE PDBs. For example, if MOLINFO is provided with a PDB containing 100 residues, but the SAS calculation is performed on residues in the range 20-80, it is necessary to provide TEMPLATE with a PDB containing only these residues, while maintaining their numbering: if the 20th residue starts with atom number 319 and the 80th residue ends with atom number 1325, the TEMPLATE PDB must start with ATOM 319 and residue number 20, and end with ATOM 1325 and residue number 80.
Warning: If a residue is included in the SAS calculation, all corresponding atoms must be present in the PDB. Missing atoms from a residue will cause the bead mapping step to fail.
#### 2. Consistency between MOLINFO and the molfile
When using the plumed driver, the supplied molfile (PDB, XTC, ...) to be analysed must be consistent with the PDB provided in MOLINFO. Specifically, there must be the same number of atoms in the same order.
#### 3. MOLINFO PDB numbering
The MOLINFO PDB must start with ATOM number 1. The residue number can start with a positive number other than 1.
#### 4. Providing the same file to MOLINFO and TEMPLATE
It is possible to provide MOLINFO and TEMPLATE with the same PDB, taking into account all three points above.
#### 5. PDB format
The naming conventions for atoms and residues can vary depending on the force field or software used. This variability, particularly in the case of nucleic acids, is a major limitation in the hySAS mapping process. Detecting the residue type and analysing the atoms belonging to a bead is essential to:
* calculate the Solvent-Accessible Surface Area, required to introduce the solvation layer contribution or the hydrogen-deuterium exchange (SANS only);
* calculate the bead centre of mass, used to define the centre of the bead, a feature which has a major influence on the final SAS profile calculation.

For these reasons, as a preliminary step, each bead type and atom composition is verified. In order to perform this process, it is not feasible to consider all possible atom and residue names.

##### Amino acids

Several histidine residue names in different protonation states are accepted: HIS, HIE/HID/HIP (AMBER), HSE/HSD/HSP (CHARMM).

Besides CYS, the cysteine involved in disulfide bridge is also allowed. In the latter case, the residue name must be CYX.

##### Nucleic acids
Only the AMBER OL3 nomenclature for RNA residue and atom names, and the AMBER OL15 nomenclature for DNA residue and atom names, are accepted. The easiest way to convert a PDB to these formats is to use the pdb4amber script which is part of the free [AmberTools](https://ambermd.org/AmberTools.php) suite. This is the command:

```
pdb4amber -i original_DNA.pdb -o DNA_amber.pdb -d -v --add-missing-atoms
```
Warning: The `-d` `--add-missing-atoms` flags combination adds the hydrogen atoms to the PDB even if they already exist with a different nomenclature. This means that this step could double the number of atoms in the PDB. A solution could be to remove the original hydrogens from the PDB allowing the script to add them again with the correct nomenclature. Note that the order of the atoms in the MOLINFO and TEMPLATE PDBs, as well as in a previously generated trajectory to be analysed with the driver, must be consistent.

Alternatively, the LEaP script, also part of the AmberTools suite, can convert the PDB. Here is a quick step-by-step guide:
##### RNA
create a `leapRNA.in` file:
```
vim leapRNA.in
```
copy the following instructions and save the file:
```
source leaprc.RNA.OL3

rna_molecule = loadpdb original_RNA.pdb

savepdb rna_molecule RNA_amber.pdb

quit
```
Command details:

`source leaprc.RNA.OL3`: Load the parameter set for RNA molecules, specifically the OL3 force field parameters. 
`rna_molecule = loadpdb original_RNA.pdb`: Load the RNA molecule from the specified PDB file (original_RNA.pdb) into the LEaP program and assign it to the variable rna_molecule. Replace original_RNA.pdb with the PDB name you wish to convert.
`savepdb rna_molecule RNA_amber.pdb`: Save the RNA molecule that was loaded into the LEaP environment into a new PDB file named RNA_amber.pdb. This new PDB file will be formatted according to the conventions used by the AMBER software suite. Replace "RNA_amber.pdb` with your preferred PDB name.

Run LEaP:
```
tleap -s -f leapRNA.in
```
##### DNA
create a `leapDNA.in` file:
```
vim leapDNA.in
```
copy the following instructions and save the file:
```
source leaprc.DNA.OL15

dna_molecule = loadpdb original_DNA.pdb

savepdb dna_molecule DNA_amber.pdb

quit
```
Run LEaP:
```
tleap -s -f leapDNA.in
```
#### 6. Special beads
##### DNA and RNA
Three additional bead types are available for DNA and RNA besides phosphate group, pentose sugar, and nucleobase:
- 5'-end pentose sugar capped with a hydroxyl moiety at C5'. To enable this, the residue name in the PDB must be followed by "5". For example, in the case of cytosine, the corresponding residue must be edited to DC5 or to C5 in DNA and RNA, respectively.
- 3'-end pentose sugar capped with an hydroxyl moiety at C3'. To enable this, the residue name in the PDB must be followed by "3". For example, in the case of cytosine, the corresponding residue must be edited to DC3 or to C3 in DNA and RNA, respectively.
- 5'-phosphorylated end with an additional hydroxyl moiety at P. To enable this, the residue name in the PDB must be followed by "T". For example, in the case of cytosine, the corresponding residue must be edited to DCT or to CT in DNA and RNA, respectively. The additional O atom can be named in the PDB as OP3 or O3P, while the additional H can be named HOP3.


##### Proteins
An additional bead type is available for proteins:
- Cysteine residue involved in disulfide bridge (the residue in the PDB must be named CYX).

#### 7. Atom names
For practical purposes, the table below lists all DNA/RNA atom names accepted for each bead category. Note that an additional bead check is performed to ensure that the correct atom is associated with the correct nucleotidee bead type. For example, if an O2' atom name is detected in a thymine bead, an error message is triggered.

| Pentose Bead Atoms                  | Nucleobase Bead Atoms                   | PO Bead Atoms     |
|-------------------------------------|-----------------------------------------|-------------------|
| O5', C5', O4', C4', O3', C3', O2', C2', C1', H5', H5'', H4', H3', H2', H2'', H2'2, H1', HO5', HO3', HO2', H5'1, H5'2, HO'2, H2'1, H5T, H3T. | N1, N2, N3, N4, N6, N7, N9, C2, C4, C5, C6, C7, C8, O2, O4, O6, H1, H2, H3, H5, H6, H8, H21, H22, H41, H42, H61, H62, H71, H72, H73. | P, OP1, OP2, OP3, O1P, O2P, O3P, HP, HOP3. |

##### [Back to hySAS home](NAVIGATION.md)
