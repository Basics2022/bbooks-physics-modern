(quantum-mechanics:analytical-mechanics)=
# Analtycal Mechanics - Notes for Quantum Mechanics

* [Lagrange and Hamiltonian mechanics]()
* [Canonical transformations]()
* [Hamilton-Jacobi formulation of mechanics]()
* [Angle-Action variables]()

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
  & = \dot{\mathbf{q}} \cdot d \mathbf{p} + \mathbf{p} \cdot d \dot{\mathbf{q}} - \partial_{\dot{\mathbf{q}}} \mathcal{L} \cdot d \dot{\mathbf{q}} - \partial_{\mathbf{q}} \mathcal{L} \cdot d \mathbf{q} - \partial_t \mathcal{L} dt \\
  & = \dot{\mathbf{q}} \cdot d \mathbf{p} - \partial_{\mathbf{q}} \mathcal{L} \cdot d \mathbf{q} - \partial_t \mathcal{L} dt \ ,
\end{aligned}$$ (eq:analytical:hamiltonian-differential)

so that Hamilton equations immediately follows

$$\left\{
\begin{aligned}
  \dot{\mathbf{q}} & = \partial_{\mathbf{p}} \mathcal{H} \\
  \dot{\mathbf{p}} & =-\partial_{\mathbf{q}} \mathcal{H} \\
\end{aligned}
\right.$$

with the relation $\partial_t \mathcal{H} = - \partial_t \mathcal{L}$. Using Hamilton's equations, it's immediately proved that $d_t \mathcal{H} = \partial_t \mathcal{H}$. The Hamiltonian function is thus conserved - an integral of motion - if the Lagrangian function doesn't explicitly depend on $t$.

```

```{dropdown} Canonical transformation
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
$$

These pair of Hamilton equations can be derived from the same variational principle of Lagrangian mechanics for two different choices of the generalized variables,

$$\begin{aligned}
  0 & = \delta \int_{t_0}^{t_1} \mathcal{L}(\mathbf{q}, \dot{\mathbf{q}}, t) \, dt \\
  0 & = \delta \int_{t_0}^{t_1} \mathscr{L}(\mathbf{Q}, \dot{\mathbf{Q}}, t) \, dt
\end{aligned}$$

In order to get the same equations of motion, the two Lagrangian functions may differ by a time derivative $\frac{d F_1}{dt}(\mathbf{q}(t), \mathbf{Q}(t), t)$, whose integral reads $F_1(\dots,)$ evaluated in the extremes of integration, and whose variation is thus zero. Thus

$$\mathcal{L}(\mathbf{q}, \dot{\mathbf{q}}, t) = \mathscr{L}(\mathbf{Q}, \dot{\mathbf{Q}}, t) + \frac{d F_1}{dt}(\mathbf{q}(t), \mathbf{Q}(t), t)$$

or as a function of the Hamiltonian functions,

$$\mathbf{p} \cdot \dot{\mathbf{q}} -\mathcal{H}(\mathbf{q}, \mathbf{p}, t) = \mathbf{P} \cdot \dot{\mathbf{Q}} - \mathscr{H}(\mathbf{Q}, \mathbf{P}, t) + \frac{d F_1}{dt}(\mathbf{q}(t), \mathbf{Q}(t), t) \ ,$$

and thus

$$\begin{aligned}
  \dfrac{d F_1}{dt}(\mathbf{q}(t), \mathbf{Q}(t), t)
  & = \mathbf{p} \cdot \dot{\mathbf{q}} - \mathbf{P} \cdot \dot{\mathbf{Q}} - \mathcal{H}(\mathbf{q}, \mathbf{p}, t) + \mathscr{H}(\mathbf{Q}(t), \mathbf{P}(t),t) = \\
  & = \partial_\mathbf{q} F_1 \cdot \dot{\mathbf{q}} + \partial_\mathbf{Q} F_1 \cdot \dot{\mathbf{Q}} + \partial_t F_1
\end{aligned}$$





```




