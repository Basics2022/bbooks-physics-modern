(statistical-mechanics:liouville-boltzmann)=
# Liouville and Boltzmann equations

(statistical-mechanics:liouville)=
## Liouville equation

```{prf:theorem} Liouville's theorem

Let $f(\mathbf{r}_i, \mathbf{v}_i, t)$ the **multi-particle** probability density function. Liouville's equations reads

$$
0 = \frac{\partial f}{\partial t} + \mathbf{v}_i \cdot \nabla_{\mathbf{r},i} f + \frac{\mathbf{F}_i}{m} \cdot \nabla_{\mathbf{v},i} f \ .
$$

```

Let $f(\mathbf{r}_i, \mathbf{v}_i, t)$ be the $N$-particle distribution of a system as a function of the $2 d N$ coordinates and components of the velocity. Probability is normalized to 1

$$1 = \int_{\overline{\Omega}} f(\mathbf{r}_i, \mathbf{v}_i, t) d \mathbf{r}_i d \mathbf{v}_i \ .$$

The governing equations of each particle read

$$\begin{cases}
  \dot{\mathbf{r}}_i = \mathbf{v}_i \\
  \dot{\mathbf{v}}_i = \frac{\mathbf{F}_i}{m} \ .
\end{cases}$$

A governing equation for the probability $P_{\Omega}$ of the system to be in a state belonging to an arbitrary "material" volume $\Omega_t$ in the state space reads

$$\begin{aligned}
  0 = \frac{d}{dt} P_{\Omega} 
  & = \frac{d}{dt} \int_{\Omega_t} f = \\
  & = \int_{\Omega_t} \frac{\partial f}{\partial t} + \oint_{\partial \Omega_t} \left( \hat{\mathbf{n}}_{\mathbf{r},i} \cdot \mathbf{v}_i + \hat{\mathbf{n}}_{\mathbf{v},i} \cdot \mathbf{a}_i \right) f = \\
  & = \int_{\Omega_t} \left\{ \frac{\partial f}{\partial t} + \nabla_{\mathbf{r},i} \cdot \left( \mathbf{v}_i f \right) + \nabla_{\mathbf{v},i} \cdot \left( \mathbf{a}_i f \right) \right\} \ ,
\end{aligned}$$

having used [Reynolds' transport theorem](https://basics2022.github.io/bbooks-math-miscellanea/ch/tensor-algebra-calculus/time-derivative-of-integrals.html#volume-density) in the state space, applied the multi-dimensional version of the divergence theorem. As this balance holds for any arbitrary volume $\Omega_t$, the differential form follows

$$
0 = \frac{\partial f}{\partial t} + \nabla_{\mathbf{r},i} \cdot \left( \mathbf{v}_i f \right) + \nabla_{\mathbf{v},i} \cdot \left( \mathbf{a}_i f \right) \ .
$$

Now, using [Hamilton equations](https://basics2022.github.io/bbooks-physics-mechanics/ch/hamilton.html) in absence of non-conservative forces, in terms of generalized coordinates and generalized momenta

$$\begin{cases}
  \dot{\mathbf{q}}^i =  \frac{\partial \mathscr{H}}{\partial \mathbf{p}_i} \\
  \dot{\mathbf{p}}_i = -\frac{\partial \mathscr{H}}{\partial \mathbf{q}^i} \ ,
\end{cases}$$

or in terms of positions and velocities

$$\begin{cases}
  \mathbf{v}_i = \dot{\mathbf{r}}_i =  \frac{1}{m} \nabla_{\mathbf{v}_i} \mathscr{H} \\
  \mathbf{a}_i = \dot{\mathbf{v}}_i = -\frac{1}{m} \nabla_{\mathbf{r}_i} \mathscr{H} \ ,
\end{cases}$$

it's possible to find the "convective form" of the Liouville's theorem

$$\begin{aligned}
  0
  & = \frac{\partial f}{\partial t} + \nabla_{\mathbf{r},i} \cdot \left( \mathbf{v}_i f \right) + \nabla_{\mathbf{v},i} \cdot \left( \mathbf{a}_i f \right) = \\
  & = \frac{\partial f}{\partial t} + f \underbrace{\left( \nabla_{\mathbf{r},i} \cdot \mathbf{v}_i + \nabla_{\mathbf{v},i} \cdot \mathbf{a}_i \right)}_{=0} + \mathbf{v}_i \cdot \nabla_{\mathbf{r},i} f + \mathbf{a}_i \cdot \nabla_{\mathbf{v},i} f \ ,
\end{aligned}$$

i.e.

$$
0 & = \frac{\partial f}{\partial t} + \mathbf{v}_i \cdot \nabla_{\mathbf{r},i} f + \mathbf{a}_i \cdot \nabla_{\mathbf{v},i} f \\
0 & = \frac{\partial f}{\partial t} + \mathbf{v}_i \cdot \nabla_{\mathbf{r},i} f + \frac{\mathbf{F}_i}{m} \cdot \nabla_{\mathbf{v},i} f \ .
$$


(statistical-mechanics:boltzmann)=
## Boltzmann equation

Integrating all but one particle,...

