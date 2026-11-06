(relativity-general:notes:examples:deflection-of-ray-of-light)=
# Deflection of a ray of light, and Eddington measurements (1919)

Newton's theory of universal gravitation is fundamentally incompatible with special relativity: in Newtonian mechanics, gravitational interactions act instantaneously across space, violating the relativistic principle that no physical signal or interaction can propagate faster than the speed of light $c$.

In this section, the equation of the trajectory of zero-mass object in Schwarzschild metrics is derived here, using perturbation method for weak gravitational fields. The equations of general relativity imply that a ray of light is deflected by a body with mass $M$ by an angle

$$\delta \simeq 4 \frac{GM}{R c^2} \ ,$$

being $R$ the minimum distance of the ray from the center of the massive body. This results is compared is twice the deflection predicted by the laws of classical mechanics using Newton gravitation, $\delta^{\rm Newton} \simeq 2 \frac{GM}{R c^2}$. **Eddington experiment** during the total solar eclipse of the 1919 measured the amount of deflection of light rays passing close to the sun, confirming that general gravitation has better predictions and matches the experimental measurements, providing the first experimental tests of Einstein theory of general relativity as a new and better theory of gravitation.



(relativity-general:notes:examples:deflection-of-ray-of-light:trajectory-schwarzschild)=
## Trajectory of zero-mass objects in Schwarzschild metrics

Light particles travel at the speed of light $c$. Thus the elementary increment of proper interval (or proper time $\tau$) is zero,

$$0 = ds^2 = g_{ij} \frac{d q^i}{d \lambda} \frac{d q^j}{d \lambda} \ .$$

Using Schwarzschild metric {eq}`eq:schwarzschild-metrics`

$$
ds^2 =
- \left(1 - \frac{r_s}{r} \right) c^2 dt^2 + 
  \left(1 - \frac{r_s}{r} \right)^{-1} dr^2 + r^2 d \theta^2 + r^2 \sin^2 \theta \, d\phi^2 \ .
$$ 

A similar procedure as the one followed to compute [orbits of non-zero mass light objects in a Schwarzschild metric](relativity-general:notes:examples:schwarzschild-orbits) is followed. The main and fundamental difference is in the use of $ds$. For non-zero mass objects the relation $ds^2 = c^2 d \tau^2 = g_{\mu \nu} d q^{\mu} d q^{\nu}$ holds, and thus $c^2 = g_{\mu \nu} \dot{q}^{\mu} \dot{q}^{\nu}$, with $\dot{q}^{\mu} = \tfrac{d q^{\mu}}{d \tau}$. For zero mass objects, it's not possible to use the proper time as a parameters (as it's constant and thus $d \tau = 0$); using an arbitrary parameter $\lambda$, it follows that $0 = \frac{d s^2}{d \lambda^2} = g_{\mu \nu} \frac{d q^{\mu}}{d \lambda} \frac{d q^{\nu}}{d \lambda}$.

Let's choose a planar trajectory with prescribed $\theta=\frac{\pi}{2}$ (or with prescribed $\phi = \overline{\phi}$). The equations of the geodesics are

$$\begin{aligned}
  0 & = \ddot{t} + \frac{1}{1 - \frac{r_s}{r}}\frac{r_s}{r} \, \dot{t} \, \dot{r} \\
  0 & = \ddot{r} + A' e^{4 A} c^2 \dot{t}^2 - A'(r) \dot{r}^2 - r \theta e^{2 A} \dot{\phi}^2 \\ 
  0 & = \ddot{\phi} + \frac{2}{r} \, \dot{r} \, \dot{\phi} \\
  0 & = \ddot{\theta} \ .
\end{aligned}$$

From the first and the third equations, the conserved quantities follow

$$\begin{aligned}
  \frac{E}{c} & = \left( 1 - \frac{r_s}{r} \right) \dot{t} = \text{const.} \\
  L & = r^2 \dot{\phi} = \text{const.}
\end{aligned}$$

Replacing these relations in the constraint $ds = 0$,

$$\begin{aligned}
0
 & = - \left(1 - \frac{r_s}{r} \right) c^2 \dot{t}^2 + \left(1 - \frac{r_s}{r} \right)^{-1} \dot{r}^2 + r^2 \, \dot{\phi}^2 = \\
 & = - E^2 \left(1 - \frac{r_s}{r} \right)^{-1} + \left(1 - \frac{r_s}{r} \right)^{-1} \dot{r}^2 + \frac{L^2}{r^2} \ ,
\end{aligned}$$ 

and thus the differential equation for $r(\lambda)$ becomes

$$0 = \dot{r}^2 - E^2 + \left( 1 - \frac{r_s}{r} \right) \frac{L^2}{r^2} \ .$$

Now, changing variable $u = \frac{1}{r}$, and exploiting a relation $r(\phi(\lambda))$

$$\dot{r} = \frac{d \phi}{d \lambda} \frac{d r}{d \phi} = \frac{L}{r^2} \frac{d r}{d \phi} = L u^2 \left( - \frac{1}{u^2} \right) u'(\phi) = - L u'(\phi) \ .$$

the equation becomes

$$0 = L^2 \left( u'(\phi) \right)^2 - E^2 + ( 1 - r_s u ) L^2 u^2 \ .$$

Differentiating both sides by $\phi$ and dividing by $2 L^2 u'(\phi)$, a second order equation for $u(\phi)$ appears

$$u''(\phi) + u(\phi) = \frac{3}{2} r_{s} u^2(\phi) = \frac{3 GM}{c^2} u^2 \ .$$

---

**Solution via perturbation method.** As $\frac{3 GM}{c^2} \to 0$, the equation becomes $u''(\phi) + u(\phi) = 0$, whose solution is $u_0(\phi) = A \cos(\phi) + B\sin(\phi)$, i.e.

$$r_{0}(\phi) = \frac{1}{A \cos(\phi) + B \sin(\phi)} \ .$$

The problem is independent from an offset in $\phi$. Setting $\lim_{\phi \to \dots} r(\phi) = +\infty$, then $B = 0$, and. **todo** *Set this condition, $\overline{\phi} = \tfrac{\pi}{2}$?* *Which condition sets $A = {1}{R}$? Minimum distance*

$$u_0(\phi) = \frac{1}{R} \cos(\phi) \ ,$$

i.e. the equation of a straight line with minimum distance $R$ from the origin of the coordinates, i.e. the trajectory of a body in free-space. Let the solution be $u(\phi) = u_0(\phi) + u_1(\phi)$. An approximate equation for $u_1$ is obtained introducing this decomposition in the original equation,

$$\begin{aligned}
0
& = u''(\phi) + u(\phi) - \frac{3}{2} r_{s} u^2(\phi) = \\
& = u_0''(\phi) + u_1''(\phi) + u_0(\phi) + u_1(\phi) - \frac{3}{2} r_{s} (u_0(\phi) + u_1(\phi) )^2 = \\
& = \underbrace{ u_0''(\phi) + u_0(\phi) }_{ = 0 } + u_1''(\phi) + u_1(\phi) - \frac{3}{2} r_{s} u_0^2(\phi) - 3 r_{s} u_0(\phi) u_1(\phi) - \frac{3}{2} r_{s} u_1^2(\phi) = \\
& = u_1''(\phi) + u_1(\phi) - \frac{3}{2} r_s u_0^2(\phi) u_1(\phi) = \\ 
& \sim u_1''(\phi) + u_1(\phi) - \frac{3}{2} \frac{r_s}{R^2} \cos^2(\phi) \ .
\end{aligned}$$

With $\cos^2(\phi) = \frac{1}{2} + \frac{1}{2} \cos(2 \phi)$, the approximate equation for $u_1(\phi)$ becomes

$$
  u_1''(\phi) + u_1(\phi) = \frac{3}{4} \frac{r_s}{R^2} \left[ 1 + \cos(2 \phi) \right] \ .
$$

The solution is

$$u_1(\phi) = A \cos(\phi) + B \sin(\phi) + \frac{3}{4} \frac{r_s}{R^2} \left[ 1 - \frac{1}{3} \cos(2\phi) \right] \ .$$

```{dropdown} Details

$$\begin{aligned}
  \dfrac{d}{dx} \cos(2 x) & = - 2 \sin (2x) \\
  \dfrac{d^2}{dx^2} \cos(2 x) & = - 4 \cos (2x)
\end{aligned}$$

$$\left( - 4 + 1 \right) D = \frac{3}{4}\frac{r_s}{R^2} \ ,$$

thus $D = - \frac{1}{4} \frac{r_s}{R^2}$.

```

Putting together the zero- and first-order contributions, the approximate solution is

$$u(\phi) = A \cos(\phi) + B \sin(\phi) + \frac{3}{2} \frac{GM}{R^2 c^2 } \left( 1 - \frac{1}{3} \cos(2 \phi) \right) \ .$$

Assuming symmetric trajectory w.r.t. $\theta = 0$, then $B = 0$. Setting the other integration constant by the condition $u(0) = \frac{1}{R}$, then

$$
\frac{1}{R} = A + \frac{GM}{R^2 c^2}
\quad \rightarrow \quad
A = \frac{1}{R} \left( 1 - \frac{GM}{ R c^2} \right)
$$

so that

$$r(\phi) = \frac{R}{\left( 1 - \frac{GM}{ R c^2} \right) \cos(\phi) + \frac{3}{2} \frac{GM}{R c^2 } \left( 1 - \frac{1}{3} \cos(2 \phi) \right)} \ .$$

```{dropdown} Extremes of the trajectory
:open:

Limit angles for $\phi = \frac{\pi}{2} - \frac{\delta}{2}$, or $\phi = - \left( \frac{\pi}{2} - \frac{\delta}{2} \right)$ with "small" $\delta > 0$.

$$\cos\left(\frac{\pi}{2} - \frac{\delta}{2} \right) = \sin \frac{\delta}{2} \sim \frac{\delta}{2} - \frac{\left(\delta/2\right)^3}{3!}$$

$$\begin{aligned}
  1 - \frac{1}{3} \cos\left[ 2 \left(\frac{\pi}{2} - \frac{\delta}{2} \right) \right]
  & = 1 - \frac{1}{3} \cos \left( \pi - \delta \right) = \\
  & = 1 + \frac{1}{3} \cos(\delta) = \\
  & \sim 1 + \frac{1}{3} \left( 1 - \frac{\delta^2}{2!} \right) = \\
  & = \frac{4}{3} - \frac{1}{12}\delta^2
\end{aligned}$$

An approximation of the denominator for "small" $\delta$ thus becomes

$$\text{den}(\delta) = \left( 1 - \gamma \right) \frac{\delta}{2} + \frac{3}{2} \gamma \left( \frac{4}{3} - \frac{1}{12} \delta^2 \right) = \left( 1 - \gamma \right) \frac{\delta}{2} + 2 \gamma - \frac{1}{8} \gamma \delta^2 \ , $$

and setting it equal to zero, neglecting the second-degree contribution

$$\delta = \frac{4 \gamma}{1 - \gamma} \sim 4 \gamma = 4 \frac{GM}{R c^2 } \ .$$ (eq:rays-of-light-deflection:relativity)

```

<!--
**todo** Compare with the results of classical mechanics using Newtonian mechanics for a hyperbolic orbit of a body with mass $m \to 0$ (the orbit is independent from the mass of the object, as $m \tfrac{d^2 \mathbf{r}}{d t^2} = - G M m \frac{\mathbf{r}}{| \mathbf{r} |^3}$.
-->

(relativity-general:notes:examples:deflection-of-ray-of-light:newton)=
## Comparison with the laws of classical mechanics - Newton gravitation

**See**: [Physics - HS: Classical Mechanics: Dynamics: Central Motions](https://basics2022.github.io/bbooks-physics-hs/ch/mechanics/dynamics-central.html)

With the laws of classical mechanics, the equation of the trajectory of central motions with force $\vec{F} = c \frac{\vec{r}}{\left| \vec{r} \right|^3}$,


$$r(\phi) = \frac{\frac{L^2}{m|c|}}{-\text{sign}(c) + \sqrt{1 + 2 \frac{E L^2}{m|c|^2}} \cos(\phi-\phi_0)} \ ,$$

being $m$ the mass of the light body, $L$ the constant angular momentum, and $E$ the constant energy of the light body, and $\phi_0$ a reference angle to describe trajectories with different orientation: without loss of generallity, let's set it equal to zero, $\phi_0 = 0$. For gravitation, $c = G M m$, so that $\text{sign}(c) = 1$.

Open trajectories have $E \ge 0$, with parabolic orbits for $E = 0$, and hyperbolic orbits for $E > 0$. The minimum distance between the bodies occurs when the denominator is maximum, and thus for $\cos( \phi ) = 1$, i.e. $\phi = 0$.

$$R = \frac{\frac{L^2}{G M m^2}}{-1 + \sqrt{1 + 2 \frac{E}{m} \frac{L^2}{G^2 M^2 m^2}} } \ .$$

Hyperbolic orbits havei asymptotes corresponding to limit angles $\phi_\infty$ and $-\phi_{\infty}$, where the denominator becomes zero. The total deflection of the trajectory is the angle $\delta$ (better, $\pi - \delta$) between the asymptotes. The limit angles satisfy the condition

$$\cos \phi_{\infty} = \frac{1}{\sqrt{1 + 2 \frac{E}{m} \frac{L^2}{G^2 M^2 m^2}}} \ .$$

The total delection is $\delta = \pi - 2 \phi_\infty$. For small deviations of the trajectory, the angles at infinity only slightly differs from $\pm \frac{\pi}{2}$. Writing $\phi_{\infty} = \frac{\pi}{2} - \frac{\delta}{2}$, then $\cos(\phi_{\infty}) = \sin\left( \frac{\delta}{2} \right)$. As $\delta \to 0$, then $\cos \phi_\infty \to 0$. Since

$$\cos \phi_\infty = \frac{1}{\sqrt{1 + \varepsilon}} = \sin\left( \frac{\delta}{2} \right) \sim \frac{\delta}{2} \ ,$$

it follows that the parameter $\varepsilon = 2 \frac{E}{m} \left( \frac{L}{GMm} \right)^2$ is "large", and the approximation of $\cos \phi_\infty$ holds

$$\cos \phi_\infty = \frac{1}{\sqrt{1 + \varepsilon}} \sim \frac{1}{\sqrt{\varepsilon}} \ .$$

If this approximation holds, the minimum distance of the trajectory from the massive body approximately is

$$R  \sim \frac{G M}{2} \frac{m}{E} \sqrt{\varepsilon} \quad \rightarrow \quad  \frac{1}{\sqrt{\varepsilon}} \sim \frac{GMm}{2ER} \ .$$

Then, the total delection for a body travelling close to the speed of light - assuming that laws of classical mechanics still hold, and that kinetic energy prevails over potential energy - $E \sim \frac{1}{2} m c^2$,

$$\delta \sim \frac{GMm}{ER} \sim \frac{2GM}{R c^2} \ .$$ (eq:rays-of-light-deflection:classical)



