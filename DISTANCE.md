# Action: DISTANCE

| Description    | Usage |
|:--------:|:--------:|
| Calculate the distance between a pair of atoms. | [![used in 4 tutorials](https://img.shields.io/badge/tutorials-4-green.svg)](https://plumed-school.github.io/browse.html?search=DISTANCE)[![used in 121 eggs](https://img.shields.io/badge/nest-121-green.svg)](https://www.plumed-nest.org/browse.html?search=DISTANCE)|

## Further details and examples 
Information for the manual from the code would go in here
## Syntax 
The input trajectory can be in any of the following formats:

                  ATOMS - the pair of atom that we are calculating the distance
                          between. For more information on how to specify lists of atoms see
                          ^Mef Group

The following options are available

  NUMERICAL_DERIVATIVES - ( default=off ) calculate the derivatives for these
                          quantities numerically
                  NOPBC - ( default=off ) ignore the periodic boundary conditions
                          when calculating distances
             COMPONENTS - ( default=off ) calculate the x, y and z components of the
                          distance separately and store them as label.x, label.y and label.z
      SCALED_COMPONENTS - ( default=off ) calculate the a, b and c scaled components
                          of the distance separately and store them as label.a, label.b
                          and label.c
