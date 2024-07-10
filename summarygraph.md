
Browse the lessons
------------------------

The graph below shows a subset of the lessons that have been submitted to the PLUMED-TUTORIALS website and suggests an order for working through them. PLUMED-TUTORIAL monitors whether PLUMED input files in these lessons are compatible with the current and development versions of the code and integrates links from these files to the PLUMED manual.  Inputs in the tutorials listed below were last tested on {{ site.data.date.date }}.
   
   You can return to a complete list of the tutorials by clicking [here](browse.md).

```mermaid   
flowchart TD
0[Free energy calculations in
crystalline solids];
1[PLUMED syntax and analysis]
2[Metadynamics];
3[Rethinking Metadynamics using
the OPES method];
4[Modelling Concentration-driven
processes with PLUMED];
5[Machine learning collective
variables with PyTorch];
6[Analysis of Plumed output by
Metadynminer];
7[Dimensionality reduction];
8[Umbrella Sampling];
9[Statistical errors in MD];
10[SASA module - The solvent
accessible surface area of
proteins as a collective
variable, and the application
of PLUMED for implicit solvent
simulations];
11[Hamiltonian replica exchange
with PLUMED and GROMACS];
12[Replica exchange methods];
13[Optimizing PLUMED performances];
1-->0;
1-->4;
1-->5;
1-->7;
1-->8;
1-->9;
1-->10;
2-->3;
2-->6;
2-->12;
2-->13;
8-->2;
12-->11;
```
