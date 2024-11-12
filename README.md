# This is the main page

The date is {{ site.data.date.date }}

Lets go [browse](browse.md)

Lets go [table](table.md)

Lets go [bussi](https://gtribello.github.io/test-nest-tables/browse.html?search=bussi)

Lets go [DISTANCE](DISTANCE.md)

Lets go [DUMPCONTOUR](DUMCONTOUR.md)

Lets go [graph](summarygraph.md)

Lets go [new graph](test-graph-width.md)

Lets go [timings](timings.md)

Lets go [hbond](check-bond.md)

<img src="https://img.shields.io/badge/v2.9-fail 0%25-green.svg" alt="tested on v2.9" />

<img src="https://img.shields.io/badge/v2.9-failed-red.svg" alt="tested on v2.9" />

$\vert a - b \vert$ 

| TYPE | FUNCTION | EXAMPLE INPUT | DEFAULT PARAMETERS | NOTES
|:----:|:--------:|:-------------:|:------------------:|:------------------:|
| RATIONAL |  $s(r)=\frac{1-\left(\frac{r- d_0}{r_0}\right)^{n}}{1-\left(\frac{r-d_0}{r_0}\right)^{m}}$ | \{RATIONAL R_0=$r_0$ D_0=$d_0$ NN=$n$ MM=$m$\} | $d_0=0.0$, $n=6$, $m=2n$ | This is the most commonly used function and is highly optimised |
| EXP | $s(r)=\exp\left(-\frac{ r - d_0 }{ r_0 }\right)$ | {EXP  R_0=$r_0$ D_0=$d_0$} | $d_0=0.0$ | |
| GAUSSIAN | $s(r)=\exp\left(-\frac{ (r - d_0)^2 }{ 2r_0^2 }\right)$ | {GAUSSIAN R_0=$r_0$ D_0=$d_0$} | $d_0=0.0f$ | |
| SMAP | $s(r) = \left[ 1 + ( 2^{a/b} -1 )\left( \frac{r-d_0}{r_0} \right)^a \right]^{-b/a}$ | {SMAP R_0=$r_0$ D_0=$d_0$ A=$a$ B=$b$} | $d_0=0.0$ | |
| Q | $s(r) = \frac{1}{1 + \exp(\beta(r_{ij} - \lambda r_{ij}^0))}$ | {Q REF=$r_{ij}^0$ BETA=$\beta$ LAMBDA=$\lambda$ } | $\lambda=1.8$, $\beta=50 nm^-1$ | You should use the default parameters here for all atom models  For a coarse grained model use $\lambda=1.5$, $\beta=50 nm^-1$ instead. }
| CUBIC | $s(r) = (y-1)^2(1+2y) \qquad \textrm{where} \quad y = \frac{r - r_1}{r_0-r_1}$ | {CUBIC D_0=$r_1$ D_MAX=$r_0$} | $d_0=0$ | |
| TANH | $s(r) = 1 - \tanh\left( \frac{ r - d_0 }{ r_0 } \right)$ | {TANH R_0=$r_0$ D_0=$d_0$} | $d_0=0$ | |
| CUSTOM | $s(r) = FUNC$ | {CUSTOM FUNC=1/(1+x^6) R_0=$r_0$ D_0=$d_0$} | $d_0=0$ | The input to the FUNC keyword can be written in terms of x or x2=$x^2$. Using x2 allows you to avoid the computationally-expensive square root operation. |
| MATHEVAL | $s(r) = FUNC$ | {CUSTOM FUNC=1/(1+x^6) R_0=$r_0$ D_0=$d_0$} | $d_0=0$ | This is equivalent to CUSTOM above and is included to ensure backwards compatibility |
