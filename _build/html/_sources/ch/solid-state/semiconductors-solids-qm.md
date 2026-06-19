(semiconductors:solids-qm)=
# Introduction to the QM of Solids

(semiconductors:solids-qm:energy-bands)=
## Energy bands

First, the energy level splitting is discussed. Then, two models (Kronig-Penny, and nearly free electron models) are introduced to describe the concept of allowed and forbidden energy bands, starting from Schrodinger equation.

### Energy level splitting

This section deal with energy level splitting in a two-element system.


```{dropdown} Non-interacting systems

Let $| L \rangle$, and $| R \rangle$ two localized eigen-states of non-interacting identical subsystems, with the same energy $E_0$,

$$\begin{aligned}
  \hat{H}_0 | L \rangle & = E_0 | L \rangle  \\
  \hat{H}_0 | R \rangle & = E_0 | R \rangle  \\
\end{aligned}$$

As these states are localized in space, they're (approximately?) orthogonal, $\langle L | R \rangle = 0$.

```

```{dropdown} Interacting subsystems - Perturbation potential

When the two systems are brought close together, they start interacting weakly, so that the Hamiltonian becomes

$$\hat{H} = \hat{H}_0 + \hat{V} \ .$$

The matrix elements of the Hamiltonian in the base $\left\{ | L \rangle, | R \rangle \right\}$ (where are all the other eigen-functions? We're not interested in them, right now, but only on the pair of eigenfunctions with the same energy when the syb-systems are not interacting) read

$$\begin{aligned}
  \langle L | \hat{H} | L \rangle & =: E_0' \\
  \langle R | \hat{H} | R \rangle & =: E_0' \\
  \langle L | \hat{H} | R \rangle & = \langle R | \hat{H} | L \rangle^* =: -t \\
\end{aligned}$$

```

```{dropdown} Energy levels - Eigenvalues of the Hamiltonian operator 

If the new eigen-functions of the interacting system can be written as a linear combination of the non-interacting functions, $| \Psi_{1,2} \rangle= \ell_{1,2} | L \rangle + r_{1,2} | R \rangle$, the eigen-problem becomes

$$\hat{H} | \Psi_{1,2} \rangle = E_{1,2} | \Psi_{1,2} \rangle \ .$$

Projecting onto $\langle L |$, and $\langle R |$,

$$
\begin{cases}
     \ell E_0' - r t    = E \ell \\
   - \ell t    + r E_0' = E r    \\
\end{cases}
\quad \rightarrow \quad
\begin{cases}
     \ell (E_0'-E) - r t    = 0 \\
   - \ell t    + r (E_0'-E) = 0 \\
\end{cases}
$$

This system has non trivial solutions, if the determinant of the linear system is zero,

$$0 = \left| \begin{matrix} E_0' - E & -t \\ -t & E_0' - E \end{matrix}\right| = ( E_0' - E ) - t^2 \ . $$

The energy levels of the interacting states are slightly shifted w.r.t. the non-interacting level,

$$E = E_0' \mp t \ .$$

```

```{dropdown} Eigen-states

The eigen-states are

* the **bonding state**, for $E = E_0' - t$, $\ell = -r$, and with normalization

   $$| \Psi \rangle_{-} = \frac{1}{\sqrt{2}} \left( | L \rangle + | R \rangle \right) \ $$

* the **anti-bonding state**, for $E = E_0' + t$, $\ell = r$, and with normalization

   $$| \Psi \rangle_{+} = \frac{1}{\sqrt{2}} \left( | L \rangle - | R \rangle \right) \ $$

```

(semiconductors:solids-qm:energy-bands:kronig-penny)=
### Kronig-Penny model

```{dropdown} Kronig-Penny potential

Kronig-Penny model is a 1-dimensional model with periodic square wave potential, 

$$V(x) = \left\{\begin{aligned}
  V_0  \quad & , \quad x \in \text{regions II} = [ n a + (n-1) b, n ( a + b )]  \\
    0  \quad & , \quad x \in \text{regions I } = [ (n-1) (a+b), n a + (n-1) b] \\
\end{aligned}\right.$$

```

```{dropdown} General expression of Bloch states

Following [Bloch's theorem](solid-state:crystals:bloch-thm), the eigen-states of an electron (in position base) in a infinite periodic lattice can be written as

$$\Psi(\mathbf{r}) = u(\mathbf{r}) e^{i \mathbf{k} \cdot \mathbf{r}} \ ,$$

with $u(\mathbf{r}) = u \left(\mathbf{r} + \sum_j n_j \mathbf{a}_i \right)$ with the same periodicity as the lattice, $n_j \in \mathbb{Z}$, or in 1-dimensional problems,

$$\Psi(x) = u(x) e^{i k x} \ .$$

```

```{dropdown} Eigenvalue problem for the Hamiltonian operator

The eigenvalue problem for the Hamiltonian operator reads

$$E \Psi = \hat{H}  \Psi = \left[ \frac{\hat{p}^2}{2m} + V(x) \right] \Psi \ ,$$

with $\hat{p}$ the momentum operator, whose expression in position base is given by {eq}`eq:qm:momentum-operator`, and in 1-dimensional problems $\hat{p} \Psi = - i \hbar \partial_x \Psi$. The operator acting twice gives $\hat{p}^2 \Psi = - \hbar^2 \partial_{xx} \Psi$.

Introducing the expression of the eigenfunctions from Bloch's theorem[^bloch-state-derivatives], it follows

[^bloch-state-derivatives]: The derivatives read $\Psi' = \left( u' + i k u \right) e^{i k x}$, and $\Psi'' = \left( u'' + 2 ik u' - k^2 u \right) e^{ikx}$.

$$E u(x) = - \frac{\hbar^2}{2m} \left( u''(x) + 2 ik u'(x) - k^2 u(x)  \right) + V(x) u(x) \ ,$$

or

$$\begin{aligned}
  0 & = u'' + 2 i k u'(x) - \left( k^2 - \frac{2m E}{\hbar^2} \right) u(x) && \text{regions I} \\
  0 & = u'' + 2 i k u'(x) - \left( k^2 - \frac{2m ( E - V_0 )}{\hbar^2} \right) u(x) && \text{regions II} \\
\end{aligned}$$

**Solution of the ODEs.**

**Continuity of $\Psi(x)$, and $\partial_x \Psi(x)$.** for matching solutions.**

**Energy levels.**


```


(semiconductors:solids-qm:energy-bands:nearly-free-electron)=
### Nearly free electron model


