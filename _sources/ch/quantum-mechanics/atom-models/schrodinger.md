(quantum-mechanics:atom-models:schrodinger)=
# Schrodinger model

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

```{dropdown} Change of variables, and asymptotic behavior
:open:

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

```{dropdown} Asymptotic behavior
:open:


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

```{dropdown}
:open:

# Radial Equation & Energy Quantization

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

$$E_n = - \frac{m q^4}{32 \pi^2 \varepsilon_0^2 \hbar^2} \frac{1}{n^2} \ .$$

**Radial solution.** Putting everything together, the radial part of the solution reads

$$R(\rho) = e^{-\rho/2} \rho^{\ell} L^{2 \ell-1}_{n-\ell-1}(\rho) \ .$$

```

```{dropdown} Further separation of variables, $\ Y_{lm}(\theta, \varphi) = \Theta(\theta) \Phi(\varphi) \ $ 
:open:


```

```{dropdown} Azimuthal equation
:open:

```

```{dropdown} Polar equation
:open:

```
