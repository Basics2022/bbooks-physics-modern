(relativity-special:rindler)=
# "Constant" acceleration observer and Rindler coordinates

**todo** Check the hand-written notes into .md converted by Gemini below

---

This section covers the kinematics of uniformly accelerated motion in Special Relativity, the construction of the reference frame of an accelerated observer, the derivation of Rindler coordinates, and their geometric properties (metric, Christoffel symbols, geodesics, zero Riemann curvature tensor, and the Newtonian/classical limit).


(relativity-special:rindler:kinematics-point)=
## 3+1 and 4D Kinematics of a point

See [Kinematics of a point](relativity-special:notes:kinematics-point).


(relativity-special:rindler:point-uniform-acceleration)=
## Uniformly accelerated point

Consider motion of a point $P$ in (the flat) space time along one spatial direction, parametrized with proper-time $\tau_P$,

$$\mathbf{X}_P(\tau_P) = X^\mu_P(\tau_P) \mathbf{E}_{\mu} =  ct_P(\tau_P) \mathbf{E}_0 + x_P(\tau_P) \mathbf{E}_1 \ ,$$

with constant proper acceleration magnitude $\alpha_P$ such that $\mathbf{A}_P \cdot \mathbf{A}_P = -\alpha_P^2$, being $\mathbf{A}(\tau) = \mathbf{X}''(\tau)$. Assuming initial conditions at $\tau = 0$, with

* position $\mathbf{X}_P(\tau_P=0) = x_{P0} \mathbf{E}_1$, 

   $$(c t, x)|_{\tau_P=0} = (0, x_{P0}) \ ,$$

* zero 3-dimensional velocity 

   $$0 = v(\tau_P = 0) = \left.\frac{d x}{dt}\right|_{\tau_P=0} = \left.\frac{d x}{d \tau}\right|_{\tau_P=0} \left.\frac{d \tau}{d t}\right|_{\tau_P=0} = U^1_P(\tau=0) \underbrace{ \gamma(v=0) }_{ = 1} = U_P^1(0) \ , $$

   being $\tfrac{d x_P}{d \tau_P} = U^1_P$ the component $1$ of the 4-velocity, and $\tfrac{d}{\tau_P}{d t_P} = \gamma^{-1}$. The time component of the velocity is $U^0 = c$, so that the initial condition for the 4-velocity is $\mathbf{U}_P(\tau_P = 0) = c \mathbf{E}_0$.

The solution of the condition about the constant proper acceleration magnitude 

$$-\alpha_P^2 = \mathbf{A}_P \cdot \mathbf{A}_P = \left( A^0 \right)^2 - \left( A^1 \right)^2 = \left( X^{0''} \right)^2 - \left( X^{1 ''} \right)^2 \ ,$$

compatible with the initial conditions and with the orthogonality condition {eq}`eq:relativity:kinematics:vel-acc-orthogonality` $\mathbf{A} \cdot \mathbf{U} = 0$ is

$$\left\{ \begin{aligned}
  c t(\tau) & = \frac{c^2}{\alpha_P} \sinh\left(\frac{\alpha_p \tau}{c}\right) \\
  x(\tau)   & = \frac{c^2}{\alpha_P} \cosh\left(\frac{\alpha_p \tau}{c}\right) - \frac{c^2}{\alpha_P} + x_{P0}
\end{aligned} \right.$$

or using the vector notation

$$
\mathbf{X}_P(\tau) = \frac{c^2}{\alpha_P} \sinh\left(\frac{\alpha_p \tau}{c}\right) \, \mathbf{E}_0 
+ \left[ \frac{c^2}{\alpha_P} \cosh\left(\frac{\alpha_p \tau}{c}\right) - \frac{c^2}{\alpha_P} + x_{P0} \right] \, \mathbf{E}_1 \ .
$$

```{dropdown} Details
:open:

4-position, 4-velocity and 4-acceleration

$$\begin{aligned}
  \mathbf{X} & = \frac{c^2}{\alpha} \sinh \left( \frac{\alpha \tau}{c} \right) \mathbf{E}_0 + \left[ \frac{c^2}{\alpha} \cosh \left( \frac{\alpha \tau}{c} \right) - \frac{c^2}{\alpha} + x_{P0} \right] \mathbf{E}_1 \\
  \mathbf{X}'  = \mathbf{U} & = c \cosh \frac{\alpha \tau}{c} \, \mathbf{E}_0 + c \sinh \left( \frac{\alpha \tau}{c} \right) \, \mathbf{E}_1 \\
  \mathbf{X}'' = \mathbf{A} & = \alpha \sinh \frac{\alpha \tau}{c} \, \mathbf{E}_0 + \alpha \cosh \left( \frac{\alpha \tau}{c} \right) \, \mathbf{E}_1 \\
\end{aligned}$$

Orthogonality $\mathbf{U} \cdot \mathbf{A} = 0$ immediately follows from $\mathbf{E}_0 \cdot \mathbf{E}_0 = 1$, $\mathbf{E}_1 \cdot \mathbf{E} = -1$. Constant magnitude of proper acceleration follows from the identity $\cosh^2 x - \sinh^2 x = 1$.


```

Choosing $x_{P0} = \frac{c^2}{\alpha_p}$, this simplifies to:

$$\begin{cases} c t = \frac{c^2}{\alpha_p} \sinh\left(\frac{\alpha_p \tau}{c}\right) \\ x = \frac{c^2}{\alpha_p} \cosh\left(\frac{\alpha_p \tau}{c}\right) \end{cases}$$

---

(relativity-special:rindler:construction)=
## Construction of the Accelerated Observer Frame & Rindler Coordinates

An accelerated observer $P$ builds a local coordinate system using:
1. **Proper time standard ($\tau$)**, measuring time along their worldline using their own clock.
2. **Orthogonal local frame**, constructing an instantaneous rest frame basis $\{\mathbf{e}_0(\tau), \mathbf{e}_1(\tau)\}$:
  
   $$\begin{aligned}
   \mathbf{e}_0(\tau) & = \frac{\mathbf{U}}{c} = \cosh\left(\frac{g \tau}{c}\right) \mathbf{E}_0 + \sinh\left(\frac{g \tau}{c}\right) \mathbf{E}_1$$ \\
   \mathbf{e}_1(\tau) & = \sinh\left(\frac{g \tau}{c}\right) \mathbf{E}_0 + \cosh\left(\frac{g \tau}{c}\right) \mathbf{E}_1 \ ,
   \end{aligned}$$
   
   here with $g = \alpha_P$. This orthogonal local frame is locally Minkowski, i.e. $\mathbf{e}_0 \cdot \mathbf{e}_0 = 1$, $\mathbf{e}_1 \cdot \mathbf{e}_1 = -1$, and $\mathbf{e}_0 \cdot \mathbf{e}_1 = 0$.

(relativity-special:rindler:construction:generic-event)=
### Generic event $Q$

An event $Q$ at spatial distance $z$ along the observer's instantaneous spatial axis $\mathbf{e}_1(\tau)$ has the spacetime position:

$$\mathbf{X}_Q(\tau, z) = \mathbf{X}_P(\tau) + z \, \mathbf{e}_1(\tau)$$

or using the inertial reference frame $\{\mathbf{E}_0, \mathbf{E}_1\}$:

$$\begin{aligned}
  \mathbf{X}_Q
  & = \mathbf{E}_0 \left( \frac{c^2}{g} \sinh\frac{g\tau}{c} + z \sinh\frac{g\tau}{c} \right) + \mathbf{E}_1 \left( \frac{c^2}{g} \cosh\frac{g\tau}{c} + z \cosh\frac{g\tau}{c} \right) = \\
  & = \left( \frac{c^2}{g} + z \right) \sinh\left(\frac{g\tau}{c}\right) \mathbf{E}_0 + \left( \frac{c^2}{g} + z \right) \cosh\left(\frac{g\tau}{c}\right) \mathbf{E}_1 = \\
  & = ct_Q \mathbf{E}_0 + x_Q \mathbf{E}_1 \ .
\end{aligned}$$ (eq:rindler:generic-events)

(relativity-special:rindler:construction:rindler-coords-def)=
### Definition of Rindler Coordinates $(\eta, \xi)$

The definition of the set of coordinates $( \eta, \xi )$,

$$\xi = \frac{c^2}{g} + z, \quad \eta = \frac{g \tau}{c} \ ,$$ (eq:rindler:def)

and the expression {eq}`eq:rindler:generic-events` of the generic evnet $Q$, maps the orthogonal coordinates of the inertial reference frame $(ct, x)$ to Rindler coordinates $(\eta, \xi)$:

$$\begin{cases} c t = \xi \sinh \eta \\ x = \xi \cosh \eta \end{cases}$$

Curves of **constant coordinate** $\xi = \xi_k$ are **hyperbolas** in the coordinates $(ct, x)$ of the inertial reference frame, $x^2 - c^2 t^2 = \xi_k^2$, and are the trajectories of observers maintaining constant acceleration $\alpha = c^2 / \xi_k$, with initial 4-position $\mathbf{X}_0 = \xi \mathbf{E}_1$, and 4-velocity $\mathbf{U}_0 = c \mathbf{E}_0$. 

Curves with **constant coordinate** $\eta$ are straight lines using the coordinates $(ct, x)$, $x = \frac{c t}{\tanh \eta}$. As $\tanh\eta \in [-1, 1]$, Rindler coordinates can only describe the right-most region of the $(ct,x)$ plane between the two **horizons** $x = ct$, and $x  = -ct$. (or can they also describe the left-most region? Anyways, they can't describe the upper and lower regions). 


(relativity-special:rindler:construction:metric tensor)=
## Metric tensor in Rindler coordinates

Differentials of the coordinate transformation are given by:

$$\left\{ \begin{aligned}
  c dt & = \cosh\eta \, d\xi + \xi \sinh\eta \, d\eta \\
  dx   & = \sinh\eta \, d\xi + \xi \cosh\eta \, d\eta \\
\end{aligned}\right.$$

Substituting these into the flat Minkowski line element $ds^2 = c^2 dt^2 - dx^2$:

$$ds^2 = (\cosh\eta \, d\xi + \xi \sinh\eta \, d\eta)^2 - (\sinh\eta \, d\xi + \xi \cosh\eta \, d\eta)^2$$
$$ds^2 = \xi^2 d\eta^2 - d\xi^2$$

Alternatively, writing the metric in terms of proper time $\tau$ and local spatial coordinate $z$, using the relations {eq}`eq:rindler:def`, the worldline element becomes

$$ds^2 = \left(1 + \frac{gz}{c^2}\right)^2 c^2 d\tau^2 - dz^2 \ .$$

(relativity-special:rindler:construction:metric tensor)=
### Natural Basis Vectors and Dual Metric Components
The natural basis vectors $\mathbf{b}_\eta = \partial_\eta \mathbf{X}$ and $\mathbf{b}_{\xi} = \partial_{\xi} \mathbf{X}$ are:

$$\begin{aligned}
  \mathbf{b}_\eta  & = \xi \cosh\eta \, \mathbf{E}_0 + \xi \sinh\eta \, \mathbf{E}_1 \\
  \mathbf{b}_{\xi} & = \sinh\eta \, \mathbf{E}_0 + \cosh\eta \, \mathbf{E}_1 \\
\end{aligned}$$

The metric components $g_{\mu\nu} = \mathbf{b}_\mu \cdot \mathbf{b}_\nu$ are:

$$g_{\eta\eta} = \xi^2, \quad g_{\xi\xi} = -1, \quad g_{\eta\xi} = 0$$

$$\mathbf{g} = \begin{pmatrix} \xi^2 & 0 \\ 0 & -1 \end{pmatrix}, \quad \mathbf{g}^{-1} = \begin{pmatrix} \frac{1}{\xi^2} & 0 \\ 0 & -1 \end{pmatrix}$$

---

## Christoffel Symbols & Riemann Tensor

### Derivatives of Basis Vectors
Calculating derivatives of the natural basis vectors with respect to coordinates $(\xi, \eta)$:

$$\begin{aligned}
  \partial_{\xi} \mathbf{b}_{\xi} & = 0 \\
  \partial_\eta  \mathbf{b}_{\xi} & = \cosh\eta \, \mathbf{E}_0 + \sinh\eta \, \mathbf{E}_1 = \frac{1}{\xi} \mathbf{b}_\eta \\
  \partial_\eta  \mathbf{b}_\eta  & = \xi \sinh\eta \, \mathbf{E}_0 + \xi \cosh\eta \, \mathbf{E}_1 = \xi \, \mathbf{b}_{\xi} \\
\end{aligned}$$

### Non-Zero Christoffel Symbols
From $\partial_\mu \mathbf{b}_\nu = \Gamma^\lambda_{\mu\nu} \mathbf{b}_\lambda$, the non-zero Christoffel symbols are:

$$\begin{aligned}
  \Gamma^\eta_{\eta \xi} = \Gamma^\eta_{\xi \eta} = \frac{1}{\xi} \\
  \Gamma^{\xi}_{\eta\eta} = \xi \\
\end{aligned}$$

### Curvature (Zero Riemann Tensor)

Using Rindler coordinates, the Riemann tensor of the flat spacetime is still zero $R^{\rho}_{\ \ \sigma \mu \nu} = 0$.

```{dropdown} Details

Calculating the Riemann curvature tensor components using 

$$R^\rho{}_{\sigma\mu\nu} = \partial_\mu \Gamma^\rho{}_{\nu\sigma} - \partial_\nu \Gamma^\rho{}_{\mu\sigma} + \Gamma^\rho{}_{\mu\lambda}\Gamma^\lambda{}_{\nu\sigma} - \Gamma^\rho{}_{\nu\lambda}\Gamma^\lambda{}_{\mu\sigma}$$

gives

$$R^{\xi}{}_{\eta\xi\eta} = \partial_{\xi}\Gamma^{\xi}_{\eta\eta} - \partial_\eta \Gamma^{\xi}_{\xi\eta} + \Gamma^{\xi}_{\xi\lambda}\Gamma^\lambda_{\eta\eta} - \Gamma^{\xi}_{\eta\lambda}\Gamma^\lambda_{\xi\eta}$$
$$R^{\xi}{}_{\eta\xi\eta} = \frac{\partial}{\partial\xi}(\xi) - 0 + 0 - \left(\Gamma^{\xi}_{\eta\eta}\Gamma^\eta_{\xi\eta}\right) = 1 - \left(\xi \cdot \frac{1}{\xi}\right) = 0$$

Thus, all components of the Riemann tensor vanish ($R^\rho{}_{\sigma\mu\nu} = 0$), confirming that the Rindler frame describes **flat spacetime** in non-inertial coordinates.

**todo** Justify the reason why all the other components are not evaluated

```

## Geodesics in Rindler Coordinates

The geodesic equations are given by:

$$\ddot{x}^\mu + \Gamma^\mu_{\alpha\beta} \dot{x}^\alpha \dot{x}^\beta = 0$$

where dots denote derivatives with respect to an affine parameter (e.g., proper time $s$).
Writing explicit components for $\xi$ and $\eta$:

$$\begin{cases} \ddot{\xi} + \Gamma^{\xi}_{\eta\eta} \dot{\eta}^2 = 0 \implies \ddot{\xi} + \xi \dot{\eta}^2 = 0 \\ \ddot{\eta} + 2 \Gamma^\eta_{\xi\eta} \dot{\xi}\dot{\eta} = 0 \implies \ddot{\eta} + \frac{2}{\xi} \dot{\xi}\dot{\eta} = 0 \end{cases}$$

---

## Classical / Newtonian Limit

For low speeds ($v \ll c$) and small spatial extents around the observer line ($z \ll c^2/g$):

1. **Coordinate expansion:**
   
   $$\xi = \frac{c^2}{g} + z \implies 1 + \frac{gz}{c^2} \approx 1$$
   
   $$\tau = \frac{c}{g} \eta \implies \eta \ll 1$$

2. **Metric limit:**
   
   $$ds^2 = \left(1 + \frac{gz}{c^2}\right)^2 c^2 d\tau^2 - dz^2 \approx \left(1 + \frac{2gz}{c^2}\right) c^2 d\tau^2 - dz^2$$
   
   Matching with the weak static field limit metric $g_{00} = 1 + \frac{2\Phi}{c^2}$, we identify the fictitious Newtonian gravitational potential:
   
   $$\Phi(z) = g z$$

3. **Geodesic / Acceleration Equation:**
   Substituting $\xi = \frac{c^2}{g} + z$ into the spatial geodesic equation with $\dot{\eta} \approx \frac{g}{c} \dot{t}$:
   
   $$\ddot{z} + \left(\frac{c^2}{g} + z\right) \left(\frac{g}{c}\right)^2 = 0 \implies \ddot{z} + g + \frac{g^2 z}{c^2} = 0$$
   
   Taking $c \to \infty$:
   
   $$\ddot{z} + g = 0 \implies \ddot{z} = -g$$

This recovers the expected non-relativistic inertial force (apparent constant downward gravitational field $-g$) experienced in a uniformly accelerating reference frame.



