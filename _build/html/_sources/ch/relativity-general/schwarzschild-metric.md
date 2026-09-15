(relativity-general:notes:examples:schwarzschild)=
# Schwarzschild metric

**Spatially spherically symmetric** and **static vacuum** solution of the Einstein equation, representing the exterior gravitational field of a **non-rotating**, **uncharged** massive body.


```{dropdown} Vacuum equation
:open:

Without mass density and electric charge and current, $\mathsf{T} = \mathsf{0}$. From the expression of {eq}`eq:einstein:alternative`, it immediately follows, $\mathsf{R} = \mathsf{0}$.

```



## Metric Ansatz & Symmetry Assumptions

The four coordinates used to parametrize the space-time are $(t, r, \theta, \phi)$. The two physical symmetry constraints in Schwarzschild solution of EFE are

1. **Spherical Symmetry:** the spatial geometry is invariant under rotation, s.t. the angular part of the metric is given by the standard round metric on $S^2$, $d\Omega^2 = d \theta^2 + \sin^2 \theta \, d\phi^2$

2. **Staticity:** the metric coefficients are independent of the time coordinate $t$ ($\partial_t g_{\mu
u} = 0$); the further assumption that the line element is invariant under time reversal eliminates cross-terms such as $dt\,dr$.

Under these assumptions, the general line element can be parameterized using two undetermined functions of radius, $A(r)$ and $B(r)$:

$$ds^2 = -e^{2A(r)} c^2 dt^2 + e^{2B(r)} dr^2 + r^2 \left( d \theta^2 + \sin^2 \theta \, d\phi^2 \right)$$

**Remark.** Using exponential parameterizations $e^{2A(r)}$ and $e^{2B(r)}$ ensures that $g_{tt} < 0$ and $g_{rr} > 0$ outside any horizon. **todo** *Add some remark/examples about the role of time, and its consequence on metrics*

From the choosen parametrization, the non-zero covariant components of the metric tensors are

$$\begin{aligned}
  g_{tt} & = - e^{- 2 A(r)} c^2 \\
  g_{rr} & =   e^{  2 B(r)}     \\
  g_{\theta \theta} & = r^2    \\
  g_{\phi \phi} & =  r^2 \sin^2 \theta     \\
\end{aligned}$$

As the metric tensor is diagonal, it's contravariant components are just the inverse of its covariant components.

## Christoffel Symbols

The Christoffel symbols of the second kind are computed via the expression {eq}`eqn:differential-geometry:gamma:g`,

$$\Gamma_{ac}^{b} = \frac{1}{2} g^{bd} \left( \partial_c g_{ad} + \partial_a g_{dc} - \partial_{d} g_{ac} \right) \ .$$ 

Writing the derivative w.r.t. $r$ as $\partial_r A(r) = A'(r)$

* $\Gamma^t_{tr} = \Gamma^t_{rt} = \frac{1}{2} g^{t d} \left( \partial_r g_{t d} + \partial_t g_{dr} - \partial_d g_{tr}  \right) = - \frac{1}{2} e^{2 A} c^{-2} \cdot ( - 2 A' ) e^{-2A} c^2 = A'$
* $\Gamma^r_{tt} = A' e^{2(A-B)} c^2$
* $\Gamma^r_{rr} = B'$
* $\Gamma^r_{\theta \theta} = -r e^{-2B}$
* $\Gamma^r_{\phi\phi} = -r \sin^2  \theta \, e^{-2B}$
* $\Gamma^\theta_{r \theta} = \Gamma^\theta_{\theta r} = \frac{1}{r}$
* $\Gamma^\theta_{\phi\phi} = -\sin\theta\cos \theta$
* $\Gamma^\phi_{r\phi} = \Gamma^\phi_{\phi r} = \frac{1}{r}$
* $\Gamma^\phi_{\theta\phi} = \Gamma^\phi_{\phi\theta} = \cot \theta$


## Components of the Ricci Tensor

The Ricci tensor is defined by contracting the Riemann curvature tensor:

$$R_{\mu
u} = \partial_{\lambda}\Gamma^{\lambda}_{\mu
u} - \partial_{
u}\Gamma^{\lambda}_{\mu\lambda} + \Gamma^{\lambda}_{\mu
u}\Gamma^{\sigma}_{\lambda\sigma} - \Gamma^{\sigma}_{\mu\lambda}\Gamma^{\lambda}_{
u\sigma}$$

Evaluating the non-zero independent components yields:

* **Time-Time Component ($R_{tt}$)**

   $$R_{tt} = e^{2(A-B)} c^2 \left[ A'' + (A')^2 - A'B' + \frac{2A'}{r} \right]$$

* **Radial-Radial Component ($R_{rr}$)**

   $$R_{rr} = -A'' - (A')^2 + A'B' + \frac{2B'}{r}$$

* **Angular Component ($R_{\theta \theta}$)**

   $$R_{\theta \theta} = 1 - e^{-2B} \left[ 1 + r(A' - B') \right]$$

**Remarks.**
* The $R_{\phi\phi}$ component yields $R_{\phi\phi} = R_{\theta \theta} \sin^2 \theta$, providing no independent equation).
* The non-diagonal components are identically zero (**todo** *prove it!*)



## Solving the Differential Equations



**Combining $R_{tt}$ and $R_{rr}$** (linear combination $e^{-2(A-B)} \frac{R_{tt}}{c^2} + R_{rr} = 0$) immediately gives

$$A'(r) = -B'(r) \ .$$

and integrating with respect to $r$,

$$A(r) + B(r) = C = \text{const.}$$

**Boundary conditions at infinity.** To satisfy the boundary condition of asymptotic flatness—that spacetime approaches flat Minkowski space as $r \rightarrow \infty$, then

$$\begin{aligned}
  g_{tt} & = - e^{2A(r)} \rightarrow - 1 && A(r) \rightarrow 0 \\
  g_{rr} & =   e^{2B(r)} \rightarrow   1 && B(r) \rightarrow 0
\end{aligned}$$

and thus $C = 0$, and $A(r) = - B(r)$.

**Solving for $A(r)$ via $R_{\theta \theta}$.** Substituting $B' = -A'$ and $e^{-2B} = e^{2A}$ into $R_{\theta \theta} = 0$:

$$\begin{aligned}
  0 
  & = R_{\theta \theta} = \\
  & = 1 - e^{2A} \left( 1 + 2rA' \right) = \\
  & = 1 - \dfrac{d}{dr} \left( r e^{2 A} \right)  \ ,
\end{aligned}$$

and thus, integrating in $r$,

$$r e^{2 A(r)} = r + C \ .$$

or

$$e^{2A(r)} = 1 + \frac{C}{r}$$

where $C$ is a constant of integration. Since $e^{2B(r)} = e^{-2A(r)}$, it follows $e^{2B(r)} = \left(1 + \frac{C}{r} \right)^{-1}$.


## Determining the Integration Constant $C$ (The Newtonian Limit)

To determine $C$, we examine the metric in the weak-field, low-velocity limit ($r \to \infty$). In this limit, general relativity recovers **Newtonian gravity**, as shown in [classical limit](relativity-general:notes:einstein-equation:classical-limit),

$$g_{tt} = \eta_{tt} + h_{tt} \approx - 1 - \frac{2}{c^2} \Phi \ ,$$

where $\Phi(r) = - \frac{GM}{r}$ is the Newtonian gravitational potential of a central mass $M$. Equating the two expression of the coefficient $g_{tt}$

$$g_{tt} = -e^{2A(r)} = - 1 - \frac{C}{r} = - 1 + \frac{2}{c^2} \frac{G M}{r} $$

and thus

$$C = - \frac{2GM}{c^2} \ .$$

Defining the **Schwarzschild radius** $r_s := \frac{2GM}{c^2}$, the expression of **Schwarzschild metric** becomes

$$
ds^2 =
- \left(1 - \frac{r_s}{r} \right) c^2 dt^2 + 
  \left(1 - \frac{r_s}{r} \right)^{-1} dr^2 + r^2 d \theta^2 + r^2 \sin^2 \theta \, d\phi^2 \ .
$$


## Special Case: Complete Vacuum ($M = 0$)

If the spacetime contains no mass ($M = 0$), the Minkowski flat spacetime follows

$$ds^2 = -c^2 dt^2 + d r^2 + r^2 d \theta^2 + r^2 \sin^2 \theta \, d\phi^2 = - c^2 dt^2 + |d \vec{r}|^2 \ , $$

or, using the common transformation between spherical and Cartesian space coordinates,

$$\begin{cases}
  t = t \\
  x = r \sin \theta \cos \phi \\
  y = r \sin \theta \sin \phi \\
  z = r \cos \theta \ ,
\end{cases}$$

$$ds^2 = - c^2 dt^2 + dx^2 + dy^2 + dz^2 \ .$$



