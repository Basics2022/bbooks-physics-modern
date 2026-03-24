(statistical-mechanics:liouville-boltzmann)=
# Liouville theorem and Boltzmann equation

(statistical-mechanics:liouville)=
## Liouville theorem

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
0 & = \frac{\partial f}{\partial t} + \mathbf{v}_i \cdot \nabla_{\mathbf{r},i} f + \frac{\mathbf{F}_i}{m} \cdot \nabla_{\mathbf{v},i} f \\
0 & = \frac{\partial f}{\partial t} + \mathbf{v}_i \cdot \nabla_{\mathbf{r},i} f + \frac{\mathbf{F}_i^{ext}}{m} \cdot \nabla_{\mathbf{v},i} f + \sum_{j \ne i} \frac{\mathbf{F}_{ij}}{m} \cdot \nabla_{\mathbf{v},i} f  \ .
$$


(statistical-mechanics:boltzmann)=
## Boltzmann equation

**Indistinguishable particles.** *State counting...*

**1-particle probability distribution function.** Integrating all but one particle (marginalizing over all the variables expect for $\mathbf{r}_1$, $\mathbf{v}_1$),

$$f_1(\mathbf{r}_1, \mathbf{v}_1, t) = \int_{\mathbf{r}_{k=2:N}} \int_{\mathbf{v}_{k=2:N}} f(\mathbf{r}_i,\mathbf{v}_i, t) d \mathbf{r}_k d \mathbf{v}_k \ ,$$

**$s$-particle probability distribution function.**

$$f_s(\mathbf{r}_{j=1:s}, \mathbf{v}_{j=1:s}, t) = \int_{\mathbf{r}_{k=s+1:N}} \int_{\mathbf{v}_{k=s+1:N}} f(\mathbf{r}_i,\mathbf{v}_i, t) d \mathbf{r}_k d \mathbf{v}_k \ ,$$

**Time derivative.**

$$\begin{aligned}
  \partial_t f_s
  & = \partial_t \int_{\mathbf{r}_{k=s+1:N}} \int_{\mathbf{v}_{k=s+1:N}} f(\mathbf{r}_i,\mathbf{v}_i, t) d \mathbf{r}_k d \mathbf{v}_k = \\
  & = - \int_{\mathbf{r}_{k=s+1:N}} \int_{\mathbf{v}_{k=s+1:N}} \left\{ \mathbf{v}_i \cdot \nabla_{\mathbf{r}_i} f + \frac{\mathbf{F}_i^{ext}}{m} \cdot \nabla_{\mathbf{v}_i} f + \sum_{j \ne i} \frac{\mathbf{F}_{ij}}{m} \cdot \nabla_{\mathbf{v}_i} f \right\} d \mathbf{r}_k d \mathbf{v}_k = \\
\end{aligned}$$

Using Hamilton's equation to get a divergence, and assuming zero probability at infinity (impossible to be at infinite distance, impossible to have infinite velocity. Sounds likely),

```{dropdown} Details

$$\begin{aligned}
  \int_{\mathbf{r}_k} \left\{ \mathbf{v}_i \cdot \nabla_{\mathbf{r}_i} f + \frac{\mathbf{F}_i}{m} \cdot \nabla_{\mathbf{v}_i} f \right\}
  & = \int_{\mathbf{r}_k} \left\{ \mathbf{v}_i \cdot \nabla_{\mathbf{r}_i} f + \frac{\mathbf{F}_i}{m} \cdot \nabla_{\mathbf{v}_i} f + f \left( \nabla_{\mathbf{r}_i} \cdot \mathbf{v}_i + \nabla_{\mathbf{v}_i} \cdot \frac{\mathbf{F}_i}{m} \right) \right\} = \\
  & = \int_{\mathbf{r}_k} \left\{ \nabla_{\mathbf{r}_i} \cdot \left(  f \mathbf{v}_i \right) + \nabla_{\mathbf{v}_i} \cdot \left( f \frac{\mathbf{F}_i}{m} \right) \right\} = \\
  & = \sum_{i \ne k} \int_{\mathbf{r}_k} \left\{ \nabla_{\mathbf{r}_i} \cdot \left(  f \mathbf{v}_i \right) + \nabla_{\mathbf{v}_i} \cdot \left( f \frac{\mathbf{F}_i}{m} \right) \right\} = \\
  & = \sum_{i \ne k} \int_{\mathbf{r}_k} \left\{ \mathbf{v}_i \cdot \nabla_{\mathbf{r}_i} f + \frac{\mathbf{F}_i}{m} \cdot \nabla_{\mathbf{v}_i} f \right\} = \\
  & = \sum_{i \ne k} \int_{\mathbf{r}_k} \left\{ \mathbf{v}_i \cdot \nabla_{\mathbf{r}_i} f + \left( \frac{\mathbf{F}^{ext}_i}{m} + \sum_{j \in K} \frac{\mathbf{F}_{ij}}{m} + \sum_{j \notin K} \frac{\mathbf{F}_{ij}}{m} \right) \cdot \nabla_{\mathbf{v}_i} f \right\} = \\
  & = \sum_{i \ne k} \left\{ \mathbf{v}_i \cdot \nabla_{\mathbf{r}_i} \int_{\mathbf{r}_k} f + \frac{\mathbf{F}^{ext}_i}{m} \cdot \nabla_{\mathbf{v}_i} \int_{\mathbf{r}_k} f + \sum_{j \notin K} \frac{\mathbf{F}_{ij}}{m} \cdot \nabla_{\mathbf{v}_i} \int_{\mathbf{r}_k} f  \right\} + \sum_{i \ne k} \sum_{j \in K} \int_{\mathbf{r}_k} \frac{\mathbf{F}_{ij}}{m} \cdot \nabla_{\mathbf{v}_i} f  = \\
  & = \sum_{i \ne k} \left\{ \mathbf{v}_i \cdot \nabla_{\mathbf{r}_i} f_s + \frac{\mathbf{F}^{ext}_i}{m} \cdot \nabla_{\mathbf{v}_i} f_s + \sum_{j \notin K} \frac{\mathbf{F}_{ij}}{m} \cdot \nabla_{\mathbf{v}_i} f_s \right\} + \sum_{i \ne k} \sum_{j \in K} \int_{\mathbf{r}_k} \frac{\mathbf{F}_{ij}}{m} \cdot \nabla_{\mathbf{v}_i} f  = \\
\end{aligned}$$

```

$$
  0 = \partial_t f_s + \sum_{i \notin K} \left\{ \mathbf{v}_i \cdot \nabla_{\mathbf{r}_i} f_s + \frac{\mathbf{F}^{ext}_i}{m} \cdot \nabla_{\mathbf{v}_i} f_s + \sum_{j \notin K} \frac{\mathbf{F}_{ij}}{m} \cdot \nabla_{\mathbf{v}_i} f_s \right\} + \sum_{i \notin K} \sum_{j \in K} \int_{\mathbf{r}_k} \frac{\mathbf{F}_{ij}}{m} \cdot \nabla_{\mathbf{v}_i} f \ .
$$

with $K = s+1:N$.

**1-particle equation.** With $K = 2:N$,

$$
  0 = \partial_t f_1 + \mathbf{v}_1 \cdot \nabla_{\mathbf{r}_1} f_1 + \frac{\mathbf{F}^{ext}_1}{m} \cdot \nabla_{\mathbf{v}_1} f_1 + \sum_{j = 2:N} \int_{\mathbf{r}_k, k \in K} \frac{\mathbf{F}_{1j}}{m} \cdot \nabla_{\mathbf{v}_1} f \, d \mathbf{r}_k d \mathbf{v}_k \ .
$$

```{dropdown} Details
:open:

...

```

**Collision integral.** Assumptions

- only 2-particle collision. Good assumption for "dilute systems". 
- a collision occurs when 2 particles are in the same position (i.e. the dimension of the particles is negligible), $\mathbf{r}_2 = \mathbf{r}_1$

$$\propto \int_{} \Gamma_{\mathbf{p}_1',\mathbf{p}_2' \rightarrow \mathbf{p}_1, \mathbf{p}_2} f(\mathbf{r}_1, \mathbf{r}_2, \mathbf{p}_1', \mathbf{p}'_2) - \Gamma_{\mathbf{p}_1 ,\mathbf{p}_2  \rightarrow \mathbf{p}_1', \mathbf{p}_2'} f(\mathbf{r}_1, \mathbf{r}_2, \mathbf{p}_1, \mathbf{p}_2)$$

with
- $\Gamma_{\mathbf{p}_1', \mathbf{p}_2' \rightarrow \mathbf{p}_1, \mathbf{p}_2}$ representing the probability of starting from $\mathbf{p}_i'$ before the collision and ending with momenta $\mathbf{p}_i$
  - this probability is determined by the analysis of 2-particle collision dynamics
  - this probability is "scaled" by the probability of being in the state before the collision $f(\mathbf{r}_1, \mathbf{r}_2 = \mathbf{r}_1, \mathbf{p}_1', \mathbf{p}_2')$


**Molecular chaos (Stosszahlansatz).** Before and after the collision

$$f_2(\mathbf{v}_1, \mathbf{v}_2, t) \sim f_1(\mathbf{v}_1) \, f(\mathbf{v}_2,t)$$

## H-theorem

Starting from Boltzmann equation for the 1-particle probability density function, with the molecular chaos assumption,

$$D_t f_1 = \int d \mathbf{v}_2 \int d\Omega \sigma(\Omega) |\mathbf{v}_1 - \mathbf{v}_2| \left( f'_1 f'_2 - f_1 f_2 \right)$$

Functional $H(t)$ is defined as

$$H(t) = \int f(\mathbf{v},t) \ln f(\mathbf{v},t) d \mathbf{v}$$

Taking time derivative (integration domain is unbounded. Use divergence theorem and boundary conditions to prove that flux contributions are zero)

$$d_t H(t) = \int \partial_t \left( f \ln f \right) d \mathbf{v} = \int \partial_t f \left( 1 + \ln f \right) d \mathbf{v} \ .$$

```{dropdown} Details
:open:

**todo** *include convective terms of Boltzmann equation*

**todo** *prove each step*

$$\begin{aligned}
  d_t H(t) 
  & = \int \partial_t f \left( 1 + \ln f \right) d \mathbf{v} = \\
  & = \int \int_{\mathbf{v}_1} |\mathbf{v}_1 - \mathbf{v}_2| (f'_1 f'_2 - f_1 f_2) \left( 1 + \ln f_1 \right) \sigma_{\Omega} d \mathbf{v}_1 d \mathbf{v}_2 d\Omega = \\
  & = \frac{1}{2} \int \int_{\mathbf{v}_1} |\mathbf{v}_1 - \mathbf{v}_2| (f'_1 f'_2 - f_1 f_2) \left( \ln f_1 + \ln f_2 \right) \sigma_{\Omega} d \mathbf{v}_1 d \mathbf{v}_2 d\Omega = \\
  & = \frac{1}{4} \int \int_{\mathbf{v}_1} |\mathbf{v}_1 - \mathbf{v}_2| (f'_1 f'_2 - f_1 f_2) \left( \ln f_1 + \ln f_2 - \ln f'_1 - \ln f'_2 \right) \sigma_{\Omega} d \mathbf{v}_1 d \mathbf{v}_2 d\Omega = \\
  & = \frac{1}{4} \int \int_{\mathbf{v}_1} |\mathbf{v}_1 - \mathbf{v}_2| (f'_1 f'_2 - f_1 f_2) \ln \frac{ f_1 f_2 }{f'_1 f'_2} \sigma_{\Omega} d \mathbf{v}_1 d \mathbf{v}_2 d\Omega = \\
  & \le 0 \ ,
\end{aligned}$$

as 

$$(a-b) \ln \frac{b}{a} \le 0 \ ,$$

since, if $a > b$ the first factor is positive and the second negative, and viceversa, and $a = b$ implies equality.

```
