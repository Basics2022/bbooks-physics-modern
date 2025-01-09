(relativity-special)=
# Special Relativity

An event is determined by spatio-temporal information together, $t, \vec{r}$. Absolute nature of physics needs vector algebra and calculus formalism

$$\mathbf{X} = c  \,t  \,\mathbf{e}_0 + \vec{r} =  c \, t \, \mathbf{e}_0 + x^1 \mathbf{e}_1 + x^2 \mathbf{e}_2 + x^3 \mathbf{e}_3 = X^{\alpha} \mathbf{E}_{\alpha} \ ,$$

having used Cartesian coordiantes for the space coordinate.

Minkowski metric reads

$$g_{\alpha \beta} = \mathbf{E}_{\alpha} \cdot \mathbf{E}_{\beta} = \text{diag}\{-1, 1, 1, 1\}$$

The reciprocal basis reads $\mathbf{E}_{\alpha} \cdot \mathbf{E}^{\beta} = \delta_{\alpha}^{\beta}$, $\mathbf{E}_{\alpha} = g_{\alpha \beta} \mathbf{E}^{\beta}$, s.t. the elementary interval between two events can be written as

$$d \mathbf{X} = d X^{\alpha} \, \mathbf{E}_{\alpha} = \underbrace{d X^{\alpha} \, g_{\alpha \beta}}_{= dX_{\beta}} \, \mathbf{E}^{\beta} = d X_{\beta} \, \mathbf{E}^{\beta} \ ,$$

having used Cartesian coordinates,

$$
  \begin{aligned}  & X^0 = c t \\  & X_0 = c t \end{aligned} \qquad
  \begin{aligned}  & X^1 =   x \\  & X_1 =  -x \end{aligned} \qquad
  \begin{aligned}  & X^2 =   y \\  & X_2 =  -y \end{aligned} \qquad
  \begin{aligned}  & X^3 =   z \\  & X_3 =  -z \end{aligned}
$$

Its "length", or better pseudo-norm with Minkowski metric, is invariant and reads

$$d s^2 = d \mathbf{X} \cdot d \mathbf{X} = \left( dX_{\alpha} \mathbf{E}^{\alpha} \right) \cdot \left( dX^{\beta} \mathbf{E}_{\beta} \right) = c^2 \, d t^2 - (dx^1)^2 - (dx^2)^2 - (dx^3)^2 = c^2 \, dt^2 - |d \vec{r}|^2 $$

```{note} $ds$ is invariant
**todo** prove it. And/or add a section about the role of invariance.
```

For a co-moving observer, $d \vec{r}' = \vec{0}$, and $t'$ is commonly indicated with $\tau$, and its differential is invariant itself, being the product of a constant ($c$ is a universal constant in special relativity) and an invariant quantity.

$$d s^2 = c^2 dt'^2 - |d \vec{r}'|^2 = c^2 d \tau^2 \ .$$

Given the invariant nature of $d s$,

$$d s^2 = c^2 \, d \tau^2 = c^2 \, dt^2 - |d \vec{r}|^2 = c^2 \, dt^2 \left[ 1 - \frac{1}{c^2}\frac{|d\vec{r}|^2}{dt^2} \right] = c^2 \, dt^2 \left[ 1 - \frac{|\vec{v}|^2}{c^2} \right]$$

and thus

$$d s = c \, d \tau = \gamma^{-1}(v/c) \, c \, dt \ ,$$

with $\gamma(w) = \frac{1}{\sqrt{1 - w^2}}$. 

**4-Velocity** Given the parametric representation of an event in space-time as a function of its proper time, $\mathbf{X}(\tau)$ or coordinate $s$, $\mathbf{X}(s)$ the derivative w.r.t. this parameter is defined as the 4-velocity of the event in space time. Using Cartesian coordinates inducing constant and uniform basis $\mathbf{E}_{\alpha}$, as a function of the observer time $t$, $c t$, $x^i(t)$, and the transformation of coordinates $t(\tau)$, with differential $d t = \frac{1}{\gamma} \, d \tau$

$$\mathbf{U}(\tau) := \mathbf{X}'(\tau) = \dfrac{d}{d \tau} \left( X^{\alpha}(\tau) \mathbf{E}_{\alpha} \right) = \dfrac{d t}{d \tau} (c t \mathbf{E}_0 + x^i(t) \mathbf{E}_i) = \gamma(v/c) \left( c \mathbf{E}_0 + \dot{x}^i(t) \mathbf{E}_i \right) = \gamma(v/c) \left( c \mathbf{E}_0 + \vec{v} \right)$$

or

$$\mathbf{U}(s) := \mathbf{X}'(s) = \dfrac{d t}{ ds } \dfrac{d}{dt} \mathbf{X}(t) = \dots = \gamma(v/c) \left( \mathbf{E}_0 + \frac{\vec{v}}{c} \right) \ .$$

```{note}
Using $s$ as the parameter, $\mathbf{U}$ is non-dimensional, and has pseudo-norm = 1,

$$\mathbf{U}(s) \cdot \mathbf{U}(s) = \gamma^2 \underbrace{\left( 1 - \frac{|\vec{v}|^2}{c^2} \right)}_{=\gamma^{-2}} = 1 \ .$$

Using $\tau$ as the parameter, $\mathbf{U}$ has physical dimension of a velocity and pseudo-norm = $c$.
```

**4-acceleration** $\mathbf{X}''(\tau)$ or $\mathbf{X}''(s)$, **todo**

## Dynamics

**4-momentum**

$$\mathbf{P} = m \mathbf{U}$$

Using Cartesian coordinates and $\tau$ as independent variable,

$$\mathbf{P} = m \mathbf{U} = m \frac{d \mathbf{X}}{d \tau} = m \gamma (c, \vec{v}) \ .$$

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

Thus, recognizing energy ($E = \gamma m c^2$) and 3-momentum ($\vec{p} = m_3 \vec{v}$, with $m_3 := \gamma m$), the 4-momentum can be written as

$$\mathbf{P} = m \mathbf{U} = \gamma m \left( 1, \frac{\vec{v}}{c} \right) =: \frac{1}{c} \left( \frac{E}{c}, \vec{p} \right)$$

Its pseudo-norm reads

$$m^2 = \mathbf{P} \cdot \mathbf{P} = \frac{1}{c^4} \left( E^2 - c^2 |\vec{p}|^2 \right) $$

and thus the relation between $E$, $\vec{p}$, $m$ and $c$,

$$E^2 = m^2 c^4 + c^2 |\vec{p}|^2 \ ,$$

from which, for $\vec{v} = \vec{0} \rightarrow \vec{p} = \vec{0}$,

$$E^2 = m^2 c^4 \ ,$$

and keeping only the solution with positive energy (**todo** *reference to Dirac's equation and anti-matter?*)

$$E = m c^2 \ .$$

### Lagrangian approach

**Free particle.**

$$\mathbf{0} = \frac{d \mathbf{P}}{d s} = \frac{d }{d s} \left( m \mathbf{X}'(s) \right)$$

Weak form

$$\begin{aligned}
  0
  & = \mathbf{W}(s) \cdot \frac{d }{d s} \left( m \mathbf{X}'(s) \right) = \\
  & = \frac{d }{d s} \left[ m \mathbf{W}(s) \cdot \mathbf{X}'(s) \right] - m \mathbf{W}'(s) \cdot \mathbf{X}'(s)  = \\
\end{aligned}$$

Using generalized coordinates $q^k(s)$, the event can be written in parametric form as $\mathbf{X}(q^k(s), s)$, while the velocity reads

$$\mathbf{U}(s) = \mathbf{X}'(s) = \frac{d}{ds} \mathbf{X}(q^k(s), s) = {q^k}'(s) \underbrace{\frac{\partial \mathbf{X}}{\partial q^k}(q^k(s), s)}_{=\frac{\partial \mathbf{X}'}{\partial {q^k}'}} + \frac{\partial \mathbf{X}}{\partial s}(q^k(s), s) = \mathbf{U}({q^k}'(s), q^k(s), s)$$

Choosing $\mathbf{W} = \frac{\partial \mathbf{X}}{\partial q^k} = \frac{\partial \mathbf{X}'}{\partial {q^k}'}$ in the weak form,

$$\begin{aligned}
0  
& = \frac{d }{d s} \left[ m \mathbf{W} \cdot \mathbf{X}' \right] - m \mathbf{W}' \cdot \mathbf{X}' = \\
& = \frac{d }{d s} \left[ m \frac{\partial \mathbf{X}'}{\partial {q^k}'} \cdot \mathbf{X}' \right] - m \dfrac{d}{ds} \frac{\partial \mathbf{X}}{\partial {q^k}} \cdot \mathbf{X}' = \\
& = \frac{1}{2} \left[ \frac{d}{d s} \left( \frac{\partial}{\partial {q^k}'}\left( m \mathbf{X}' \cdot \mathbf{X}' \right)  \right) - \frac{\partial}{\partial q^k}\left( m \mathbf{X}' \cdot \mathbf{X}' \right)  \right] =
\end{aligned}$$

Defining

$$ f\left({q^k}'(s), q^k(s), s \right) = - m \mathbf{X}'\left({q^k}'(s), q^k(s), s\right) \cdot \mathbf{X}'\left({q^k}'(s), q^k(s), s\right) = - m \ ,$$

multiplying by a "regular" generic function $w(s)$, neglecting factor $\frac{1}{2}$ and integrating by parts

$$\begin{aligned}
 0
 & = - \int_{s=s_a}^{s_b} w(s) \left[ \frac{d}{ds} \frac{\partial f}{\partial {q^k}'} - \frac{\partial f}{\partial q^k} \right] \, ds = \\
 & = - \left.\left[ w(s) \frac{\partial f}{\partial {q^k}'} \right]\right|_{s=s_a}^{s_b} + \int_{s=s_a}^{s_b} \left[ w'(s) \frac{\partial f}{\partial {q^k}'} + \frac{\partial f}{\partial q^k} \right] \, ds = \\
 & = - \left.\left[ w(s) \frac{\partial f}{\partial {q^k}'} \right]\right|_{s=s_a}^{s_b} + \delta \int_{s=s_a}^{s_b} f\left( {q^k}'(s), q^k(s), s \right) \, ds \ .
\end{aligned}$$

Thus, provided that $w(s_1) = w(s_2) = 0$, equation of motion of free particle implies stationariety of functional 

$$\int_{s=s_a}^{s_b} f\left( {q^k}'(s), q^k(s), s \right) \, ds \ ,$$

i.e.

$$\delta \int_{s=s_a}^{s_b} f\left( {q^k}'(s), q^k(s), s \right) \, ds = 0$$

Using $t$ as independent parameter, $ds = \gamma^{-1} \, c \, dt$, the functional can be recast as

$$\int_{t=t_a}^{t_b}  -m \, c  \, \sqrt{1 - \frac{|\vec{v}|^2}{c^2}} \, dt \ ,$$

to find the (3-dimensional) Lagrangian (multiply by $c$ to get the right physical dimension; check if it's required and wheter it's possible to make $c$ appear before),

$$\mathscr{L} = - \sqrt{1 - \frac{|\vec{v}|^2}{c^2}} \, m \, c^2 \ ,$$

and retrieve 3-momentum as (being $\vec{v} = \dot{\vec{r}})$

$$\begin{aligned}
  \vec{p} 
  & := \frac{\partial \mathscr{L}}{\partial \dot{\vec{r}}} = \\
  &  = - m c^2 \frac{1}{2} \left(1-\frac{|\vec{v}|^2}{c^2} \right)^{-\frac{1}{2}} \left( - 2 \frac{\vec{v}}{c^2}\right) = \\
  &  = m \left(1-\frac{|\vec{v}|^2}{c^2} \right)^{-\frac{1}{2}} \vec{v} = \\
  &  = \gamma \, m \, \vec{v} \ ,
\end{aligned}$$

and energy as

$$\begin{aligned}
  E
  & := \vec{p} \cdot \vec{v} - \mathscr{L} = \\
  & = \gamma \, m \, |\vec{v}|^2 + \gamma^{-1} \, m \, c^2 = \\
  & = \gamma \, m \, c^2 \left( \frac{|\vec{v}|^2}{c^2} + \gamma^{-2} \right) = \\
  & = \gamma \, m \, c^2 \left( \frac{|\vec{v}|^2}{c^2} + 1 - \frac{|\vec{v}|^2}{c^2} \right) = \\
  & = \gamma \, m \, c^2 \ .
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


### Point particle in electromagnetic field

### Electromagnetic field

### Lorentz force



