(general-relativity:geodesics)=
# Geodesics

## ... 

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

<!--
The equation of the geodesics with parameters $s$ has velocity $\mathbf{U}(q^{\mu}(\lambda,s)) = \partial_{\lambda} q^{\mu} \partial_{\mu} \mathbf{X} = \partial_{\lambda} q^{\mu} \mathbf{b}_{\mu}$

$$\mathbf{0} = \frac{\partial}{\partial \lambda} \mathbf{U}(\lambda, s) = \left. \left\{ \dfrac{\partial^2 q^\mu}{\partial \lambda^2} + \Gamma^{\mu}_{\nu \sigma} \dfrac{\partial q^{\nu}}{\partial \lambda} \dfrac{\partial q^{\sigma}}{\partial \lambda} \right\} \mathbf{b}_{\mu} \right|_{(\lambda,s)} \ ,$$

since $\partial_\lambda \mathbf{b}_{\mu} = \partial_{\lambda} q^{\nu} \, \partial_{\nu} \mathbf{b}_{\mu} = U^\nu \Gamma^{\sigma}_{\nu \mu} \mathbf{b}_{\sigma}$.
-->
