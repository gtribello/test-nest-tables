# Action: DUMPCONTOUR
| Description    | Usage |
|:--------:|:--------:|
| Print the contour | ![used in 0 tutorials](https://img.shields.io/badge/tutorials-0-red.svg)![used in 0 eggs](https://img.shields.io/badge/nest-0-red.svg)| 
## Further details and examples 
Information for the manual from the code would go in here 
## Syntax 

The following arguments are compulsory: 

                 STRIDE - ( default=1 ) the frequency with which the grid should be 
                          output to the file. 
                   FILE - ( default=density ) the file on which to write the grid. 
                    ARG - the input for this action is the scalar output from one or 
                          more other actions. The particular scalars that you will use are 
                          referenced using the label of the action. If the label appears on its 
                          own then it is assumed that the Action calculates a single 
                          scalar value. The value of this scalar is thus used as the input 
                          to this new action. If * or *.* appears the scalars calculated 
                          by all the proceeding actions in the input file are taken. 
                          Some actions have multi-component outputs and each component of 
                          the output has a specific label. For example a ef DISTANCE 
                          action labelled dist may have three components x, y and z. To take 
                          just the x component you should use dist.x, if you wish to take 
                          all three components then use dist.*.More information on the 
                          referencing of Actions can be found in the section of the manual on the 
                          PLUMED ef Syntax. Scalar values can also be referenced using 
                          POSIX regular expressions as detailed in the section on ef 
                          Regex. To use this feature you you must compile PLUMED with the 
                          appropriate flag.. You can use multiple instances of this keyword i.e. 
                          ARG1, ARG2, ARG3... 
                    FMT - the format that should be used to output real numbers 

