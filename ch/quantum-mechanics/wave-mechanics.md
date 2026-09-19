(quantum-mechanics:wave-mechanics)=
# Wave quantum mechanics

> If the system behaves like a wave, it must satisfy a wave function

> As the geometrical optics is the short wave-length approximation of the ondulatory optics, classical mechanics may be the short wave-length approximation of ondulatory mechanics

## De Broglie


## Schrodinger

### Derivation

From the probability interpretation of the wave function $| \Psi_t \rangle$, and the unitary condition $\langle \Psi_t | \Psi_t \rangle = 1$, for every $t$, the evolution of the system must be governed by a unitary operator $U_{t,t_0}$,

$$ | \Psi_t \rangle = U_{t,t_0} | \Psi_{t_0} \rangle \ ,$$

for the unitary condition to hold at every $t$,

$$1 =  \langle \Psi_{t} | \Psi_{t} \rangle = \langle U_{t,t_0} \Psi_{t_0} |  U_{t,t_0} \Psi_{t_0} \rangle = \langle \Psi_{t_0} | \underbrace{U^{\dagger}_{t,t_0}  U_{t,t_0}}_{= \hat{\mathbf{1}}} | \Psi_{t_0} \rangle =  \langle \Psi_{t_0} | \Psi_{t_0} \rangle \ ,$$

i.e.

$$U_{t,t_0}^{-1} = U^{\dagger}_{t,t_0} \ .$$

Taking the time derivative w.r.t. $t$ of the evolution relation, it follows

$$| \dot{\Psi}_t \rangle = \partial_t U_{t,t_0} | \Psi_{t_0} \rangle = \underbrace{ \partial_t U_{t,t_0} U^{\dagger}_{t,t_0}}_{ \hat{A}(t,t_0)} | \Psi_{t} \rangle \ .$$

**Composition.** As $| \Psi_{t} \rangle = U_{t,t_1} | \Psi_{t_1} \rangle =  U_{t,t_1} U_{t_1,t_0}| \Psi_{t_0} \rangle$,

$$U_{t,t_0} = U_{t,t_1} U_{t_1,t_0} \ .$$

**Indpendence of $\hat{A}(t,t_0) = \partial_t U_{t,t_0} U_{t,t_0}$ from $t_0$.** The operator $\hat{A}(t,t_0) = \partial_t U_{t,t_0} U_{t,t_0}$ can thus be written as

$$\hat{A}(t,t_0) = \partial_t U_{t,t_0} U_{t,t_0}^{\dagger} = \partial_t U_{t,t_1} \underbrace{U_{t_1,t_0} U_{t_1, t_0}^{\dagger}}_{ = \hat{\mathbf{1}} } U_{t,t_1}^{\dagger} = \partial_t U_{t,t_1} U_{t,t_1}^{\dagger} = \hat{A}(t,t_1) \ ,$$

showing that it's independent from the initial time, $\hat{A}(t,t_0) = \hat{A}(t)$.

**$\hat{A}(t)$ is anti-Hermitian.** As 

$$0 = \partial_t \underbrace{\left( U_{t,t_0} U_{t,t_0}^{\dagger} \right)}_{= \hat{\mathbf{1}} } = \underbrace{ \partial_t U_{t,t_0} U_{t,t_0}^\dagger}_{ = \hat{A}(t)} + \underbrace{ U_{t,t_0} \, \partial_t U_{t,t_0}^\dagger}_{= \hat{A}^\dagger(t)} = \hat{A}(t) + \hat{A}^\dagger(t) \ ,$$

and thus $\hat{A} = - \hat{A}^\dagger$. Thus the operator $\hat{A}$ can be written as $\hat{A} = i \hat{\tilde{H}}$, being $\hat{\tilde{H}}$ and Hermitian operator. For the correspondence principle (classical limit for $\hbar \rightarrow 0$) the Hermitian operator is found to be $\hat{\tilde{H}} = -\frac{1}{\hbar} \hat{H}$, being $\hat{H}$ the Hamiltonian operator. **todo** *Add a link to "correspondence principle", either Ehrenfest theorem and/ or equations in Heisenberg picture*

Thus, the wave equation becomes

$$| \dot{\Psi} \rangle = \frac{1}{i \hbar} \hat{H} | \Psi \rangle \qquad \text{or} \qquad i \hbar | \dot{\Psi} \rangle = \hat{H} | \Psi \rangle \ .$$ (eq:schrodinger)

The Hamiltonian can be written as a function of the unitary operator $U_{t,t_0}$ and its time derivative as

$$\hat{H} = i \hbar \, \partial_t U_{t,t_0} U^{\dagger}_{t,t_0} \ .$$ (eq:h-u-dtu)

### Energy eigen-states

$$\hat{H} | \Psi_k \rangle = E_k | \Psi_k \rangle \ .$$

Let the Hamiltonian be independent from time, thus also the eigenvalues and eigenfunctions are independent from time. Let a state be a superposition (linear combination) of eigenfunctions of the Hamiltonian operator

$$| \Psi_t \rangle = c_{k}(t) | \Psi_k \rangle \ ,$$

the time evolution immedately follows as

$$\begin{aligned}
  i \hbar \dot{c}_k | \Psi_k \rangle = c_k \hat{H} | \Psi_k \rangle = c_k E_k | \Psi_k \rangle \ ,
\end{aligned}$$

from orthogonality condition $\langle \Psi_j | \Psi_k \rangle = \delta_{jk}$, that gives the dynamical equation for the coefficients $c_i$,

$$\dot{c}_k = - i \frac{E_k}{\hbar} c_k \ ,$$

whose solution is $c_k(t) = c_{k,0} \exp \left( - i \frac{E_k}{\hbar} t \right)$. The evolution of the state is

$$| \Psi_t \rangle = | \Psi_k \rangle c_{k,0} \exp\left( - i \frac{E_k}{\hbar} t \right) = | \Psi_k \rangle \langle \Psi_k | \Psi_0 \rangle \exp\left( - i \frac{E_k}{\hbar} t \right)$$

**Properties.** If an **isolated system** starts in an eigen-state of the Hamiltonian operator, i.e. $| \Psi_0 \rangle = | \Psi_a \rangle$, $|c_{k,0}|^2 = \delta_{ka}$, then the evolution of the system reads

$$| \Psi_t \rangle = | \Psi_a \rangle \exp\left( - i \frac{E_a}{\hbar} t \right) \ ,$$

i.e. the probability of measuring the $k^{th}$ energy is

$$p(E = E_k) = | \langle \Psi_k | \Psi_t \rangle |^2 = \left| \underbrace{\langle \Psi_k | \Psi_a \rangle}_{\delta_{ka}} \exp\left(-i \frac{E_a}{\hbar} t\right) \right|^2 = \delta_{ka} \ ,$$

i.e. there's probability of finding it in the same state as the initial state $a$ is $p(E = E_a) = 1$, while the probability of finding in any other state is zero, $p(E = E_k) = 0$, $k \ne a$.


### Space and momentum operators



````{dropdown} Position operator

```{dropdown} Definition
:open:

$$\hat{\mathbf{r}} | \mathbf{r} \rangle = \mathbf{r} | \mathbf{r} \rangle$$

```


```{dropdown} Wave function in space basis
:open:

$$\Psi(\mathbf{r}, t) := \langle \mathbf{r} | \Psi_t \rangle \ .$$


```

```{dropdown} Orthonality, and identity operator
:open:

$$\begin{aligned}
  1
  & = \int_{\mathbf{r} \in \Omega} \Psi^*(\mathbf{r},t) \Psi(\mathbf{r},t) d \mathbf{r} = \\
  & = \langle \Psi_t | \, \underbrace{\int_{\mathbf{r} \in \Omega} | \mathbf{r} \rangle \langle \mathbf{r} | d \mathbf{r}}_{= \hat{\mathbf{1}} } \, | \Psi_t \rangle  = \\
  & = \langle \Psi_t | \Psi_t \rangle \ .
\end{aligned}$$

So that the identity operator in space basis reads $\hat{\mathbf{1}} = \int_{\mathbf{r} \in \Omega} | \mathbf{r} \rangle \langle \mathbf{r} | d \mathbf{r}$. A wave function can be thus written as

$$| \Psi \rangle = \int_{\mathbf{r}' \in \Omega} | \mathbf{r}' \rangle \langle \mathbf{r}' | \, d \mathbf{r}' \, | \Psi \rangle \ .$$ (eq:quantum:space-representation)

```

```{dropdown} Expansion in space basis
:open:

$$\begin{aligned}
  \langle \mathbf{r} | \Psi \rangle = \Psi(\mathbf{r},t)
  & = \int_{\mathbf{r}' \in \Omega} \delta(\mathbf{r} - \mathbf{r}') \Psi(\mathbf{r}',t) \, d \mathbf{r}'
\end{aligned}$$

Comparing the last expression, with the projection of the expression {eq}`eq:quantum:space-representation` over $\langle \mathbf{r} |$,

$$\begin{aligned}
  \langle \mathbf{r} | \Psi \rangle = \langle \mathbf{r} |  \ , \int_{\mathbf{r}' \in \Omega} | \mathbf{r}' \rangle \langle \mathbf{r}' | \, d \mathbf{r}' \, | \Psi \rangle = \int_{\mathbf{r}' \in \Omega} \langle \mathbf{r} | \mathbf{r}' \rangle \langle \mathbf{r}' | \Psi \rangle \,  d \mathbf{r}' = \int_{\mathbf{r}' \in \Omega} \langle \mathbf{r} | \mathbf{r}' \rangle \Psi(\mathbf{r'},t ) \,  d \mathbf{r}' \ ,
\end{aligned}$$

if follows the orthogonality condition $\langle \mathbf{r} | \mathbf{r}' \rangle = \delta(\mathbf{r} - \mathbf{r}')$.

```
````

The classical Hamiltonian of  the system reads

$$H(\mathbf{r}, \mathbf{p}) = \frac{| \mathbf{p} |^2 }{2m} - \frac{q^2}{4 \pi \varepsilon | \mathbf{r} |} \ ,$$

the promotion to the Hamiltonian operator is thus

$$\hat{H} = \frac{| \hat{\mathbf{p}} |^2}{2 m } - \frac{q^2}{4 \pi \varepsilon} \hat{|\mathbf{r}|}^{-1} \ .$$

````{dropdown} Power of an operator

Positive integer power 

$$\hat{A}^n = \underbrace{\hat{A} \dots \hat{A}}_{\text{$n$ times}}$$

Let the eigenproblem of the operator be $\hat{A} | a \rangle = a | a \rangle$, with $a \in \mathbb{R}$. Then, the eigenproblem for the operator $\hat{A}^n$ reads

$$\hat{A}^n | a \rangle = a^n | a \rangle \ .$$

The inverse of an operator has the eigenproblem

$$\hat{A}^{-1} | a \rangle = \frac{1}{a} | a \rangle \ ,$$

as $| a \rangle = \hat{A} \left( \hat{A}^{-1} | a \rangle \right) = \frac{1}{a} \hat{A} | a \rangle = \frac{1}{a} \, a | a \rangle = | a \rangle$.

````

````{dropdown} Vector operators
:open:

Momentum operator, $\hat{\mathbf{p}}$, in space base $\langle \mathbf{r} | \hat{\mathbf{p}} = -i \hbar \nabla_{\mathbf{r}} \langle \mathbf{r} |$.
Using Cartesian coordinates

$$ \hat{\mathbf{e}}_a \, \langle \mathbf{r} | \hat{p}_a = - \hat{\mathbf{e}}_a \, i \hbar \partial_a \langle \mathbf{r} |$$

The operator of the square magnitude reads

$$\hat{\left( | \mathbf{p}|^2 \right)} = \hat{\left( p_x^2 + p_y^2 + p_z^2 \right)} = \hat{p_x^2} +  \hat{p_y^2} + \hat{p_z^2} \ , $$

and in space coordinates

$$\langle \mathbf{r} | \hat{\left( |\mathbf{p} |^2 \right)} = - \hbar^2 \partial_{aa} \langle \mathbf{r} | = - \hbar^2 \nabla^2 \langle \mathbf{r} | $$

````







