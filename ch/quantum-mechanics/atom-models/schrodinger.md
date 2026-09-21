(quantum-mechanics:atom-models:schrodinger)=
# Schrodinger model

```{dropdown} Contents
:open:

* [Mathematical details of the analytical solution](quantum-mechanics:atom-models:schrodinger:analytical-sln)
* [Gallery of orbitals](quantum-mechanics:atom-models:schrodinger:gallery)

```

**Schrodinger equation.** Schrodinger equation in space basis for the electron in a $\text{H}$ atom reads

$$i \hbar \partial_t \Psi(\mathbf{r},t) = \left[ -\frac{\hbar^2}{2m} \nabla^2 - \frac{q^2}{4 \pi \varepsilon}\frac{1}{|\mathbf{r}|} \right] \Psi(\mathbf{r},t) \ $$

where the Hamiltonian is the sum of the kinetic energy and a Coulomb potential contribution, $\hat{V}$, so that $\langle \mathbf{r} | \hat{V} | \Psi \rangle = - \frac{q^2}{4 \pi \varepsilon |\mathbf{r}|} \Psi(\mathbf{r},t)$

**Spectral decomposition of the Hamiltonian operator.** The stationary states, and the corresponding energy levels - i.e. the eigenfunctions, and the eigenvalues of the Hamiltonian operator $\hat{H}$ - are the result of the eigenvalue problem, $\hat{H} | \Psi \rangle = E | \Psi \rangle$, or using space basis,

$$\left[ -\frac{\hbar^2}{2m} \nabla^2 - \frac{q^2}{4 \pi \varepsilon}\frac{1}{|\mathbf{r}|} \right] \Psi(\mathbf{r}) = E \Psi(\mathbf{r}) \ .$$

**Quantum numbers.** The stationary states depend on **three** - in this model, no spin exists - **quantum numbers**:
* **principal** quantum number $n \in \{ 1, 2, \dots \}$ 
* **azimuthal** quantum number $\ell \in \{ 0, 1,\dots, n-1 \} $
* **magnetic** quantum number $m_{\ell} \in \{ -\ell, -\ell+1, \dots, \ell \}$

Energy levels only depend on the principal quantum number, $E(n)$. Thus, Schrodinger model of the atom has **degenerate** stationary states, i.e. stationary states with the same energy value.

**Commutation of $\hat{H}$, $\hat{L}^2$, $\hat{L}_z$.** As angular momentum operators $\hat{L}^2$, $\hat{L}_z$ commute with the Hamiltonian operator $\hat{H}$ of the $\text{H}$ atom, these three operators share common eigenvectors.

**todo** *add the proof - already there in hand-written notes*
