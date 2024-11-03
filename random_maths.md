$$
d(X,X') = \sqrt{ \sum_i \sum_\alpha^{x,y,z}  \frac{w_i}{\sum_j w_j} ( X _{i,\alpha}-com _\alpha(X)-{X'} _{i,\alpha}+com _\alpha(X') )^2 }
$$

with

$$
com_\alpha (X) = \sum_i \frac{w'_{i}}{\sum_j w'_j} X _{i,\alpha}
$$

and

$$
com_\alpha(X')= \sum_i  \frac{w'_{i}}{\sum_j w'_j}X' _{i,\alpha}
$$

$$
\begin{align}
X & = \frac{\sum_i X_i*\exp(-\lambda D_i(x))}{\sum_i  \exp(-\lambda D_i(x))} \\
Y & = \frac{\sum_i Y_i*\exp(-\lambda D_i(x))}{\sum_i  \exp(-\lambda D_i(x))} \\
& \cdots\\
zzz & =-\frac{1}{\lambda}\log(\sum_i  \exp(-\lambda D_i(x)))
\end{align}
$$ 

$$
\AA
$$

EEF1 is a solvent-accessible surface area based model, where the free energy of solvation is computed using a pairwise interaction term for non-hydrogen atoms:

$$
    \Delta G^\mathrm{solv}_i = \Delta G^\mathrm{ref}_i - \sum_{j \neq i} f_i(r_{ij}) V_j
$$

where $\Delta G^\mathrm{solv}_i$ is the free energy of solvation, $\Delta G^\mathrm{ref}_i$ is the reference solvation free energy, $V_j$ is the volume of atom $j$ and

$$
    f_i(r) 4\pi r^2 = \frac{2}{\sqrt{\pi}} \frac{\Delta G^\mathrm{free}_i}{\lambda_i} \exp\left\{ - \frac{(r-R_i)^2}{\lambda^2_i}\right\}
$$

where $\Delta G^\mathrm{free}_i$ is the solvation free energy of the isolated group, $\lambda_i$ is the correlation length equal to the width of the first solvation shell and $R_i$ is the van der Waals radius of atom $i$.


