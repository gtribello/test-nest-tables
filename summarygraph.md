
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

Another graph

```mermaid
flowchart TB;
  A[Lecture I] ==> B[Instructions];
  A -.-> C[using pandas];
  B ==> D[Lecture II];
  C -.-> D;
  D --> E[solution];
  click A "video1.html" "A lecture that was given on January 18th 2021 as part of the plumed masterclass series that introduces you to the exercises in this lesson"
  click B "INSTRUCTIONS.html" "The instructions for the exercises"
  click C "notebooks/plumed-pandas.html" "A python notebook file that illustrates how you can use pandas to read in COLVAR files that are generated with PLUMED"
  click D "video2.html" "A lecture that was given on January 25th 2021 as part of the plumed masterclass series that goes through the solutions to the exercises in the lesson"
  click E "notebooks/solution.html" "A python notebook file that provides a complete set of solutions to the exercises"
```
