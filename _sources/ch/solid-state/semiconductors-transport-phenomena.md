(semiconductors:transport-phenomena)=
# Carrier Transport Phenomena

In this section:
- [Currents in semiconductors](semiconductors:transport-phenomena:currents):hole and electron number current, and electric current density
- [Einstein relation](semiconductors:transport-phenomena:einstein-relation)
- [Balance equations](semiconductors:transport-phenomena:equations): number and charge density dynamical equations


(semiconductors:transport-phenomena:currents)=
## Currents in semiconductors

Two main processes:
1. **diffusion** due to non-uniform density
2. **drift** due to an electric field $\mathbf{e}(\mathbf{r})$

The overall current has the contribution of the motion of both electrons ($n$, for negative charges) and holes ($p$, for positive "charges"),

$$\mathbf{j}(\mathbf{r},t) = \mathbf{j}_n(\mathbf{r},t) + \mathbf{j}_p(\mathbf{r},t) \ ,$$

and both these contributions have their diffusion and drift part,

$$\begin{aligned}
  \mathbf{j}_n & = \mathbf{j}_{n,diff} + \mathbf{j}_{n,drift} \\
  \mathbf{j}_p & = \mathbf{j}_{p,diff} + \mathbf{j}_{p,drift} \\
\end{aligned}$$

For the contribution of the electrons, the diffusion current follows a Fick's law for the number density $n$ (multiplied by the constant charge $-q$ of the elementary charge), while the drift coefficient is written as the product of the negative charge density and their drift velocity,

$$\begin{aligned}
  \mathbf{j}_n 
  & = \mathbf{j}_{n,diff} + \mathbf{j}_{n,drift} = \\
  & = - D_n (-q) \nabla n + \underbrace{(-q) n}_{\rho_n} \mathbf{v}_n = \\
  & = D_n q \nabla n + q \mu_n n \mathbf{e} \ ,
\end{aligned}$$  (eq:semi:charge-current-n)

being the average drift velocity, $\mathbf{v}_n = - \mu_n \mathbf{e}$, a function on the local electric field through the electron mobility $\mu_n$. Here the minus sign follows the definition of the electron mobility with positive value, and from the opposite direction of the local electric field $\mathbf{e}$ and the drift velocity of negative charges.

For the contribution of the holes,

$$\begin{aligned}
  \mathbf{j}_p 
  & = - D_p q \nabla p + q \mu_p p \mathbf{e} \ .
\end{aligned}$$  (eq:semi:charge-current-p)

|      | $\mu_n \, [\dots]$ | $\mu_p \, [\dots]$ |
| :--- | --- | --- |
| Silicon                   |  1350 |  480 |
| Gallium Arsenide          |  8500 |  400 |
| Germanium                 |  3900 | 1900 |

**Remark.** While charges in free-space have acceleration proportional to the electric field, in solids they have drift velocity proportional to the electric field, due to collisions with the lattice. This mechanism can be described in terms of conductivity $\sigma$ (or its inverse, resistivity $\rho_R$) of the medium, similarly to Ohm's law

$$\mathbf{j} = \sigma \mathbf{e} \quad , \quad \mathbf{e} = \rho_R \mathbf{j} \ .$$

Using the expression of the drift current, as the sum of the $n$ and $p$ contributions in {eq}`eq:semi:charge-current-n` and {eq}`eq:semi:charge-current-p` respectively,

$$\mathbf{j}_{drift} = q ( \mu_n n + \mu_p p ) \mathbf{e} \ ,$$

it immediatley follows the formula for the resistivity (and the conductivity)

$$\rho_R = \frac{1}{\sigma} = \frac{1}{q (\mu_n n + \mu_p p)} \ .$$ (eq:semi:resistivity)

**todo** *See discussion about this relation in 5.1.4. Velocity Saturation*

(semiconductors:transport-phenomena:einstein-relation)=
## Einstein relation

...

$$\frac{D_n}{\mu_n} = \frac{D_p}{\mu_p} = \frac{k T}{q} \ .$$ (eq:semi:einstein-relation)

(semiconductors:transport-phenomena:equations)=
## Balance equations

The density of free electrons and holes are governed by the following PDEs

$$\begin{aligned}
  & \partial_t n - \nabla \cdot \left( \frac{\mathbf{j}_n}{q} \right) = ( G_n - R_n ) \\
  & \partial_t p + \nabla \cdot \left( \frac{\mathbf{j}_p}{q} \right) = ( G_p - R_p ) \\
\end{aligned}$$ (eq:semi:num-balance)

where the expression of current densities $\mathbf{j}_n$, $\mathbf{j}_p$ are given in {eq}`eq:semi:charge-current-n`, {eq}`eq:semi:charge-current-p` respectively, and the terms $G_{n,p}$, $R_{n,p}$ represent source and sink terms representing **generation** or **recombination** of free charges and holes.

As for a new free electron there's a new hole, then $G_n = G_p$. As recombination occurs between the same number of free electrons and holes, $R_n = R_g$.

Multiplying the first and the second equation in {eq}`eq:semi:num-balance` by $-q$ and $q$ respectively, the balance equation for the *free* charge density $\rho_f = - q n + q p$,

$$\partial_t \rho_f + \nabla \cdot \mathbf{j} = 0 \ .$$







