(relativity-special)=
# Special Relativity - Notes

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

### Electromagnetic potential

$$\begin{cases}
 \vec{b} = \nabla \times \vec{a} \\
 \vec{e} = -\partial_t \vec{a} - \nabla \varphi \\
\end{cases}$$

$$\mathbf{A} = \mathbf{E}_{\alpha} A^{\alpha} = \frac{\varphi}{c} \mathbf{E}_0 + \vec{a}$$

$$\symbf{\nabla} \mathbf{A} =
\left( \mathbf{E}^{\alpha} \frac{\partial}{\partial X^{\alpha}} \right) \left( A^{\beta} \mathbf{E}_{\beta} \right)
= \frac{\partial A^{\beta}}{\partial X^{\alpha}} \mathbf{E}^{\alpha} \otimes \mathbf{E}_{\beta} 
= g_{\alpha \gamma} \frac{\partial A^{\beta}}{\partial X^{\alpha}} \mathbf{E}_{\gamma} \otimes \mathbf{E}_{\beta}  \ .$$

whose components may be collected in a 2-dimensional array (first index for rows, second index for columns),

$$(\nabla \mathbf{A})_{\alpha}^{\beta} = \frac{\partial A^{\beta}}{\partial X^{\alpha}} =
\begin{bmatrix}
 c^{-2} \partial_t \varphi & c^{-1}\partial_x \varphi & c^{-1}\partial_y \varphi & c^{-1}\partial_z \varphi \\
 c^{-1} \partial_t a_x     &       \partial_x a_x     &       \partial_y a_x     &       \partial_z a_x     \\
 c^{-1} \partial_t a_y     &       \partial_x a_y     &       \partial_y a_y     &       \partial_z a_y     \\
 c^{-1} \partial_t a_z     &       \partial_x a_z     &       \partial_y a_z     &       \partial_z a_z     \\
\end{bmatrix}$$

or covariant-covariant coomponents,

$$(\nabla \mathbf{A})_{\alpha \beta} = \frac{\partial A_{\beta}}{\partial X^{\alpha}} = g_{\beta \gamma} \frac{\partial A^{\gamma}}{\partial X^{\alpha}} = 
\begin{bmatrix}
  c^{-2}\partial_t \varphi & c^{-1}\partial_x \varphi & c^{-1}\partial_y \varphi & c^{-1}\partial_z \varphi \\
 -c^{-1}\partial_t a_x     &      -\partial_x a_x     &      -\partial_y a_x     &      -\partial_z a_x     \\
 -c^{-1}\partial_t a_y     &      -\partial_x a_y     &      -\partial_y a_y     &      -\partial_z a_y     \\
 -c^{-1}\partial_t a_z     &      -\partial_x a_z     &      -\partial_y a_z     &      -\partial_z a_z     \\
\end{bmatrix}$$

or contravariant-contravariant coomponents,

$$(\nabla \mathbf{A})^{\alpha \beta} = \frac{\partial A^{\beta}}{\partial X_{\alpha}} = g_{\beta \gamma} \frac{\partial A^{\alpha}}{\partial X^{\gamma}} = 
\begin{bmatrix}
  c^{-2}\partial_t \varphi &-c^{-1}\partial_x \varphi &-c^{-1}\partial_y \varphi &-c^{-1}\partial_z \varphi \\
  c^{-1}\partial_t a_x     &      -\partial_x a_x     &      -\partial_y a_x     &      -\partial_z a_x     \\
  c^{-1}\partial_t a_y     &      -\partial_x a_y     &      -\partial_y a_y     &      -\partial_z a_y     \\
  c^{-1}\partial_t a_z     &      -\partial_x a_z     &      -\partial_y a_z     &      -\partial_z a_z     \\
\end{bmatrix}$$

The electromagnetic field tensor is defined as the anti-symmetric part of the gradient of the 4-electromagnetic potential,

$$\mathbf{F} = \left[ \symbf{\nabla} \mathbf{A} - \left( \symbf{\nabla} \mathbf{A} \right)^T \right]$$

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
  \begin{bmatrix} 0 & - c \underline{d}^T \\ c \underline{d} & \underline{h}_{\times} \ .
  \end{bmatrix}
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

   $$0 =  \partial_{\mu} F_{\mu \xi} + \partial_{\mu} \underbrace{F_{\xi \mu}}_{-F_{\mu xi}} + \partial_{\xi} \underbrace{F_{\mu \mu}}_{=0} = 0 \ , $$

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

$$\begin{aligned}
  \frac{\partial u      }{\partial t} & = \\
  \frac{\partial \vec{s}}{\partial t} & = \\
\end{aligned}$$

...

$$\symbf{\nabla} \cdot \mathbf{T} = - \mathbf{F} \cdot \mathbf{J}$$











