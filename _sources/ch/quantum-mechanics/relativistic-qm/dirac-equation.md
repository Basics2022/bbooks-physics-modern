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


