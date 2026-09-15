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

