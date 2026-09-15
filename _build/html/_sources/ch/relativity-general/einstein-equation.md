(relativity-general:notes:einstein-equation)=
# Einstein's equation

Idea:
1. Try with **the simplest relation** between momentum-energy tensor $\mathsf{T}$ and a second order tensor representing the geometry of space, i.e. **proportionality** with Ricci's curvature tensor $\mathsf{R}$

   $$\mathsf{R} = \kappa \mathsf{T} \ .$$

   **Remark.** This relationship doesn't agree with local energy-momentum balance $\nabla \cdot \mathsf{T} = \mathbf{0}$, as $\nabla \cdot \mathsf{R} \ne \mathbf{0}$,

   $$\begin{aligned}
     \nabla_{\mu} R^{\mu}_{\ \ \nu} & = \frac{1}{2} \nabla_{\nu} R \\
     \nabla_{\mu} R^{\mu \sigma} & = \nabla_{\mu} \left( g^{\sigma \nu} R^{\mu}_{\ \ \nu} \right) = g^{\sigma \nu} \nabla_{\mu} R^{\mu}_{\ \ \nu} = \frac{1}{2}  g^{\sigma \nu }\nabla_{\nu} R = \nabla_{\mu} \left( \frac{1}{2} g^{\sigma \mu} R \right) , \\
   \end{aligned}$$

   as the covariant derivative of the metric components of the metric tensor are identically zero. Moving the extreme terms of this equality on the same side of the equal sign, $\nabla_{\mu} \left( R^{\mu \sigma} - \frac{1}{2} g^{\mu \sigma} R \right) = 0$.

   ```{dropdown} Covariant derivative of the metric tensor
   :open:

   $$\begin{aligned}
     \nabla_{\nu} g_{\mu \eta}
     & = \partial_{\nu} g_{\mu \eta} - \Gamma_{\nu \mu}^{\sigma} g_{\sigma \eta} - \Gamma_{\nu \eta}^{\sigma} g_{\mu \sigma} = 0 \ ,
   \end{aligned}$$

   as $\partial_{\nu} g_{\mu \eta} = \Gamma_{\nu \mu}^{\sigma} g_{\sigma \eta} + \Gamma_{\nu \eta}^{\sigma} g_{\mu \sigma}$ (see the derivative of the components of the metric tensor in [Differential geometry for general relativity](relativity-general:notes:differential-geometry).

   ```

2. Correct the relation, replacing Ricci's tensor with its divergence-free part

   $$R^{\mu \sigma} - \frac{1}{2} g^{\mu \sigma} R = \kappa T^{\mu \sigma} \ ,$$

   or

   $$\mathsf{R} - \frac{1}{2} \mathsf{g} R = \kappa \mathsf{T} \ .$$

3. Check against the classical limit, to find:
   * if Newton gravitation is the classical limit of general relativity
   * the values of the constants involved in the model, $\kappa$

   Under some assumptions:
   * **weak gravitation** for the linearization of the metric tensor $g_{\mu \nu} = \eta_{\mu \nu} + h_{\mu \nu}$ around Minkowski flat time-space (here $\eta_{\mu \nu}$ describing Minkowski metrics).
   * **pressure-less mass distribution at rest**
   * **mass** distribution "at rest" (w.r.t. the "quasi inertial observer")

(relativity-general:notes:einstein-equation:alternative)=
## Alternative expression of Einstein's equations

Let's evaluate the trace of $\mathsf{R}$, i.e. $R = R^{\sigma}_{\ \ \sigma}$ as a function of the trace of $\mathsf{T}$.

$$\begin{aligned}
  R
  & := R^{\sigma}_{\ \ \sigma} = \\
  & = g_{\sigma \varphi} R^{\varphi \sigma} = \\
  & = g_{\sigma \varphi} \left( \frac{1}{2} g^{\varphi \sigma} R + \kappa T^{\varphi \sigma} \right) = 2 R + \kappa T \\
\end{aligned}$$

and thus the relation $R = - \kappa T$ holds between the trace of Ricci and energy-momentum tensors (here $g_{\sigma \varphi} g^{\sigma \varphi} = \delta_{\sigma}^{\sigma} = 4$ in the 4-dimensional time-space). Thus, Einstein equation can be recast as

 $$\mathsf{R} = \kappa \left( \mathsf{T} - \frac{1}{2} \mathsf{g} \, T \right) \ .$$ (eq:einstein:alternative)

(relativity-general:notes:einstein-equation:classical-limit)=
## Classical limit

**1. Linearization of the metric tensor.** $g_{\mu \nu} = \eta_{\mu \nu} + h_{\mu \nu}$, and the inverse (linearized) relation gives $g^{\mu \nu} = \eta^{\mu \nu} - h^{\mu \nu}$

**2. Linearization of Christoffel symbols.**

$$\Gamma_{00}^{i} = - \frac{1}{2} \partial_i h_{00}$$

in the static limit, $\partial_0 \equiv 0$, for the spatial components, $i = 1:3$.

**3. Linearization of the geodesics equation.**

$$\ddot{q}^{\mu} + \Gamma_{\nu \sigma}^{\mu} \dot{q}^{\nu} \dot{q}^{\mu} = 0$$

For $\mu = i = 1:3$, as the $\tau \sim t$ in the slow-regime limit, and $q^0 \sim c t$ and $q^i = x_i$,

$$\ddot{x}_i = - c^2 \Gamma_{00}^i = \frac{c^2}{2} \partial_i h_{00} \ .$$

This equation must be compared with the dynamical equation of the Newtonian mechanics, $\ddot{\vec{r}} = - \nabla \Phi$. In order to get the same equation, $\partial_i h_{00} = - \frac{2}{c^2} \partial_i \Phi$, and thus - except for an arbitrary constant (irrelevant) - $h_{00} = - \frac{2}{c^2} \Phi$.

**4. Linearized Einstein equation**, with energy-momentum tensor (of the pressure-less medium) $T^{\mu \nu} = \rho c^2 \delta^{\mu}_0 \delta^{\nu}_0$, so that its trace reads $T = \rho c^2$. Thus the linearized $00$ component of Einstein equation reads

$$R_{00} = \kappa \left( \rho c^2 - \frac{1}{2} \rho c^2 \right) = \kappa \frac{1}{2} \rho c^2$$

**5. Linearized relation between curvature tensor and the linearized metrics.**

$$R_{00} = \partial_i \Gamma^{i}_{00} = - \frac{1}{2} \partial_{ii} h_{00} = \frac{1}{c^2} \nabla^2_{\vec{r}} \Phi$$

**6. Comparison of the two expressions of $R_{00}$.** 

$$\frac{\kappa}{2} \rho c^2 = \frac{1}{c^2} \nabla^2_{\vec{r}} \Phi \ , $$

or rearranging,

$$\nabla^2 \Phi = \frac{\kappa c^4}{2} \rho \ .$$

By direct comparison with the Poisson equation for Newtonian gravitation, $\nabla^2 \Phi = 4 \pi G \rho$, it follows that

$$\kappa = \frac{8 \pi G}{c^4} \ .$$

