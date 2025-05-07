(relativity-special:notes)=
# Special Relativity - Notes

An event is determined by spatio-temporal information together, $t, \vec{r}$. Absolute nature of physics needs vector algebra and calculus formalism

$$\mathbf{X} = c  t  \mathbf{E}_0 + \vec{r} =  c  t  \mathbf{E}_0 + x^1 \mathbf{E}_1 + x^2 \mathbf{E}_2 + x^3 \mathbf{E}_3 = X^{\alpha} \mathbf{E}_{\alpha} \ ,$$

having used Cartesian coordiantes for the space coordinate.

**Geometry of time-space in special relativity.** Minkowski metric reads

$$g_{\alpha \beta} = \mathbf{E}_{\alpha} \cdot \mathbf{E}_{\beta} = \text{diag}\{1, -1, -1, -1\}$$

```{dropdown} Reciprocal basis

The reciprocal basis reads $\mathbf{E}_{\alpha} \cdot \mathbf{E}^{\beta} = \delta_{\alpha}^{\beta}$, $\mathbf{E}_{\alpha} = g_{\alpha \beta} \mathbf{E}^{\beta}$, s.t. the elementary interval between two events can be written as

$$d \mathbf{X} = d X^{\alpha} \, \mathbf{E}_{\alpha} = \underbrace{d X^{\alpha} \, g_{\alpha \beta}}_{= dX_{\beta}} \, \mathbf{E}^{\beta} = d X_{\beta} \, \mathbf{E}^{\beta} \ ,$$

having used Cartesian coordinates,

$$
  \begin{aligned}  & X^0 = c t \\  & X_0 = c t \end{aligned} \qquad
  \begin{aligned}  & X^1 =   x \\  & X_1 =  -x \end{aligned} \qquad
  \begin{aligned}  & X^2 =   y \\  & X_2 =  -y \end{aligned} \qquad
  \begin{aligned}  & X^3 =   z \\  & X_3 =  -z \end{aligned}
$$
```
<!--
Its "length", or better pseudo-norm with Minkowski metric, is invariant and reads
-->

**Elementary interval** between two events

$$d s^2 = d \mathbf{X} \cdot d \mathbf{X} = \left( dX_{\alpha} \mathbf{E}^{\alpha} \right) \cdot \left( dX^{\beta} \mathbf{E}_{\beta} \right) = c^2 \, d t^2 - (dx^1)^2 - (dx^2)^2 - (dx^3)^2 = c^2 \, dt^2 - |d \vec{r}|^2 $$

## Kinematics of point

**Proper time.** For a co-moving observer, $d \vec{r}' = \vec{0}$, and $t'$ is commonly indicated with $\tau$, and its differential is invariant itself, being the product of a constant ($c$ is a universal constant in special relativity) and an invariant quantity.

$$d s^2 = c^2 dt'^2 - |d \vec{r}'|^2 = c^2 d \tau^2 \ .$$

Given the invariant nature of $d s$,

$$d s^2 = c^2 \, d \tau^2 = c^2 \, dt^2 - |d \vec{r}|^2 = c^2 \, dt^2 \left[ 1 - \frac{1}{c^2}\frac{|d\vec{r}|^2}{dt^2} \right] = c^2 \, dt^2 \left[ 1 - \frac{|\vec{v}|^2}{c^2} \right]$$

and thus

$$d s = c \, d \tau = \gamma^{-1}(v/c) \, c \, dt \ ,$$

with $\gamma(w) = \frac{1}{\sqrt{1 - w^2}}$. 

```{note} $ds$ is invariant
**todo** prove it. And/or add a section about the role of invariance.
```


**4-Velocity.** Given the parametric representation of an event in space-time as a function of its proper time, $\mathbf{X}(\tau)$ or coordinate $s$, $\mathbf{X}(s)$ the derivative w.r.t. this parameter is defined as the 4-velocity of the event in space time. Using Cartesian coordinates inducing constant and uniform basis $\mathbf{E}_{\alpha}$, as a function of the observer time $t$, $c t$, $x^i(t)$, and the transformation of coordinates $t(\tau)$, with differential $d t = \frac{1}{\gamma} \, d \tau$

$$\mathbf{U}(\tau) := \mathbf{X}'(\tau) = \dfrac{d}{d \tau} \left( X^{\alpha}(\tau) \mathbf{E}_{\alpha} \right) = \dfrac{d t}{d \tau} (c t \mathbf{E}_0 + x^i(t) \mathbf{E}_i) = \gamma(v/c) \left( c \mathbf{E}_0 + \dot{x}^i(t) \mathbf{E}_i \right) = \gamma(v/c) \left( c \mathbf{E}_0 + \vec{v} \right)$$

or

$$\mathbf{U}(s) := \mathbf{X}'(s) = \dfrac{d t}{ ds } \dfrac{d}{dt} \mathbf{X}(t) = \dots = \gamma(v/c) \left( \mathbf{E}_0 + \frac{\vec{v}}{c} \right) \ .$$

```{note}
Using $s$ as the parameter, $\mathbf{U}$ is non-dimensional, and has pseudo-norm = 1,

$$\mathbf{U}(s) \cdot \mathbf{U}(s) = \gamma^2 \underbrace{\left( 1 - \frac{|\vec{v}|^2}{c^2} \right)}_{=\gamma^{-2}} = 1 \ .$$

Using $\tau$ as the parameter, $\mathbf{U}$ has physical dimension of a velocity and pseudo-norm = $c$.
```

**4-acceleration** $\mathbf{X}''(\tau)$ or $\mathbf{X}''(s)$, **todo**

## Dynamics of a point mass

**4-momentum**

$$\mathbf{P} = m \mathbf{U}$$

Using Cartesian coordinates and $\tau$ as independent variable,

$$\mathbf{P} = m \mathbf{U} = m \frac{d \mathbf{X}}{d \tau} = m \gamma (c, \vec{v}) \ .$$

```{dropdown} Low-speed limit - classical mechanics

The spatial component is $\gamma$ times the 3-dimensional momentum $\vec{p} = m \vec{v}$; the time component reads

$$P^0 = m \gamma(w) c \ ,$$

and for small ratio $w:= \frac{v}{c}$ it can be expanded in Taylor series around $w = 0$ as

$$\gamma(w) \sim \gamma(0) + w \, \gamma'(0) + \frac{1}{2} \, w^2 \gamma''(0) + o(w^2) \ ,$$

with

$$\begin{aligned}
\left.\gamma(w)  \right|_{w=0} & = \left.\frac{1}{\sqrt{1 - w^2}}\right|_{w=0} = 1 \\
\left.\gamma'(w) \right|_{w=0} & = \left.-\frac{1}{2}(1 - w^2)^{-\frac{3}{2}} (- 2 w)\right|_{w=0} = w (1 - w^2)^{-\frac{3}{2}}= 0 \\
\left.\gamma''(w)\right|_{w=0} & = \left. \left( (1-w^2)^{-\frac{3}{2}} + w \left(-\frac{3}{2} \right)(1-w^2)^{-\frac{5}{2}} (- 2 w)  \right)\right|_{w=0} = \\ 
  & = \left. \left( (1-w^2)^{-\frac{3}{2}} + 3 w^2 (1-w^2)^{-\frac{5}{2}} \right)\right|_{w=0} = 1 \\
\end{aligned}$$

and thus

$$\gamma(w) = 1 + \frac{1}{2} w^2 + o(w^2)$$

and

$$\gamma(v/c) \, m \, c \sim m \, c \left( 1 + \frac{v^2}{c^2} \right) = \frac{1}{c} \left( mc^2 + \frac{1}{2} m |\vec{v}|^2 \right) $$
```

```{dropdown} Energy-momentum relation
Recognizing energy ($E = \gamma m c^2$) and 3-momentum ($\vec{p} = m_3 \vec{v}$, with $m_3 := \gamma m$)[^e-p-from-lagrange], the 4-momentum can be written as

[^e-p-from-lagrange]: This definitions naturally arise in Lagrange approach.

$$\mathbf{P} = m \mathbf{U} = \gamma m \left( 1, \frac{\vec{v}}{c} \right) =: \frac{1}{c} \left( \frac{E}{c}, \vec{p} \right)$$

Its pseudo-norm reads

$$m^2 = \mathbf{P} \cdot \mathbf{P} = \frac{1}{c^4} \left( E^2 - c^2 |\vec{p}|^2 \right) $$

and thus the relation between $E$, $\vec{p}$, $m$ and $c$,

$$E^2 = m^2 c^4 + c^2 |\vec{p}|^2 \ ,$$

from which, for $\vec{v} = \vec{0} \rightarrow \vec{p} = \vec{0}$,

$$E^2 = m^2 c^4 \ ,$$

and keeping only the solution with positive energy (**todo** *reference to Dirac's equation and anti-matter?*)

$$E = m c^2 \ .$$

```

**4-force and dynamical equation for a point mass.** The dynamical equation of a point mass subject to a 4-force $\mathbf{f}$ reads

$$\dfrac{d \mathbf{P}}{d \tau} = \mathbf{f} \ .$$ (eq:point:dynamics)

Examples:
- **Free particle** is subject to no net force, $\mathbf{f}$,
- Point charge $q$ in EM field is subject to **Lorentz force**, $\mathbf{f} = q \mathbf{F} \cdot \mathbf{U}$, being $\mathbf{F}$ the EM field tensor, {eq}`eq:tensor:em-field`,

   $$\mathbf{F} = \nabla \mathbf{A} - \left( \nabla \mathbf{A} \right)^T \ .$$

### Lagrangian approach

Here variational approach to the motion of point particle in a force field $\mathbf{f}$ is derived from the weak form of the dynamical equation {eq}`eq:point:dynamics`. In particular, the derivation is performed for a particle moving in a known EM field. The motion of a free particle immediately follows if the EM field is zero.

$$m \dfrac{d \mathbf{U}}{d \tau} = q \mathbf{F} \cdot \mathbf{U}$$

The equation of motion can be manipulated to get Lagrange equations

$$\begin{aligned}
  \mathbf{0} 
  & = m \dfrac{d \mathbf{U}}{d \tau} - q \nabla \mathbf{A} \cdot \mathbf{U} + q \left( \nabla \mathbf{A} \right)^T \cdot \mathbf{U} = \\
  & = \dfrac{d}{d\tau} \left[ m \mathbf{U} + q \mathbf{A}(\mathbf{X}(\tau)) \right] - \nabla \left( q \mathbf{A} \cdot \mathbf{U} \right) = (1) \\
  & = \dfrac{d}{d\tau} \left[ \mathbf{E}^\alpha \dfrac{\partial}{\partial U^\alpha} \left( m c \sqrt{\mathbf{U} \cdot \mathbf{U}}  + q \mathbf{A}(\mathbf{X}(\tau)) \cdot \mathbf{U} \right) \right] - \mathbf{E}^\alpha \dfrac{\partial}{\partial X^\alpha} \left( m c \sqrt{\mathbf{U} \cdot \mathbf{U}}  + q \mathbf{A} \cdot \mathbf{U} \right) = (2) \\
  & = \mathbf{E}^{\alpha} \left[ \dfrac{d}{d\tau} \dfrac{\partial \mathscr{L}}{\partial X^{'\alpha}} - \dfrac{\partial \mathscr{L}}{\partial X^{\alpha}} \right] = \\
  & = \dfrac{d}{d\tau} \dfrac{\partial \mathscr{L}}{\partial \mathbf{X}^{'}} - \dfrac{\partial \mathscr{L}}{\partial \mathbf{X}}
\end{aligned}$$ (eq:point:dynamics:lagrange)

since (1) $\mathbf{U} = \mathbf{E}^{\alpha} U_\alpha = c \mathbf{E}^{\alpha} \frac{\partial}{\partial U^\alpha} \sqrt{U^{\beta} U_{\beta}}$, see {eq}`eq:proof:vel:der-c2`, and $\sqrt{\mathbf{U} \cdot \mathbf{U}}$ independent from $\mathbf{X}$, and equal to $c^2$ and (2) with the definition of the **Lagrangian function**

$$\mathscr{L}(\mathbf{X}'(\tau), \mathbf{X}(\tau), \tau) := - m c \sqrt{\mathbf{X}'(\tau) \cdot \mathbf{X}'(\tau)} - q \mathbf{A}(\mathbf{X}(\tau)) \cdot \mathbf{X}'(\tau)$$

```{dropdown} Proof of the relation used in (1)
:open:

$$\begin{aligned}
   \mathbf{E}^{\alpha} \frac{\partial}{\partial U^\alpha} \sqrt{U^{\beta} U_{\beta}}
   & = \mathbf{E}^{\alpha} \frac{\partial}{\partial U^\alpha} \sqrt{ g_{\beta \gamma} U^{\beta} U^{\gamma}} = \\
   & = \mathbf{E}^{\alpha} \dfrac{1}{2 \sqrt{U^\beta U_\beta}} \left( g_{\beta \gamma} \delta^{\beta}_{\alpha} U^{\gamma} +  g_{\beta \gamma} U^{\beta}\delta_{\alpha}^{\gamma} \right) = \\
   & = \mathbf{E}^{\alpha} \dfrac{1}{2 \sqrt{U^\beta U_\beta}} \left( 2 U_{\alpha} \right) = \\
   & = \mathbf{E}^{\alpha} \dfrac{U_{\alpha}}{\sqrt{U^\beta U_\beta}} = \\
   & = \dfrac{\mathbf{U}}{\sqrt{\mathbf{U} \cdot \mathbf{U}}}     
     = \dfrac{\mathbf{U}}{c}  \ .
\end{aligned}$$ (eq:proof:vel:der-c2)

since $\mathbf{U} \cdot \mathbf{U} = c^2$ and the components of the metric tensor are independent from the velocity.

```

Weak form of the problem is derived from the Lagrange equation {eq}`eq:point:dynamics:lagrange`, with dot product with arbitrary 4-vector $\mathbf{W}$,

$$\begin{aligned}
  0 
  & = \mathbf{W} \cdot \left[ \dfrac{d}{d\tau} \dfrac{\partial \mathscr{L}}{\partial \mathbf{X}^{'}} - \dfrac{\partial \mathscr{L}}{\partial \mathbf{X}} \right] \ .
\end{aligned}$$

and integrating over an interval of proper time and using integration by parts,

$$\begin{aligned}
  0 
  & = \int_{\tau = \tau_0}^{\tau_1} \mathbf{W} \cdot \left[ \dfrac{d}{d\tau} \dfrac{\partial \mathscr{L}}{\partial \mathbf{X}^{'}} - \dfrac{\partial \mathscr{L}}{\partial \mathbf{X}} \right] \, d \tau = \\
  & = \left.\left[ \mathbf{W}(\tau) \cdot \dfrac{\partial \mathscr{L}}{\partial \mathbf{X}'}(\mathbf{X}'(\tau), \mathbf{X}(\tau), \tau) \right]\right|_{\tau_0}^{\tau_1} - \int_{\tau = \tau_0}^{\tau_1} \left[ \mathbf{W}' \cdot \dfrac{\partial \mathscr{L}}{\partial \mathbf{X}^{'}} +  \mathbf{W} \cdot \dfrac{\partial \mathscr{L}}{\partial \mathbf{X}} \right] \, d \tau \ .
\end{aligned}$$

With the choice of the test function $\mathbf{W}(\tau)$ as the variation of the position of the particle, $\mathbf{W} = \delta \mathbf{X}$ just to remember its variational nature, with given values at $\tau_0$, $\tau_1$ and thus $\mathbf{W}(\tau_0) = \mathbf{W}(\tau_1) = 0$, the weak form of the dynamical equations is thus recast as the stationary condition of an action functional in a **variational principle**,

$$0 = - \delta S = - \delta \int_{\tau = \tau_0}^{\tau_1} \mathscr{L}\left(\mathbf{X}'(\tau), \mathbf{X}(\tau), \tau \right) \, d \tau \ .$$

**todo** *Repeat the process using generalized coordinates $q^k(\tau)$, $\mathbf{X}(q^k(\tau), \tau)$*...
```{dropdown} Lagrange equations and variational principle with generalized coordinates


Choosing the test function as it's usually done in deriving Lagrange formulation of mechanics from the strong formulation, after writing the position and its velocity of the particle as a function of generalized coordinates $q^k$,

$$\begin{aligned}
  & \mathbf{X}\left(q^k(\tau), \tau \right) \\
  & \mathbf{U}\left(q^k(\tau), \tau \right) = \dfrac{d \mathbf{X}}{d \tau} = q^{k'}(\tau) \underbrace{\dfrac{\partial \mathbf{X}}{\partial q^k}}_{= \dfrac{\partial \mathbf{X}'}{\partial q^{k'}}} + \dfrac{\partial \mathbf{X}}{\partial \tau} \\
\end{aligned}$$


With the particular choice of the test function, $\mathbf{W} = w^k(\tau) \dfrac{\partial \mathbf{X}}{\partial q^k}(q^l(\tau),\tau)$

```

**Variational principle as a function of time.** Using the relation between proper time $\tau$ and the observer time $t$, $d \tau = \gamma^{-1} \, d t = \sqrt{1 - \frac{|\vec{v}|^2}{c^2}} d t$,

$$\begin{aligned}
  S
  & = \int_{\tau = \tau_0}^{\tau_1} \mathscr{L}\left(\mathbf{X}'(\tau), \mathbf{X}(\tau), \tau \right) \, d \tau = \\
  & = \int_{ t   =  t_0  }^{ t_1  } \mathscr{L}\left(\mathbf{X}'(\tau), \mathbf{X}(\tau), \tau \right) \, \gamma^{-1} \, d t = \\
  & = \int_{ t   =  t_0  }^{ t_1  } \sqrt{1 - \dfrac{|\vec{v}|^2}{c^2}} \left( - m c^2 - \gamma q \phi(\vec{r},t) + \gamma q \vec{a}(\vec{r},t) \cdot \vec{v}(t) \right) \, d t = \\
  & = \int_{ t   =  t_0  }^{ t_1  } \left( - \sqrt{1 - \dfrac{|\vec{v}|^2}{c^2}} m c^2 - q \phi(\vec{r},t) + q \vec{a}(\vec{r},t) \cdot \vec{v}(t) \right) \, d t = \\
  & = \int_{t = t_0}^{t_1} L\left(\vec{v}(t), \vec{r}(t), t \right) \, dt
\end{aligned}$$

**Three-dimensional momentum** can be defined as the partial derivative of the Lagrangian function $L$ w.r.t. the velocity $\vec{v}$,

$$\vec{p} := \dfrac{\partial L}{\partial \vec{v}} = \gamma \dfrac{\vec{v}}{c^2}  m c^2 + q \vec{a} = \gamma m \vec{v} + q \vec{a}$$

The Hamiltoninan function reads

$$\begin{aligned}
  H
  & = \vec{v} \cdot \dfrac{\partial L}{\partial \vec{v}} - L = \\
  & = \gamma m |\vec{v}|^2 + q \vec{a} \cdot \vec{v} + \gamma^{-1} m c^2 + q \phi - q \vec{a} \cdot \vec{v} = \\
  & = \gamma m |\vec{v}|^2 \left[ 1 + \left( 1 - \dfrac{|\vec{v}|^2}{c^2} \right) \dfrac{c^2}{|\vec{v}|^2} \right] + q \phi = \\
  & = \gamma m c^2 + q \phi \ .
\end{aligned}$$

The expressions of the Hamiltonian function (divided by the light speed) and the three-dimensional momentum can be recognized to be respectively the time and space components of 4-momentum,

$$\mathbf{P} = m \mathbf{U} + q \mathbf{A} \ ,$$

remembering the expression of the contravariant components of the 4-velocity and the 4-EM potential,

$$\begin{aligned}
  \left[\mathbf{P}\right]^{\alpha} = \left( \gamma m c + q \dfrac{\phi}{c} , \ \gamma m \vec{v} + q \vec{a} \right) = \left( \dfrac{H}{c} , \ \vec{p}  \right)
\end{aligned}$$



## Electromagnetism

### Classical electromagnetic theory

#### Maxwell equations
Maxwell equations read

$$\begin{cases}
\nabla \cdot \vec{d} = \rho_f \\
\nabla \times \vec{e} + \partial_t \vec{b} = \vec{0} \\
\nabla \cdot \vec{b} = 0 \\
\nabla \times \vec{h} - \partial_t \vec{d} = \vec{j}_f
\end{cases}$$

or in vacuum, with $\rho_f = \rho$, $\vec{j} = \vec{j}_f$, $\vec{d} = \varepsilon_0 \vec{e}$, $\vec{b} = \mu_0 \vec{h}$

$$\begin{cases}
\nabla \cdot \vec{e} = \frac{\rho}{\varepsilon_0} \\
\nabla \times \vec{e} + \partial_t \vec{b} = \vec{0} \\
\nabla \cdot \vec{b} = 0 \\
\nabla \times \vec{b} - \mu_0 \varepsilon_0 \partial_t \vec{e} = \mu_0 \vec{j}
\end{cases}$$

#### Electromagnetic potentials
The electromagnetic field can be written in terms of the electromagnetic potentials

$$\begin{cases}
 \vec{b} = \nabla \times \vec{a} \\
 \vec{e} = -\partial_t \vec{a} - \nabla \varphi \\
\end{cases}$$

#### Lorentz force

A particle in motion in a electromagnetic field is subject to Lorentz force. In classical electromagnetism, the expression of Lorentz force reads

$$\vec{F} = q \left( \vec{e} - \vec{b} \times \vec{v} \right) \ ,$$

whose power is

$$\vec{v} \cdot \vec{F} = \vec{v} \cdot q \left( \vec{e} - \vec{b} \times \vec{v} \right) = q \vec{v} \cdot \vec{e} \ . $$

### Electromagnetic potential

$$\begin{cases}
 \vec{b} = \nabla \times \vec{a} \\
 \vec{e} = -\partial_t \vec{a} - \nabla \varphi \\
\end{cases}$$

$$\mathbf{A} = \mathbf{E}_{\alpha} A^{\alpha} = \frac{\varphi}{c} \mathbf{E}_0 + \vec{a}$$

$$\symbf{\nabla} \mathbf{A} =
\left( \mathbf{E}^{\alpha} \frac{\partial}{\partial X^{\alpha}} \right) \left( A^{\beta} \mathbf{E}_{\beta} \right)
= \frac{\partial A^{\beta}}{\partial X^{\alpha}} \mathbf{E}^{\alpha} \otimes \mathbf{E}_{\beta} 
= g^{\alpha \gamma} \frac{\partial A^{\beta}}{\partial X^{\alpha}} \mathbf{E}_{\gamma} \otimes \mathbf{E}_{\beta}  \ .$$

whose components may be collected in a 2-dimensional array (first index for rows, second index for columns),

$$(\nabla \mathbf{A})_{\alpha}^{\ \ \beta} = \frac{\partial A^{\beta}}{\partial X^{\alpha}} =
\begin{bmatrix}
 c^{-2} \partial_t \varphi & c^{-1}\partial_x \varphi & c^{-1}\partial_y \varphi & c^{-1}\partial_z \varphi \\
 c^{-1} \partial_t a_x     &       \partial_x a_x     &       \partial_y a_x     &       \partial_z a_x     \\
 c^{-1} \partial_t a_y     &       \partial_x a_y     &       \partial_y a_y     &       \partial_z a_y     \\
 c^{-1} \partial_t a_z     &       \partial_x a_z     &       \partial_y a_z     &       \partial_z a_z     \\
\end{bmatrix}$$

or covariant-covariant coomponents,

$$(\nabla \mathbf{A})_{\alpha \beta} = \frac{\partial A_{\beta}}{\partial X^{\alpha}} =\frac{\partial A^{\gamma}}{\partial X^{\alpha}} g_{\gamma \beta}  = 
\begin{bmatrix}
  c^{-2}\partial_t \varphi &-c^{-1}\partial_x \varphi &-c^{-1}\partial_y \varphi &-c^{-1}\partial_z \varphi \\
  c^{-1}\partial_t a_x     &      -\partial_x a_x     &      -\partial_y a_x     &      -\partial_z a_x     \\
  c^{-1}\partial_t a_y     &      -\partial_x a_y     &      -\partial_y a_y     &      -\partial_z a_y     \\
  c^{-1}\partial_t a_z     &      -\partial_x a_z     &      -\partial_y a_z     &      -\partial_z a_z     \\
\end{bmatrix}$$

or contravariant-contravariant coomponents,

$$(\nabla \mathbf{A})^{\alpha \beta} = \frac{\partial A^{\beta}}{\partial X_{\alpha}} = g_{\alpha \gamma} \frac{\partial A^{\beta}}{\partial X^{\gamma}} = 
\begin{bmatrix}
  c^{-2}\partial_t \varphi & c^{-1}\partial_x \varphi & c^{-1}\partial_y \varphi & c^{-1}\partial_z \varphi \\
 -c^{-1}\partial_t a_x     &      -\partial_x a_x     &      -\partial_y a_x     &      -\partial_z a_x     \\
 -c^{-1}\partial_t a_y     &      -\partial_x a_y     &      -\partial_y a_y     &      -\partial_z a_y     \\
 -c^{-1}\partial_t a_z     &      -\partial_x a_z     &      -\partial_y a_z     &      -\partial_z a_z     \\
\end{bmatrix}$$

The electromagnetic field tensor is defined as the anti-symmetric part of the gradient of the 4-electromagnetic potential,

$$\mathbf{F} = \left[ \symbf{\nabla} \mathbf{A} - \left( \symbf{\nabla} \mathbf{A} \right)^T \right]$$ (eq:tensor:em-field)

whose components may be collected in a 2-dimensional array (first index for rows, second index for columns),

$$F^{\alpha \beta} = 
\begin{bmatrix}
                        0 & -\frac{\underline{e}^T}{c} \\
  \frac{\underline{e}}{c} & \underline{b}_{\times}
\end{bmatrix}
\qquad , \qquad 
F_{\alpha \beta} = 
\begin{bmatrix}
                        0 & \frac{\underline{e}^T}{c} \\
 -\frac{\underline{e}}{c} & \underline{b}_{\times}
\end{bmatrix}
$$
$$
F_{\alpha}^{\ \ \beta} = 
\begin{bmatrix}
                        0 &-\frac{\underline{e}^T}{c} \\
 -\frac{\underline{e}}{c} &-\underline{b}_{\times}
\end{bmatrix}
\qquad , \qquad 
F^{\alpha}_{\ \ \beta} = 
\begin{bmatrix}
                        0 & \frac{\underline{e}^T}{c} \\
  \frac{\underline{e}}{c} &-\underline{b}_{\times}
\end{bmatrix}
$$

### Electromagnetic field and electromagnetic field equations

The pair of Maxwell equations

$$\begin{cases}
  \rho_f    = \nabla \cdot \vec{d}  \\
  \vec{j}_f = - \partial_t \vec{d} + \nabla \times \vec{h}  \\
\end{cases}$$

can be re-written in $4$-formalism, using $4$-gradient in Cartesian coordinates

$$\symbf{\nabla} = \mathbf{E}^{\alpha} \frac{\partial}{\partial X^{\alpha}}
 = \mathbf{E}_0 \, \frac{\partial }{c \partial t} + \mathbf{E}_i \frac{\partial}{\partial x^i}
 = \mathbf{E}_0 \, \frac{\partial }{c \partial t} + \nabla \ ,$$

and the definition of the 4-current density vector

$$\mathbf{J} = J^{\alpha} \mathbf{E}_{\alpha} = c \rho \, \mathbf{E}_0 + \vec{j}$$

so that

$$\begin{aligned}
  c \rho \mathbf{E}_0 + \vec{j} = \symbf{\nabla} \cdot \mathbf{F} 
  = \symbf{\nabla} \cdot
   [ & ( 0\, \mathbf{E}_0 + c \vec{d} ) \otimes \mathbf{E}_0 + ( - \mathbf{E}_0 c \vec{d} + \vec{h}_{\times} ) ] \ ,
\end{aligned}$$

with the displacement field tensor,

$$\mathbf{D} = D^{\alpha \beta} \, \mathbf{E}_{\alpha} \, \mathbf{E}_{\beta} \ , $$

with components (rows for the first index, columns for the second index)

$$D^{\alpha \beta} = 
  \begin{bmatrix}     0 & -c d_x & - c d_y & - c d_z \\
                  c d_x &      0 & -   h_z &     h_y \\
                  c d_y &    h_z &       0 & -   h_x \\
                  c d_z & -  h_y &     h_x &       0 \\
  \end{bmatrix} =
  \begin{bmatrix} 0 & - c \underline{d}^T \\ c \underline{d} & \underline{h}_{\times}
  \end{bmatrix} \ .
$$


<!--
$$\begin{aligned}
  \mathbf{0} = \symbf{\nabla} \cdot \mathbf{F} 
  = \symbf{\nabla} \cdot
   [ & ( 0\, \mathbf{E}_0 + b_x \mathbf{E}_1 + b_y \mathbf{E}_2 + b_z \mathbf{E}_3 ) \otimes \mathbf{E}_0 + \\
   + & ( b_x \mathbf{E}_0 + 0\, \mathbf{E}_1 + e_z \mathbf{E}_2 - e_y \mathbf{E}_3 ) \otimes \mathbf{E}_1 + \\
   + & ( b_y \mathbf{E}_0 - e_z \mathbf{E}_1 + 0\, \mathbf{E}_2 + e_x \mathbf{E}_3 ) \otimes \mathbf{E}_2 + \\
   + & ( b_z \mathbf{E}_0 + e_y \mathbf{E}_1 - e_x \mathbf{E}_2 + 0\, \mathbf{E}_3 ) \otimes \mathbf{E}_3 ] \\
  = \symbf{\nabla} \cdot
   [ & ( 0\, \mathbf{E}^0 + b_x \mathbf{E}^1 + b_y \mathbf{E}^2 + b_z \mathbf{E}^3 ) \otimes \mathbf{E}_0 + \\
   + & ( b_x \mathbf{E}^0 + 0\, \mathbf{E}^1 + e_z \mathbf{E}^2 - e_y \mathbf{E}^3 ) \otimes \mathbf{E}_1 + \\
   + & ( b_y \mathbf{E}^0 + e_z \mathbf{E}^1 + 0\, \mathbf{E}^2 + e_x \mathbf{E}^3 ) \otimes \mathbf{E}_2 + \\
   + & ( b_z \mathbf{E}^0 - e_y \mathbf{E}^1 + e_x \mathbf{E}^2 + 0\, \mathbf{E}^3 ) \otimes \mathbf{E}_3 ]
\end{aligned}$$
-->

The pair of Maxwell equations

$$\begin{cases}
  \nabla \cdot \vec{b} = 0 \\
  \partial_t \vec{b} + \nabla \times \vec{e} = \vec{0} \\
\end{cases}$$

can be re-written in $4$-formalism as

$$0 = \partial_{\mu} F_{\eta \xi} + \partial_{\eta} F_{\xi \mu} + \partial_{\xi} F_{\mu \eta} $$

Among these $64 = 4^3$ equations, there are only 4 independent equations.
- If 2 indices are the same, the corresponding equation is the identity $0 = 0$. As an example, if $\mu = \eta$

   $$0 =  \partial_{\mu} F_{\mu \xi} + \partial_{\mu} \underbrace{F_{\xi \mu}}_{-F_{\mu \xi}} + \partial_{\xi} \underbrace{F_{\mu \mu}}_{=0} = 0 \ , $$

   thus only combinations with different indices may provide some information.

- Given the ordered set of indices $(\mu, \eta, \xi)$, switching a pair of indices provides the same equation. As an example, switching $\mu$ and $\eta$

  $$\begin{aligned}
    0 & = \partial_{\eta} F_{\mu  \xi} + \partial_{\mu} F_{\xi \eta} + \partial_{\xi} F_{\eta \mu} = \\
      & = \partial_{\eta} ( - F_{\xi \mu} ) + \partial_{\mu} ( - F_{\eta \xi} ) + \partial_{\xi} ( -F_{\mu \eta} ) \ .
  \end{aligned}$$

- Thus, only 4 combination of different indices, without taking order into account, provide independent information

  $$\begin{aligned}
    (1,2,3): & \quad 0 = \partial_{1} F_{23} + \partial_{2} F_{31} + \partial_{3} F_{12} = \partial_x (-b_x) + \partial_y (-b_y) + \partial_z (-b_z)  \\
    (2,3,0): & \quad 0 = \partial_{2} F_{30} + \partial_{3} F_{02} + \partial_{0} F_{23} = \partial_y \left(-\frac{e_z}{c} \right) + \partial_z \left( \frac{e_y}{c} \right) + \partial_{ct} (-b_x) \\
    (3,0,1): & \quad 0 = \partial_{3} F_{01} + \partial_{0} F_{13} + \partial_{1} F_{30} = \partial_z \left(\frac{e_x}{c}\right) + \partial_{ct} (-b_y) + \partial_x  \left(-\frac{e_z}{c}\right) \\
    (0,1,2): & \quad 0 = \partial_{0} F_{12} + \partial_{1} F_{20} + \partial_{2} F_{01} = \partial_{ct} (-b_z) + \partial_x \left(-\frac{e_y}{c}\right) + \partial_y  \left(\frac{e_x}{c}\right)     \\
  \end{aligned}$$

  i.e.
  
  $$\begin{aligned}
    (1,2,3): & \quad 0 = - \nabla \cdot \vec{b} \\
    (2,3,0): & \quad 0 = -\frac{1}{c} \left[ \partial_t b_x + (\partial_y e_z - \partial_z e_y ) \right] \\ 
    (3,0,1): & \quad 0 = -\frac{1}{c} \left[ \partial_t b_y + (\partial_z e_x - \partial_x e_z ) \right] \\
    (0,1,2): & \quad 0 = -\frac{1}{c} \left[ \partial_t b_z + (\partial_x e_y - \partial_y e_x ) \right] \\
  \end{aligned}$$

  i.e.

  $$\begin{cases}
        0  = \nabla \cdot \vec{b} \\
   \vec{0} = \partial_t \vec{b} + \nabla \times \vec{e} \\
  \end{cases}$$

### Point particle in electromagnetic field

Lorentz 4-force acting on a point charge of electric charge charge $q$ reads

$$\mathbf{f} = \mathbf{F} \cdot \mathbf{J} = q \, \mathbf{F} \cdot \mathbf{U} \ .$$

so that the dynamical equation reads

$$m \, \mathbf{X}'' = q \, \mathbf{F} \cdot \mathbf{X}'$$


### Energy balance

Continuity

$$\nabla \cdot \mathbf{J} = 0$$

Maxwell's equations

$$\begin{aligned}
  \nabla \cdot \mathbf{D} = \mathbf{J} \\
  \nabla \cdot \left( \symbf{\varepsilon} : \mathbf{F} \right) = \mathbf{0} \\
\end{aligned}$$

Energy and momentum balance equation of the EM field using 3-dimensional formalism,

$$\begin{aligned}
  \frac{\partial u      }{\partial t} + \nabla \cdot \vec{s} & = - \vec{e} \cdot \vec{j}^f \\
  \frac{\partial \vec{s}}{\partial t} + \nabla \cdot \left\{ c^2 \left[ \dfrac{1}{2} \left( \vec{d} \cdot \vec{e} + \vec{h} \cdot \vec{b} \right) \mathbb{I} - \left( \vec{d} \otimes \vec{e} + \vec{h} \otimes \vec{b} \right) \right] \right\} & = - c^2 (\rho^f \vec{e} - \vec{b} \times \vec{j}^f) \\
\end{aligned}$$

$$\begin{aligned}
  \frac{1}{c} \frac{\partial u}{\partial t} + \nabla \cdot \left( \frac{\vec{s}}{c} \right) & = - \frac{\vec{e}}{c} \cdot \vec{j}^f \\
  \frac{1}{c} \frac{\partial}{\partial t} \frac{ \vec{s}}{c} + \nabla \cdot \left[ \dfrac{1}{2} \left( \vec{d} \cdot \vec{e} + \vec{h} \cdot \vec{b} \right) \mathbb{I} - \left( \vec{d} \otimes \vec{e} + \vec{h} \otimes \vec{b} \right) \right] & = - \rho^f c \frac{\vec{e}}{c} + \vec{b} \times \vec{j}^f \\
\end{aligned}$$ (eq:energy-momentum-equation:3d)

The governing equations of energy and momentum of the EM field can be recast in 4-dimensional formalism,

$$\symbf{\nabla} \cdot \mathbf{T} = - \mathbf{F} \cdot \mathbf{J}$$

with the **energy-momentum-stress tensor**, $\mathbf{T}$, 

$$\begin{aligned}
  T^{\alpha \beta} & = \dfrac{1}{4} g^{\alpha \beta} F_{\mu \nu} D^{\mu \nu} - F^{\alpha \nu} D^{\beta}_{\ \ \nu} = \\
                   & = \dfrac{1}{4} g^{\alpha \beta} F_{\mu \nu} D^{\mu \nu} - F^{\alpha \nu} g^{\beta \mu} D_{\mu \nu} = \\
                   & = \dfrac{1}{4} g^{\alpha \beta} F_{\mu \nu} D^{\mu \nu} + F^{\alpha \nu} D_{\nu \mu} g^{\mu \beta} \\
\end{aligned}$$ (eq:energy-momentum-tensor:0)

```{dropdown} Term $\ \mathbf{g} \ \mathbf{F} : \mathbf{D} $

$$\mathbf{F} : \mathbf{D} = F_{\mu \nu} D^{\mu \nu} =
  \begin{bmatrix} 0 & \frac{\underline{e}^T}{c} \\ -\frac{\underline{e}}{c} & \underline{b}_{\times} \end{bmatrix} :
  \begin{bmatrix} 0 & -c \underline{d}^T \\ c \underline{d} & \underline{h}_{\times} \end{bmatrix} = - 2 \underline{e}^T \underline{d} + 2 \underline{b}^T \underline{h} = 2 \left( - \vec{e} \cdot \vec{d} + \vec{b} \cdot \vec{h} \right) \ .
$$ (eq:energy-momentum-tensor:1)

```

```{dropdown} Term $\ F^{\alpha \nu} D^{\beta}_{\ \ \nu}$

$$F^{\alpha \nu} D^{\beta}_{\ \ \nu} =
  \begin{bmatrix} 0 & -\frac{\underline{e}^T}{c} \\ \frac{\underline{e}}{c} & \underline{b}_{\times} \end{bmatrix} 
  \begin{bmatrix} 0 & c \underline{d}^T \\ c \underline{d} & -\underline{h}^T_{\times} \end{bmatrix} = 
  \begin{bmatrix}
    - \underline{e}^T \underline{d} & \frac{\left( \underline{h} \times \underline{e} \right)^T}{c} \\
      c  \underline{b} \times \underline{d} & \underline{e} \underline{d}^T + \underline{b}_{\times} \underline{h}_{\times}
  \end{bmatrix}
$$ (eq:energy-momentum-tensor:2)

being

$$\underline{e}^T \underline{h}^T_{\times} = e_i \varepsilon_{kji} h_j = \left( \vec{h} \times \vec{e} \right)_k$$

$$\left[ \underline{b}_{\times} \underline{h}_{\times} \right]_{im} = \varepsilon_{ijk} b_{j} \varepsilon_{klm} h_{l} = \left( \delta_{il} \delta_{jm} - \delta_{im} \delta_{jl} \right) b_j h_l = h_i b_m - b_l h_l \delta_{im} = \underline{h} \underline{b}^T - \underline{b}^T \underline{h} \underline{\underline{I}}_3 \ .$$

```

```{dropdown} Energy-stress tensor
:open:

Putting together the expression {eq}`eq:energy-momentum-tensor:1` of term $\frac{1}{4} g^{\alpha \beta} F_{\mu \nu} D^{\mu \nu}$ and {eq}`eq:energy-momentum-tensor:2` of term $F^{\alpha \nu} D^{\beta}_{\ \ \nu}$, with $\underline{d} = \varepsilon \underline{e}$, $\underline{b} = \mu \underline{h}$ (**todo** do energy balance for all charges and currents and spearating contributions of free and bound charges and currents)

$$\begin{aligned}
 T^{\alpha \beta}
& =
\dfrac{1}{4} \begin{bmatrix} 2(-\underline{e}^T \underline{d} + \underline{b}^T \underline{h}) & \underline{0}^T \\ \underline{0} & - 2(-\underline{e}^T \underline{d} + \underline{b}^T \underline{h}) \underline{\underline{I}} \end{bmatrix}
- 
  \begin{bmatrix}
    - \underline{e}^T \underline{d} & \frac{\left( \underline{e} \times \underline{h} \right)^T}{c} \\
      c \underline{b} \times \underline{d} & \underline{e} \underline{d}^T + \underline{b}_{\times} \underline{h}_{\times}
  \end{bmatrix} = \\
& =
\begin{bmatrix} \dfrac{1}{2}\left(\underline{e}^T \underline{d} + \underline{b}^T \underline{h} \right) & \frac{\left( \underline{e} \times \underline{h} \right)^T}{c} \\ \frac{\underline{e} \times \underline{h}}{c} & \dfrac{1}{2}(\underline{e}^T \underline{d} + \underline{b}^T \underline{h}) \underline{\underline{I}}_3 - \underline{e} \underline{d}^T - \underline{b} \underline{h}^T \end{bmatrix} = \\
& =
\begin{bmatrix} u & \dfrac{\vec{s}}{c} \\ \dfrac{\vec{s}}{c} & u \mathbb{I} - \vec{e} \otimes \vec{d} - \vec{b} \otimes \vec{h} \end{bmatrix}
\end{aligned}$$

```

```{dropdown} Energy-stress equation in 4-dimensional formalism
:open:

Energy and momentum balance equations {eq}`eq:energy-momentum-equation:3d` can be recast using 4-dimensional formalism,

$$\begin{aligned}
  \nabla \cdot \mathbf{T} & = - \mathbf{F} \cdot \mathbf{J}  \\
  \dfrac{\partial T^{\nu \mu} }{\partial X^{\nu}} & = - F^{\mu \nu} J_{\nu}
\end{aligned}$$

as

<!--
$$F^{\alpha}_{\ \ \beta} J^{\beta} = \begin{bmatrix} 0 & - \frac{\underline{e}^T}{c} \\ - \frac{\underline{e}}{c} & - \underline{b}_{\times} \end{bmatrix} \begin{bmatrix} \rho c \\ \underline{j} \end{bmatrix} = $$
-->

<!--
$$F^{\alpha}_{\ \ \beta} J^{\beta} = \begin{bmatrix} 0 &   \frac{\underline{e}^T}{c} \\ \frac{\underline{e}}{c} &-\underline{b}_{\times} \end{bmatrix} \begin{bmatrix} \rho c \\ \underline{j} \end{bmatrix} = \begin{bmatrix} \frac{1}{c} \underline{e}^T \underline{j} \\ \rho \underline{e} - \underline{b}_\times \underline{j} \end{bmatrix}$$

or equivalently
-->

$$F^{\mu \nu} J_{\nu} = \begin{bmatrix} 0 &  -\frac{\underline{e}^T}{c} \\ \frac{\underline{e}}{c} & \underline{b}_{\times} \end{bmatrix} \begin{bmatrix} \rho c \\ - \underline{j} \end{bmatrix} = \begin{bmatrix} \frac{1}{c} \underline{e}^T \underline{j} \\ \rho \underline{e} - \underline{b}_\times \underline{j} \end{bmatrix}$$

$$\begin{aligned}
  0   & : \quad \dfrac{\partial T^{\nu 0}}{\partial X^{\nu}} = - F^{0 \nu} J_{\nu} && \dfrac{1}{c}\dfrac{\partial}{\partial t} u + \dfrac{\partial}{\partial x_k} \dfrac{s_k}{c} = - \dfrac{1}{c} e_k j_k \\
  1:3 & : \quad \dfrac{\partial T^{\nu i}}{\partial X^{\nu}} = - F^{i \nu} J_{\nu} && \dfrac{1}{c}\dfrac{\partial}{\partial t} \dfrac{s_i}{c} + \dfrac{\partial \sigma_{ki}}{\partial x_k} = - \rho e_i + \varepsilon_{ijk} b_j j_k  \\
\end{aligned}$$

```

<!--
$$\dfrac{\partial D^{\alpha \beta}}{\partial X^{\alpha}} = J^{\beta}$$

$$\begin{aligned}
  - F_{\gamma \beta} \dfrac{\partial D^{\alpha \beta}}{\partial X^{\alpha}} & = - F_{\gamma \beta} J^{\beta}
\end{aligned}$$
-->


**Relativity under Lorentz's transformation.** Components of the description of two inertial observers in relative motion, with aligned Cartesian space coordinates, are related by Lorentz's transformation

```{dropdown} Energy-momentum-stress tensor
:open:

Contravariant (Cartesian in space) components of the energy-momentu-stress tensor can be collected in a symmetric matrix

$$\begin{aligned}
  \begin{bmatrix} u' & \mathbf{s}^{'T}/c \\ \mathbf{s}'/c & \symbf{\sigma}' \end{bmatrix} 
  & = \begin{bmatrix} \gamma & - \gamma \mathbf{v}^T \\ -\gamma \mathbf{v} & \mathbf{I}_3 + (\gamma-1) \mathbf{\hat{v}}\mathbf{\hat{v}}^T  \end{bmatrix} \begin{bmatrix} u' & \mathbf{s}^{'T}/c \\ \mathbf{s}'/c & \symbf{\sigma}' \end{bmatrix} \begin{bmatrix} \gamma & - \gamma \mathbf{v}^T \\ -\gamma \mathbf{v} & \mathbf{I}_3 + (\gamma-1) \mathbf{\hat{v}}\mathbf{\hat{v}}^T \end{bmatrix}^T = \\
  & = \begin{bmatrix} \gamma & - \gamma \mathbf{v}^T \\ -\gamma \mathbf{v} & \mathbf{I}_3 + (\gamma-1) \mathbf{\hat{v}}\mathbf{\hat{v}}^T  \end{bmatrix} \begin{bmatrix} \gamma c v d_v & - c \mathbf{d}^T - (\gamma-1) c d_v \hat{\mathbf{v}}^T \\ \gamma c \mathbf{d} - \gamma \mathbf{h}_\times \mathbf{v} & -\gamma c \mathbf{d} \mathbf{v}^T + \mathbf{h}_\times + (\gamma-1) \mathbf{h}_\times \mathbf{\hat{v}} \mathbf{\hat{v}}^T \end{bmatrix} = \\
  & = \begin{bmatrix} 0 & \text{anti-sym} \\ c \mathbf{d}' & \mathbf{h}'_{\times} \end{bmatrix} = \\
\end{aligned}$$

with

$$\begin{aligned}
  c \mathbf{d}'
  & = - \gamma^2 c v^2 \mathbf{\hat{v}} d_v + \gamma c \mathbf{d} - \gamma \mathbf{h}_\times \mathbf{v} + \gamma(\gamma-1) c \hat{\mathbf{v}}d_v
  = \\
  & = c \gamma^2 \hat{\mathbf{v}} d_v \underbrace{(1 - v^2)}_{= \gamma^{-2}} + \gamma c \mathbf{d} - \gamma \mathbf{h} \times \mathbf{v} - \gamma c \hat{\mathbf{v}} d_v = \\
  & = \gamma c \mathbf{d} - \gamma \mathbf{h} \times \mathbf{v} + ( 1 - \gamma ) c \hat{\mathbf{v}} \hat{\mathbf{v}} \cdot \mathbf{d} \ ,
\end{aligned}$$

and

$$\begin{aligned}
  \mathbf{h}'_{\times} & = && (1) \\
  & = \gamma c v \hat{\mathbf{v}} \mathbf{d}^T + \gamma (\gamma - 1) c v d_v \hat{\mathbf{v}} \hat{\mathbf{v}}^T + \\
  & - \gamma c v \mathbf{d} \hat{\mathbf{v}} + \mathbf{h}_{\times} + (\gamma - 1) (\mathbf{h} \times \hat{\mathbf{v}}) \hat{\mathbf{v}}^T - \gamma (\gamma - 1) c v d_v \hat{\mathbf{v}} \hat{\mathbf{v}}^T + (\gamma-1) \hat{\mathbf{v}} \mathbf{v}^T \mathbf{h}_{\times} + \mathbf{0} = && (2) \\
  & = \gamma c v \left( \hat{\mathbf{v}} \mathbf{d}^T - \mathbf{d} \hat{\mathbf{v}}^T \right) + \mathbf{h}_{\times} + (\gamma-1) \left( \left( \mathbf{h}_\times \hat{\mathbf{v}}  \right) \hat{\mathbf{v}}^T  - \hat{\mathbf{v}} \left( \mathbf{h}_\times \hat{\mathbf{v}}\right)^T \right) = && (3) \\
  & = \gamma c v \left( \mathbf{d} \times \hat{\mathbf{v}} \right)_{\times} + \mathbf{h}_{\times} + (\gamma-1) \left( \hat{\mathbf{v}} \times (\mathbf{h} \times \hat{\mathbf{v}}) \right)_{\times}
\end{aligned}$$

having (1) recognized that $\hat{\mathbf{v}} \hat{\mathbf{v}}^T \mathbf{h}_\times \hat{\mathbf{v}} \hat{\mathbf{v}}^T = \hat{\mathbf{v}}( \hat{\mathbf{v}} \cdot ( \mathbf{h} \times \hat{\mathbf{v}}) ) \hat{\mathbf{v}} = \mathbf{0}$, (2) $\{ \mathbf{v}^T \mathbf{h}_{\times} \}_k = v_i \varepsilon_{ijk} h_j = - \{ \mathbf{h}\times \hat{\mathbf{v}} \}_k$ and (3)

$$\begin{aligned}
  \left[ \left(\mathbf{a}_{\times} \mathbf{b} \right)_{\times} \right]_{ij} 
  & = \varepsilon_{ikj} \varepsilon_{klm} a_l b_m = \\
  & = \left( \delta_{jl} \delta_{im} - \delta_{jm} \delta_{il} \right) a_l b_m = \\
  & = a_j b_i - a_i b_j = \left[ \mathbf{b} \mathbf{a}^T - \mathbf{a} \mathbf{b}^T \right]_{ij} \ . 
\end{aligned}$$

Thus 

$$\begin{aligned}
\mathbf{h}' 
  & = \mathbf{h} - \gamma c \mathbf{v} \times \mathbf{d} + (1 -\gamma) (\mathbf{h} \times \hat{\mathbf{v}}) \times \hat{\mathbf{v}} = \\
  & = \mathbf{h} - \gamma c \mathbf{v} \times \mathbf{d} + (1 -\gamma) \left( \hat{\mathbf{v}} \hat{\mathbf{v}} \cdot \mathbf{h} - \mathbf{h}  \right) = \\
  & = \gamma \mathbf{h} - \gamma c \mathbf{v} \times \mathbf{d} + (1 -\gamma) \hat{\mathbf{v}} \hat{\mathbf{v}} \cdot \mathbf{h} \ .
\end{aligned}$$

Going back from non dimensional velocity to dimensional velocity $c \mathbf{v} \rightarrow \mathbf{v}$,

$$\begin{aligned}
  \mathbf{d}' & = \gamma \left( \mathbf{d} - \dfrac{\mathbf{h} \times \mathbf{v}}{c^2} \right) + (1-\gamma) \hat{\mathbf{v}} \, \hat{\mathbf{v}} \cdot \mathbf{d} \\
  \mathbf{h}' & = \gamma \left( \mathbf{h} - \mathbf{v} \times \mathbf{d} \right) + (1 - \gamma) \hat{\mathbf{v}} \, \hat{\mathbf{v}} \cdot \mathbf{h} \\
\end{aligned}$$

Repeating the same process for the electromagnetic field tensor

$$\begin{aligned}
  \left[\mathbf{F}\right]^{\alpha \beta} = \begin{bmatrix} 0 & - \dfrac{\mathbf{e}^T}{c} \\ \dfrac{\mathbf{e}}{c} & \mathbf{b}_{\times} \end{bmatrix} 
\end{aligned}$$

$$\begin{aligned}
  \mathbf{e}' & = \gamma \left( \mathbf{e} -        \mathbf{b} \times \mathbf{v}       \right) + (1-\gamma) \hat{\mathbf{v}} \, \hat{\mathbf{v}} \cdot \mathbf{e} \\
  \mathbf{b}' & = \gamma \left( \mathbf{b} - \dfrac{\mathbf{v} \times \mathbf{e}}{c^2} \right) + (1 - \gamma) \hat{\mathbf{v}} \, \hat{\mathbf{v}} \cdot \mathbf{b} \\
\end{aligned}$$



```






```{dropdown} Electromagnetic field tensor
Contravariant components of the electromagnetic field tensor

$$\begin{aligned}
  \begin{bmatrix} 0 & - c \mathbf{d}'^T \\ c \mathbf{d}' & \mathbf{h}'_{\times} \end{bmatrix} 
  & = \begin{bmatrix} \gamma & - \gamma \mathbf{v}^T \\ -\gamma \mathbf{v} & \mathbf{I}_3 + (\gamma-1) \mathbf{\hat{v}}\mathbf{\hat{v}}^T  \end{bmatrix} \begin{bmatrix} 0 & - c \mathbf{d}^T \\ c \mathbf{d} & \mathbf{h}_{\times}\end{bmatrix} \begin{bmatrix} \gamma & - \gamma \mathbf{v}^T \\ -\gamma \mathbf{v} & \mathbf{I}_3 + (\gamma-1) \mathbf{\hat{v}}\mathbf{\hat{v}}^T \end{bmatrix}^T = \\
  & = \begin{bmatrix} \gamma & - \gamma \mathbf{v}^T \\ -\gamma \mathbf{v} & \mathbf{I}_3 + (\gamma-1) \mathbf{\hat{v}}\mathbf{\hat{v}}^T  \end{bmatrix} \begin{bmatrix} \gamma c v d_v & - c \mathbf{d}^T - (\gamma-1) c d_v \hat{\mathbf{v}}^T \\ \gamma c \mathbf{d} - \gamma \mathbf{h}_\times \mathbf{v} & -\gamma c \mathbf{d} \mathbf{v}^T + \mathbf{h}_\times + (\gamma-1) \mathbf{h}_\times \mathbf{\hat{v}} \mathbf{\hat{v}}^T \end{bmatrix} = \\
  & = \begin{bmatrix} 0 & \text{anti-sym} \\ c \mathbf{d}' & \mathbf{h}'_{\times} \end{bmatrix} = \\
\end{aligned}$$

with

$$\begin{aligned}
  c \mathbf{d}'
  & = - \gamma^2 c v^2 \mathbf{\hat{v}} d_v + \gamma c \mathbf{d} - \gamma \mathbf{h}_\times \mathbf{v} + \gamma(\gamma-1) c \hat{\mathbf{v}}d_v
  = \\
  & = c \gamma^2 \hat{\mathbf{v}} d_v \underbrace{(1 - v^2)}_{= \gamma^{-2}} + \gamma c \mathbf{d} - \gamma \mathbf{h} \times \mathbf{v} - \gamma c \hat{\mathbf{v}} d_v = \\
  & = \gamma c \mathbf{d} - \gamma \mathbf{h} \times \mathbf{v} + ( 1 - \gamma ) c \hat{\mathbf{v}} \hat{\mathbf{v}} \cdot \mathbf{d} \ ,
\end{aligned}$$

and

$$\begin{aligned}
  \mathbf{h}'_{\times} & = && (1) \\
  & = \gamma c v \hat{\mathbf{v}} \mathbf{d}^T + \gamma (\gamma - 1) c v d_v \hat{\mathbf{v}} \hat{\mathbf{v}}^T + \\
  & - \gamma c v \mathbf{d} \hat{\mathbf{v}} + \mathbf{h}_{\times} + (\gamma - 1) (\mathbf{h} \times \hat{\mathbf{v}}) \hat{\mathbf{v}}^T - \gamma (\gamma - 1) c v d_v \hat{\mathbf{v}} \hat{\mathbf{v}}^T + (\gamma-1) \hat{\mathbf{v}} \mathbf{v}^T \mathbf{h}_{\times} + \mathbf{0} = && (2) \\
  & = \gamma c v \left( \hat{\mathbf{v}} \mathbf{d}^T - \mathbf{d} \hat{\mathbf{v}}^T \right) + \mathbf{h}_{\times} + (\gamma-1) \left( \left( \mathbf{h}_\times \hat{\mathbf{v}}  \right) \hat{\mathbf{v}}^T  - \hat{\mathbf{v}} \left( \mathbf{h}_\times \hat{\mathbf{v}}\right)^T \right) = && (3) \\
  & = \gamma c v \left( \mathbf{d} \times \hat{\mathbf{v}} \right)_{\times} + \mathbf{h}_{\times} + (\gamma-1) \left( \hat{\mathbf{v}} \times (\mathbf{h} \times \hat{\mathbf{v}}) \right)_{\times}
\end{aligned}$$

having (1) recognized that $\hat{\mathbf{v}} \hat{\mathbf{v}}^T \mathbf{h}_\times \hat{\mathbf{v}} \hat{\mathbf{v}}^T = \hat{\mathbf{v}}( \hat{\mathbf{v}} \cdot ( \mathbf{h} \times \hat{\mathbf{v}}) ) \hat{\mathbf{v}} = \mathbf{0}$, (2) $\{ \mathbf{v}^T \mathbf{h}_{\times} \}_k = v_i \varepsilon_{ijk} h_j = - \{ \mathbf{h}\times \hat{\mathbf{v}} \}_k$ and (3)

$$\begin{aligned}
  \left[ \left(\mathbf{a}_{\times} \mathbf{b} \right)_{\times} \right]_{ij} 
  & = \varepsilon_{ikj} \varepsilon_{klm} a_l b_m = \\
  & = \left( \delta_{jl} \delta_{im} - \delta_{jm} \delta_{il} \right) a_l b_m = \\
  & = a_j b_i - a_i b_j = \left[ \mathbf{b} \mathbf{a}^T - \mathbf{a} \mathbf{b}^T \right]_{ij} \ . 
\end{aligned}$$

Thus 

$$\begin{aligned}
\mathbf{h}' 
  & = \mathbf{h} - \gamma c \mathbf{v} \times \mathbf{d} + (1 -\gamma) (\mathbf{h} \times \hat{\mathbf{v}}) \times \hat{\mathbf{v}} = \\
  & = \mathbf{h} - \gamma c \mathbf{v} \times \mathbf{d} + (1 -\gamma) \left( \hat{\mathbf{v}} \hat{\mathbf{v}} \cdot \mathbf{h} - \mathbf{h}  \right) = \\
  & = \gamma \mathbf{h} - \gamma c \mathbf{v} \times \mathbf{d} + (1 -\gamma) \hat{\mathbf{v}} \hat{\mathbf{v}} \cdot \mathbf{h} \ .
\end{aligned}$$

Going back from non dimensional velocity to dimensional velocity $c \mathbf{v} \rightarrow \mathbf{v}$,

$$\begin{aligned}
  \mathbf{d}' & = \gamma \left( \mathbf{d} - \dfrac{\mathbf{h} \times \mathbf{v}}{c^2} \right) + (1-\gamma) \hat{\mathbf{v}} \, \hat{\mathbf{v}} \cdot \mathbf{d} \\
  \mathbf{h}' & = \gamma \left( \mathbf{h} - \mathbf{v} \times \mathbf{d} \right) + (1 - \gamma) \hat{\mathbf{v}} \, \hat{\mathbf{v}} \cdot \mathbf{h} \\
\end{aligned}$$

Repeating the same process for the electromagnetic field tensor

$$\begin{aligned}
  \left[\mathbf{F}\right]^{\alpha \beta} = \begin{bmatrix} 0 & - \dfrac{\mathbf{e}^T}{c} \\ \dfrac{\mathbf{e}}{c} & \mathbf{b}_{\times} \end{bmatrix} 
\end{aligned}$$

$$\begin{aligned}
  \mathbf{e}' & = \gamma \left( \mathbf{e} -        \mathbf{b} \times \mathbf{v}       \right) + (1-\gamma) \hat{\mathbf{v}} \, \hat{\mathbf{v}} \cdot \mathbf{e} \\
  \mathbf{b}' & = \gamma \left( \mathbf{b} - \dfrac{\mathbf{v} \times \mathbf{e}}{c^2} \right) + (1 - \gamma) \hat{\mathbf{v}} \, \hat{\mathbf{v}} \cdot \mathbf{b} \\
\end{aligned}$$



```





