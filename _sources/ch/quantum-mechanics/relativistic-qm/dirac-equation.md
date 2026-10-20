(quantum-mechanics:relativistic:dirac-equation)=
# Dirac equation

(quantum-mechanics:relativistic:dirac-equation:klein-gordon-free)=
## Klein-Gordon equation for a free particle

The relation between energy and momentum for a massive particle in [special relativity](relativity-special:notes)

$$m^2 c^2 = \frac{E^2}{c^2} - | \mathbf{p} |^2 \ ,$$ (eq:dirac-eq:einstein:en-mom)

can be seamlessly promoted to a operator equation, $\mathbf{p} \rightarrow \hat{\mathbf{p}}$, $E \rightarrow \hat{H}t$, to only get Klein-Gordon equation

$$ \frac{m^2}{c^2}{\hbar^2} = \frac{\hat{H}^2}{c^2} - |\hat{\mathbf{p}}|^2 \ ,$$

or in position representation, where $\langle \mathbf{r} | \hat{\mathbf{p}} = - i \hbar \nabla \langle \mathbf{r} |$, $\langle \mathbf{r} | \hat{H} = i \hbar \partial_t \langle \mathbf{r} |$, applied to a wave function $| \Psi \rangle$

$$\left\{ \square + \frac{m^2 \hbar^2}{c^2} \right\} \Psi(\mathbf{r},t) = 0 \ .$$

(quantum-mechanics:relativistic:dirac-equation:dirac-free)=
## Dirac equation for a free particle

Dirac's equation follows from the expression of the Hamiltonian operator as a linear combination of the components of the momentum operator and the $m c$,

$$\hat{H} = \alpha_0 m c + \sum_{k=1}^{3} \alpha_k \hat{p}_k \ ,$$

that satisfies the relation {eq}`eq:dirac-eq:einstein:en-mom`.

```{dropdown} Details of the solution
:open:

**todo**...

```

The Hamiltonian operator becomes

$$\hat{H} = m c^2 \beta + c \boldsymbol\alpha \cdot \hat{\mathbf{p}} = m c^2 \beta - i \hbar c \boldsymbol\alpha \cdot \nabla \ , $$

so that the position representation of Dirac's equation can be written using 3+1 formalism (space+time) as

$$\begin{aligned}
  i \hbar \partial_t \Psi(\mathbf{r},t) 
  & = \langle \mathbf{r} | \hat{H} | \Psi \rangle = \\
  & = - i \hbar c \boldsymbol\alpha \cdot \nabla \Psi(\mathbf{r},t) + m c^2 \beta \Psi(\mathbf{r},t) \ ,
\end{aligned}$$

with the set of $4 \times 4$ complex matrices $\beta = \gamma^0$, $\gamma^k = \beta \alpha_k$

$$
  \gamma^0 = \begin{bmatrix} I_2 & \cdot \\ \cdot & -I_2 \end{bmatrix}
  \quad , \quad
  \gamma^k = \begin{bmatrix} \cdot & \sigma_k \\ -\sigma_k & \cdot \end{bmatrix} \ ,
$$

built with $2 \times 2$ identity and [Pauli matrices](quantum-mechanics:angular-momentum:spin:pauli-matrices) $\sigma_k$. Dirac's equation can be recast in the 4-dimensional formalism of special relativity, after multiplication by $\beta$, as

$$\begin{aligned}
 \left( i \hbar \gamma^\mu \partial_\mu - m c \right) \Psi = 0 \ ,
\end{aligned}$$

since

$$\begin{aligned}
 0
 & = i \hbar \left( \beta \partial_t + c \beta \boldsymbol\alpha \cdot \nabla \right) \Psi - m c^2 \Psi = \\
 & = i \hbar c \gamma^\mu \partial_\mu \Psi - m c^2 \Psi \ .
\end{aligned}$$

### Elementary solutions of Dirac equation for a free particle

$$
\left\{
i \frac{\hbar}{c} \begin{bmatrix} 1 & & & \\ & 1 & & \\ & & -1 & \\ & & & -1 \end{bmatrix} \partial_t
+ i \hbar \begin{bmatrix} & & & 1 \\ & & 1 & \\ & -1 & & \\ -1 & & &  \end{bmatrix} \partial_x
+ i \hbar \begin{bmatrix} & & & -i \\ & & i & \\ & i & & \\ -i & & &  \end{bmatrix} \partial_y
+ i \hbar \begin{bmatrix} & & 1 & \\ & & & -1 \\ -1 & & & \\ & 1 & &  \end{bmatrix} \partial_z
- m c \right\} \Psi(t, \mathbf{r}) = \mathbf{0} \ .
$$


#### Dimensional Reduction to 1D and Component Decoupling

To better understand the internal dynamics of the spinor, we can study a simplified scenario by assuming homogeneity along the $y$ and $z$ axes, setting spatial derivatives to zero ($\partial_y = \partial_z = 0$). Dirac's equation reduces to

$$
\left\{
i \frac{\hbar}{c} \begin{bmatrix} 1 & & & \\ & 1 & & \\ & & -1 & \\ & & & -1 \end{bmatrix} \partial_t
+ i \hbar \begin{bmatrix} & & & 1 \\ & & 1 & \\ & -1 & & \\ -1 & & &  \end{bmatrix} \partial_x
- m c \right\} \Psi(t, x) = \mathbf{0} \ .
$$

Expanding the matrix equation for a four-component spinor $\Psi = \begin{pmatrix} \psi_1 & \psi_2 & \psi_3 & \psi_4 \end{pmatrix}^T$, the system splits naturally into **two independent pairs of coupled equations**:
1. A coupling between **$\psi_1$ and $\psi_4$**
2. A coupling between **$\psi_2$ and $\psi_3$**

For the first pair ($\psi_1$ and $\psi_4$), the system reads:

$$\begin{cases}
\frac{i\hbar}{c} \partial_t \psi_1 - mc \, \psi_1 + i\hbar \partial_x \psi_4 = 0 \\[6pt]
-i\hbar \partial_x \psi_1 - \frac{i\hbar}{c} \partial_t \psi_4 - mc \, \psi_4 = 0
\end{cases}$$

**Reduction to Klein-Gordon Equation for individual components.**
By isolating $\partial_x \psi_4$ from the first equation and substituting it into the second, the mixed temporal-spatial derivative terms cancel out, demonstrating that each individual component satisfies the relativistic dispersion relation:

$$\left( \square + \frac{m^2 c^2}{\hbar^2} \right) \psi_1 = 0 \ ,$$

where $\square = \frac{1}{c^2}\partial_t^2 - \partial_x^2$ is the d'Alembertian operator.

```{dropdown} Details

$$\partial_x \psi_4 = \frac{1}{i\hbar} \left( m c \psi_1 - \frac{i \hbar}{c} \partial_t \psi_1 \right) \ ,$$

and thus

$$\begin{aligned}
  0 
  & = -i \hbar \partial_{xx} \psi_1 - \left( \frac{i \hbar}{c} \partial_t + m c \right) \partial_x \psi_4 = \\
  & = -i \hbar \partial_{xx} \psi_1 + \frac{1}{i \hbar} \left( \frac{i \hbar}{c} \partial_t + m c \right) \left( \frac{i \hbar}{c} \partial_t - m c  \right) \psi_1 = \\
  & = - i \hbar \partial_{xx} \psi_1 - \frac{i}{\hbar} \left( - \frac{\hbar^2}{c^2} \partial_{tt} - m^2 c^2 \right) \psi_1 \ ,
\end{aligned}$$

and thus, after dividing by $i \hbar$,

$$\left( \frac{1}{c^2} \partial_{tt} - \partial_{xx} + \frac{m^2 c^2}{\hbar^2} \right) \psi_1 = 0 \ .$$

```

#### Plane Wave Solutions and Component Relations

Assuming a plane wave ansatz for the components of the form $\psi_1 = K_{\mathbf{p}} e^{-\frac{i}{\hbar}(Et - p_x x)}$, the **dispersion relation** $- \frac{E^2}{\hbar^2 c^2} + \frac{p_x^2}{\hbar^2} + \frac{m^2 c^2}{\hbar^2} = 0$ is found between the energy and the momentum of the free particle, or after multiplying by $\hbar^2$,

$$E^2 = p_x^2 c^2 + m^2 c^4 = 0 \quad \rightarrow \quad E = \mp c \sqrt{ p_x^2 + m^2 c^2 } \ ,$$

i.e. the very same Einstein energy-momentum equation {eq}`eq:dirac-eq:einstein:en-mom`. Convert the differential coupling into an algebraic relation between the "large" and "small" components, the first equation

$$i\hbar \partial_x \psi_4 = \left( \frac{i\hbar}{c} \partial_t - mc \right) \psi_1$$

becomes

$$i \hbar \cdot i \frac{p_x}{\hbar} \psi_4 = \left( \frac{i\hbar}{c} \left(- \frac{i E}{\hbar} \right) - mc \right) \psi_1 $$

Thus, the relation between $\psi_1$ and $\psi_4$ is the ratio

$$\psi_4 = \frac{mc^2 - E}{c \, p_x} \psi_1 \ .$$

An identical decoupling procedure applies symmetrically to the second pair ($\psi_2$ and $\psi_3$).

```{dropdown} Physical Insights and Interpretation
:open:

1. **Large vs. Small Components:**
   * The upper pair $(\psi_1, \psi_2)$ represents the **large components**, which in the non-relativistic limit ($v \ll c$) reduce to the standard two-component Pauli spinor describing spin.
   * The lower pair $(\psi_3, \psi_4)$ represents the **small components**, suppressed by a factor of $v/c$, which carry the relativistic corrections responsible for spin-orbit coupling and magnetic moments.

2. **Emergence of Spin:**
   Unlike non-relativistic quantum mechanics where spin is added ad-hoc via Pauli matrices, spin emerges naturally in the Dirac equation as a direct consequence of the linearization required for Lorentz covariance, combining with orbital angular momentum into a conserved total angular momentum $\mathbf{J} = \mathbf{L} + \mathbf{S}$.

3. **Antimatter and Negative Energies:**
   The dispersion relation permits both positive ($E = +\sqrt{c^2p^2 + m^2c^4}$) and negative ($E = -\sqrt{...}$) energy solutions. In modern quantum field theory, these negative energy states are reinterpreted through second quantization as antiparticles (such as the positron), resolving historical vacuum stability issues.

```

## Dirac equation for a particle in the EM field

Following the **minimal coupling**, the momentum of a free particle is replaced by the momentum of a charged particle in a EM field,[^sr-em]

$$\mathbf{P} \rightarrow  \mathbf{P} + q \mathbf{A} \ ,$$

[^sr-em]: [Math: Calculus of Variations: Examples: Lagrange Equations in Special Relativity Using Tensor Formalism](https://basics2022.github.io/bbooks-math-miscellanea/ch/calculus-variations/examples.html#lagrange-equations-in-special-relativity)

with $\mathbf{P} = m \mathbf{U} = \gamma m ( c, \mathbf{v} ) = \left( \frac{E}{c}, \mathbf{p} \right)$, and $\mathbf{A} = \left( \frac{\varphi}{c}, \mathbf{a} \right)$, so that

$$\left\{ \mathbf{P} + q \mathbf{A} \right\}^{\mu} = \left( \frac{E + q \varphi}{c}, \mathbf{p} + q \mathbf{a} \right)$$
$$\left\{ \mathbf{P} + q \mathbf{A} \right\}_{\mu} = \left( \frac{E + q \varphi}{c}, -\mathbf{p} - q \mathbf{a} \right)$$

and the Hamiltonian in space representation becomes

$$\begin{aligned}
  \hat{H} & = m c^2 \beta - i \hbar c \boldsymbol\alpha \cdot \nabla \\
\quad \rightarrow \quad \hat{H} & = m c^2 \beta + q \varphi + c \boldsymbol\alpha \cdot \left( - i \hbar \nabla + q\mathbf{a} \right)
\end{aligned}$$

$$\begin{aligned}
  0
  & = i \hbar \beta \partial_t \Psi - \beta \hat{H} \Psi = \\
  & = i \hbar \beta \partial_t \Psi - m c^2 - q \beta \varphi \Psi + i c \hbar \beta \alpha_k \partial_k \Psi - c q \beta \alpha_k a_k \Psi = \\
  & = i \hbar c \gamma^0 \frac{1}{c}\partial_t \Psi + i \hbar c \gamma^k \partial_k \Psi - m c^2 \Psi + q c \gamma^0 \frac{\varphi}{c} \Psi - q c \gamma^k a_k \Psi = \\
\end{aligned}$$

and thus, after dividing by $c$,

$$\left( i \hbar \gamma^\mu \left( \partial_{\mu} - q A_\mu \right) - m c^2 \right) \Psi = 0 \ .$$

**todo**
* check signs, when switching to 3+1 to 4 formalism
* motivation of the introduction of $\varphi$ in the minimal coupling. Why is it without $\beta$? Does it go with $E$, from the transformation $\frac{E}{c} \rightarrow \frac{E + q \varphi}{c}$?
* Invariance in special relativity
* Limit cases

```{dropdown} Special Relativity and Invariance
:open:

**todo**...

```


