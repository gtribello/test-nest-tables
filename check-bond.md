Adjacency matrix in which two atoms are adjacent if there is a hydrogen bond between them.

A useful tool for developing complex collective variables is the notion of the
so called adjacency matrix.  An adjacency matrix is an $N \times N$ matrix in which the $i$th, $j$th element tells you whether
or not the $i$th and $j$th atoms/molecules from a set of $N$ atoms/molecules are adjacent or not.  As detailed in the documentation
for CONTACT_MATRIX there are then a range of further analyses that you can perform on these matrices.  

For this action the elements of the adjacency matrix are calculated using:

$$
a_{ij} = \sigma_{oo}( r_{ij} ) \sum_{k=1}^N \sigma_{oh}( r_{ik} ) \sigma_{\theta}( \theta_{kij} )
$$

This expression was derived by thinking about how to detect if there is a hydrogen bond between atoms $i$ and $j$.  The notion is that
if the hydrogen bond is present atoms $i$ and $j$ should be within a certain cutoff distance.  In addition, there should be a hydrogen
within a certain cutoff distance of atom $i$ and this hydrogen should lie on or close to the vector connecting atoms $i$ and $j$.
As such $\sigma_{oo}(r_{ij})$ is a switching function that acts on the modulus of the vector connecting atom $i$ to atom
$j$.  The sum over $k$ then runs over all the hydrogen atoms that are specified using using HYDROGEN keyword.  $\sigma_{oh}(r_{ik})$
is a switching function that acts on the modulus of the vector connecting atom $i$ to atom $k$ and $\sigma_{\theta}(\theta_{kij})$
is a switching function that acts on the angle between the vector connecting atoms $i$ and $j$ and the vector connecting atoms $i$ and
$k$.

It is important to note that hydrogen bonds, unlike regular bonds, are asymmetric. In other words, the hydrogen atom does not sit at the
mid point between the two other atoms in this three-center bond.  As a result of this adjacency matrices calculated using HBOND_MATRIX are not
symmetric like those calculated by CONTACT_MATRIX.  

The following input can be used to analyze the number of hydrogen bonds each of the oxygen atoms in a box of water participates in.  Each
water molecule can participate in a hydrogen bond in one of two ways.  It can either donate one of its hydrogen atom to the neighboring oxygen or
it can accept a bond between the hydrogen of a neighboring water molecule and its own oxygen.  The input below allows you to output information
on the number of hydrogen bonds each of the water molecules donates and accepts.  This information is output in two xyz files which each contain
five columns of data.  The first four of these columns are a label for the atom and the x, y and z position of the oxygen.  The last column is then
the number of accepted/donated hydrogen bonds.

```plumed
mat: HBOND_MATRIX ATOMS=1-192:3 HYDROGENS=2-192:3,3-192:3 SWITCH={RATIONAL R_0=3.20} HSWITCH={RATIONAL R_0=2.30} ASWITCH={RATIONAL R_0=0.167pi}
ones: ONES SIZE=64
rsums: MATRIX_VECTOR_PRODUCT ARG=mat,ones 
DUMPATOMS ATOMS=1-192:3 ARG=rsums FILE=donors.xyz
```

An equation

$$
\rho_{ij} = \max_{m \in M} \left[ \frac{M}{d_\textrm{max}} \right] \sum_k f(r_{ik}, r_{ij})
$$

$$
  \int_{(m-1)d_{\textrm{max}}/M}^{ md_{\textrm{max}} /M } \textrm{d}x K\left( x - \mathbf{r}_{ks} \cdot \mathbf{r}_{ij}} / | \mathbf{r}_{ks} | \right) 
$$
