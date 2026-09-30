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


In the Heisenberg picture of quantum mechanics, operators evolve in time while state vectors remain stationary. For an operator $\hat{A}_H(t)$, its time evolution is governed by the Heisenberg equation of motion:

$$\frac{d\hat{A}_H}{dt} = \frac{1}{i\hbar} [\hat{A}_H, \hat{H}_H] + \left(\frac{\partial \hat{A}}{\partial t}\right)_H$$

For fundamental operators like position $\hat{\mathbf{x}}_H$ and momentum $\hat{\mathbf{p}}_H$ (assuming no explicit time dependence):

$$\dot{\hat{\mathbf{x}}}_H = \frac{1}{i\hbar} [\hat{\mathbf{x}}_H, \hat{H}_H] = \frac{\hat{\mathbf{p}}_H}{m}$$

$$\dot{\hat{\mathbf{p}}}_H = \frac{1}{i\hbar} [\hat{\mathbf{p}}_H, \hat{H}_H] = -[\nabla V(\hat{\mathbf{x}})]_H$$

### Commutator Evaluation using Position Representation
Using $U_{t,t_0} = \exp\left(-\frac{i}{\hbar}\hat{H}(t - t_0)\right)$ to transform operators from Schrödinger to Heisenberg picture:

$$[\hat{p}_a, V(\hat{\mathbf{x}})]\psi = -i\hbar \partial_a (V \psi) + V (i\hbar \partial_a \psi) = -i\hbar (\partial_a V)\psi$$

Transforming back yields:

$$[\hat{p}_{a,H}, \hat{H}_H] = -i\hbar \left(\frac{\partial V}{\partial x_a}\right)_H$$

---

## 2. Matrix Components in Energy Basis

Evaluating the time derivative of matrix elements of an operator $\hat{A}_H(t)$ between stationary energy eigenstates $|j\rangle$ and $|k\rangle$ with energies $E_j, E_k$:

$$\langle j | \hat{A}_H(t) | k \rangle = \langle j | e^{\frac{i}{\hbar}\hat{H}t} \hat{A}_S e^{-\frac{i}{\hbar}\hat{H}t} | k \rangle = \exp\left( \frac{i}{\hbar} (E_j - E_k)t \right) A_{jk}(0)$$

Defining the transition frequency $\nu_{jk} = \frac{E_j - E_k}{\hbar} = \omega_{jk}$:

$$(A_H)_{jk}(t) = A_{jk}(0) e^{i \omega_{jk} t}$$

The time derivative of the matrix element gives:

$$\frac{d}{dt} \langle j | \hat{A}_H | k \rangle = i \omega_{jk} A_{jk}(t) = \frac{i}{\hbar} (E_j - E_k) A_{jk}(t)$$

Directly using the commutator definition:

$$\langle j | \frac{1}{i\hbar} [\hat{A}_H, \hat{H}_H] | k \rangle = \frac{1}{i\hbar} \sum_m \left( A_{jm} H_{mk} - H_{jm} A_{mk} \right) = \frac{1}{i\hbar} (E_k - E_j) A_{jk} = i \omega_{jk} A_{jk}$$

---

## 3. Equations of Motion in the Form of Hamilton's Equations

To express matrix equations analogous to classical canonical equations $\dot{q} = \frac{\partial H}{\partial p}$ and $\dot{p} = -\frac{\partial H}{\partial q}$, we write polynomial function traces or general operator derivatives.

Given $\hat{H} = \frac{\hat{\mathbf{p}}^2}{2m} + V(\hat{\mathbf{x}})$, we examine components:

$$\dot{x}_{a,jk} = \frac{p_{a,jk}}{m} = \left( \frac{\partial H}{\partial p_a} \right)_{jk}$$

$$\dot{p}_{a,jk} = -\left( \frac{\partial V}{\partial x_a} \right)_{jk} = -\left( \frac{\partial H}{\partial x_a} \right)_{jk}$$

### General Matrix Product Property
For any polynomial in operators, Born and Jordan showed that using trace properties and partial derivatives of matrix components:

$$\frac{\partial}{\partial A_{kl}} \mathrm{Tr}(\hat{A}\hat{B}\hat{C}...) = (\hat{B}\hat{C}...)_{lk}$$

This ensures that the quantum matrix equations preserves the structural symmetry of classical Hamiltonian dynamics.

---

## 4. Canonical Commutation Relations (CCR) in Energy Basis and Ladenburg Dispersion Formula

The fundamental canonical commutation relation is:

$$[\hat{x}, \hat{p}] = i\hbar \hat{I}$$

Evaluating matrix elements in the energy eigenbasis:

$$\langle j | [\hat{x}, \hat{p}] | k \rangle = \sum_m \left( x_{jm} p_{mk} - p_{jm} x_{mk} \right) = i\hbar \delta_{jk}$$

Since $p_{mk} = m \dot{x}_{mk} = i m \omega_{mk} x_{mk}$:

$$\sum_m \left( x_{jm} (i m \omega_{mk} x_{mk}) - (i m \omega_{jm} x_{jm}) x_{mk} \right) = i\hbar \delta_{jk}$$

For the diagonal elements ($j = k$):

$$m \sum_m \left( \omega_{mk} |x_{km}|^2 + \omega_{km} |x_{km}|^2 \right) = \hbar \quad \implies \quad \frac{2m}{\hbar} \sum_m \omega_{mk} |x_{km}|^2 = 1$$

### Connection to Ladenburg Dispersion Formula
In classical optics/early quantum theory, Ladenburg’s quantum dispersion formula for the oscillator strength $f_{km}$ associated with a transition $k \to m$ is defined as:

$$f_{km} = \frac{2m \omega_{km}}{\hbar} |x_{km}|^2$$

The diagonal CCR condition directly yields the **Thomas-Reiche-Kuhn (TRK) sum rule**:

$$\sum_m f_{km} = 1$$

This showed that Heisenberg's matrix mechanics naturally incorporated the empirically validated dispersion theory of Ladenburg, Kramers, and Kronig.

---

## 5. Historical Derivation of CCR: Bohr-Sommerfeld Quantization and Born-Kramers Reinterpretation

Historically, Heisenberg and Born arrived at the canonical commutation rule without initially postulating $[\hat{x}, \hat{p}] = i\hbar$. They reinterpreted classical periodic motion.

### 1. Bohr-Sommerfeld Quantization Rule
The classical action variable $J$ is quantized according to:

$$J = \oint p \, dq = \int_0^T p \, \dot{q} \, dt = n h$$

Using Fourier expansion for classical periodic motion with fundamental frequency $\omega$:

$$q(t) = \sum_\alpha q_\alpha(n) e^{i \alpha \omega t}, \quad p(t) = \sum_\alpha p_\alpha(n) e^{i \alpha \omega t}$$

The integral yields:

$$J = 2\pi \sum_\alpha \alpha \, q_{-\alpha}(n) p_\alpha(n) m = n h$$

### 2. Born-Kramers Reinterpretation Rule
Born recognized that derivatives with respect to the action quantum number $n$ should be replaced by quantum differences between discrete states $n$ and $n - \alpha$:

$$\frac{\partial \Phi(n)}{\partial n} \longrightarrow \frac{\Phi(n, n-\alpha) - \Phi(n-\alpha, n)}{\Delta n} = \Phi_{n, n-\alpha} - \Phi_{n-\alpha, n}$$

Applying this transition rule to $1 = \frac{d(nh)}{dn} = \frac{dJ}{dn}$:

$$1 = \frac{d}{dn} \left( 2\pi \sum_\alpha \alpha \, p_\alpha(n) q_{-\alpha}(n) \right)$$

Replacing differential increments with matrix transitions between discrete levels $n, m, k$:

$$1 = \frac{2\pi}{h} \sum_m \left( p_{nm} q_{mn} - q_{nm} p_{mn} \right) \cdot i$$

Multiplying through by $\frac{h}{2\pi} = \hbar$:

$$\sum_m (q_{nm} p_{mn} - p_{nm} q_{mn}) = i\hbar$$

which is precisely the diagonal component of $[\hat{q}, \hat{p}] = i\hbar$.

---

## 6. Application: The Linear Harmonic Oscillator

For the harmonic oscillator Hamiltonian $\hat{H} = \frac{\hat{p}^2}{2m} + \frac{1}{2}m\omega_0^2 \hat{x}^2$:

### Equations of Motion
$$\dot{\hat{x}} = \frac{\hat{p}}{m}, \quad \dot{\hat{p}} = -m\omega_0^2 \hat{x}$$

Taking the second time derivative:

$$\ddot{\hat{x}} + \omega_0^2 \hat{x} = 0$$

In matrix components:

$$(-\omega_{mn}^2 + \omega_0^2) x_{mn} = 0$$

Thus, non-zero matrix elements $x_{mn}$ can only exist if $\omega_{mn} = \pm \omega_0$, meaning transitions only occur between adjacent levels: $m = n \pm 1$.

### Matrix Elements & Energy Spectrum
Using the diagonal CCR $\frac{2m}{\hbar} \sum_m \omega_{mn} |x_{nm}|^2 = 1$:

$$\frac{2m\omega_0}{\hbar} \left( |x_{n, n+1}|^2 - |x_{n, n-1}|^2 \right) = 1$$

With the boundary condition $x_{0,-1} = 0$ for the ground state:

$$|x_{n, n+1}|^2 = \frac{\hbar}{2m\omega_0} (n+1)$$

The energy matrix elements give the discrete eigenvalues:

$$E_n = \hbar \omega_0 \left( n + \frac{1}{2} \right)$$

---

## 7. Transition Probabilities as Dipole Matrix Elements

When an atom interacts with an electromagnetic field, the interaction Hamiltonian is dominated by the electric dipole coupling:

$$\hat{V}(t) = - \hat{\mathbf{d}} \cdot \mathbf{E}(t) = - q \hat{\mathbf{x}} \cdot \mathbf{E}_0 \cos(\omega t)$$

The probability amplitude for a transition from state $|n\rangle$ to state $|m\rangle$ is dictated by the matrix element of the position/dipole operator:

$$x_{mn} = \langle m | \hat{x} | n \rangle$$

The transition rate $W_{n \to m}$ (spontaneous emission / absorption probability) is proportional to the square of the dipole matrix element:

$$W_{n \to m} \propto |\mathbf{d}_{mn}|^2 = q^2 |\langle m | \hat{\mathbf{x}} | n \rangle|^2$$

---

## 8. Perturbation Theory for Transition Probabilities in Weak Electric Fields

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



