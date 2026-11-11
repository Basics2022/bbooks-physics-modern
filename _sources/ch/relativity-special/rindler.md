(relativity-special:rindler)=
# "Constant" acceleration observer and Rindler coordinates

**todo** Check the hand-written notes into .md converted by Gemini below

---

This section covers the kinematics of uniformly accelerated motion in Special Relativity, the construction of the reference frame of an accelerated observer, the derivation of Rindler coordinates, and their geometric properties (metric, Christoffel symbols, geodesics, zero Riemann curvature tensor, and the Newtonian/classical limit).

---

## 3+1 and 4D Kinematics of an Accelerated Point

### 4-Vector Definitions in an Inertial Frame
Consider an inertial reference frame with Cartesian basis vectors $\{\underline{E}_\mu\}$ such that $\underline{E}_\mu \cdot \underline{E}_\nu = \eta_{\mu\nu} = \text{diag}(1, -1, -1, -1)$.

* **4-position:**

  $$\underline{X}(\tau) = X^\mu(\tau) \underline{E}_\mu = c t \underline{E}_0 + x_i \underline{E}_i$$

  where $\tau$ is the proper time defined by:
  
  $$c^2 d\tau^2 = c^2 dt^2 - |d\vec{x}|^2 = c^2 \left(1 - \frac{|\vec{v}|^2}{c^2}\right) dt^2 \implies d\tau = \gamma^{-1} dt$$
  
  with $\gamma = \left(1 - \frac{|\vec{v}|^2}{c^2}\right)^{-1/2}$.

* **4-velocity:**
  
  $$\underline{U} = \frac{d\underline{X}}{d\tau} = \frac{dt}{d\tau} \frac{d\underline{X}}{dt} = c \gamma \underline{E}_0 + \gamma v_i \underline{E}_i$$
  
  which satisfies $\underline{U} \cdot \underline{U} = c^2$.

* **4-acceleration:**
  
  $$\underline{A} = \frac{d\underline{U}}{d\tau} = \gamma \frac{d\underline{U}}{dt}$$
  
  Expanding component-wise:
  
  $$\frac{d}{dt}(\gamma c) = c \frac{d\gamma}{dt} = c \left(-\frac{1}{2}\right) \left(1 - \frac{|\vec{v}|^2}{c^2}\right)^{-3/2} \left(-2 \vec{v} \cdot \frac{d\vec{v}}{dt}\right) \frac{1}{c^2} = \frac{\gamma^3}{c} (\vec{v} \cdot \vec{a})$$
  $$\frac{d}{dt}(\gamma v_i) = \gamma^3 \frac{1}{c^2} (\vec{v} \cdot \vec{a}) v_i + \gamma a_i$$

  Combining these gives:
  
  $$\underline{A} = \left( \frac{\gamma^4}{c} (\vec{v} \cdot \vec{a}), \, \gamma^2 \vec{a} + \frac{\gamma^4}{c^2} \vec{v} (\vec{v} \cdot \vec{a}) \right)$$
  
  Using the longitudinal/transverse decomposition of acceleration:
  
  $$\underline{A} = \gamma^4 \left\{ \frac{\vec{v} \cdot \vec{a}}{c}, \, \frac{\vec{v}}{c} \left(\frac{\vec{v}}{c} \cdot \vec{a}\right) + \left(1 - \frac{|\vec{v}|^2}{c^2}\right) \vec{a}_\perp \right\}$$

---

## Uniformly Accelerated Trajectory

Consider motion along one spatial direction ($x$) with constant proper acceleration magnitude $\alpha_p$ such that $\underline{A} \cdot \underline{A} = -\alpha_p^2$. 

Assuming initial conditions at $\tau = 0$:

$$(c t, x)|_{\tau=0} = (0, x_{P0}), \quad v(0) = 0$$

The solution to the equations of motion yields hyperbolic motion:

$$c t(\tau) = \frac{c^2}{\alpha_p} \sinh\left(\frac{\alpha_p \tau}{c}\right)$$
$$x(\tau) = \frac{c^2}{\alpha_p} \cosh\left(\frac{\alpha_p \tau}{c}\right) - \frac{c^2}{\alpha_p} + x_{P0}$$

Choosing $x_{P0} = \frac{c^2}{\alpha_p}$, this simplifies to:

$$\begin{cases} c t = \frac{c^2}{\alpha_p} \sinh\left(\frac{\alpha_p \tau}{c}\right) \\ x = \frac{c^2}{\alpha_p} \cosh\left(\frac{\alpha_p \tau}{c}\right) \end{cases}$$

---

## Construction of the Accelerated Observer Frame & Rindler Coordinates

An accelerated observer $P$ builds a local coordinate system using:
1. **Proper time standard ($\tau$):** Measuring time along their worldline using their own clock.
2. **Orthogonal local frame:** Constructing an instantaneous rest frame basis $\{\underline{e}_0(\tau), \underline{e}_1(\tau)\}$:
   
   $$\underline{e}_0(\tau) = \frac{\underline{U}}{c} = \cosh\left(\frac{g \tau}{c}\right) \underline{E}_0 + \sinh\left(\frac{g \tau}{c}\right) \underline{E}_1$$
   
   $$\underline{e}_1(\tau) = \sinh\left(\frac{g \tau}{c}\right) \underline{E}_0 + \cosh\left(\frac{g \tau}{c}\right) \underline{E}_1$$
   
   where $g = \alpha_p$. Note that $\underline{e}_0 \cdot \underline{e}_0 = 1$, $\underline{e}_1 \cdot \underline{e}_1 = -1$, and $\underline{e}_0 \cdot \underline{e}_1 = 0$.

### Coordinate Assignment for Event $Q$

An event $Q$ at spatial distance $z$ along the observer's instantaneous spatial axis $\underline{e}_1(\tau)$ has the spacetime position:

$$\underline{X}_Q(\tau, z) = \underline{X}_P(\tau) + z \, \underline{e}_1(\tau)$$

Expanding in the Minkowski background frame $\{\underline{E}_0, \underline{E}_1\}$:

$$\underline{X}_Q = \underline{E}_0 \left( \frac{c^2}{g} \sinh\frac{g\tau}{c} + z \sinh\frac{g\tau}{c} \right) + \underline{E}_1 \left( \frac{c^2}{g} \cosh\frac{g\tau}{c} + z \cosh\frac{g\tau}{c} \right)$$
$$\underline{X}_Q = \left( \frac{c^2}{g} + z \right) \sinh\left(\frac{g\tau}{c}\right) \underline{E}_0 + \left( \frac{c^2}{g} + z \right) \cosh\left(\frac{g\tau}{c}\right) \underline{E}_1$$

### Definition of Rindler Coordinates $(\eta, \bar{\xi})$
Define the transformed coordinates:

$$\bar{\xi} = \frac{c^2}{g} + z, \quad \eta = \frac{g \tau}{c}$$

This maps Minkowski coordinates $(ct, x)$ to Rindler coordinates $(\eta, \bar{\xi})$:

$$\begin{cases} c t = \bar{\xi} \sinh \eta \\ x = \bar{\xi} \cosh \eta \end{cases}$$

Curves of constant spatial coordinate $\bar{\xi} = \bar{\xi}_k$ represent hyperbolas ($x^2 - c^2 t^2 = \bar{\xi}_k^2$) corresponding to observers maintaining constant acceleration $\alpha = c^2 / \bar{\xi}_k$.

---

## Metric Tensor in Rindler Coordinates

Differentials of the coordinate transformation are given by:

$$c dt = \cosh\eta \, d\bar{\xi} + \bar{\xi} \sinh\eta \, d\eta$$
$$dx = \sinh\eta \, d\bar{\xi} + \bar{\xi} \cosh\eta \, d\eta$$

Substituting these into the flat Minkowski line element $ds^2 = c^2 dt^2 - dx^2$:

$$ds^2 = (\cosh\eta \, d\bar{\xi} + \bar{\xi} \sinh\eta \, d\eta)^2 - (\sinh\eta \, d\bar{\xi} + \bar{\xi} \cosh\eta \, d\eta)^2$$
$$ds^2 = \bar{\xi}^2 d\eta^2 - d\bar{\xi}^2$$

Alternatively, writing the metric in terms of proper time $\tau$ and local spatial coordinate $z$:

$$ds^2 = \left(1 + \frac{gz}{c^2}\right)^2 c^2 d\tau^2 - dz^2$$

### Natural Basis Vectors and Dual Metric Components
The natural basis vectors $\underline{b}_\eta = \partial_\eta \underline{X}$ and $\underline{b}_{\bar{\xi}} = \partial_{\bar{\xi}} \underline{X}$ are:

$$\underline{b}_\eta = \bar{\xi} \cosh\eta \, \underline{E}_0 + \bar{\xi} \sinh\eta \, \underline{E}_1$$
$$\underline{b}_{\bar{\xi}} = \sinh\eta \, \underline{E}_0 + \cosh\eta \, \underline{E}_1$$

The metric components $g_{\mu\nu} = \underline{b}_\mu \cdot \underline{b}_\nu$ are:

$$g_{\eta\eta} = \bar{\xi}^2, \quad g_{\bar{\xi}\bar{\xi}} = -1, \quad g_{\eta\bar{\xi}} = 0$$

$$\mathbf{g} = \begin{pmatrix} \bar{\xi}^2 & 0 \\ 0 & -1 \end{pmatrix}, \quad \mathbf{g}^{-1} = \begin{pmatrix} \frac{1}{\bar{\xi}^2} & 0 \\ 0 & -1 \end{pmatrix}$$

---

## Christoffel Symbols & Riemann Tensor

### Derivatives of Basis Vectors
Calculating derivatives of the natural basis vectors with respect to coordinates $(\bar{\xi}, \eta)$:

$$\partial_{\bar{\xi}} \underline{b}_{\bar{\xi}} = 0$$
$$\partial_\eta \underline{b}_{\bar{\xi}} = \cosh\eta \, \underline{E}_0 + \sinh\eta \, \underline{E}_1 = \frac{1}{\bar{\xi}} \underline{b}_\eta$$
$$\partial_\eta \underline{b}_\eta = \bar{\xi} \sinh\eta \, \underline{E}_0 + \bar{\xi} \cosh\eta \, \underline{E}_1 = \bar{\xi} \, \underline{b}_{\bar{\xi}}$$

### Non-Zero Christoffel Symbols
From $\partial_\mu \underline{b}_\nu = \Gamma^\lambda_{\mu\nu} \underline{b}_\lambda$, the non-zero Christoffel symbols are:

$$\Gamma^\eta_{\eta \bar{\xi}} = \Gamma^\eta_{\bar{\xi} \eta} = \frac{1}{\bar{\xi}}$$
$$\Gamma^{\bar{\xi}}_{\eta\eta} = \bar{\xi}$$

### Curvature (Zero Riemann Tensor)
Calculating the Riemann curvature tensor components using $R^\rho{}_{\sigma\mu\nu} = \partial_\mu \Gamma^\rho{}_{\nu\sigma} - \partial_\nu \Gamma^\rho{}_{\mu\sigma} + \Gamma^\rho{}_{\mu\lambda}\Gamma^\lambda{}_{\nu\sigma} - \Gamma^\rho{}_{\nu\lambda}\Gamma^\lambda{}_{\mu\sigma}$:

$$R^{\bar{\xi}}{}_{\eta\bar{\xi}\eta} = \partial_{\bar{\xi}}\Gamma^{\bar{\xi}}_{\eta\eta} - \partial_\eta \Gamma^{\bar{\xi}}_{\bar{\xi}\eta} + \Gamma^{\bar{\xi}}_{\bar{\xi}\lambda}\Gamma^\lambda_{\eta\eta} - \Gamma^{\bar{\xi}}_{\eta\lambda}\Gamma^\lambda_{\bar{\xi}\eta}$$
$$R^{\bar{\xi}}{}_{\eta\bar{\xi}\eta} = \frac{\partial}{\partial\bar{\xi}}(\bar{\xi}) - 0 + 0 - \left(\Gamma^{\bar{\xi}}_{\eta\eta}\Gamma^\eta_{\bar{\xi}\eta}\right) = 1 - \left(\bar{\xi} \cdot \frac{1}{\bar{\xi}}\right) = 0$$

Thus, all components of the Riemann tensor vanish ($R^\rho{}_{\sigma\mu\nu} = 0$), confirming that the Rindler frame describes **flat spacetime** in non-inertial coordinates.

---

## Geodesics in Rindler Coordinates

The geodesic equations are given by:

$$\ddot{x}^\mu + \Gamma^\mu_{\alpha\beta} \dot{x}^\alpha \dot{x}^\beta = 0$$

where dots denote derivatives with respect to an affine parameter (e.g., proper time $s$).
Writing explicit components for $\bar{\xi}$ and $\eta$:

$$\begin{cases} \ddot{\bar{\xi}} + \Gamma^{\bar{\xi}}_{\eta\eta} \dot{\eta}^2 = 0 \implies \ddot{\bar{\xi}} + \bar{\xi} \dot{\eta}^2 = 0 \\ \ddot{\eta} + 2 \Gamma^\eta_{\bar{\xi}\eta} \dot{\bar{\xi}}\dot{\eta} = 0 \implies \ddot{\eta} + \frac{2}{\bar{\xi}} \dot{\bar{\xi}}\dot{\eta} = 0 \end{cases}$$

---

## Classical / Newtonian Limit

For low speeds ($v \ll c$) and small spatial extents around the observer line ($z \ll c^2/g$):

1. **Coordinate expansion:**
   
   $$\bar{\xi} = \frac{c^2}{g} + z \implies 1 + \frac{gz}{c^2} \approx 1$$
   
   $$\tau = \frac{c}{g} \eta \implies \eta \ll 1$$

2. **Metric limit:**
   
   $$ds^2 = \left(1 + \frac{gz}{c^2}\right)^2 c^2 d\tau^2 - dz^2 \approx \left(1 + \frac{2gz}{c^2}\right) c^2 d\tau^2 - dz^2$$
   
   Matching with the weak static field limit metric $g_{00} = 1 + \frac{2\Phi}{c^2}$, we identify the fictitious Newtonian gravitational potential:
   
   $$\Phi(z) = g z$$

3. **Geodesic / Acceleration Equation:**
   Substituting $\bar{\xi} = \frac{c^2}{g} + z$ into the spatial geodesic equation with $\dot{\eta} \approx \frac{g}{c} \dot{t}$:
   
   $$\ddot{z} + \left(\frac{c^2}{g} + z\right) \left(\frac{g}{c}\right)^2 = 0 \implies \ddot{z} + g + \frac{g^2 z}{c^2} = 0$$
   
   Taking $c \to \infty$:
   
   $$\ddot{z} + g = 0 \implies \ddot{z} = -g$$

This recovers the expected non-relativistic inertial force (apparent constant downward gravitational field $-g$) experienced in a uniformly accelerating reference frame.



