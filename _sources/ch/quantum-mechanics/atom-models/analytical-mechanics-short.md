(analytical-mechanics-short)=
# Analytical mechanics - short notes


To understand the theoretical justification behind the **Wilson-Sommerfeld Quantization Rule**, we must examine the formal framework of classical analytical mechanics. Old Quantum Theory did not apply quantization conditions to arbitrary coordinates; rather, it relied on the natural canonical coordinates provided by **action-angle variables**.


(analytical-mechanics-short:lagrange-hamilton)=
## Lagrangian and Hamiltonian mechanics

**Lagrangian mechanics.** Consider a classical physical system with $f$ degrees of freedom described by generalized coordinates $\mathbf{q} = (q_1, q_2, \dots, q_f)$ and generalized velocities $\mathbf{\dot{q}} = (\dot{q}^1, \dot{q}^2, \dots, \dot{q}^f)$. The equations of motion can be derived from the principle of stationariety of the action, $S$,

$$0 = \delta S = \delta \int_{t_0}^{t_1} L \left( \dot{\mathbf{q}}(t), \mathbf{q}(t), t \right) \, dt \ ,$$

with prescribed ends $\delta \mathbf{q}(t_0) = \delta \mathbf{q}(t_1) = \mathbf{0}$, and $L(\dot{\mathbf{q}}(t), \mathbf{q}(t), t)$ the Lagrangian function

$$
  L(\mathbf{q}, \mathbf{\dot{q}}, t) = T(\mathbf{q}, \mathbf{\dot{q}}) - V(\mathbf{q}) \ .
$$

The canonical (or conjugate) momentum associated with coordinate $q_i$ is defined as:

$$
p_i = \frac{\partial L}{\partial \dot{q}_i}
$$

**Hamiltonian mechanics.** Via a *Legendre transformation*, we transition from the $(\mathbf{q}, \mathbf{\dot{q}})$ state space to the canonical phase space $(\mathbf{q}, \mathbf{p})$, introducing the **Hamiltonian**, nothing but the mechanical energy of the system as a function of generalized coordinates and momenta,

$$
H(\mathbf{q}, \mathbf{p}, t) = \sum_{i=1}^f p_i \dot{q}_i - L(\mathbf{q}, \mathbf{\dot{q}}, t)
$$

Taking the differential of $H$, the equations of motion follows

$$\left\{ 
\begin{aligned}
  \dot{q}_i & =  \frac{\partial H}{\partial p_i} \\
  \dot{p}_i & = -\frac{\partial H}{\partial q_i}
\end{aligned} \right.$$

while $\partial_t H = - \partial_t L$.

(analytical-mechanics-short:canonical-transformations)=
## Canonical Transformations and Hamilton-Jacobi Theory

```{dropdown} Canonical transformations and invariance
:open:

Transformation $\mathbf{z} = (\mathbf{q}, \mathbf{p}) \leftrightarrow  \mathbf{Z} = (\mathbf{Q}, \mathbf{P})$

$$
\left\{ \begin{aligned}
  \dot{\mathbf{q}} & = \partial_{\mathbf{p}} H \\
  \dot{\mathbf{p}} & =-\partial_{\mathbf{q}} H \\
\end{aligned} \right.
\qquad , \qquad
\left\{ \begin{aligned}
  \dot{\mathbf{Q}} & = \partial_{\mathbf{P}} K \\
  \dot{\mathbf{P}} & =-\partial_{\mathbf{Q}} K \\
\end{aligned} \right.
$$

or 

$$
 \dot{\mathbf{z}} = \mathbf{J} \nabla_{\mathbf{z}} H
 \qquad , \qquad
 \dot{\mathbf{Z}} = \mathbf{J} \nabla_{\mathbf{Z}} K \ ,
$$

with 

$$\mathbf{J} = \begin{bmatrix} \mathbf{0} & \mathbf{I} \\ -\mathbf{I} & \mathbf{0} \end{bmatrix} \ .$$

As $\mathbf{z}(\mathbf{Z},t)$,

$$\begin{aligned}
  \dot{z}_i        & = \dot{Z}_k \, \partial_{Z_K} z_i + \partial_t z_i \\
  \partial_{z_i} f & = \partial_{z_i} Z_k \, \partial_{Z_k} f
\end{aligned}$$

for a regular transformation, with non-singular gradient $\partial_{Z_k} z_i \, \partial_{z_i} Z_j = \delta_{kj}$,

$$\begin{aligned}
  \dot{Z}_j
  & = \partial_{z_i} Z_j \left( \dot{z}_i - \partial_t z_i \right) = \\
  & = \partial_{z_i} Z_j \left( J_{il} \partial_{z_l} H - \partial_t z_i \right) = \\
  & = \partial_{z_i} Z_j \, J_{il} \, \partial_{z_l} Z_{m} \, \partial_{Z_m} H -  \partial_{z_i} Z_j \, \partial_t z_i \ ,
\end{aligned}$$

or with matrix formalism

$$\dot{\mathbf{Z}} = \mathbf{G}^T \mathbf{J} \mathbf{G} \nabla_{\mathbf{Z}} H - \mathbf{G}^T \, \partial_t \mathbf{z} \ .$$

* Stationary change of variables $\mathbf{z}(\mathbf{Z})$, $\partial_t \mathbf{z} = 0$, and thus

   $$\nabla_{\mathbf{Z}} K = \mathbf{G}^T \mathbf{J} \mathbf{G} \nabla_{\mathbf{Z}} H$$

   ...

* Non-stationary transformation

   ...

...

```

```{dropdown} Properties of canonical transformations

* Inverse of $\mathbf{J}$, $\mathbf{J}^{-1} = - \mathbf{J}$.

* Value of $\mathbf{G}^T \mathbf{J} \mathbf{G}$

   *Fix and uncomment*
<!--
   $$\begin{aligned}
     \mathbf{G}^T \mathbf{J} \mathbf{G}
     & = \begin{bmatrix} 
           \nabla_{\mathbf{q}} \mathbf{Q}^T & \nabla_{\mathbf{p}} \mathbf{Q}^T \\ 
           \nabla_{\mathbf{q}} \mathbf{P}^T & \nabla_{\mathbf{p}} \mathbf{P}^T \\ 
         \end{bmatrix} 
         \begin{bmatrix} \mathbf{0} & \mathbf{I} \\ - \mathbf{I} & \mathbf{0} \end{bmatrix}
         \begin{bmatrix} 
           \nabla_{\mathbf{q}} \mathbf{Q} & \nabla_{\mathbf{q}} \mathbf{P} \\ 
           \nabla_{\mathbf{p}} \mathbf{Q} & \nabla_{\mathbf{p}} \mathbf{P} \\ 
         \end{bmatrix} = \\
     & = \begin{bmatrix} 
           \nabla_{\mathbf{q}} \mathbf{Q}^T & \nabla_{\mathbf{p}} \mathbf{Q}^T \\ 
           \nabla_{\mathbf{q}} \mathbf{P}^T & \nabla_{\mathbf{p}} \mathbf{P}^T \\ 
         \end{bmatrix} 
         \begin{bmatrix} 
           \nabla_{\mathbf{p}} \mathbf{Q} &  \nabla_{\mathbf{p}} \mathbf{P} \\ 
          -\nabla_{\mathbf{q}} \mathbf{Q} & -\nabla_{\mathbf{q}} \mathbf{P} \\ 
         \end{bmatrix} = \\
     & = \begin{bmatrix}
            \partial_{q^k} Q^i \partial_{p_k} Q^j - \partial_{p_k} Q^i \partial_{q^k} Q^j & 
            \partial_{q^k} Q^i \partial_{p_k} P_j - \partial_{p_k} Q^i \partial_{q^k} P_j \\
            \partial_{q^k} P_i \partial_{p_k} Q^j - \partial_{p_k} P_i \partial_{q^k} Q^j & 
            \partial_{q^k} P_i \partial_{p_k} P_j - \partial_{p_k} P_i \partial_{q^k} P_j \\
         \end{bmatrix}
   \end{aligned}$$
-->

* Invariance of Poisson brackets

   *todo*

* Determinant of $\mathbf{G}^T \mathbf{J} \mathbf{G} = \mathbf{J}$

   $$| \mathbf{G} |^2 |\mathbf{J}| = |\mathbf{J}| \quad \rightarrow \quad | \mathbf{G} | = \mp 1 \ .$$

   The orientation-preserving transformation is the one with $| \mathbf{G} | = 1$.

* Elementary volume in the phase space

  $$|d \mathbf{q} d \mathbf{p}| = | \mathbf{G}| \, | d \mathbf{Q} \, d \mathbf{P} | = | d \mathbf{Q} \, d \mathbf{P} |$$

```

A transformation from coordinates $(\mathbf{q}, \mathbf{p})$ to new variables $(\mathbf{Q}, \mathbf{P})$ is **canonical** if it preserves the form of Hamilton’s equations under a new Hamiltonian $K(\mathbf{Q}, \mathbf{P}, t)$.

Using two sets of coordinates, the principle of stationary action reads

$$0 = \delta \int_{t_0}^{t_1} L(\dot{\mathbf{q}}, \mathbf{q},t) \, dt = \delta \int_{t_0}^{t_1} \mathcal{L}(\dot{\mathbf{Q}}, \mathbf{Q},t) \, dt \ .$$

The two Lagrangian functions can differ by a time-derivative $\dfrac{d}{dt} F_{1}(\mathbf{q}(t), \mathbf{Q}(t),t)$ at most. Thus, using the relation between the Lagrangian and the Hamiltonian function, it follows

$$\mathbf{p} \cdot \dot{\mathbf{q}} - H(\mathbf{q},\mathbf{p},t) = \mathbf{P} \cdot \dot{\mathbf{Q}} - K(\mathbf{Q}, \mathbf{P}, t) + \frac{d}{dt} F_1(\mathbf{q}, \mathbf{Q},t)$$

Moving $ \frac{d F_1}{dt}$ on one side, and expanding the time derivative,

$$\begin{aligned}
  \dfrac{d F_1}{dt}
  & = \dot{\mathbf{q}} \cdot \partial_{\mathbf{q}} F_1 + \dot{\mathbf{Q}} \cdot \partial_{\mathbf{Q}} F_1 + \partial_t F_1 = \\
  & = \mathbf{p} \cdot \dot{\mathbf{q}} - \mathbf{P} \cdot \dot{\mathbf{Q}} - H(\mathbf{q},\mathbf{p},t) + K(\mathbf{Q}, \mathbf{P}, t)
\end{aligned}$$

Exploiting the arbitrariness of the functions involved, the following relations hold

$$\begin{aligned}
  \mathbf{p} = \partial_{\mathbf{q}} F_1 \qquad , \qquad
  \mathbf{P} =-\partial_{\mathbf{Q}} F_1 \qquad , \qquad
  K - H      = \partial_{t} F_1 \\
\end{aligned}$$

Another *Legendre transformation* introduces a type-2 generating function $F_2(\mathbf{q}, \mathbf{P}, t)$,

$$F_2(\mathbf{q}, \mathbf{P}, t) := F_1(\mathbf{q}, \mathbf{Q}, t) + \mathbf{Q} \cdot \mathbf{P} \ ,$$

that allows to go from the independent pair of variables $(\mathbf{q}, \mathbf{Q})$ to $(\mathbf{q}, \mathbf{P})$, as

$$\begin{aligned}
  d_t F_2 
  & = \partial_t F_1 + \dot{\mathbf{q}} \cdot \partial_{\mathbf{q}} F_1 + \dot{\mathbf{Q}} \cdot \underbrace{\left( \partial_{\mathbf{Q}} F_1 + \mathbf{P} \right)}_{= \mathbf{0}} + \dot{\mathbf{P}} \cdot \mathbf{Q} = \\
  & =\partial_t F_1 + \dot{\mathbf{q}} \cdot \partial_{\mathbf{q}} F_1 + \dot{\mathbf{P}} \cdot \mathbf{Q} \ ,
\end{aligned}$$

so that

$$\begin{aligned}
  \partial_{\mathbf{q}} F_2 = \partial_{\mathbf{q}} F_1 = \mathbf{p} \qquad , \qquad
  \partial_{\mathbf{P}} F_2 = \mathbf{Q} \qquad , \qquad
  \partial_t F_2 = \partial_{t} F_1 = K - H \\
\end{aligned}$$

(analytical-mechanics-short:hamilton-jacobi-equation)=
## The Hamilton-Jacobi Equation

```{dropdown} Hamilton-Jacobi equation and angle-action variables
:open:

$$\begin{aligned}
  0
  & = K = \\
  & = H(\mathbf{q},\mathbf{p},t) + \partial_t F_2(\mathbf{q}, \mathbf{P}, t) = \\
  & = H(\mathbf{q},\partial_{\mathbf{q}} F_2,t) + \partial_t F_2(\mathbf{q}, \mathbf{P}, t) = \\
\end{aligned}$$

If $H$ is not explicitly dependent on $t$, and thus the system is conservative as $d_t H = \partial_t H = 0$, it follows $H(\mathbf{q}, \mathbf{p}) = E$, constant. Hamilton-Jacobi equation thus becomes

$$0 = H\left( \mathbf{q}, \partial_{\mathbf{q}} F_2 \right) + \partial_t F_2 \ .$$

As $H$ doesn't explicitly depends on time, it's possible to look for a solution of the equation $F_2(\mathbf{q}, \mathbf{P}, t) = S(\mathbf{q}, \mathbf{P}) - T(t)$,

$$0 = H \left( \mathbf{q}, \partial_{\mathbf{q}} S \right) + \dot{T} = 0 \ ,$$

and thus

$$H \left( \mathbf{q}, \partial_{\mathbf{q}} S \right) = - \dot{T} = E \ ,$$

and thus

$$\begin{aligned}
  T(t) & = - E t + T_0 \\
  H \left( \mathbf{q}, \partial_{\mathbf{q}} S \right) & = E \ .
\end{aligned}$$


```

The ultimate goal of Hamilton-Jacobi theory is to find a canonical transformation to a set canonical variables $(\mathbf{w}, \mathbf{J})$ with **constant** momentum variables $\mathbf{J}$ and making the new Hamiltonian identically zero ($K = 0$). Hamilton equations read

$$\left\{\begin{aligned}
  \dot{\mathbf{w}} & = \partial_{\mathbf{J}} K \\
  \dot{\mathbf{J}} & =-\partial_{\mathbf{w}} K \\
\end{aligned}\right.$$

If $\mathbf{J}$ is constant, thus $\dot{\mathbf{J}} = \mathbf{0}$ and $\partial_{\mathbf{Q}} K = 0$. Thus $K(\mathbf{J}, t)$. As $K(\mathbf{J}, t) = 0$, and $\mathbf{J}$ constant, thus $0 = d_t K = \partial_t K$. Then it follows that $K(\mathbf{J}) = 0$. As $\mathbf{J}$ are constant, then $\partial_{\mathbf{J}} K$ is constant as well. The first Hamilton equation implies $\mathbf{w}(t) = \partial_{\mathbf{J}} K \cdot t + \mathbf{w}_0$.

```{dropdown} old

Time derivative of Type-1 generating function, $F_1(\mathbf{q},\mathbf{Q},t)$, becomes 

$$\begin{aligned}
  d_t F_1 
  & = \dot{\mathbf{q}} \cdot \mathbf{p} - \underbrace{ \dot{\mathbf{w}} }_{=\partial_{\mathbf{J}} K} \cdot \mathbf{J} + \underbrace{ K }_{=0} - H(\mathbf{q}, \mathbf{p}, t) = \\
\end{aligned}$$

Time derivative of Type-2 generating function, $F_2(\mathbf{q},\mathbf{P},t)$, becomes 

$$\begin{aligned}
  d_t F_2 
  & = \partial_t F_1 + \dot{\mathbf{q}} \cdot \partial_{\mathbf{q}} F_1 + \underbrace{\dot{\mathbf{J}} \cdot \mathbf{w}}_{=\mathbf{0}} = \\
  & = - H(\mathbf{q}, \mathbf{p}, t) + \dot{\mathbf{q}} \cdot \mathbf{p} \\
\end{aligned}$$

Choosing $F_2(\mathbf{q}, \boldsymbol{\alpha}, t) = S(\mathbf{q}, \boldsymbol{\alpha}) - E t$, where $S(\mathbf{q}, \boldsymbol{\alpha})$ is **Hamilton's characteristic function**, Hamilton's principal equation reduces to the time-independent **Hamilton-Jacobi Equation**:

```

If $H(\mathbf{q}, \mathbf{p}$, then the system is conservative. Exploiting separation of variables, $F_{2}(\mathbf{q}, \mathbf{J}, t) = S(\mathbf{q}, \mathbf{J}) - E t$

$$
H\left(\mathbf{q}, \partial_{\mathbf{q}} S(\mathbf{q}, \mathbf{J}) \right) = E \ .
$$

As $\dot{\mathbf{J}} = 0$, the time derivative of $S$ reads

$$\dot{S} = \dot{\mathbf{q}} \cdot \partial_{\mathbf{q}} S + \underbrace{\dot{\mathbf{J}} \cdot \partial_{\mathbf{J}} S}_{= \mathbf{0}} = \dot{\mathbf{q}} \cdot \mathbf{p}(\mathbf{q}, \mathbf{J}) \ .$$

If the system is **separable**, $S(\mathbf{q}, \boldsymbol{\alpha})$ splits into independent single-variable functions:

$$
S(\mathbf{q}, \mathbf{J}) = \sum_{i=1}^f S_i(q^i, \mathbf{J})
$$

so that its time derivative reads

$$\dot{S} = \dot{q}^i \, S'_i(q_i, \mathbf{J}) = \dot{q}^i \, p_i(q^i, \mathbf{J}) \ .$$


## Action-Angle Variables

For bound, periodic systems whose Hamilton-Jacobi equations are separable, the most suitable coordinate system consists of **Action-Angle Variables** $(\mathbf{w}, \mathbf{J})$.

### Definition of Action Variables

The **Action Variable** $J_i$ associated with the $i$-th degree of freedom is defined as the line integral of momentum over one complete cycle of motion in phase space:

$$
J_i \equiv \oint p_i \, dq_i = \oint \frac{\partial S_i(q_i, \boldsymbol{\alpha})}{\partial q_i} \, dq_i
$$

Here, the loop $\oint$ denotes:
* A complete libration (back-and-forth oscillation between turning points), or
* A $2\pi$ rotation for angular coordinates.

### Angle Variables and Frequencies

Because the action variables $J_i$ are constants of motion, we can express the total Hamiltonian purely as a function of the action variables: $H = H(J_1, J_2, \dots, J_f)$.

The canonical conjugates to $J_i$ are the **Angle Variables** $w_i$, defined via the generating function $S(\mathbf{q}, \mathbf{J})$:

$$
w_i = \frac{\partial S(\mathbf{q}, \mathbf{J})}{\partial J_i}
$$

Hamilton's equations of motion in action-angle variables simplify to:

$$
\dot{J}_i = -\frac{\partial H}{\partial w_i} = 0 \implies J_i = \text{constant}
$$

$$
\dot{w}_i = \frac{\partial H(J_1, \dots, J_f)}{\partial J_i} \equiv \nu_i (\mathbf{J}) \implies w_i(t) = \nu_i t + w_i(0)
$$

Where $\nu_i$ is the exact **fundamental frequency** of the classical motion along coordinate $q_i$.

---

## 4. The Wilson-Sommerfeld Quantization Postulate

The central insight of William Wilson (1915) and Arnold Sommerfeld (1916) was that quantization should **not** be applied arbitrarily to any set of phase space coordinates. Instead, quantization conditions must be invariant under canonical transformations.

The integral invariants of Poincaré show that the total phase space volume element $\sum_i \oint p_i dq_i$ is a canonical invariant. Therefore, quantization must be imposed directly onto the adiabatic invariants of the classical motion: **the Action Variables $J_i$**.

### The Quantization Rule

The Wilson-Sommerfeld quantization rule dictates that each action variable $J_i$ is restricted to integer multiples of Planck's constant $h$:

$$
J_i = \oint p_i \, dq_i = n_i h, \quad n_i \in \mathbb{N}
$$

### Summary of Connection to Quantum Mechanics

1. **Separability:** The classical system must be separable in coordinates $(q_1, \dots, q_f)$.
2. **Phase Space Loops:** The integral $\oint p_i dq_i$ measures the area enclosed by the periodic trajectory in the $(q_i, p_i)$ 2D projection of phase space.
3. **Discretization:** Quantizing $J_i = n_i h$ slices phase space into discrete cells of volume $h^f$.
4. **Energy Spectrum:** Inverting $H(J_1, \dots, J_f)$ with $J_i \to n_i h$ yields the quantized energy levels $E(n_1, n_2, \dots, n_f)$.

