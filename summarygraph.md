
   Browse the lessons
   ------------------------

   The graph below shows a subset of the lessons that have been submitted to the PLUMED-TUTORIALS website and suggests an order for working through them.
   PLUMED-TUTORIAL monitors whether PLUMED input files in these lessons are compatible with the current and development
   versions of the code and integrates links from these files to the PLUMED manual.  Inputs in the tutorials listed below were last tested on {{ site.data.date.date }}.
   
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
7[Dimensionality reduction]
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
click 0 "lessons/22/012/data/NAVIGATION.html" "**Authors: Pablo Piaggi** An introduction to the Environmental similarity CV and the calculation of chemical potentials of liquids and solids"
click 1 "lessons/21/001/data/NAVIGATION.html" "**Authors: Max Bonomi** Basic features of the PLUMED input syntax with a particular focus on PBCs and selection tools"
click 2 "lessons/21/004/data/NAVIGATION.html" "**Authors: Max Bonomi** How to calculate statistical averages and free energy surfaces using metadynamics"
click 3 "lessons/22/003/data/NAVIGATION.html" "**Authors: Michele Invernizzi** An introduction to the On-the-fly Probability Enhanced Sampling method"
click 4 "lessons/22/008/data/NAVIGATION.html" "**Authors: Matteo Salvalaglio** An introduction to the tools that are available in PLUMED for simulating concentration-driven processes such as nucleation, growth and diffusion."
click 5 "lessons/22/005/data/NAVIGATION.html" "**Authors: Luigi Bonati** An introduction to designing data-driven CVs using two methods (DeepLDA and DeepTICA)."
click 6 "lessons/22/002/data/NAVIGATION.html" "**Authors: Vojtech Spiwok** An introduction to the R package Metadynminer which can be used to analyse the output from metadynamics simulatiosn"
click 7 "lessons/21/006/data/NAVIGATION.html" "**Authors: Gareth Tribello** An introduction to tehcniques such as dimensionality reduction, path collective variables and indistinguishablity that you may need to use in your own research projects"
click 8 "lessons/21/003/data/NAVIGATION.html" "**Authors: Giovanni Bussi** How to calculate statistical averages and free energy surfaces using umbrella sampling"
click 9 "lessons/21/002/data/NAVIGATION.html" "**Authors: Gareth Tribello** How to calculate errors on averages calculated from unbiased and biased MD simulations using the method of block averages."
click 10 "lessons/22/013/data/NAVIGATION.html" "**Authors: Andrea Arsiccio** An introduction to the SASA module and a description of how PLUMED can be used for implicit solvent simulations."
click 11 "lessons/22/010/data/NAVIGATION.html" "**Authors: Giovanni Bussi** An introduction to running Hamiltonian replica exchange calculations using PLUMED and GROMACS."
click 12 "lessons/21/005/data/NAVIGATION.html" "**Authors: Giovanni Bussi** Runninge umbrella sampling with replica exchange, bias exchange metadynamics and parallel tempering metadynamics"
click 13 "lessons/21/007/data/NAVIGATION.html" "**Authors: Max Bonomi** Some lessons on monitoring and improving the performance of PLUMED and gromacs"
```
