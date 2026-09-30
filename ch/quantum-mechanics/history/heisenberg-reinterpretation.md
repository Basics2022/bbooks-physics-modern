(quantum-mechanics:history:heisenberg-reinterpretation)=
# Modern reinterpretation of Heisenberg mechanics


(quantum-mechanics:history:heisenberg-reinterpretation:eoms)=
## Heisenberg Equations of Motion in the Heisenberg Picture

Time derivative of an operator $\hat{A}_H$ in Heisenberg picture satisfies the relation {eq}`eq:qm:heisenberg:dAdt`,

$$\dfrac{d \hat{A}_H}{dt} = \frac{1}{i \hbar} \left[ \hat{A}_H , \hat{H}_H \right] + \left( \partial_t \hat{A} \right)_H \ .$$

Applying this relation to the position and momentum operators, $\hat{\mathbf{x}}_H$ and $\hat{\mathbf{p}}_H$, Heisenberg found the quantum mechanics counterpart of the equations of motion in classical mechanics,

$$\left\{
\begin{aligned}
  \dot{\hat{\mathbf{x}}}_H & = \frac{1}{i \hbar} \left[ \hat{\mathbf{x}}_H , \hat{H}_H \right] = \frac{\hat{\mathbf{p}}_H}{m} \\
  \dot{\hat{\mathbf{p}}}_H & = \frac{1}{i \hbar} \left[ \hat{\mathbf{p}}_H , \hat{H}_H \right] = - \left( \nabla_{\mathbf{r}} V\left( \hat{\mathbf{r}}\right) \right)_H \\
\end{aligned}
\right.$$ (eq:qm:heisenberg:eoms-1)

````{dropdown} Details
:open:

If $\hat{H} = \frac{|\hat{\mathbf{p}|}^2}{2 m} + V\left(\hat{\mathbf{r}}\right)$,

```{dropdown} $\left[ \hat{\mathbf{x}}_H, \hat{H}_H \right] = i \hbar \frac{\hat{\mathbf{p}}_H}{m}$

$$\begin{aligned}
  \left[ \hat{\mathbf{x}}_H, \hat{H}_H \right] 
  & = \mathscr{U}_{t,t_0}^{\dagger} \left( \left[ \hat{\mathbf{x}}, \frac{\left|\hat{\mathbf{p}}\right|^2}{2m} \right] + \left[ \hat{\mathbf{x}}, V\left(\hat{\mathbf{r}}\right) \right] \right) \mathscr{U}_{t,t_0} = \\
  & = \mathscr{U}_{t,t_0}^{\dagger} \left( i \hbar \frac{\hat{\mathbf{p}}}{m} \right) \mathscr{U}_{t,t_0} = \\
  & = i \hbar \frac{\hat{\mathbf{p}}_H}{m} \ .
\end{aligned}$$

since 
1. $\hat{\mathbf{x}}$ and $V(\hat{\mathbf{r}})$ commute, as it can be proved using power expansion - if required - of $V(\hat{\mathbf{r}})$; 
2. the commutator of $\hat{\mathbf{x}}$ and the kinetic contribution of the Hamiltonian operator reads (sum over $b$ repeated index),
    
    $$\begin{aligned}
      \left[ \hat{x}_a, \hat{p}_b \hat{p}_b \right] 
      & = \hat{x}_a \hat{p}_b \hat{p}_b - \hat{p}_b \hat{x}_a \hat{p}_b + \hat{p}_b \hat{x}_a \hat{p}_b - \hat{p}_b \hat{x}_b \hat{p}_a = \\
      & = \left[ \hat{x}_a , \hat{p}_b \right] \hat{p}_b + \hat{p}_b \left[ \hat{x}_a , \hat{p}_b \right] = \\
      & = 2 i \hbar \delta_{ab} \hat{p}_b = \\
      & = 2 i \hbar \hat{p}_a \ .
    \end{aligned}$$
```

```{dropdown} $\left[ \hat{\mathbf{p}}_H, \hat{H}_H \right] = - i \hbar \left( \nabla_{\mathbf{r}} V\left( \hat{\mathbf{r}}\right) \right)_H$

$$\begin{aligned}
  \left[ \hat{\mathbf{p}}_H, \hat{H}_H \right] 
  & = \mathscr{U}_{t,t_0}^{\dagger} \left( \left[ \hat{\mathbf{p}}, \frac{\left|\hat{\mathbf{p}}\right|^2}{2m} \right] + \left[ \hat{\mathbf{p}}, V\left(\hat{\mathbf{r}}\right) \right] \right) \mathscr{U}_{t,t_0} = \\
\end{aligned}$$

since, the commutator of the momentum and potential energy operator reads $\left[ \hat{\mathbf{p}}, V(\hat{\mathbf{r}}) \right] = $

$$\begin{aligned}
  \langle \mathbf{r} | \left[ \hat{\mathbf{p}}, V\left(\hat{\mathbf{r}}\right) \right] | \Psi \rangle
  & = \langle \mathbf{r} | \hat{\mathbf{p}} V\left(\hat{\mathbf{r}}\right) | \Psi \rangle - \langle \mathbf{r} | V\left(\hat{\mathbf{r}}\right) \hat{\mathbf{p}} | \Psi \rangle = \\
  & = - i \hbar \nabla_{\mathbf{r}} \langle \mathbf{r} | V\left(\hat{\mathbf{r}}\right) | \Psi \rangle - V\left(\mathbf{r}\right) \langle \mathbf{r} | \hat{\mathbf{p}} | \Psi \rangle = \\
  & = - i \hbar \nabla_{\mathbf{r}} \left( V(\mathbf{r}) \Psi(\mathbf{r}, t) \right) + i \hbar V(\mathbf{r}) \nabla_{\mathbf{r}} \Psi(\mathbf{r}, t) = \\
  & = - i \hbar \nabla_{\mathbf{r}} V(\mathbf{r}) \, \Psi(\mathbf{r},t) = \\
  & = \langle \mathbf{r} | - i \hbar \nabla_{\mathbf{r}} V\left( \hat{\mathbf{r}} \right) | \Psi \rangle \ . 
\end{aligned}$$

as $\langle \mathbf{r} | \hat{\mathbf{p}} \rangle = - i \hbar \nabla_{\mathbf{r}} \langle \mathbf{r} |$, and $V\left( \hat{\mathbf{r}} \right) | \mathbf{r} \rangle = V( \mathbf{r} ) | \mathbf{r} \rangle$, and

$$\begin{aligned}
  f(x) \Psi(x,t)
  & = \int_{x'} f(x) \Psi(x', t) \delta(x-x') \, dx' = \\
  & = \int_{x'} f(x) \langle x' | \Psi \rangle \langle x | x' \rangle \, dx' = \\
  & = \int_{x'} \langle x | f(x) | x' \rangle \langle x' | \Psi \rangle \, dx' = \\
  & = \langle x | f \left(\hat{x}\right) \underbrace{\int_{x'} | x' \rangle \langle x' | dx'}_{=\hat{\mathbf{1}}} | \Psi \rangle = \\
  & = \langle x | f\left(\hat{x}\right) | \Psi \rangle \ .
\end{aligned}$$

```

````

(quantum-mechanics:history:heisenberg-reinterpretation:eoms-matrix-components)=
## Matrix components in energy basis of the equations of motion

The matrix components in energy basis of the equations of motion {eq}`eq:qm:heisenberg:eoms-1` read

$$\left\{
\begin{aligned}
 i \omega_{jk} X_{jk}^H & = \frac{P_{jk}^H}{m} \\
 i \omega_{jk} P_{jk}^H & = - \left( \nabla V \right)^{H}_{jk} \\
\end{aligned}
\right.$$ (eq:qm:heisenberg:eoms-2)

with $\omega_{jk} := \frac{E_j - E_k}{\hbar}$.


````{dropdown} Details

If the Hamiltonian is not an explicit function of time, $\mathscr{U}_{t,0} = \exp\left[ -i \frac{\hat{H}}{\hbar} t \right]$, and thus

$$\begin{aligned}
  \left( \hat{\mathbf{x}}_H  \right)
  & = \left( | j \rangle \langle j | \hat{\mathbf{x}}_H | k \rangle \langle k | \right) = \\
  & = \left( | j \rangle \langle j | \mathscr{U}_{t,0}^{\dagger} \hat{\mathbf{x}} \mathscr{U}_{t,0} | k \rangle \langle k | \right) = \\
  & = | j \rangle \langle k | \left[ \exp\left(- i \frac{E_k-E_j}{\hbar} t  \right) \langle j | \hat{\mathbf{x}} | k \rangle  \right] 
\end{aligned}$$

i.e. 

$$X^{H}_{jk}(t) = X^{S}_{jk} \exp\left( i \frac{E_j - E_k}{\hbar} t \right) \ .$$

The time-derivative of the matrix elements of the position operator in Heisenber picture reads

$$\dot{X}^{H}_{jk} = i \omega_{jk} X^{S}_{jk} \exp\left( i \omega_{jk} t \right) = i \omega_{jk} X^H_{jk} \ ,$$

with $\omega_{jk} := \frac{E_j - E_k}{\hbar}$.


````

(quantum-mechanics:history:heisenberg-reinterpretation:hamilton-eqns)=
## Equations of motion as Hamilton's equations

The equations of motion {eq}`eq:qm:heisenberg:eoms-1`, or {eq}`eq:qm:heisenberg:eoms-2`, can be recast in the form of Hamilton's equations

$$
\left\{
\begin{aligned}
  \dot{\hat{\mathbf{q}}}_H & = \dfrac{\partial \mathsf{H}}{\partial \hat{\mathbf{p}}_H} \\
  \dot{\hat{\mathbf{p}}}_H & =-\dfrac{\partial \mathsf{H}}{\partial \hat{\mathbf{q}}_H} \\
\end{aligned}
\right.
$$

and

$$
\left\{
\begin{aligned}
  \dot{X}^{H}_{jk} & = \dfrac{\partial \mathsf{H}}{\partial P^{H}_{jk}} \\
  \dot{P}^{H}_{jk} & =-\dfrac{\partial \mathsf{H}}{\partial Q^{H}_{jk}} \\
\end{aligned}
\right.
$$

with $\mathsf{H} = \text{tr} \left( \hat{H} \right) = \sum_a \langle a | \hat{H} | a \rangle $.

````{dropdown} Details
:open:




````

(quantum-mechanics:history:heisenberg-reinterpretation:ccr-quantization-rule)=
## CCR and quantization rule

### Modern approach. Matrix form of the CCR

Given the CCR 

$$\left[ \hat{\mathbf{x}}, \hat{\mathbf{p}} \right] = \mathbb{I} i \hbar \qquad , \qquad \left[ \hat{x}_a, \hat{p}_b \right] = i \hbar \delta_{ab} \ ,$$

its matrix components are

$$\begin{aligned}
  i \hbar \delta_{ab} \delta_{jk} 
  & = \sum_{\ell} \left\{ X^{a}_{j \ell} P^{b}_{\ell k} - P^{b}_{j \ell} X^{a}_{\ell k} \right\} \ .
\end{aligned}$$ (eq:qm:heisenberg:ccr-matrix)


```{dropdown} Details

$$\begin{aligned}
  i \hbar \delta_{ab} \delta_{jk} 
  & = \langle j | i \hbar \delta_{ab} | k \rangle = \\
  & = \langle j | \left[ \hat{x}_a , \hat{p}_b \right] k \rangle = \\
  & = \langle j | \hat{x}_a \hat{p}_b - \hat{p}_b \hat{x}_a | k \rangle = \\
  & = \sum_{\ell} \left\{ \langle j | \hat{x}_a | \ell \rangle \langle \ell | \hat{p}_b | k \rangle - \langle j | \hat{p}_b | \ell \rangle \langle \ell | \hat{x}_a | k \rangle \right\} = \\
  & = \sum_{\ell} \left\{ X^{a}_{j \ell} P^{b}_{\ell k} - P^{b}_{j \ell} X^{a}_{\ell k} \right\} \ .
\end{aligned}$$

```
...

### From Bohr-Sommerfeld quantization to CCR

In old quantum mechanics - i.e. quantum mechanics before a quantum mechanics theory - Bohr-Sommerfeld quantization rule was

$$J = n h = \oint p_n d q_n = \oint p_n \dot{q}_n \, dt $$

**Classical trajectory.** Using Fourier series of a periodic trajectory,

$$q_n(t) = \sum_{\alpha} q_\alpha(n) e^{i \alpha \omega_n t} \ ,$$

the time derivative of $q_n(t)$ reads

$$\begin{aligned}
  \dot{q}_n(t) & = \sum_{\alpha} i \alpha \omega_n q_{\alpha}(n) e^{i \alpha \omega_n t} \ ,
\end{aligned}$$

while momentum can be written as

$$p_n(t) = \sum_{\beta} p_\beta(n) e^{i \beta \omega_n t} \ ,$$

Using these expression in the Bohr-Sommerfeld quantization rule,

$$\begin{aligned}
  J
  & = \dots = \\
  & = i \, 2 \pi \sum_{\alpha} \alpha p^*_{\alpha}(n) q_{\alpha}(n) \ ,
\end{aligned}$$

so that the derivative w.r.t. $J$ reads

$$1 = i \, 2 \pi \sum_{\alpha} \alpha \dfrac{\partial}{\partial J} \left( p^*_{\alpha}(n) q_{\alpha}(n) \right) \ . $$


**Quantum reinterpretation.** Let a function $\Phi(n,\alpha)$, then

$$\begin{aligned}
  \Phi(n, \alpha) - \Phi(n - \alpha, \alpha) 
  & \sim \alpha \partial_n \Phi(n, \alpha) + o(\alpha) = \\
  & = \alpha h \partial_J \Phi(n, \alpha) + o(\alpha) \ ,
\end{aligned}$$

and the **Born-Kramers correspondence principle follows**,

$$\frac{\Phi(n, \alpha) - \Phi(n - \alpha, \alpha) }{ h } \sim \alpha \dfrac{\partial \Phi}{\partial J} (n, \alpha) \ .$$

Let $p_\alpha(n) = p(n,\alpha) = p_{n+\alpha,n}$, then the reinterpretation of the classical quantization rule gives

$$\begin{aligned}
  1
  & = i \, \frac{2 \pi}{h} \sum_{\alpha} \left\{ p^*_{n+\alpha,n} q_{n+\alpha,n} - p^*_{n,n-\alpha} q_{n,n-\alpha} \right\} = \\
  & = i \, \frac{2 \pi}{h} \sum_{\alpha} \left\{ p^*_{n+\alpha,n} q_{n+\alpha,n} - \sum_\alpha p^*_{n,n-\alpha} q_{n,n-\alpha} \right\} = \\
  & = i \, \frac{2 \pi}{h} \sum_{\alpha} \left\{ p_{n,n+\alpha} q_{n+\alpha,n}   - \sum_\alpha q_{n,n-\alpha} p_{n-\alpha,n}  \right\} = \\
  & = \frac{1}{i \hbar} \sum_{\alpha} \left\{  q_{n,\alpha} p_{\alpha,n} - p_{n,\alpha} q_{\alpha,n} \right\}
\end{aligned}$$

These relations are nothing but the diagonal components of the matrix form {eq}`eq:qm:heisenberg:ccr-matrix` of the CCR. The out-of-diagonal components are identically zero, as P.Jordan proved with the following trick

```{dropdown} How P.Jordan proved that out-of-diagonal components of the CCR are identically zero
:open:

...

```


(quantum-mechanics:history:heisenberg-reinterpretation:ccr-ladenburg)=
## CCR in Energy Basis and Ladenburg Dispersion Formula

Introducing the expression of matrix components of the momentum $\hat{\mathbf{p}}_H = m \dot{\hat{\mathbf{x}}}_H$, $P^a_{jk} = i m \omega_{jk} X^{a}_{jk}$ into the matrix form {eq}`eq:qm:heisenberg:ccr-matrix` of the CCR relation

$$\begin{aligned}
  i \hbar \delta_{ab} \delta_{jk} 
  & = \sum_{\ell} \left\{ X^{a}_{j \ell} P^{b}_{\ell k} - P^{b}_{j \ell} X^{a}_{\ell k} \right\} = \\
  & = \sum_{\ell} \left\{ i m \omega_{\ell k} X^{a}_{j \ell} X^{b}_{\ell k} - i m \omega_{j \ell} X^{b}_{j \ell} X^{a}_{\ell k} \right\} \ .
\end{aligned}$$

The diagonal components $j = k$ are

$$\begin{aligned}
  i \hbar \delta_{ab} 
  & = \sum_{\ell} \left\{ i m \omega_{\ell k} X^{a}_{k \ell} X^{b}_{\ell k} - i m \omega_{k \ell} X^{b}_{k \ell} X^{a}_{\ell k} \right\} = \\
\end{aligned}$$

If $a = b$,

$$\begin{aligned}
  i \hbar 
  & = \sum_{\ell} \left\{ i m \omega_{\ell k} X^{a}_{k \ell} X^{a}_{\ell k} - i m \omega_{k \ell} X^{a}_{k \ell} X^{a}_{\ell k} \right\} = \\
  & = \sum_{\ell} \left\{ i m \omega_{\ell k} X^{a}_{k \ell} X^{a \, *}_{k \ell} - i m \omega_{k \ell} X^{a}_{k \ell} X^{a \, *}_{k \ell} \right\} = \\
  & = i 2 m \, \sum_{\ell} \omega_{\ell k} \left| X^{a}_{k \ell} \right|^2  \ ,
\end{aligned}$$

so that 

$$
 \frac{2 m}{\hbar} \, \sum_{\ell} \omega_{\ell k} \left| X^{a}_{k \ell} \right|^2  = 1 \ .
$$

**todo** *CHECK if there's a factor $3$, summing over all the components indexed by $a$*

**Connection to Ladenburg Dispersion Formula.**
In classical optics/early quantum theory, Ladenburg’s quantum dispersion formula for the oscillator strength $f_{km}$ associated with a transition $k \to m$ is defined as:

$$f_{km} = \frac{2m \omega_{km}}{\hbar} |x_{km}|^2$$

The diagonal CCR condition directly yields the **Thomas-Reiche-Kuhn (TRK) sum rule**:

$$\sum_m f_{km} = 1$$

This showed that Heisenberg's matrix mechanics naturally incorporated the empirically validated dispersion theory of Ladenburg, Kramers, and Kronig.


## Application: The Linear Harmonic Oscillator


```{dropdown} Linear harmonic oscillator

For the harmonic oscillator Hamiltonian $\hat{H} = \frac{\hat{p}^2}{2m} + \frac{1}{2}m\omega_0^2 \hat{x}^2$:

**Equations of Motion.**
$$\dot{\hat{x}} = \frac{\hat{p}}{m}, \quad \dot{\hat{p}} = -m\omega_0^2 \hat{x}$$

Taking the second time derivative:

$$\ddot{\hat{x}} + \omega_0^2 \hat{x} = 0$$

In matrix components:

$$(-\omega_{mn}^2 + \omega_0^2) x_{mn} = 0$$

Thus, non-zero matrix elements $x_{mn}$ can only exist if $\omega_{mn} = \pm \omega_0$, meaning transitions only occur between adjacent levels: $m = n \pm 1$.

**Matrix Elements & Energy Spectrum.**
Using the diagonal CCR $\frac{2m}{\hbar} \sum_m \omega_{mn} |x_{nm}|^2 = 1$:

$$\frac{2m\omega_0}{\hbar} \left( |x_{n, n+1}|^2 - |x_{n, n-1}|^2 \right) = 1$$

With the boundary condition $x_{0,-1} = 0$ for the ground state:

$$|x_{n, n+1}|^2 = \frac{\hbar}{2m\omega_0} (n+1)$$

The energy matrix elements give the discrete eigenvalues:

$$E_n = \hbar \omega_0 \left( n + \frac{1}{2} \right)$$

```

## Transition Probabilities as Dipole Matrix Elements

When an atom interacts with an electromagnetic field, the interaction Hamiltonian is dominated by the electric dipole coupling:

$$\hat{V}(t) = - \hat{\mathbf{d}} \cdot \mathbf{E}(t) = - q \hat{\mathbf{x}} \cdot \mathbf{E}_0 \cos(\omega t)$$

The probability amplitude for a transition from state $|n\rangle$ to state $|m\rangle$ is dictated by the matrix element of the position/dipole operator:

$$x_{mn} = \langle m | \hat{x} | n \rangle$$

The transition rate $W_{n \to m}$ (spontaneous emission / absorption probability) is proportional to the square of the dipole matrix element:

$$W_{n \to m} \propto |\mathbf{d}_{mn}|^2 = q^2 |\langle m | \hat{\mathbf{x}} | n \rangle|^2$$


## Perturbation Theory for Transition Probabilities in Weak Electric Fields

Consider a time-dependent perturbation $\hat{V}(t) = \hat{W} \cos(\omega t) = -q \hat{\mathbf{x}} \cdot \mathbf{E}_0 \cos(\omega t)$.

### First-Order Amplitude
Writing state expansion $|\psi(t)\rangle = \sum_n c_n(t) e^{-\frac{i}{\hbar}E_n t} |n\rangle$, the equations for $c_m(t)$ are:

$$i\hbar \dot{c}_m(t) = \sum_n \langle m | \hat{V}(t) | n \rangle c_n(t) e^{i \omega_{mn} t}$$

Assuming the system starts in initial state $c_k(0) = 1$ and $c_m(0) = 0$ for $m \neq k$:

$$c_m^{(1)}(t) = -\frac{i}{\hbar} \int_0^t V_{mk}(t') e^{i \omega_{mk} t'} dt'$$

Substituting $V_{mk}(t') = -q E_0 x_{mk} \frac{e^{i\omega t'} + e^{-i\omega t'}}{2}$:

$$c_m^{(1)}(t) = \frac{q E_0 x_{mk}}{2\hbar} \left[ \frac{1 - e^{i(\omega_{mk} + \omega)t}}{\omega_{mk} + \omega} + \frac{1 - e^{i(\omega_{mk} - \omega)t}}{\omega_{mk} - \omega} \right]$$

### Resonant Approximation (Rotating Wave Approximation)
Near resonance ($\omega \approx \omega_{mk}$ with $E_m > E_k$):

The term with denominator $(\omega_{mk} - \omega)$ dominates:

$$|c_m^{(1)}(t)|^2 \approx \frac{q^2 E_0^2 |x_{mk}|^2}{4\hbar^2} \frac{\sin^2\left(\frac{(\omega_{mk} - \omega)t}{2}\right)}{\left(\frac{\omega_{mk} - \omega}{2}\right)^2}$$

### Second-Order Expansion for $|c_n(t)|^2$
To compute probability to second order without assuming immediate resonance, we expand $c_k(t)$ and $c_m(t)$:

$$|c_k(t)|^2 = 1 + c_k^{(1)}(t) + c_k^{(1)*}(t) + |c_k^{(1)}(t)|^2 + \dots$$

Since $V_{kk} = 0$ for parity-symmetric unperturbed states ($x_{kk} = 0$), the first-order correction to the initial state $c_k^{(1)}(t) = 0$.

The conservation of total probability yields:

$$|c_k(t)|^2 = 1 - \sum_{m \neq k} |c_m^{(1)}(t)|^2$$

This confirms that weak external monochromatic fields cause probability transitions whose rates are directly dictated by matrix elements $x_{mk}$ of Heisenberg's matrix mechanics.



