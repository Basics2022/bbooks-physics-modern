(relativity-general:notes:examples:schwarzschild-orbits)=
# Planetary orbits in Schwarzschild spacetime

Schwarzschild metrics {eq}`eq:schwarzschild-metrics` provides the metrics induced by a massive object in the vacuum spacetime around. The motion of a light object approximately doesn't affect the massive object generating the steady Schwarzschild metrics. The light object moves following the geodesics.
Let the motion occurs in the equatorial plane, i.e. $\theta = \frac{\pi}{2}$, and $d \theta = 0$. Thus 

$$
- c^2 d \tau^2 = ds^2 =
- \left(1 - \frac{r_s}{r} \right) c^2 dt^2 + 
  \left(1 - \frac{r_s}{r} \right)^{-1} dr^2 + r^2 \, d\phi^2 \ .
$$

<!--
```{dropdown} Rearranging $\ ds^2$

$$\begin{aligned}
  ds^2
  & = - \left( 1 - \frac{1}{\rho} \right) c^2 dt^2 + \frac{1}{1-\frac{1}{\rho}} dr^2 + r^2 d \phi^2 = \\
  & = - \left( 1 - \frac{1}{\rho} \right) c^2 dt^2 + \frac{\frac{1}{\rho}}{1 - \frac{1}{\rho}} dr^2 + dr^2 + r^2 d \phi^2 = \\
  & = - \frac{\rho - 1}{\rho} c^2 dt^2 + \frac{1}{\rho - 1}  dr^2 + dr^2 + r^2 d \phi^2 \ .
\end{aligned}$$

```
-->

**Geodesics.** With $A(r) = \frac{1}{2} \ln \left( 1 - \frac{r_s}{r} \right)$, $A'(r) = \frac{1}{2} \frac{1}{1 - \frac{r_s}{r}} \frac{r_s}{r^2}$

$$0 = \ddot{q}^k + \Gamma_{a b}^k \dot{q}^{a} \dot{q}^b$$

$$\begin{aligned}
  t : \qquad 
  0 & = \ddot{t} + \Gamma_{ab}^t \dot{q}^a \dot{q}^b = \\
    & = \ddot{t} + 2 \Gamma_{tr}^t \dot{t} \dot{r} = \\
    & = \ddot{t} + \frac{1}{1 - \frac{r_s}{r}} \frac{r_s}{r^2} \dot{t} \dot{r} \\
  0 & = \left(1 - \frac{r_s}{r} \right)^{-1} \left[ \left( 1-\frac{r_s}{r}\right) \ddot{t} + \frac{r_s}{r^2} \dot{t} \dot{r} \right] = \\
  0 & = \left(1 - \frac{r_s}{r} \right)^{-1} \dfrac{d}{d \tau} \left[ \left( 1-\frac{r_s}{r} \right) \dot{t} \right] \quad \rightarrow \quad \left( 1-\frac{r_s}{r} \right) \dot{t} =: \frac{E}{c} = \text{const.} \\
  r : \qquad 
  0 & = \ddot{r} + \Gamma_{ab}^r \dot{q}^a \dot{q}^b = \\
    & = \ddot{r} + \Gamma_{tt}^r \dot{t}^2 + \Gamma_{rr}^r \dot{r}^2 + \Gamma_{\theta \theta}^{r} \dot{\theta}^2 + \Gamma_{\phi \phi}^{r} \dot{\phi}^2 = && (\dot{\theta} = 0 )\\
    & = \ddot{r} + \Gamma_{tt}^r \dot{t}^2 + \Gamma_{rr}^r \dot{r}^2 + \Gamma_{\phi \phi}^{r} \dot{\phi}^2 = \\
    & = \ddot{r} + A' e^{4 A} c^2 \dot{t}^2 - A'(r) \dot{r}^2 - r \sin^2 \theta e^{2 A} \dot{\phi}^2 = \\
    & = \ddot{r} + A' e^{4 A} c^2 \dot{t}^2 - A'(r) \dot{r}^2 - r \theta e^{2 A} \dot{\phi}^2 = \\
  \phi : \qquad 
  0 & = \ddot{\phi} + \Gamma_{ab}^{\phi} \dot{q}^a \dot{q}^b  \\
    & = \ddot{\phi} + 2 \Gamma_{r \phi}^\phi \dot{r} \dot{\phi} + 2 \Gamma_{\theta \phi}^\phi \dot{\theta} \dot{\phi} =  && ( \dot{\theta} = 0 ) \\
    & = \ddot{\phi} + 2 \Gamma_{r \phi}^\phi \dot{r} \dot{\phi} = \\
    & = \ddot{\phi} + 2 \frac{1}{r} \dot{r} \dot{\phi} \ , \\
  0 & = \frac{1}{r^2} \dfrac{d}{d \tau} \left( r^2 \dot{\phi} \right) \quad \rightarrow \quad r^2(\tau) \dot{\phi}(\tau) =: L = \text{const.} \\
  \theta : \qquad 
  0 & = \ddot{\theta} + \Gamma_{ab}^{\theta} \dot{q}^a \dot{q}^b  \\
    & = \ddot{\theta} + 2 \Gamma_{r \phi}^\theta \dot{\theta} \dot{\phi} + \Gamma_{\phi \phi}^\theta \dot{\phi}^2 = && ( \dot{\theta} = 0 ) \\
    & = \ddot{\theta} - \sin \theta \cos \theta \Gamma_{\phi \phi}^\theta \dot{\phi}^2 = \\
    & = \ddot{\theta} \ .
\end{aligned}$$

Replacing the expression for $\dot{t}$ and $\dot{\phi}$ into the relation $u^\mu u_{\mu} = - c^2$ (from $ds^2/d \tau^2$)

$$\begin{aligned}
  -c^2 
  & = - \left( 1 - \frac{r_s}{r} \right) c^2 \dot{t}^2 + \left( 1 - \frac{r_s}{r} \right)^{-1} \dot{r}^2 + r^2 \dot{\phi}^2 = \\
  & = - \left( \right)^{-1} E^2  + \left(  \right)^{-1} \dot{r}^2 + \frac{L}{r^2} \\
\end{aligned}$$

and thus

$$
  \dot{r}^2 = E^2 - c^2 \left( 1 - \frac{r_s}{r} \right) \left( 1 + \frac{L}{r^2 c^2} \right) \ .
$$

Now, changing variable $u := \frac{1}{r}$ and using the relation $\phi(\tau)$ to write

$$\dot{r} = \frac{d r}{d\tau} = \frac{d \phi}{d \tau} \frac{d}{d \phi} = \frac{L}{r^2} \frac{d r}{d \phi} = L u^2 \left( - \frac{1}{u^2} \right) u'(\phi) = - L u'(\phi) \ ,$$

the equation becomes

$$ L^2 {u'}^2 = E - c^2 ( 1 - r_s u ) \left( 1 + \frac{L^2}{c^2} u^2 \right) \ .$$

Differentiating both sides by $\phi$

$$0 = L^2 2 u' u'' - c^2 r_s u' \left( 1 + \frac{L^2}{c^2} u^2 \right) + c^2 ( 1 - r_s u) 2 \frac{L^2}{c^2} u u' $$

or dividing by $2 L^2 u'$,

$$0 = u'' - \frac{c^2 r_s}{2 L^2} - \frac{3}{2}r_s u^2 + u$$

or, with $r_s = \frac{2 GM}{c^2}$

$$u'' + u = \frac{c^2 r_s}{2 L^2} + \frac{3}{2} r_s u^2 = \frac{GM}{L^2} + \frac{3 GM}{c^2} u^2 \ .$$

**Solution via perturbation method.** As $\frac{3 GM}{c^2} \to 0$, the equation becomes the equation of the Kepler orbits.

Let the solution be $u(\phi) = u_0(\phi) + u_1(\phi)$, with $u_0(\phi)$ the solution of the equations of classical mechanics.

$$u_0(\phi) = \frac{GM}{L^2}(1 + e \cos \phi) \ . $$

As

$$0 = \underbrace{u_0'' + u_0 - \frac{GM}{L}}_{=0} + u_1'' + u_1 - \frac{3GM}{c^2} (u_0 + u_1)^2 \ ,$$

the perturbation $u_1(\phi)$ (of order $\frac{GM}{c^2}$ must satisfy (approximately, truncation) the equation

$$\begin{aligned}
  u_1'' + u_1
  & \approx \frac{3 GM}{c^2} u_0^2(\phi) = \\
  & = \frac{3 (GM)^2}{c^2 L^2} \left( 1 + 2 e \cos \phi + e^2 \cos^2 \phi \right) = && ( \cos 2 x = 2 \cos^2 x - 1 ) = \\
  & = 3 \left( \frac{GM}{L c} \right)^2 \left( 1 + 2 e \cos \phi + \frac{e^2}{2} \left( 1 + \cos ( 2 \phi ) \right) \right) = \\
  & = 3 \left( \frac{GM}{L c} \right)^2 \left( 1 + \frac{e}{2} + 2 e \cos \phi + \frac{e^2}{2} \cos ( 2 \phi ) \right) \ ,
\end{aligned}$$

whose solution undergoes resonance

$$u(\phi) = a \cos \phi + b \sin \phi + c + d \phi \cos \phi + e \phi \sin \phi + f \cos (2 \phi) $$

