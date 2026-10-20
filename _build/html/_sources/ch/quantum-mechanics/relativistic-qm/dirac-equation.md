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

Dirac's equation is found to be

$$i \hbar \partial_t \Psi(\mathbf{r},t) = - i \hbar c \boldsymbol\alpha \cdot \nabla \Psi(\mathbf{r},t) + m c^2 \beta \Psi(\mathbf{r},t) \ ,$$

using the set of matrices $\beta = \gamma^0$, $\gamma^k = \beta \alpha_k$

$$
  \gamma^0 = \begin{bmatrix} I_2 & \cdot \\ \cdot & -I_2 \end{bmatrix}
  \quad , \quad
  \gamma^k = \begin{bmatrix} \cdot & \sigma_k \\ -\sigma_k & \cdot \end{bmatrix} \ .
$$

Dirac's equation can be recast, multipyling by $\beta$, as

$$\begin{aligned}
 0
 & = i \hbar \left( \beta \partial_t + c \beta \boldsymbol\alpha \cdot \nabla \right) \Psi - m c^2 \Psi = \\
 & = i \hbar \gamma^\mu \partial_\mu \Psi - m c^2 \Psi \ ,
\end{aligned}$$

and thus

$$\begin{aligned}
 \left( i \hbar \gamma^\mu \partial_\mu - m c^2 \right) \Psi = 0 \ .
\end{aligned}$$
