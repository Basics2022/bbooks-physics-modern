(quantum-mechanics:atom-models:schrodinger:notes)=
# Auxiliary Results on Operators for the Schrödinger Model of the Hydrogen Atom

1. All components of $\hat{\mathbf{L}}$ commute with the kinetic term $\frac{\hat{p}^2}{2m}$ and with $\hat{L}^2$, [proof](quantum-mechanics:atom-models:schrodinger:notes:commutation:L-p2)

   $$[\hat{p}^2, \hat{L}_b] = 0$$

2. All components of $\hat{\mathbf{L}}$ commute with the potential $\hat{V}_{\text{Coulomb}}$, [proof](quantum-mechanics:atom-models:schrodinger:notes:commutation:L-V)

   $$[\hat{V}_{\text{Coulomb}}, \hat{L}_b] = 0$$

3. Therefore, all components of $\hat{\mathbf{L}}$ commute with the $\text{H}$ atom Hamiltonian $\hat{H}_{\text{H-atom}} = \frac{\hat{p}^2}{2m} + \hat{V}_{\text{Coulomb}}$:

   $$[\hat{H}_{\text{H-atom}}, \hat{L}_b] = 0$$

4. Simultaneous Commutative Set:

   $$\boxed{[\hat{H}_{\text{H-atom}}, \hat{L}^2] = 0, \quad [\hat{H}_{\text{H-atom}}, \hat{L}_a] = 0, \quad [\hat{L}^2, \hat{L}_a] = 0}$$

   i.e. the Hamiltonian $\hat{H}_{\text{H-atom}}$, total angular momentum squared $\hat{L}^2$, and any component $\hat{L}_a$ all mutually commute, and thus share a set of common eigenvectors. For the commutation relation $[\hat{L}^2, \hat{L}_a] = 0$, see the section about [spatial angular momentum](quantum-mechanics:angular-momentum:spatial).



## Hamiltonian & Basic Definitions

The Hamiltonian of the electron in the Hydrogen atom with Coulomb potential is given by

$$\hat{H} = \frac{\hat{p}^2}{2m} + \hat{V}_{Coulomb} \ ,$$

that in space basis becomes

$$\langle \mathbf{r} | \hat{H} = - \frac{\hbar^2}{2 m} \nabla^2 \langle \mathbf{r} | - \frac{q^2}{4 \pi \varepsilon |\mathbf{r}|} \langle \mathbf{r} | \ .$$

```{dropdown} Space Basis Representations
:open:

$$\langle \mathbf{r} | \Psi \rangle = \Psi(\mathbf{r}, t)$$

$$\langle \mathbf{r} | \hat{\mathbf{r}} = \mathbf{r} \langle \mathbf{r} | \quad \implies \quad \langle \mathbf{r} | \hat{\mathbf{r}} | \Psi \rangle = \mathbf{r} \, \Psi(\mathbf{r}, t)$$

$$\langle \mathbf{r} | \hat{\mathbf{p}} = -i\hbar \nabla_{\mathbf{r}} \langle \mathbf{r} | \quad \implies \quad \langle \mathbf{r} | \hat{\mathbf{p}} | \Psi \rangle = -i\hbar \nabla \Psi(\mathbf{r}, t)$$

```

```{dropdown} Angular Momentum Operator
:open:

$$\hat{\mathbf{L}} = \hat{\mathbf{r}} \times \hat{\mathbf{p}}$$

In Levi-Civita component notation, using Cartesian coordinates

$$\hat{\mathbf{L}} = \hat{\mathbf{e}}_a \hat{L}_a =  \hat{\mathbf{e}}_a \varepsilon_{abc} \, \hat{r}_b \hat{p}_c$$

In the space (position) basis (Cartesian coordinates):

$$\begin{aligned}
  \langle \mathbf{r} | \hat{\mathbf{L}} | \Psi \rangle 
  & = \langle \mathbf{r} | \hat{\mathbf{e}}_a \hat{L}_a | \Psi \rangle = \\
  & = \hat{\mathbf{e}}_a \varepsilon_{abc} \, r_b (-i\hbar \partial_c \langle \mathbf{r} | \Psi \rangle) = \\
  & =-i\hbar \hat{\mathbf{e}}_a \varepsilon_{abc} \, r_b \, \partial_c \Psi(\mathbf{r},t) = \\
  & = - i \hbar \mathbf{r} \times \nabla_{\mathbf{r}} \Psi(\mathbf{r},t) \ .
\end{aligned}$$

```

```{dropdown} $\langle \mathbf{r} | \hat{\mathbf{p}} | \Psi \rangle$
:open:

$$\langle \mathbf{r} | \hat{\mathbf{p}} | \Psi \rangle = \int \langle \mathbf{r} | \hat{\mathbf{p}} | \mathbf{r}' \rangle \langle \mathbf{r}' | \Psi \rangle \, d\mathbf{r}' = \int \delta(\mathbf{r} - \mathbf{r}') \left(-i\hbar \nabla_{\mathbf{r}'} \Psi(\mathbf{r}', t)\right) d\mathbf{r}' = -i\hbar \nabla_{\mathbf{r}} \Psi(\mathbf{r}, t)$$

```

```{dropdown} $\langle \mathbf{r} | \hat{p}_b \hat{r}_a | \Psi \rangle$
:open:

$$\langle \mathbf{r} | \hat{p}_b \hat{r}_a | \Psi \rangle = -i\hbar \partial_b \langle \mathbf{r} | \hat{r}_a | \Psi \rangle  = -i\hbar \partial_b \left( r_a \langle \mathbf{r} | \Psi \rangle \right) = - i \hbar \partial_b \left( r_a \Psi(\mathbf{r},t) \right) = -i\hbar (\delta_{ab} \Psi + r_a \partial_b \Psi)$$

```

## Canonical Commutation Relations (CCR)

Using postion basis and Cartesian coordinates, the CCR $[ \hat{\mathbf{r}}, \hat{\mathbf{P}} ] = i \hbar \mathbb{I}$ reads

$$[r_a, p_b] \Psi = r_a (-i\hbar \partial_b \Psi) - (-i\hbar \partial_b (r_a \Psi)) = i\hbar \, \delta_{ab} \Psi \ ,$$

i.e.

$$[r_a, p_b] = i\hbar \, \delta_{ab}$$


## Commutators of Angular Momentum with Position and Momentum

### Commutator $[r_a, L_b]$

$$r_a L_b \Psi = r_a (-i\hbar \varepsilon_{bcd} \, r_c \partial_d \Psi) = -i\hbar \varepsilon_{bcd} \, r_a r_c \partial_d \Psi$$

$$L_b r_a \Psi = -i\hbar \varepsilon_{bcd} \, r_c \partial_d (r_a \Psi) = -i\hbar \varepsilon_{bcd} \, r_c \delta_{ad} \Psi - i\hbar \varepsilon_{bcd} \, r_c r_a \partial_d \Psi$$

Subtracting the two expressions gives:

$$[r_a, L_b] \Psi = i\hbar \varepsilon_{bcd} \, r_c \delta_{ad} \Psi = i\hbar \varepsilon_{bca} \, r_c \Psi \ ,$$

and thus

$$[r_a, L_b] =-  i \hbar \, (\mathbf{r} \times)_{a b} \, \Psi \quad \left(\text{in general } \neq 0\right)$$

*(Recall: $(\mathbf{a} \times \mathbf{b})_i = \varepsilon_{ijk} a_j b_k = \{ \mathbf{a}_{\times} \}_{ik} \cdot \{ \mathbf{b} \}_k$, i.e. $\{ \mathbf{a}_{\times} \}_{ik} = \varepsilon_{ijk} a_j$)*


### Commutator $[p_a, L_b]$

$$p_a L_b \Psi = -i\hbar \partial_a \left(-i\hbar \varepsilon_{bcd} \, r_c \partial_d \Psi\right) = -\hbar^2 \varepsilon_{bcd} \, \partial_a (r_c \partial_d \Psi) = -\hbar^2 \varepsilon_{bad} \, \partial_d \Psi - \hbar^2 \varepsilon_{bcd} \, r_c \partial_a \partial_d \Psi$$

$$L_b p_a \Psi = -i\hbar \varepsilon_{bcd} \, r_c \partial_d (-i\hbar \partial_a \Psi) = -\hbar^2 \varepsilon_{bcd} \, r_c \partial_d \partial_a \Psi$$

Subtracting the two expressions gives:

$$[p_a, L_b] \Psi = -\hbar^2 \varepsilon_{bad} \, \partial_d \Psi = \hbar^2 \varepsilon_{abd} \, \partial_d \Psi = i\hbar \varepsilon_{abc} \, p_c \Psi$$

**Cartesian coordinates.**
- $[p_x, L_x] \equiv 0$
- $[p_x, L_y] = \hbar^2 \varepsilon_{xyz} \, \partial_z \Psi = i\hbar p_z$
- $[p_x, L_z] = \hbar^2 \varepsilon_{xzy} \, \partial_y \Psi = -\hbar^2 \partial_y \Psi = -i\hbar p_y$

---

(quantum-mechanics:atom-models:schrodinger:notes:commutation:L-p2)=
### Commutator $[\hat{p}^2, L_b]$


$$[p^2, L_b] = \sum_a p_a p_a L_b - L_b \sum_a p_a p_a = \sum_a \Big( p_a [p_a, L_b] + [p_a, L_b] p_a \Big)$$

Using $[p_a, L_b] = i\hbar \varepsilon_{abc} p_c$:

$$\sum_a \left( p_a (i\hbar \varepsilon_{abc} p_c) + (i\hbar \varepsilon_{abc} p_c) p_a \right) = i\hbar \varepsilon_{abc} (p_a p_c + p_c p_a)$$

Since $p_a p_c = p_c p_a$ (symmetric in $a, c$) and $\varepsilon_{abc}$ is antisymmetric in $a, c$, the sum vanishes identically:

$$[p^2, L_b] = 0 \quad \text{for all components } b$$

**Example.** For $b = x$:

$$[p^2, L_x] = -i\hbar^3 \Big[ 1 \cdot \partial_z \partial_y \Psi - 1 \cdot \partial_y \partial_z \Psi \Big] = 0$$

(quantum-mechanics:atom-models:schrodinger:notes:commutation:L-V)=
## Commutator of Coulomb Potential $\hat{V}$ with Angular Momentum $\hat{L}_b$

In space basis, the Coulomb potential reads:

$$\langle \mathbf{r} | \hat{V} | \Psi \rangle = -\frac{q^2}{4\pi\varepsilon_0} \frac{1}{r} \Psi(\mathbf{r}, t) = -k \frac{1}{|\mathbf{r}|} \Psi(\mathbf{r}, t)$$

Let's evaluate whether $\hat{V}$ and $\hat{L}_b$ commute:

1. **Action of $\hat{V} \hat{L}_b$:**

   $$\langle \mathbf{r} | \hat{V} \hat{L}_b | \Psi \rangle = -k \frac{1}{\sqrt{x_a x_a}} \left( -i\hbar \varepsilon_{bcd} \, r_c \, \partial_d \Psi \right)$$

2. **Action of $\hat{L}_b \hat{V}$, with $|\mathbf{r}| = \sqrt{ x_a x_a }$:**
   
   $$\langle \mathbf{r} | \hat{L}_b \hat{V} | \Psi \rangle = -i\hbar \varepsilon_{bcd} \, r_c \, \partial_d \left( -k \frac{\Psi}{\sqrt{x_a x_a}} \right) = i\hbar k \varepsilon_{bcd} \, r_c \left[ -\frac{\partial_d |\mathbf{r}|}{|\mathbf{r}|^2} \Psi + \frac{1}{|\mathbf{r}|} \partial_d \Psi \right]$$

   Since $\partial_d | \mathbf{r}| = \partial_d \sqrt{x_a x_a} = \frac{x_d}{|\mathbf{r}|}$:

   $$\langle \mathbf{r} | \hat{L}_b \hat{V} | \Psi \rangle = i\hbar k \varepsilon_{bcd} \, r_c \left[ -\frac{r_d}{|\mathbf{r}|^3} \Psi + \frac{1}{|\mathbf{r}|} \partial_d \Psi \right]$$

3. **Commutator $[\hat{V}, \hat{L}_b]$:**

   $$\langle \mathbf{r} | [\hat{V}, \hat{L}_b] | \Psi \rangle = -i\hbar k \, \frac{\varepsilon_{bcd} \, r_c r_d}{|\mathbf{r}|^3} \Psi = 0$$

   *Why?* The product $r_c r_d$ is **symmetric** under swapping $c \leftrightarrow d$, while $\varepsilon_{bcd}$ is **antisymmetric** under swapping $c \leftrightarrow d$. Summing over $c, d$ gives zero!

   **Example for $b = x$.** $\varepsilon_{xcd} r_c r_d = \varepsilon_{xyz} y z + \varepsilon_{xzy} z y = yz - zy = 0$.



