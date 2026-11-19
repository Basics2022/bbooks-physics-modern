(general-relativity:geodesics)=
# Geodesics

A worldline is the a one-dimensional curve describing the trajectory of a point in the four-dimensional spacetime. Events in the four-dimensional spacetime can be parametrized with a set of coordinates $\{ q^\mu \}$ as $X( q^{\mu} )$.[^x-not-a-vector] A worldine $\ell$ can be represented with the 1-parameter equation $X_{\ell}(\lambda) = X\left( q^{\mu}_{\ell}(\lambda) \right)$.

[^x-not-a-vector]: The function $X( q^{\mu} )$ represents the events in the spacetime as points on a manifold. In general events can't be represented as a (position) vector if the space is not flat, or if the $n$-dimensional manifold is not embedded in a $n+1$-dimensional space.

The line element in space time can be defined as $d \mathbf{X} = d \lambda \, \partial_\lambda q^{\mu} \, \partial_{\mu} X$ $= d \lambda \, \partial_\lambda q^{\mu} \, \mathbf{b}_{\mu}$, with $\mathbf{b}_{\mu} = \partial_{\mu} X$ the vectors of the natural basis induced by the parametrization of the spacetime. The magnitude of the line element reads

$$ds^2 = d \mathbf{X} \cdot d \mathbf{X} = d\lambda^2 \, g_{\mu \nu}\left(q^\varphi(\lambda)\right) \, \partial_\lambda q^{\mu}(\lambda) \, \partial_\lambda q^{\nu}(\lambda) \ ,$$

with $g_{\mu \nu} := \mathbf{b}_{\mu} \cdot \mathbf{b}_{\nu}$ the components of the metric tensor in the natural basis induced by the parametrization of space.

(general-relativity:geodesics:equation)=
## Geodesics equation

A geodesics between two events $P_0$, $P_1$ in spacetime is the worldline connecting the events for which the $\Delta s = \int_{P_0}^{P_1} ds$ is stationary. Using a parameters $\lambda$ that's affine with the arc-length, the equation of the geodesics reads

$$\ddot{q}^{\mu} + \Gamma^{\mu}_{\nu \sigma} \dot{q}^\nu \dot{q}^\sigma = 0 \ .$$

Defining the 4-velocity of a point $P$ in spacetime as  w.r.t. the affine parameter $\lambda$ - remark: an affine parameter just differs from the arc-length by an offset and a scale parameter, like a different choice of unit of measurements,

$$\mathbf{U} = \partial_\lambda X\left( q^\mu(\lambda) \right) = \partial_\lambda q^{\mu} \, \partial_{q^{\mu}} X = \dot{q}^{\mu} \mathbf{b}_{\mu} = U^{\mu} \mathbf{b}_{\mu} \ ,$$

it readily follows that a geodesics is a worldine s.t. the acceleration on that orbit is zero, $\partial_\lambda \mathbf{U} = \mathbf{0}$, as the expression of the acceleration induced by the choice of the coordinates $\{ q^\mu \}$ is

$$\mathbf{A} := \partial_\lambda \mathbf{U} = \partial_\lambda \left( \dot{q}^\mu \mathbf{b}_{\mu} \right) = \left\{ \ddot{q}^{\mu} + \Gamma^{\mu}_{\nu\sigma} \dot{q}^\nu \dot{q}^\sigma \right\} \mathbf{b}_{\mu} \ .$$


````{dropdown} Geodesics from variational principles
:open:

Or move this to [Math: Calculus of variations: examples](https://basics2022.github.io/bbooks-math-miscellanea/ch/calculus-variations/examples.html)

$$\begin{aligned}
  0
  & = \delta \int_{\lambda_0}^{\lambda_1} ds
    = \delta \int_{\lambda_0}^{\lambda_1} \sqrt{ g_{\mu \nu}(q^\varphi(\lambda)) \, \dot{q}^{\mu}(\lambda) \dot{q}^{\nu}(\lambda) } \, d \lambda 
    = \delta \int_{\lambda_0}^{\lambda_1} \dot{s}(\lambda) \, d \lambda 
\end{aligned}$$
Lagrange equation reads

$$\frac{d}{d \lambda} \dfrac{\partial \mathcal{L}}{\partial \dot{q}^\xi} - \dfrac{\partial \mathcal{L}}{\partial q^\xi} = 0 \ .$$

The evaluation of the derivatives gives

$$\frac{\partial \mathcal{L}}{\partial q^\xi} = \frac{1}{2} \left( g_{\mu \nu} \dot{q}^{\mu} \dot{q}^{\nu} \right)^{-\frac{1}{2}} \partial_{\xi} g_{\mu \nu} \dot{q}^{\mu} \dot{q}^{\nu} = \frac{1}{2} \dot{s}^{-1} \partial_{\xi} g_{\mu \nu} \dot{q}^{\mu} \dot{q}^{\nu}$$

$$\begin{aligned}
  \frac{d}{d \lambda} \frac{\partial \mathcal{L}}{\partial \dot{q}^\xi} 
  & = \dfrac{d}{d\lambda} \left[ \frac{1}{2} \left( g_{\sigma \eta} \dot{q}^{\sigma} \dot{q}^{\eta} \right)^{-\frac{1}{2}} \left( g_{\xi \nu} \dot{q}^{\nu} + g_{\mu \xi} \dot{q}^{\mu} \right) \right] = \\
  & = \dfrac{d}{d\lambda} \left[ \dot{s}^{-1} \, g_{\xi \nu} \, \dot{q}^{\nu}  \right] = \\
  & = \left( \dot{q}^\zeta \partial_{q^\zeta} \dot{s}^{-1} + \ddot{q}^\zeta \partial_{\dot{q}^\zeta} \dot{s}^{-1} \right) g_{\xi \nu} \dot{q}^{\nu} + \dot{s}^{-1} \left( \dot{q}^{\zeta} \partial_{\zeta} g_{\xi \nu} \dot{q}^{\nu} + g_{\xi \nu} \ddot{q}^{\nu} \right) = \\
  & = - \dot{s}^{-2} \ddot{s} \, g_{\xi \nu} \dot{q}^{\nu} + \dot{s}^{-1} \left( \partial_{\zeta} g_{\xi \nu} \dot{q}^{\nu} \dot{q}^{\zeta} + g_{\xi \nu} \ddot{q}^{\nu} \right) \ .
\end{aligned}$$

Putting everything together,

$$\begin{aligned}
  0
  & = \dfrac{d}{d \lambda} \frac{\partial \mathcal{L}}{\partial \dot{q}^\xi} - \frac{\partial \mathcal{L}}{\partial q^\xi} = \\
  & = - \dot{s}^{-2} \ddot{s} \, g_{\xi \mu} \dot{q}^{\mu} + \dot{s}^{-1} \left( \partial_{\mu} g_{\xi \nu} \dot{q}^{\mu} \dot{q}^{\nu} + g_{\xi \mu} \ddot{q}^{\mu} \right) - \frac{1}{2} \dot{s}^{-1} \partial_{\xi} g_{\mu \nu} \dot{q}^{\mu} \dot{q}^{\nu} = \\
  & = - \dot{s}^{-2} \ddot{s} \, g_{\xi \mu} \dot{q}^{\mu} + \dot{s}^{-1} \left[  g_{\xi \mu} \ddot{q}^{\mu} + \left( \partial_{\mu} g_{\xi \nu} - \frac{1}{2} \partial_{\xi} g_{\mu \nu} \right) \dot{q}^{\mu} \dot{q}^{\nu} \right] = \\
  & = - \dot{s}^{-2} \ddot{s} \, g_{\xi \mu} \dot{q}^{\mu} + \dot{s}^{-1} \left\{ \, g_{\xi \mu} \ddot{q}^{\mu} + \left( \Gamma^{\sigma}_{\mu \xi} g_{\sigma \nu} + \Gamma^{\sigma}_{\mu \nu} g_{\xi \sigma} - \frac{1}{2} \Gamma_{\xi \mu}^{\sigma} g_{\sigma \nu} - \frac{1}{2} \Gamma_{\xi \nu}^{\sigma} g_{\sigma \mu} \right) \dot{q}^{\mu} \dot{q}^{\nu} \right\} = \\
  & = - \dot{s}^{-2} \ddot{s} \, g_{\xi \mu} \dot{q}^{\mu} + \dot{s}^{-1} \left\{ \, g_{\xi \mu} \ddot{q}^{\mu} + \Gamma^{\sigma}_{\mu \nu} g_{\xi \sigma} \dot{q}^{\mu} \dot{q}^{\nu} \right\} \ ,
\end{aligned}$$

or rearranging the indices

$$\ddot{q}^{\mu} + \Gamma^{\mu}_{\nu \sigma} \dot{q}^\nu \dot{q}^\sigma = \dfrac{\ddot{s}}{\dot{s}^3} \dot{q}^{\mu} \ .$$


If $\lambda$ is an **affine parameter**, so that its relation with the arc-length is $\lambda = a s + b$, with $a$, $b$ constant, then $\ddot{s} = 0$, and the $\mu^{\rm th}$ components of the geodesics equation reads

$$\ddot{q}^{\mu} + \Gamma^{\mu}_{\nu \sigma} \dot{q}^{\nu} \dot{q}^{\sigma} = 0 \ .$$


```{dropdown} Useful results for derivatives and manipulations

$$\begin{aligned}
  \partial \dot{s}^2 & = 2 \dot{s} \partial \dot{s} \\
  \partial \dot{s}^n & = n \dot{s}^{n-1} \partial \dot{s} = \frac{n}{2} \dot{s}^{n-2} \partial \dot{s}^2 \\
\end{aligned}$$

$$\begin{aligned}
  \partial_{q^{\xi}} \dot{s}^2 & = \partial_{q^\xi} \left( g_{\mu \nu} \dot{q}^{\mu} \dot{q}^{\nu} \right) = \partial_{\xi} g_{\mu \nu} \dot{q}^\mu \dot{q}^\nu \\
  \partial_{\dot{q}^{\xi}} \dot{s}^2 & = \partial_{\dot{q}^\xi} \left( g_{\mu \nu} \dot{q}^{\mu} \dot{q}^{\nu} \right) = g_{\mu \xi} \dot{q}^\mu + g_{\xi \nu} \dot{q}^\nu  = 2 g_{\xi \mu} q^{\mu}
\end{aligned}$$

$$\partial_{\xi} g_{\mu \nu} = \Gamma_{\xi \mu}^{\sigma} g_{\sigma \nu} + \Gamma_{\xi \nu}^{\sigma} g_{\sigma \mu}$$

```

````



(general-relativity:geodesics:deviation)=
## Geodesics deviation equation

Let a region of spacetime be parametrized by two parameters, $\mathbf{X}\left( q^{\mu}(\lambda, s) \right)$, so that 

* **geodesics** are constant-$s$ lines parametrized by $\lambda$, $\mathbf{X}(\lambda, \bar{s})$. The velocity vector is 

  $$\mathbf{U} = \partial_{\lambda} \mathbf{X} = \partial_{\lambda} q^{\mu} \mathbf{b}_{\mu} = U^{\mu} \mathbf{b}_{\mu}$$

* two neighboring geodesics are separated by 

   $$\Delta \mathbf{X} = \mathbf{X}(\lambda, s+ds) - \mathbf{X}(\lambda, s) \sim ds \, \partial_s \mathbf{X} = ds \, \partial_s q^{\mu} \, \partial_{\mu} \mathbf{X} = ds \, \xi^{\mu} \mathbf{b}_{\mu} \ .$$

Since mixed partial derivatives of a multi-variable function are equal, and $U^{\mu} = \partial_{\lambda} q^{\mu}$, $\xi^{\mu} = \partial_s q^{\mu}$, then

$$\partial_s U^{\mu} = \partial_\lambda \xi^{\mu} \ .$$

(general-relativity:geodesics:deviation:velocity)=
### Velocity of the geodesics deviation

The evolution of the deviation elementary "segment" $\Delta \mathbf{X} = \Delta s \, \partial_s q^{\mu} \mathbf{b}_{\mu}$ follows from the comparison of two neighboring geodesics. The velocity of the deviation is 

$$\begin{aligned}
  \Delta \mathbf{U} 
  & := \partial_\lambda \Delta \mathbf{X} = \\
  & = \partial_\lambda q^{\mu}(\lambda,s+ds) \mathbf{b}_{\mu}(\lambda,s+ds) - \partial_\lambda q^{\mu}(\lambda,s) \mathbf{b}_{\mu}(\lambda,s) = \\
  & = \Delta s \left\{ \partial_{\lambda s} q^{\mu} + \Gamma^{\mu}_{\nu \sigma} \dfrac{\partial q^{\nu}}{\partial s} \dfrac{\partial q^{\sigma}}{\partial \lambda} \right\} \mathbf{b}_{\mu} + o\left(\Delta s\right) \ ,
\end{aligned}$$

with $\partial_s \mathbf{b}_{\mu} = \partial_s q^{\nu} \partial_{\nu} \mathbf{b}_{\mu} = \partial_s q^{\nu} \Gamma^{\sigma}_{\nu \mu} \mathbf{b}_{\sigma}$. 


(general-relativity:geodesics:deviation:acceleration)=
### Acceleration of the geodesics deviation

The acceleration of the deviation is

$$\Delta \mathbf{A} = \Delta s \, R^{\rho}_{\ \ \sigma \mu \nu} U^{\sigma} U^{\mu} \xi^{\nu} \, \mathbf{b}_{\rho} + o(\Delta s) \ ,$$

with $R^{\rho}_{\ \ \sigma \mu \nu}$ the components of the Riemann tensor in the natural basis induced by the coordinates $q^{\mu}$.

```{dropdown} Details

The acceleration of the deviation

$$\begin{aligned}
  \Delta \mathbf{A}
  & := \partial_{\lambda} \Delta \mathbf{U} = \\
  & = \Delta s \Big\{
    \underbrace{{\color{red}\partial_{\lambda \lambda s} q^{\mu}}}_{\partial_s \partial_{\lambda \lambda} q^{\mu}} + \partial_{\lambda} \Gamma^{\mu}_{\nu \sigma} \partial_s q^{\nu} \partial_\lambda q^{\sigma} + \Gamma^{\mu}_{\nu \sigma} \partial_{\lambda s} q^{\nu} \partial_\lambda q^{\sigma} + \Gamma^{\mu}_{\nu \sigma} \partial_s q^{\nu} \underbrace{ {\color{blue} \partial_{\lambda \lambda} q^{\sigma} } }_{-\Gamma^{\sigma}_{\xi \chi} \partial_\lambda q^{\xi} \partial_\lambda q^{\chi}, \ \text{geodesics}}        + \\
  & \qquad \ \  + \left. \partial_{\lambda s} q^{\chi} \partial_\lambda q^{\nu} \Gamma^{\mu}_{\chi \nu} + \partial_s q^{\nu} \partial_\lambda q^{\sigma} \partial_{\lambda} q^{\xi} \Gamma^{\chi}_{\nu \sigma} \Gamma^{\mu}_{\xi \chi} 
  \right\} \mathbf{b}_{\mu} + o(\Delta s) = && (1) \\
  & = \Delta s \Big\{
  {\color{red}
  - \partial_{s} \Gamma^{\mu}_{\nu \sigma} \partial_\lambda q^{\nu} \partial_\lambda q^{\sigma}  }
  {\color{red} - } \underbrace{{\color{red} \Gamma^{\mu}_{\nu \sigma} \partial_{\lambda s} q^{\nu} \partial_\lambda q^{\sigma}}}_{1}
  {\color{red} - } \underbrace{{\color{red} \Gamma^{\mu}_{\nu \sigma} \partial_\lambda q^{\nu} \partial_{\lambda s} q^{\sigma}}}_{2}
  + \\
  & \qquad \quad + \left. \partial_{\lambda} \Gamma^{\mu}_{\nu \sigma} \partial_s q^{\nu} \partial_\lambda q^{\sigma} + \underbrace{ \Gamma^{\mu}_{\nu \sigma} \partial_{\lambda s} q^{\nu} \partial_\lambda q^{\sigma} }_{1} {\color{blue} - } \Gamma^{\mu}_{\nu \sigma} {\color{blue} \Gamma^{\sigma}_{\xi \chi} \partial_\lambda q^{\xi} \partial_\lambda q^{\chi} } \partial_s q^{\nu} \right. + \\
  & \qquad \quad + \left. \underbrace{ \partial_{\lambda s} q^{\sigma} \partial_\lambda q^{\nu} \Gamma^{\mu}_{\sigma \nu} }_{2} + \partial_s q^{\nu} \partial_\lambda q^{\sigma} \partial_{\lambda} q^{\xi} \Gamma^{\chi}_{\nu \sigma} \Gamma^{\mu}_{\xi \chi} 
  \right\} \mathbf{b}_{\mu} + o(\Delta s) = && (2) \\
  & = \Delta s \left\{
  - \partial_{\sigma} \Gamma^{\rho}_{\mu \nu} + \partial_{\mu} \Gamma^{\rho}_{\nu \sigma} - \Gamma^{\rho}_{\sigma \lambda} \Gamma^{\lambda}_{\mu \nu} + \Gamma^{\lambda}_{\sigma \mu} \Gamma^{\rho}_{\nu \lambda} 
  \right\} \, \partial_s q^{\sigma} \partial_{\lambda} q^{\mu} \partial_{\lambda} q^{\nu} \,  \mathbf{b}_{\rho} + o(\Delta s) = && (3) \\
  & = \Delta s \left\{
     \partial_{\mu} \Gamma^{\rho}_{\nu \sigma} - \partial_{\nu} \Gamma^{\rho}_{\mu \sigma} + \Gamma^{\rho}_{\mu \lambda} \Gamma^{\lambda}_{\nu \sigma} - \Gamma^{\rho}_{\nu \lambda} \Gamma^{\lambda}_{\mu \sigma}
  \right\} \, \partial_s q^{\nu} \partial_{\lambda} q^{\mu} \partial_{\lambda} q^{\sigma} \,  \mathbf{b}_{\rho} + o(\Delta s) \ ,
\end{aligned}$$

since $(1)$ the geodesics equation reads $\partial_{\lambda \lambda} q^{\mu} = - \Gamma^{\mu}_{\nu \sigma} \partial_\lambda q^{\nu} \partial_\lambda q^{\sigma}$; $(2)$ $\partial_s \Gamma^{\mu}_{\nu \sigma} = \partial_s q^{\chi} \partial_{\chi} \Gamma^{\mu}_{\nu \sigma}$; $(3)$ symmetry allows swapping some indices to make the components of the Riemann tensor in the natural basis appear

$$R^{\rho}_{\ \ \sigma \mu \nu} = \partial_{\mu} \Gamma^{\rho}_{\ \ \nu \sigma} - \partial_{\nu} \Gamma^{\rho}_{\ \ \mu \sigma} + \Gamma^{\rho}_{\ \ \mu \lambda} \Gamma^{\lambda}_{\ \ \nu \sigma} - \Gamma^{\rho}_{\ \ \nu \lambda} \Gamma^{\lambda}_{\ \ \mu \sigma} \ .$$

```

