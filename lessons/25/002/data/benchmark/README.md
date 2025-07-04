# bAIes-SM benchmark
## Data to reproduce the bAIes benchmark

Details about the systems used in our benchmark are
reported in the table below. Instructions to install [GROMACS](https://www.gromacs.org) and [PLUMED](https://www.plumed.org)
as well as a tutorial on preparing the bAIes model for one of these systems can be found [here](https://github.com/COSBlab/bAIes-SM).

**Benchmark systems for structural accuracy and ligand docking accuracy**
| ID | PDB | # Protein<br>residues | # protein<br>chains | # lipids | Ligand | AF<br>pLDDT | Resolution<br>[Å] | 
|:--:|:---:| :-------------------: | :-----------------: | :------: | :----: | :---------: | :---------------: |
| 01 | 1D3G |        367            |         1          |    0     |  BRE   |     97      |       1.6        |
| 02 | 2AM9 |        266            |         1          |    0     |  TES   |     99      |       1.6        |
| 03 | 1UDT |        324            |         1          |    0     |  VIA   |     95      |       2.3        |
| 04 | 1SQT |        245            |         1          |    0     |  UI3   |     98      |       1.9        |
| 05 | 2NNQ |        131            |         1          |    0     |  T4B   |     98      |       1.8        |
| 06 | 2ICA |        183            |         1          |    0     |  2IC   |     96      |       1.6        |
| 07 | 1UYG |        236            |         1          |    0     |  PU2   |     96      |       2.0        |
| 08 | 4LDO |        589            |         1          |    316   |  ALE   |     98      |       3.2        |
| 09 | 3KBA |        506            |         2          |    0     |  WOW   |     88      |       3.2        |
| 10 | 3BGS |        289            |         1          |    0     |  DIH   |     97      |       2.1        |
| 11 | 3G6Z |        682            |         2          |    0     |  A7T   |     89      |       2.0        |
| 12 | 3PBL |        962            |         2          |    935   |  ETQ   |     85      |       2.8        |
| 13 | 2UZ3 |        972            |         4          |    0     |  TTP   |     96      |       2.5        |
| 14 | 3F9M |        470            |         1          |    0     |  MRK   |     92      |       1.5        |
| 15 | 3ERD |        548            |         4          |    0     |  DES   |     98      |       2.0        |


**Benchmark systems for virtual screening of large libraries**
| ID | PDB  | # Protein<br>residues | # protein<br>chains | # active ligands | # decoys |
|:--:|:---: | :-------------------: | :-----------------: | :--------------: | :------: |
| 01 | 3ERD |        548            |         4           |    391           | 21642    | 
| 02 | 3BGS |        289            |         1           |    233           | 7016     |
| 03 | 1H00 |        299            |         1           |    798           | 28329    |


**Contact**

For any technical questions, please write to mbonomi_at_pasteur.fr.
