(quantum-mechanics:atom-models:schrodinger:analytical-sln)=
# Schrodinger model - Mathematical details of the analytical solution

**Schrodinger equation** for the hydrogen atom in space basis reads

$$i \hbar \Psi(\mathbf{r},t) = \left[ - \frac{\hbar^2}{2 m} \nabla^2 - \frac{q^2}{4 \pi \varepsilon} \frac{1}{r} \right] \Psi(\mathbf{r},t) \ . $$

The **eigenproblem of the Hermitian operator** (projected onto space basis, as well) reads

$$E_n \Psi_n(\mathbf{r}) = - \frac{\hbar^2}{2 m} \nabla^2 \Psi_n(\mathbf{r}) - \frac{q^2}{4 \pi \varepsilon r} \Psi_n(\mathbf{r}) \ .$$

Given the symmetries of the system, the solution of the eigenproblem is evaluated using spherical coordinates $\{ r, \theta, \varphi \}$, and the method of separation of variables. Using **spherical coordinates**,

$$- \frac{\hbar^2}{2m} \left\{ \frac{1}{r^2} \partial_r \left( r^2 \partial_r \right) + \frac{1}{r^2 \sin\theta} \partial_\theta \left( \sin\theta \partial_\theta \right) + \frac{1}{r^2 \sin^2\theta} \partial_{\varphi\varphi} \right\} \Psi_n - \frac{q^2}{4\pi \varepsilon_0 r} \Psi_n = E_n \Psi_n$$

```{dropdown} Separation of variables, $\ \Psi_{nlm}(r, \theta, \varphi) = R_n(r) Y_{lm}(\theta, \varphi) \ $ 

With the **method of separation of variables**, we look for solutions in product form:

$$\Psi_{nlm}(r, \theta, \varphi) = R_n(r) Y_{lm}(\theta, \varphi) \ ,$$

and substituting into the Schrödinger equation:

$$\left( E_n + \frac{q^2}{4\pi \varepsilon_0 r} \right) R_n Y_{lm} = - \frac{\hbar^2}{2m} \left[ \frac{1}{r^2} \left( r^2 R_n' \right)' Y_{lm} + R_n \left( \frac{1}{r^2 \sin\theta} \partial_\theta \left( \sin\theta \partial_\theta Y_{lm} \right) + \frac{1}{r^2 \sin^2\theta} \partial_{\varphi\varphi} Y_{lm} \right) \right]$$

Dividing by $R_n Y_{lm}$, and multiplying by $r^2 \frac{2m}{\hbar^2}$,

$$0 = \underbrace{\frac{1}{R_n} (r^2 R_n')' + \frac{2m r^2}{\hbar^2} \left( E_n + \frac{q^2}{4\pi \varepsilon_0 r} \right)}_{f(r)} + \underbrace{\frac{1}{Y_{lm}} \left\{ \frac{1}{\sin\theta} \partial_\theta (\sin\theta \partial_\theta Y_{lm}) + \frac{1}{\sin^2\theta} \partial_{\varphi\varphi} Y_{lm} \right\}}_{g(\theta, \varphi)}$$

Since $f(r) + g(\theta, \varphi) = 0$, both terms must equal equal-and-opposite constant $C$ for all valid domains $r \in (0, +\infty)$, $\theta \in (0, \pi)$, $\varphi \in (0, 2\pi)$

$$C = f(r) = - g(\theta, \varphi) \ .$$

```

````{dropdown} Radial equation, and energy levels
:open:

The radial component determines the energy level,

$$E_n = - \frac{m q^4}{32 \pi^2 \varepsilon_0^2 \hbar^2} \frac{1}{n^2} \ .$$ (eq:atom:schrodinger:energy)

being $n \in \{ 1, 2, \dots \}$.

The radial distribution of the energy state functions is

$$R(\rho) = e^{-\rho/2} \rho^{\ell} L^{2 \ell+1}_{n-\ell-1}(\rho) \ ,$$

with $\rho = r \frac{\sqrt{-8 m E_n}}{\hbar}$ the non dimensional radius, $\ell \in \{ 0, 1, \dots, n-1 \}$, and $L_{p}^{k}(x)$ the solution of the associated Laguerre differential equation $x y'' + ( k + 1 - x ) y' + p y = 0$.

```{dropdown} Change of variables, and asymptotic behavior

Defining $C = \ell(\ell+1)$, and dividing the equation $f(r) = C$ by $r^2$, for the states with $E_n <0$,

$$\frac{1}{r^2} \frac{d}{dr} \left( r^2 R' \right) + \left[ \frac{2m}{\hbar^2} \left( E + \frac{q^2}{4\pi \varepsilon_0 r} \right) - \frac{\ell(\ell + 1)}{r^2} \right] R = 0$$

Defining the **dimensionless radial variable** $\rho = \kappa r$, so $\frac{d}{dr} = \kappa \frac{d}{d\rho}$, and factoring out $\kappa^2$

$$0 = \kappa^2 \left\{ \frac{1}{\rho^2} \frac{d}{d\rho} \left( \rho^2 \frac{dR}{d\rho} \right) + \left( \frac{2m E}{\hbar^2 \kappa^2} + \frac{2m q^2}{\hbar^2 \kappa \cdot 4\pi \varepsilon_0 \rho} - \frac{\ell(\ell + 1)}{\rho^2} \right) \right\} R$$

By choosing $\kappa^2 = -\frac{8 m E}{\hbar^2}$ (where $\kappa = \frac{\sqrt{-8 m E}}{\hbar}$ for $E < 0$), the first term inside the parentheses becomes $-1$. Defining the constant parameter $\rho_0$:

$$\rho_0 = \frac{2m q^2}{\hbar^2 \kappa \cdot 4\pi \varepsilon_0} = \frac{2m q^2}{\hbar^2 \sqrt{-8 m E} \cdot 4\pi \varepsilon_0} = \frac{q^2}{8\pi \varepsilon_0 \hbar} \sqrt{\frac{2m}{-E}} \ ,$$

the dimensionless radial equation simplifies to:

$$0 = \frac{1}{\rho^2} \frac{d}{d\rho} \left( \rho^2 \frac{dR}{d\rho} \right) + R \left[ - \frac{\ell(\ell + 1)}{\rho^2} - \frac{1}{4} + \frac{\rho_0}{\rho} \right]$$

Boundary conditions required for regular wavefunctions:

$$R(\rho = 0) < \infty, \quad R(\rho \to +\infty) = 0$$

```

```{dropdown} Asymptotic behavior for $\ r \rightarrow 0$, and $\ r \rightarrow +\infty$

**Large Distance Limit ($\rho \to +\infty$).** For large $\rho$, terms proportional to $\frac{1}{\rho}$ and $\frac{1}{\rho^2}$ become negligible:

$$\frac{1}{\rho^2} \frac{d}{d\rho} \left( \rho^2 R' \right) = R'' + \frac{2}{\rho} R' \sim R''$$

The equation reduces to:

$$R'' - \frac{1}{4} R \sim 0$$

General solution:

$$R(\rho) = A e^{-\rho/2} + B e^{\rho/2}$$

To satisfy the non-divergent boundary condition at infinity, set $B = 0$:

$$R(\rho) \sim e^{-\rho/2} \quad \text{as } \rho \to +\infty$$

**Small Distance Limit ($\rho \to 0$).** For $\rho \to 0$, the centrifugal term $\frac{\ell(\ell+1)}{\rho^2}$ dominates over the constant and $\frac{1}{\rho}$ terms:

$$R'' + \frac{2}{\rho} R' - \frac{\ell(\ell + 1)}{\rho^2} R \sim 0$$

Proposing a power-law ansatz $R(\rho) \sim \rho^s$:

$$s(s - 1) \rho^{s-2} + 2s \rho^{s-2} - \ell(\ell + 1) \rho^{s-2} = 0$$
$$s^2 + s - \ell(\ell + 1) = 0$$

Solving the quadratic characteristic equation for $s$:

$$s_{1,2} = \frac{-1 \mp \sqrt{1 + 4\ell(\ell + 1)}}{2} = \frac{-1 \mp (1 + 2\ell)}{2}$$
$$s_1 = \ell, \quad s_2 = -(\ell + 1)$$

Since $\ell \ge 0$, $s_2 = -(\ell + 1)$ leads to divergence at the origin $\rho \to 0$. Retaining only the physically acceptable solution $s = \ell$:

$$R(\rho) \sim \rho^\ell \quad \text{as } \rho \to 0$$


**Transformation & Differential Equation for $v(\rho)$.** Combining both asymptotic behaviors, we represent the full radial solution as:

$$R(\rho) = \rho^\ell e^{-\rho/2} v(\rho)$$

Writing out derivatives of $R(\rho)$:

$$R' = \left( \ell \rho^{\ell-1} - \frac{1}{2} \rho^\ell \right) e^{-\rho/2} v + \rho^\ell e^{-\rho/2} v'$$

After expanding $\frac{1}{\rho^2} \frac{d}{d\rho} \left( \rho^2 R' \right) + R \left[ - \frac{\ell(\ell + 1)}{\rho^2} - \frac{1}{4} + \frac{\rho_0}{\rho} \right] = 0$:

$$= e^{-\rho/2} \Big\{ \rho^\ell v'' + v' \left[ 2\ell \rho^{\ell-1} - \frac{1}{2} \rho^\ell + 2 \rho^{\ell-1} \right] + v \left[ \rho^\ell \ell(\ell+1) - \rho^{\ell+1} \left( \ell + 1 \right) + \frac{1}{4} \rho^{\ell+2} - \ell(\ell+1) \rho^{\ell} - \frac{1}{4} \rho^{\ell+2} + \rho_0 \rho^{\ell+1} \right] \Big\} = 0$$

Dividing out non-zero factor $\rho^{\ell-1} e^{-\rho/2}$:

$$\rho v''(\rho) + [2(\ell + 1) - \rho] v'(\rho) + (\rho_0 - \ell - 1) v(\rho) = 0$$


```

```{dropdown} Polynomial expansion, energy quantization $\ E_n \ $ and radial distribution $\ R_n(\rho)$

Starting from the transformed radial equation:

$$\rho v''(\rho) + [2(\ell + 1) - \rho] v'(\rho) + (\rho_0 - \ell - 1) v(\rho) = 0$$

Looking for a power series solution:

$$\begin{aligned}
    v(\rho) & = \sum_{k=0}^{\infty} c_k \rho^k  \\
   v'(\rho) & = \sum_{k=0}^{\infty} k c_k \rho^{k-1} \\
  v''(\rho) & = \sum_{k=0}^{\infty} k(k-1) c_k \rho^{k-2} \\
\end{aligned}$$

Substituting into the differential equation:

$$\sum_{k=0}^{\infty} k(k-1) c_k \rho^{k-1} + \sum_{k=0}^{\infty} 2(\ell + 1) k c_k \rho^{k-1} - \sum_{k=0}^{\infty} k c_k \rho^k + (\rho_0 - \ell - 1) \sum_{k=0}^{\infty} c_k \rho^k = 0$$

Shift indices to group terms by power $\rho^k$:

$$\sum_{k=0}^{\infty} \Big\{ (k+1)(k) c_{k+1} + 2(\ell + 1)(k+1) c_{k+1} - k c_k + (\rho_0 - \ell - 1) c_k \Big\} \rho^k = 0$$


**Recurrence Relation.** Equating coefficients to zero yields the recurrence relation for $c_k$:

$$c_{k+1} = c_k \frac{k + \ell + 1 - \rho_0}{(k + 1)(k + 2\ell + 2)}$$


**Asymptotic Behavior & Series Termination.** If the power series does not terminate, as $k \to +\infty$:

$$\frac{c_{k+1}}{c_k} \longrightarrow \frac{1}{k}$$

This asymptotic behavior matches that of the exponential expansion $e^\rho \sim \sum \frac{\rho^k}{k!}$ and thus $\frac{c_{k+1}}{c_k} = \frac{1}{k+1} \sim \frac{1}{k}$.
Thus, an infinite series $v(\rho) \sim e^\rho$, would lead to $R(\rho) \sim e^{-\rho/2} e^\rho = e^{\rho/2}$, which diverges as $\rho \to +\infty$.
Thus, in order to maintain physical normalizability, the series must terminate at a maximum power $k_{\max} = N$:

$$c_{N+1} = 0 \implies N + \ell + 1 - \rho_0 = 0 \implies \rho_0 = N + \ell + 1 \equiv n$$

where:
* $N \ge 0$ is the radial quantum number.
* $n = N + \ell + 1$ is the **Principal Quantum Number** ($n \ge 1$).
* $\forall n$, the orbital angular momentum quantum number satisfies $0 \le \ell \le n - 1$.

**Energy Quantization.** Recalling the definition of $\rho_0$, $n = \rho_0 = \sqrt{\frac{2m}{-E}} \frac{q^2}{4\pi \varepsilon_0 \hbar}$, and solving for the bound state energies $E_n$ ($E < 0$), the relation between the energy $E_n$ of the $n^{th}$ energy level and the principal quantum number $n$ follows

$$E_n = - \frac{m q^4}{32 \pi^2 \varepsilon_0^2 \hbar^2} \frac{1}{n^2} \ .$$ (eq:atom:schrodinger:energy:details)

**Remark.** The value of energy $E_n$ of Schrodinger model coincides with the value {eq}`eq:atom:bohr:energy` of the energy produced by [Bohr model](quantum-mechanics:atom-models:bohr).

**Radial solution.** Putting everything together, the radial part of the solution reads

$$R(\rho) = e^{-\rho/2} \rho^{\ell} L^{2 \ell+1}_{n-\ell-1}(\rho) \ ,$$

being $L_{p}^{k}(x)$ the solution of the associated Laguerre differential equation $x y'' + ( k + 1 - x ) y' + p y = 0$.

```
````

````{dropdown} Azimuthal and polar equations
:open:

```{dropdown} Further separation of variables, $\ Y_{\ell m}(\theta, \varphi) = \Theta(\theta) \Phi(\varphi) \ $ 
:open:

With $Y(\theta, \varphi) = \Theta(\theta) \Psi(\varphi)$, the equation 

$$
\frac{1}{Y_{lm}} \left\{ \frac{1}{\sin\theta} \partial_\theta (\sin\theta \partial_\theta Y_{lm}) + \frac{1}{\sin^2\theta} \partial_{\varphi\varphi} Y_{lm} \right\} = - \ell ( \ell + 1 ) \ . 
$$

becomes - after multipyling by $\sin^2 \theta$,

$$\underbrace{\frac{\sin \theta}{\Theta} \left( \sin \theta \, \Theta' \right)' + \ell ( \ell + 1 ) \, \sin^2 \theta}_{F(\theta)} = -\underbrace{\frac{\Phi''}{\Phi}}_{G(\varphi)} \ ,$$

and thus

$$F(\theta) = - G(\varphi) = m_\ell^2 \ ,$$

with a non-negative constant $m_{\ell}^2$ in order to match periodic conditions for $\Phi(\varphi = 0) = \Phi(\varphi = 2 \pi)$.

```

```{dropdown} Azimuthal equation
:open:

$$\Phi'' + m_\ell^2 \Phi = 0 \ ,$$

whose solution is $\Phi(\varphi) \propto \exp \left( \mp i m_{\ell} \varphi \right)$. In order to satisfy periodic conditoins, $m_{\ell} \in \mathbb{Z}$. This parameter will be furthered constrained later, in the solution of the polar equation, to be $m_{\ell} \in \{ - \ell, -\ell+1, \dots, \ell \}$, with $\ell \in \mathbb{N}$. Thus, selecting only the independent solutions, the azimuthal distribution of the eigenfunctions of the Hamiltonian is 

$$\Phi(\varphi) \propto \exp\left( i m_{\ell} \varphi \right) \ , \quad m_{\ell} \in \{ - \ell, -\ell+1, \dots \ell \} \ .$$


```

```{dropdown} Polar equation
:open:

Multiplying the equation $F(\theta) = m_{ell}^2$ by $\Theta$, the polar equation becomes,

$$ \sin \theta \left( \sin \theta \, \Theta' \right)' + \left[ \ell ( \ell + 1 ) \, \sin^2 \theta - m_{\ell}^2 \right] \Theta = 0 \ .$$

```

```{dropdown} Polar equation as an associated Legendre equation
:open:

Dividing by $\sin^2 \theta= 1 - \cos^2 \theta$, the second term can be immediately recast as the second term in the associated Legendre equation, if $x = \cos \theta$.

As $\frac{d x}{d \theta} = - \sin \theta$, then $\frac{d}{d\theta} = \frac{d x}{d \theta} \frac{d}{d x} = - \sin \theta \frac{d}{d x}$, the first term - divided by $\sin^2 \theta$ - becomes

$$-\frac{1}{\sin^2 \theta} \sin^2 \theta \dfrac{d}{dx} \left( - \sin^2 \theta \dfrac{d}{dx} \Theta \right) = \dfrac{d}{dx}\left[ ( 1 - x^2) \dfrac{d}{dx} \Theta \right]$$

Thus the polar equation can be recast as

$$0 = \frac{d}{dx} \left[ ( 1 - x^2 ) \dfrac{d \Theta}{dx} \right] + \left[ \ell(\ell+1) - \frac{m_\ell^2}{1 - x^2} \right] \Theta  \ ,$$

i.e. as the associated Legendre equation whose solution (see below) is $\Theta(x) = P_\ell^{m_{\ell}}(x)$, for $m_{\ell} \in \{ - \ell, \dots, \ell\}$, $\ell \in \mathbb{N}$.

```

```{dropdown} Legendre differential equation and associated Legendre equation
:open:

**Legendre differential equations** read

$$\begin{aligned}
  0
  & = (1- x^2) P_n''(x) - 2 x P_n'(x) + n(n+1) P_n(x) =  \quad , \qquad x \in [-1, 1] \\
  & = \dfrac{d}{dx} \left[ ( 1-x^2 ) P_n'(x) \right] + n(n+1) P_n(x) \ ,
\end{aligned}$$

with the solution $P_n(x)$ be the Legendre polynomial. The **associated Legendre differential equations** are defined as

$$\begin{aligned}
  0
  & = \dfrac{d}{dx} \left[ ( 1-x^2 ) P_n'(x) \right] + \left[ n(n+1) - \frac{m^2}{1-x^2} \right] P_n(x) \quad , \qquad x \in [-1, 1] \\
\end{aligned}$$

and the solution reads $P_{n}^{m}(x) = (-1)^{m} \left( 1 - x^2 \right)^{\frac{m}{2}} \dfrac{d^m}{dx^m} P_{n}(x)$, for $m \ge 0$.
The soutions for $m < 0$ are defined via symmetry conditions, or Rodrigues' formula, as $P_{\ell}^{-m} = (-1)^{m} \frac{(\ell-m)!}{(\ell+m)!} P_{\ell}^{m}(x)$, see [Wikipedia: associated Lagendre polynomials](https://en.wikipedia.org/wiki/Associated_Legendre_polynomials).

```



