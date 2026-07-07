(semiconductors:equilibrium)=
# Semiconductors in Equilibrium

(semiconductors:equilibrium:structure)=
## Structure of a semi-semiconductor


| Symbol | Concentration of |
| :----: | :------ |
| $p$     | Holes in the valence bands of $Si$-atom lattice |
| $n$     | Free electrons in the conduction band           | 
| $N_A$   | Acceptor atoms, usually class $\text{III}$      |
| $N_D$   | Donor atoms, usually class $\text{V}$           |
| $N_A^-$ | Ionized acceptor atoms, having collected $e^-$ (usually from neighboring $Si$ atoms)  |
| $N_D^+$ | Ionized donor atoms, having released $e^-$      |

Usually, $N_A$, $N_D$, $N_A^-$, $N_D^+$ only depends on the space coordinate, as a consequencen of doping. The concentration of free electrons and holes may be time dependent instead (...).

(semiconductors:equilibrium:structure:intrinsic)=
### Intrinsic semiconductor

Lattice of $\text{Si}$ atoms. Some free electrons have left the valence bands of the atoms and entered the conduction band. For a new free electron, a new hole is left behind in the lattice. If the medium is **electrically neutral** the numbers of free electrons and holes are locally equal, and thus their concentrations

$$n_i(\mathbf{r}) = p_i(\mathbf{r}) \ .$$

(semiconductors:equilibrium:structure:doped)=
### Doped semiconductors

(semiconductors:equilibrium:structure:doped:p-type)=
#### $p$-type

The semiconductor is doped with atoms of class $\text{III}$, replacing some of the $\text{Si}$ atoms in the lattice. These atoms introduce a hole in the lattice and are prone to collect $e^-$ from neighboring $\text{Si}$ atoms.

Under [full-ionization condition](semiconductors:equilibrium:structure:doped:full-ionization), all the doping atoms are ionized, and thus $N_A^- = N_A$. In a **electrically netural** region with no donor atoms, the concentration of the holes is equal to the sum of the concentration of the ionized acceptor atoms and the free electrons,

$$p = n + N_A^- \ .$$

In a standard $p$-type semiconductor, $N_A >> n_i$, and thus $p \sim N_A^-$.

(semiconductors:equilibrium:structure:doped:n-type)=
#### $n$-type

The semiconductor is doped with atoms of class $\text{V}$, replacing some of the $\text{Si}$ atoms in the lattice. These atoms introduce a "extra" loosely bound electron in the lattice and are prone to release it in the conduction band of the semiconductor.

Under [full-ionization condition](semiconductors:equilibrium:structure:doped:full-ionization), all the doping atoms are ionized, and thus $N_D^+ = N_D$. In a **electrically netural** region with no acceptor atoms, the concentration of the free electrons is equal to the sum of the concentration of the ionized donor atoms and holes,

$$n = p + N_D^+ \ .$$

In a standard $n$-type semiconductor, $N_D >> p_i$, and thus $n \sim N_D^+$.

(semiconductors:equilibrium:structure:doped:full-ionization)=
#### Full ionization

**todo**

(semiconductors:equilibrium:charge-density)=
## Electric charge density

$$\rho(\mathbf{r},t) = -q n(\mathbf{r},t) + q p(\mathbf{r},t) + q N_D^+(\mathbf{r},t) - q N_A^-(\mathbf{r},t) \ ,$$ (eq:semi:charge-density)

being

* $q$ the elementary charge, the charge of the electron (here the opposite to get a positive numerical value of $q$ in Coulomb)
* $n(\mathbf{r},t)$ the number volume density of the mobile electrons
* $p(\mathbf{r},t)$ the number volume density of the holes in the valence bands of the lattice
* $N_D^+(\mathbf{r},t)$ the number volume density of the positive donor ions
* $N_A^-(\mathbf{r},t)$ the number volume density of the negative acceptor ions

Usually, $N_D^+(\mathbf{r})$, $N_A^-(\mathbf{r})$, corresponding to the density of the donor and acceptor atoms in the lattice, that have fixed positions.

**Remark.** **todo** *Discuss the values of $N_D^+$ and $N_D$ in terms of energy levels at different temperatures.* Add this discussion to [full-ionization section](semiconductors:equilibrium:structure:doped:full-ionization) or in another section and then point to it?

