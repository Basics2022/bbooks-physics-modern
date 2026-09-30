(quantum-mechanics:analytical-mechanics)=
# Analtycal Mechanics - Notes for Quantum Mechanics

```{dropdown} Contents
:open:

* [Lagrange and Hamiltonian mechanics](quantum-mechanics:analytical-mechanics:lagrange-hamilton)
* [Canonical transformations](quantum-mechanics:analytical-mechanics:canonical-transformations) Canonical transformations are pure kinematics (kinematics+inertia, as they involve generalized momentum), independent from the physics of the system of interest, i.e. independent from the specific form of the Lagrangian function or of the Hamiltonian function.
* [Hamilton-Jacobi formulation of mechanics](quantum-mechanics:analytical-mechanics:hamilton-jacobi)
* [Angle-Action variables](quantum-mechanics:analytical-mechanics:angle-action)

```

````{dropdown} Topics and tools
:open:

* Calculus of variations
* Legendre transformation, in the definition of functions with different independent variables.

   ```{dropdown} Examples
   :open:

   * From Lagrangian function to Hamiltonian function $\mathcal{H}(\mathbf{q}, \mathbf{p}, t) := \mathbf{p} \cdot \dot{\mathbf{q}} - \mathcal{L}(\mathbf{q}, \dot{\mathbf{q}},t)$
   * From one generating function to another, e.g. $F_2(\mathbf{q}, \mathbf{P}, t) := \mathbf{P} \cdot \mathbf{Q} + F_1(\mathbf{q}, \mathbf{Q}, t)$
   * ...

   ```

* Properties of canonical transformations can be derived with a proper application of rules of derivation of **composite functions**, **paying attention to the set of independent variables** of these functions.


````


(quantum-mechanics:analytical-mechanics:lagrange-hamilton)=
## Lagrange and Hamiltonian Mechanics

```{dropdown} Lagrangian mechanics
:open:

Equations of motion follow the principle of stationary action functional

$$0 = \delta S[\mathbf{q}(t)] = \int_{t_0}^{t_1} \mathcal{L}( \mathbf{q}(t), \dot{\mathbf{q}}(t),t ) \, dt \ ,$$ (eq:analytical:stationary-action)

with prescribed extreme values, so that $\delta \mathbf{q}(t_0) = \delta \mathbf{q}(t_1) = \mathbf{0}$. Here $\mathcal{L}$ is the Lagrangian function, with $\mathbf{q}(t)$ the vector of generalized coordinates, and $t$ the time. Equations of motion are the Lagrange equations

$$\dfrac{d}{dt}\left( \dfrac{\partial \mathcal{L}}{\partial \dot{\mathbf{q}}} \right) - \dfrac{\partial \mathcal{L}}{\partial \mathbf{q}} = \mathbf{0} \ .$$ (eq:analytical:lagrange-eqns)

The generalized momentum is defined as $\mathbf{p} := \frac{\partial \mathcal{L}}{\partial \dot{\mathbf{q}}}$. If the Lagrangian function doesn't explicitly depend on the generalized coordinate $q^k(t)$, the generalized momentum $p_k(t) = \frac{\partial \mathcal{L}}{\partial q^k}$ is constant.

```

```{dropdown}  Hamiltonian mechanics. 
:open:

Hamiltonian function is defined as $\mathcal{H}(\mathbf{q}, \mathbf{p}, t) := \mathbf{p} \cdot \dot{\mathbf{q}} - \mathcal{L}(\mathbf{q}, \dot{\mathbf{q}}, t)$, with $\dot{\mathbf{q}}(\mathbf{q}, \mathbf{p}, t)$. It's differential reads

$$\begin{aligned}
  d \mathcal{H}
  & = \dot{\mathbf{q}} \cdot d \mathbf{p} + \mathbf{p} \cdot d \dot{\mathbf{q}} - \partial_{\dot{\mathbf{q}}} \mathcal{L} \cdot d \dot{\mathbf{q}} - \partial_{\mathbf{q}} \mathcal{L} \cdot d \mathbf{q} - \partial_t \mathcal{L} dt = \\
  & = \dot{\mathbf{q}} \cdot d \mathbf{p} - \partial_{\mathbf{q}} \mathcal{L} \cdot d \mathbf{q} - \partial_t \mathcal{L} dt \ ,
\end{aligned}$$ (eq:analytical:hamiltonian-differential)

by the definition of the generalized momentum, $\mathbf{p} = \partial_{\dot{\mathbf{q}}} \mathcal{L}$. Hamilton equations immediately follows

$$\left\{
\begin{aligned}
  \dot{\mathbf{q}}(t) & = \partial_{\mathbf{p}} \mathcal{H}(\mathbf{q}(t), \mathbf{p}(t), t) \\
  \dot{\mathbf{p}}(t) & =-\partial_{\mathbf{q}} \mathcal{H}(\mathbf{q}(t), \mathbf{p}(t), t) \\
\end{aligned}
\right.$$

with the relation 

$$\left.\partial_t \mathcal{H}\right|_{\mathbf{q}, \mathbf{p}}(\mathbf{q}(t), \mathbf{p}(t),t) = - \left.\partial_t \mathcal{L}\right|_{\mathbf{q}, \dot{\mathbf{q}}}(\mathbf{q}(t), \dot{\mathbf{q}}(t),t) \ . $$

Using Hamilton's equations, it's immediately proved that $d_t \mathcal{H} = \partial_t \mathcal{H}$. The Hamiltonian function is thus conserved - an integral of motion - if the Lagrangian function doesn't explicitly depend on $t$.

```

(quantum-mechanics:analytical-mechanics:canonical-transformations)=
## Canonical transformations

```{dropdown} Definition
:open:

A canonical transformation is defined as a change of coordinates from $(\mathbf{q}, \mathbf{p})$ to $(\mathbf{Q}, \mathbf{P})$ so that the equations of motion have the same expression

$$
\left\{
\begin{aligned}
  \dot{\mathbf{q}} & = \partial_{\mathbf{p}} \mathcal{H} \\
  \dot{\mathbf{p}} & =-\partial_{\mathbf{q}} \mathcal{H} \\
\end{aligned}
\right.
\qquad , \qquad
\left\{
\begin{aligned}
  \dot{\mathbf{Q}} & = \partial_{\mathbf{P}} \mathscr{H} \\
  \dot{\mathbf{P}} & =-\partial_{\mathbf{Q}} \mathscr{H} \\
\end{aligned}
\right.
$$ (eq:analytics:canonical:hamilton-eqns)



```

```{dropdown} Simplectic structure
:open:

Let's define 

$$
\boldsymbol\eta = \begin{pmatrix} \mathbf{q} \\ \mathbf{p} \end{pmatrix} 
\qquad , \qquad
\boldsymbol\zeta = \begin{pmatrix} \mathbf{Q} \\ \mathbf{P} \end{pmatrix} 
$$

whose relation is assumed to be invertible for each time $t$, 

$$\boldsymbol\zeta( \boldsymbol\eta, t) \qquad , \qquad \boldsymbol\eta ( \boldsymbol\zeta, t) \ . $$ (eq:analytics:canonical:coord-transf)

**Hamilton equations.** Hamilton equations {eq}`eq:analytics:canonical:hamilton-eqns` can be recast as

$$
\dot{\boldsymbol{ \eta}} = \mathbf{J} \nabla_{\boldsymbol{ \eta}} \mathcal{H} \qquad , \qquad
\dot{\boldsymbol{\zeta}} = \mathbf{J} \nabla_{\boldsymbol{\zeta}} \mathscr{H} \ ,
$$ (eq:analytics:canonical:hamilton-eqns:simplectic)

with the matrix $\mathbf{J} = \begin{pmatrix} \mathbf{0} & \mathbf{I} \\ -\mathbf{I} & \mathbf{0} \end{pmatrix}$.

**Recasting Hamilton equations in new coordinates, using derivatives of composite functions.** As the the vector of the new coordinates $\boldsymbol\zeta(t)$ can be written as a function of the old coordinates $\boldsymbol\eta(t)$ through the function {eq}`eq:analytics:canonical:coord-transf`

$$\begin{aligned}
 \dfrac{d}{dt} \boldsymbol{\zeta} \left(\boldsymbol\eta(t), t\right)
 & = \dot{\boldsymbol\eta} \cdot \nabla_{\boldsymbol\eta} \boldsymbol\zeta|_t + \partial_t \boldsymbol\zeta|_{\boldsymbol\eta} = \\
 & = \mathbf{M}^T(\boldsymbol\eta(t), t) \dot{\boldsymbol\eta} + \partial_t \boldsymbol\zeta|_{\boldsymbol\eta} = \\
 & = \mathbf{M}^T \, \mathbf{J} \, \nabla_{\boldsymbol\eta} \mathcal{H} + \partial_t \boldsymbol\zeta|_{\boldsymbol\eta} \ ,
\end{aligned}$$

and changing from $(\boldsymbol\zeta, t)$ to $(\boldsymbol\eta, t)$ variables

$$\begin{aligned}
 \dot{\boldsymbol{\zeta}}
 & = \mathbf{M}^T \mathbf{J} \mathbf{M} \, \nabla_{\boldsymbol\zeta} \left.\mathcal{H}\right|_t + \partial_t \boldsymbol\zeta|_{\boldsymbol\eta} \ ,
\end{aligned}$$ (eq:analytics:canonical:coord-transf-zeta)

with $\left\{ \mathbf{M} \right\}_{ij} = \frac{\partial \zeta_j}{\partial \eta_i}(\boldsymbol\eta, t)$, and the rule of transformation of the gradient of a scalar function,

$$f = f( \boldsymbol\eta, t) = f( \boldsymbol\eta(\boldsymbol\zeta, t), t) = \mathscr{f}( \boldsymbol\zeta, t) = \mathscr{f}( \boldsymbol\zeta( \boldsymbol\eta, t), t) \ ,$$

$$\begin{aligned}
  \nabla_{\boldsymbol\eta} f(\boldsymbol\eta(\boldsymbol\zeta(t), t), t) = \left.\nabla_{\boldsymbol\eta} \boldsymbol\zeta\right|_t \cdot \left.\nabla_{\boldsymbol\zeta} \mathscr{f} \right|_t = \mathbf{M} \nabla_{\boldsymbol\zeta} f \ .
\end{aligned}$$

The equation {eq}`eq:analytics:canonical:coord-transf-zeta` must be compared with the Hamilton equations $\dot{\boldsymbol{\zeta}} = \mathbf{J} \nabla_{\boldsymbol\zeta} \mathscr{H}$ from {eq}`eq:analytics:canonical:hamilton-eqns:simplectic`.


```

```{dropdown} Comparison between different forms of Hamilton equations - canonical transformations are pure kinematics, independent from the physics of the system of interest
:open:

From the comparison

$$\left\{
\begin{aligned}
 \dot{\boldsymbol{\zeta}}
 & = \mathbf{M}^T \mathbf{J} \mathbf{M} \, \nabla_{\boldsymbol\zeta} \left.\mathcal{H}\right|_t + \partial_t \boldsymbol\zeta|_{\boldsymbol\eta} \\
 \dot{\boldsymbol{\zeta}} & = \mathbf{J} \nabla_{\boldsymbol\zeta} \mathscr{H}
\end{aligned}
\right.$$

it follows

$$
 \mathbf{M}^T \mathbf{J} \mathbf{M} \, \nabla_{\boldsymbol\zeta} \left.\mathcal{H}\right|_t + \partial_t \boldsymbol\zeta|_{\boldsymbol\eta}
 = \mathbf{J} \nabla_{\boldsymbol\zeta} \mathscr{H}
$$

**System 0.** Let the system zero be a physical system whose Hamiltonian $\mathcal{H}_0(\mathbf{q}, \mathbf{p}, t) := 0$. **Remark** This is the functional definition of the Hamiltonian, not 1-dimensional constraint between variables. It follows that

$$
 \partial_t \boldsymbol\zeta|_{\boldsymbol\eta} = \mathbf{J} \nabla_{\boldsymbol\zeta} \mathscr{H}_0 \ .
$$

**Generic system.** Exploiting the latter relation, for a generic system

$$
 \mathbf{M}^T \mathbf{J} \mathbf{M} \, \nabla_{\boldsymbol\zeta} \left.\mathcal{H}\right|_t
 = \mathbf{J} \nabla_{\boldsymbol\zeta} \left( \mathscr{H} - \mathscr{H}_0 \right) \ .
$$

As this relation must hold for any system, two relations follow:

* the simplectic condition

   $$\mathbf{M}^T \mathbf{J} \mathbf{M} = \mathbf{J} \ .$$

* a relation between the Hamiltonian functions

   $$\mathcal{H} - \mathscr{H} + \mathscr{H}_0 = f(t)$$

A comparison with the partial derivatives {eq}`eq:analytics:gen-fun-2:derivatives` of of **type-2** generating function $F_2(\mathbf{q}, \mathbf{P}, t)$, it follows that[^simpl-gen-derivatives] 

$$\left.\partial_t F_2\right|_{\mathbf{q}, \mathbf{P}} = \mathscr{H} - \mathcal{H} =\mathscr{H}_0 - f(t) \ .$$

[^simpl-gen-derivatives]: The link between simplectic structure and generating functions can be derived with a proper use of derivatives of composit functions.

```

## Generating functions


```{dropdown} Generating functions
:open:

The pair of Hamilton equations {eq}`eq:analytics:canonical:hamilton-eqns` can be derived from the same variational principle of Lagrangian mechanics for two different choices of the generalized variables,

$$\begin{aligned}
  0 & = \delta \int_{t_0}^{t_1} \mathcal{L}(\mathbf{q}(t), \dot{\mathbf{q}}(t), t) \, dt \\
  0 & = \delta \int_{t_0}^{t_1} \mathscr{L}(\mathbf{Q}(t), \dot{\mathbf{Q}}(t), t) \, dt
\end{aligned}$$

In order to get the same equations of motion, the two Lagrangian functions may differ by a time derivative $\frac{d F_1}{dt}(\mathbf{q}(t), \mathbf{Q}(t), t)$, whose integral reads $F_1(\dots,)$ evaluated in the extremes of integration, and whose variation is thus zero. Thus

$$\mathcal{L}(\mathbf{q}(t), \dot{\mathbf{q}}(t), t) = \mathscr{L}(\mathbf{Q}(t), \dot{\mathbf{Q}}(t), t) + \frac{d F_1}{dt}(\mathbf{q}(t), \mathbf{Q}(t), t)$$

or as a function of the Hamiltonian functions,

$$\mathbf{p} \cdot \dot{\mathbf{q}} -\mathcal{H}(\mathbf{q}, \mathbf{p}, t) = \mathbf{P} \cdot \dot{\mathbf{Q}} - \mathscr{H}(\mathbf{Q}, \mathbf{P}, t) + \frac{d F_1}{dt}(\mathbf{q}(t), \mathbf{Q}(t), t) \ ,$$

and thus

$$\begin{aligned}
  \dfrac{d F_1}{dt}(\mathbf{q}(t), \mathbf{Q}(t), t)
  & = \mathbf{p} \cdot \dot{\mathbf{q}} - \mathbf{P} \cdot \dot{\mathbf{Q}} - \mathcal{H}(\mathbf{q}, \mathbf{p}, t) + \mathscr{H}(\mathbf{Q}(t), \mathbf{P}(t),t) = \\
  & = \partial_\mathbf{q} F_1 \cdot \dot{\mathbf{q}} + \partial_\mathbf{Q} F_1 \cdot \dot{\mathbf{Q}} + \partial_t F_1
\end{aligned}$$

so that - using the arbitariness of the result on the choice of coordinates and the physics of the system - its differential reads

$$d F_1 = \mathbf{p} \cdot d \mathbf{q} - \mathbf{P} \cdot d \mathbf{Q} + ( \mathscr{H} - \mathcal{H} ) dt \ .$$

and its partial derivatives

$$
\left.\partial_{\mathbf{q}} F_1\right|_{\mathbf{q}, t         } = \mathbf{p}
\qquad , \qquad
\left.\partial_{\mathbf{Q}} F_1\right|_{\mathbf{Q}, t         } = -\mathbf{P}
\qquad , \qquad
\left.\partial_{t         } F_1\right|_{\mathbf{q}, \mathbf{Q}} = \mathscr{H} - \mathcal{H} \ .
$$ (eq:analytics:gen-fun-1:derivatives)

This is **Type-1** generating function. **Type-2** generating function is defined as 

$$F_2(\mathbf{q}, \mathbf{P}, t) = \mathbf{P} \cdot \mathbf{Q} + F_1(\mathbf{q}, \mathbf{P}, t) \ ,$$

and its differential gives

$$d F_2 = \mathbf{p} \cdot d \mathbf{q} + \mathbf{Q} \cdot d \mathbf{P} + ( \mathscr{H} - \mathcal{H} ) dt \ , $$

and its partial derivatives

$$
\left.\partial_{\mathbf{q}} F_2\right|_{\mathbf{P}, t} = \mathbf{p}
\qquad , \qquad
\left.\partial_{\mathbf{P}} F_2\right|_{\mathbf{q}, t} = \mathbf{Q}
\qquad , \qquad
\left.\partial_{t         } F_2\right|_{\mathbf{q}, \mathbf{P}} = \left.\partial_t F_1\right|_{\mathbf{q}, \mathbf{Q}} = \mathscr{H} - \mathcal{H} \ .
$$ (eq:analytics:gen-fun-2:derivatives)

**Type-3.**

**Type-4.**


```

(quantum-mechanics:analytical-mechanics:hamilton-jacobi)=
## Hamilton-Jacobi formulation of mechanics

Let a set of canonical variables $(\mathbf{Q}, \mathbf{P})$ exist so that $\mathscr{H}(\mathbf{Q}, \mathbf{P}, t) = 0$.[^canonical-hj] **Remark** This is the definition of the function, not a 1-dimensional constraint. For this set of canonical variables, Hamilton's equations implies that $\mathbf{Q}$, and $\mathbf{P}$ are integrals of motion

[^canonical-hj]: Does this set of variables exist? For short-time? For long-time?

$$\left\{
\begin{aligned}
  \dot{\mathbf{Q}} & = \nabla_{\mathbf{P}} \mathscr{H} && \qquad \rightarrow \qquad \mathbf{Q}(t) = \overline{\mathbf{Q}} \\
  \dot{\mathbf{P}} & =-\nabla_{\mathbf{Q}} \mathscr{H} && \qquad \rightarrow \qquad \mathbf{P}(t) = \overline{\mathbf{P}} \\
\end{aligned}
\right.$$

Using type-2 generating function, and its partial derivatives {eq}`eq:analytics:gen-fun-2:derivatives`, $\mathbf{p} = \partial_{\mathbf{q}} F_2(\mathbf{q}, \mathbf{P}, t)$,

$$\begin{aligned}
  0
  & = \partial_t F_2\left( \mathbf{q}, \mathbf{P}, t \right) - \underbrace{\mathscr{H}(\mathbf{Q}, \mathbf{P}, t)}_{=0} + \mathcal{H}(\mathbf{q}, \mathbf{p}, t) \ ,
\end{aligned}$$

or, calling $F_2(\mathbf{q}(t), \overline{\mathbf{P}}, t) := S(\mathbf{q}(t), t; \overline{\mathbf{P}})$ - as it can be seen as the action functional as a function of the ending time $t$ and generalized coordinates $\mathbf{q}(t)$, see [below](quantum-mechanics:analytical-mechanics:action-functional-type-2-gen-fun) - the common form of the Hamilton-Jacobi equation follows

$$\begin{aligned}
  0 = \partial_t S\left( \mathbf{q}(t), t; \overline{\mathbf{P}} \right) + \mathcal{H}\left(\mathbf{q}(t), \partial_{\mathbf{q}} S(\mathbf{q}(t), t; \overline{\mathbf{P}}) , t \right) \ .
\end{aligned}$$ (eq:analytics:hamilton-jacobi)

**Stationary problems.** For problems whose Hamiltonian is not explicitly function of time, $\mathcal{H}(\mathbf{q}, \mathbf{p})$, the Hamiltonian is constant and equal to the energy of the system, $\mathcal{H}(\mathbf{q}, \mathbf{p}) = E$. Integration in $t$ gives

$$S\left(\mathbf{q}(t), t; \overline{\mathbf{P}} \right) = - E t + W\left(\mathbf{q}(t); \overline{\mathbf{P}} \right) \ .$$

The constant energy $E$ is a function of the integrals of motion $\overline{\mathbf{P}}$ only.

Introducing this expression in the Hamilton-Jacobi equation {eq}`eq:analytics:hamilton-jacobi` gives an equation for $W\left( \mathbf{q}, \overline{\mathbf{P}} \right)$,

$$E = \mathcal{H}\left( \mathbf{q}, \partial_{\mathbf{q}} W\left(\mathbf{q}, \overline{\mathbf{P}} \right) \right) \ .$$

(quantum-mechanics:analytical-mechanics:action-functional-type-2-gen-fun)=
### Action functional and type-2 generating function


(quantum-mechanics:analytical-mechanics:angle-action)=
## Angle-action variables

Let the system of interest be a **conservative system** using the original set of variables $(\mathbf{q}, \mathbf{p})$, so that the Hamiltonian doesn't explicitly depend on time $t$, and it's constant $\mathcal{H}(\mathbf{q}, \mathbf{p}) = E$.
Let a set of canonical variables $(\mathbf{Q}, \mathbf{P}) =: (\mathbf{w}, \mathbf{J})$ exist so that $\mathbf{J}(t) = \overline{\mathbf{J}}$ are integrals of motion, and $\mathscr{H}(\mathbf{w}, \overline{\mathbf{J}}, t) = \mathcal{H}(\mathbf{q}, \mathbf{p}) = E$, *trajectory-wise*.

$$\left\{
\begin{aligned}
  \dot{\mathbf{w}} & = \nabla_{\mathbf{J}} \mathscr{H} \\
  \dot{\mathbf{J}} & =-\nabla_{\mathbf{w}} \mathscr{H} = \mathbf{0} && \qquad \rightarrow \qquad \mathscr{H}(\mathbf{\overline{J}}, t) \\
\end{aligned}
\right.$$

Partial derivative of $F_1(\mathbf{q}, \mathbf{Q}, t)$ w.r.t. time $t$ is therefore zero

$$\partial_t F_1|_{\mathbf{q}, \mathbf{w}} = \mathscr{H} - \mathcal{H} = 0 \qquad \rightarrow \qquad F_1(\mathbf{q}, \mathbf{w}) \ .$$

and alos the hamiltonian $\mathscr{H}$ can't be a function of time, $\mathcal{H}(\mathbf{q}, \mathbf{p}) = \mathscr{H}(\overline{\mathbf{J}}) = E(\overline{\mathbf{J}})$, *trajectory-wise*. Thus the gradient of the Hamiltonian $\mathscr{H}$ w.r.t. $\mathbf{J}$ is constant as well $\nabla_{\mathbf{J}} \mathscr{H} =: \overline{\boldsymbol\omega}$, and the evolution of the generalized coordinate is linear (including periodic orbits, if the coordinates are cycical),

$$\mathbf{w}(t) = \mathbf{w}_0 + \overline{ \boldsymbol{\omega} } \, t \ .$$

**Differentials of the generating functions.** With this choice of conjugated variables, the differential of the type-1 generating function becomes

$$d F_1(\mathbf{q}, \mathbf{w}, t) = \mathbf{p} \cdot d \mathbf{q} - \overline{\mathbf{J}} \cdot d \mathbf{w} \ ,$$

and the integration along a closed trajectory $\gamma$ in the space $(\mathbf{q}, \mathbf{w})$ gives, if the function $F_1$ is regular in the region where integration occurs, so that $\oint d F_1 = 0$.

$$\begin{aligned}
  \oint_{\gamma_k} d F_1
  & = \oint_{\gamma_k} \mathbf{p} \cdot d \mathbf{q} - \oint_{\gamma_k} \overline{\mathbf{J}} \cdot  \overline{\boldsymbol{\omega}} dt = \\
  & = \oint_{\gamma_k} \mathbf{p} \cdot d \mathbf{q} - \overline{\mathbf{J}} \cdot  \overline{\boldsymbol{\omega}} \, T_{k} = \\
  & = \oint_{\gamma_k} \mathbf{p} \cdot d \mathbf{q} - \dfrac{1}{2\pi} \sum_{i} \overline{J}_i \, \frac{T_{k}}{T_i} \ ,
\end{aligned}$$

with $T_{\gamma}$ the period of the trajectory $\gamma$. The differential of the type-2 generating function reads

$$\begin{aligned}
  d F_2 
  & = \mathbf{J} \cdot d \mathbf{w} + \mathbf{w} \cdot d \mathbf{J} + d F_1 = \\
  & = \mathbf{p} \cdot d \mathbf{q} + \mathbf{w} \cdot d \mathbf{J}
\end{aligned}$$

and its integration over a closed trajectory in the $(\mathbf{q}, \mathbf{J})$ space, with $\mathbf{J} = \overline{\mathbf{J}}$, $\mathbf{w} = \mathbf{w}_0 + \overline{\boldsymbol\omega} \, t$, gives

$$\oint d F_2 = \oint d F_1 + \oint \overline{\mathbf{J}} \cdot \overline{\boldsymbol\omega} \, dt = \oint \mathbf{p} \cdot d \mathbf{q} \ . $$

**Remark. todo** Discussion about the regularity of $F_2$ and the domain of integration. Integration of an exact differential over a closed path different from zero implies that something "strange" is happening.

**todo**
* Separable systems
* definition of action variables in separable systems

