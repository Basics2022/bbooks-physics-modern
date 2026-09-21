(quantum-mechanics:intro)=
# Quantum Mechanics

- Principles and postulates
  - statistics and measurements outcomes (Heisenberg built its matrix mechanics only on observables...)
  - CCR
- angluar momentum, spin, and atom

(quantum-mechanics:intro:math)=
## Mathematical tools for quantum mechanics

```{prf:definition} Operator
:label: Operator


```

```{prf:definition} Adjoint operator
:label: Adjoint Operator

Given an operator $\hat{A}: U \rightarrow V$, its adjoint operator $\hat{A}^*: V \rightarrow U$ is the operator s.t.

$$(\mathbf{v}, \ \hat{A} \mathbf{u})_{V} = (\mathbf{u}, \hat{A}^* \mathbf{v} )_{U}$$

holds for $\forall \mathbf{u} \in U, \ \mathbf{v} \in V$.

```



(quantum-mechanics:math:operators:self-adjoint)=
```{prf:definition} Hermitian (self-adjoint) operator
:label: Self-Adjoint Operator

The operator $\hat{A}: U \rightarrow U$ is a self-adjoint operator if 

$$\hat{A}^* = \hat{A} \ .$$

```

Self-adjoint operators have real eigenvalues, and orthogonal eigenvectors (at least those associated to different eigenvalues; those associated with the same eigenvalues can be used to build an orthogonal set of vectors with orthogonalization process).


(quantum-mechanics:intro:postulates)=
## Postulates of Quantum Mechanics
- ...
- Canonical Commutation Relation (CCR) *and Canonical Anti-Commutation Relation...*
- ...

(quantum-mechanics:intro:non-relativistic)=
## Non-relativistic Mechanics

(quantum-mechanics:intro:non-relativistic:wave-function)=
### Wave function
The state of a system is described by a wave function $|\Psi\rangle$ 

**todo**
- properties: domain, image,...
- unitary $1 = \langle \Psi | \Psi \rangle = \left| \Psi \right|^2$, for statistical interpretation of $\left| \Psi \right|^2$ as a density probability function

(quantum-mechanics:intro:non-relativistic:observables-operators)=
### Operators and Observables
Physical **observable** quantities are represented by [Hermitian operators](quantum-mechanics:math:operators:self-adjoint). Possible outcomes of measurement are the eigenvalues of the operator

Given $\hat{A}$ and the set of its eigenvectors $\{ |A_i \rangle \}_i$ (**todo** *continuous or discrete spectrum..., need to treat this difference quite in details*), with associated eigenvalues $\{ a_i \}_i$

$$\hat{A} |A_i \rangle = a_i |A_i\rangle$$

$$| \Psi \rangle = | A_i \rangle \langle A_i | \Psi \rangle =  | A_i \rangle \Psi_i^A $$

$$\langle A_j | \Psi \rangle = \langle A_j | A_i \rangle \langle A_i | \Psi \rangle = \Psi_j^A $$

and thus

$$\begin{aligned}
  \Psi_j^A    & = \langle A_j  | \Psi \rangle \\
  \Psi_j^{A*} & = \langle \Psi | A_j \rangle \\
\end{aligned}$$

- identity operator $\sum_i | A_i \rangle \langle A_i | = \mathbb{I}$, since

  $$\sum_i | A_i \rangle \langle A_i | \Psi \rangle = \sum_i | A_i \rangle \langle A_i | \Psi_j^A A_j \rangle =
  \sum_i | A_i \rangle \delta_{ij} \Psi_j^A = \sum_i | A_i \rangle  \Psi_i^A  = | \Psi \rangle$$


- Normalization:

  $$1 =\langle \Psi | \Psi \rangle = \Psi_j^{A*} \underbrace{\langle A_j | A_i \rangle}_{\delta_{ij}} \Psi_i^{A} = \sum_i \left| \Psi_i^A \right|^2$$

  with $|\Psi_i^A|^2$ that can be interpreted as the probability of finding the system in state $|\Psi_i^a\rangle$

- Expected value of the physical quantity in the a state $|\Psi\rangle$, with possible values $a_i$ with probability $|\Psi_i^A|^2$

  $$\begin{aligned}
    \bar{A}_{\Psi} & = \sum_i a_i |\Psi_i^A|^2 = \\
            & = \sum_i a_i \Psi_i^{A*} \Psi_i^A =  \\ 
            & = \sum_i a_i \langle \Psi | A_i \rangle \langle A_i | \Psi \rangle = \\
            & = \langle \Psi | \left( \sum_i a_i | A_i \rangle \langle A_i | \right) | \Psi \rangle = \\
            & = \langle \Psi | \hat{A} | \Psi \rangle = \\
  \end{aligned}$$


  since an operator $\hat{A}$ can be written as a function of its eigenvalues and eigenvectors

   $$\begin{aligned}
   \left( \sum_i a_i | A_i \rangle \langle A_i | \right) \Psi \rangle 
   & = \left( \sum_i a_i | A_i \rangle \langle A_i | \right) c_k | A_k \rangle = \\
   & =  \sum_i a_i | A_i \rangle c_i = \\
   & =  \sum_i \hat{A} | A_i \rangle c_i = \\
   & = \hat{A} \sum_i | A_i \rangle c_i = \hat{A} | \Psi \rangle \ . 
   \end{aligned}$$


<!--
$$\begin{aligned}
  \langle A_j| \Psi \rangle = \langle A_j | A_i \rangle \langle A_i | \Psi \rangle 
\end{aligned}$$
-->


(quantum-mechanics:intro:non-relativistic:basis)=
### Space and Momentum Representation

(quantum-mechanics:intro:non-relativistic:basis:space)=
#### Space Representation

**Position operator** $\hat{\mathbf{r}}$ has eigenvalues $\mathbf{r}$ identifying the possible measurements of the position

$$\hat{\mathbf{r}} | \mathbf{r} \rangle = \mathbf{r} | \mathbf{r} \rangle \ ,$$

being $\mathbf{r}$ the result of the measurement (position in space, mathematically it could be a vector), and $| \mathbf{r} \rangle$ the state function corresponding to the measurement $\mathbf{r}$ of the position.

- Result of measurement, $\mathbf{r}$, is a position in space. As an example, it could be a point in an Euclidean space $P \in E^n$. It could be written using properties of Dirac's delta "function"

  $$
    \mathbf{r} = \int_{\mathbf{r}'} \delta (\mathbf{r}'-\mathbf{r}) \, \mathbf{r}' d \mathbf{r}'
  $$

- Projection of wave function over eigenstates of position operator

  $$\begin{aligned}
  \langle \mathbf{r} | \Psi \rangle(t) = \Psi(\mathbf{r}, t)
  & = \int_{\mathbf{r}'} \delta(\mathbf{r} - \mathbf{r}') \Psi(\mathbf{r}',t) d \mathbf{r}' = \\
  & = \int_{\mathbf{r}'} \langle \mathbf{r} | \mathbf{r}' \rangle \Psi(\mathbf{r}',t) d \mathbf{r}' = \\
  & = \int_{\mathbf{r}'} \langle \mathbf{r} | \mathbf{r}' \rangle \langle \mathbf{r}' | \Psi \rangle (t) d \mathbf{r}' = \\
  & = \langle \mathbf{r} | \underbrace{\left( \int_{\mathbf{r}'} | \mathbf{r}' \rangle \langle \mathbf{r}' | d \mathbf{r}' \right)}_{= \hat{\mathbf{1}}} | \Psi \rangle (t) \ .
  \end{aligned}$$

- having used orthogonality (**todo** *why? provide definition and examples of operators with continuous spectrum*)

  $$\langle \mathbf{r}' | \mathbf{r} \rangle = \delta(\mathbf{r}' - \mathbf{r})$$

- Expansion of a state function $|\Psi\rangle (t)$ over the basis of the position operator

  $$\begin{aligned}
  | \Psi \rangle (t) = \hat{\mathbf{1}} | \Psi \rangle(t) 
    = \left( \int_{\mathbf{r}'} | \mathbf{r}' \rangle \langle \mathbf{r}' d \mathbf{r}' \right) | \Psi \rangle(t) 
    = \int_{\mathbf{r}'} | \mathbf{r}' \rangle \langle \mathbf{r}' | \Psi \rangle(t) \, d \mathbf{r}' \ .
  \end{aligned}$$

- Unitariety and probability density

  $$\begin{aligned}
  1 = \langle \Psi | \Psi \rangle (t) 
    & = \langle \Psi | \left( \int_{\mathbf{r}'} | \mathbf{r}' \rangle \langle \mathbf{r}' d \mathbf{r}' \right) | \Psi \rangle \\
    & = \int_{\mathbf{r}'} \langle \Psi | \mathbf{r}' \rangle \langle \mathbf{r}' | \Psi \rangle \, d \mathbf{r}' \\
    & = \int_{\mathbf{r}'} \Psi^*(\mathbf{r}',t) \Psi(\mathbf{r}',t) \, d \mathbf{r}' \\
    & = \int_{\mathbf{r}'} \left| \Psi(\mathbf{r}',t) \right|^2 \, d \mathbf{r}' \\
  \end{aligned}$$
  
  and thus $\left|\Psi(\mathbf{r},t)\right|^2$ can be interpreted as the **probability density function** of measuring position of the system equal to $\mathbf{r}'$.

- Average value of the operator

  $$\begin{aligned}
  \bar{\mathbf{r}} & = \langle \Psi | \hat{\mathbf{r}} | \Psi \rangle = \\
  & = \int_{\mathbf{r}'} \langle \Psi | \mathbf{r}' \rangle \langle \mathbf{r}' | d \mathbf{r}' \ | \hat{\mathbf{r}} | \ \int_{\mathbf{r}''} | \mathbf{r}'' \rangle \langle \mathbf{r}'' | \Psi \rangle \, d \mathbf{r}'' \\
  & = \int_{\mathbf{r}'} \int_{\mathbf{r}''} \langle \Psi | \mathbf{r}' \rangle \langle \mathbf{r}' | \hat{\mathbf{r}} |  \mathbf{r}'' \rangle \langle \mathbf{r}'' | \Psi \rangle \, d \mathbf{r}'  d \mathbf{r}'' = \\
  & = \int_{\mathbf{r}'} \int_{\mathbf{r}''} \langle \Psi | \mathbf{r}' \rangle \underbrace{\langle \mathbf{r}' |  \mathbf{r}'' \rangle}_{=\delta(\mathbf{r}'-\mathbf{r}'')} \mathbf{r}'' \langle \mathbf{r}'' | \Psi \rangle \, d \mathbf{r}'  d \mathbf{r}'' = \\
  & = \int_{\mathbf{r}'} \langle \Psi | \mathbf{r}' \rangle \mathbf{r}' \langle \mathbf{r}' | \Psi \rangle \, d \mathbf{r}' = \\
  & = \int_{\mathbf{r}'} \Psi^*(\mathbf{r}',t) \ \mathbf{r}' \ \Psi(\mathbf{r}',t) \, d \mathbf{r}' = \\
  & = \int_{\mathbf{r}'}  \left| \Psi(\mathbf{r}',t) \right|^2 \, \mathbf{r}' \, d \mathbf{r}' \ .
  \end{aligned}$$

(quantum-mechanics:intro:non-relativistic:basis:momentum)=
#### Momentum Representation

**Momentum operator** as the limit of...**todo** *prove the expression of the momentum operator as the limit of the generator of translation*

$$\langle \mathbf{r} | \hat{\mathbf{p}} = - i \hbar \nabla \langle \mathbf{r} | $$ (eq:qm:momentum-operator)

- Spectrum

  $$\hat{\mathbf{p}} | \mathbf{p} \rangle = \mathbf{p} | \mathbf{p} \rangle$$

  $$\langle \mathbf{r} | \hat{\mathbf{p}} | \mathbf{p} \rangle = - i \hbar \nabla \langle \mathbf{r} | \mathbf{p} \rangle = \mathbf{p} \langle \mathbf{r} | \mathbf{p} \rangle$$

  and thus the eigenvectors in space base $\mathbf{p}(\mathbf{r}) = \langle \mathbf{r} | \mathbf{p} \rangle$ are the solution of the differential equation

  $$- i \hbar \nabla \mathbf{p}(\mathbf{r}) = \mathbf{p} \mathbf{p}(\mathbf{r}) \ ,$$

  that in Cartesian coordinates reads

  $$- i \hbar \partial_j p_k(\mathbf{r}) = p_j p_k(\mathbf{r})$$

  $$p_k(\mathbf{r}) = p_{k,0} \exp \left[ i \frac{p_j}{\hbar} r_j \right]$$

  or

  $$\langle \mathbf{r} | \mathbf{p} \rangle = \mathbf{p}(\mathbf{r}) = \mathbf{p}_0 \exp \left[ i \frac{\mathbf{p} \cdot \mathbf{r}}{\hbar} \right]$$

  **todo**
  - normalization factor $\frac{1}{(2 \pi)^{\frac{3}{2}}}$

    $$\mathscr{F}\{ \delta(x) \}(k) = \int_{-\infty}^{\infty} \delta(x) e^{-ikx} \, dx = 1$$

  - Fourier transform and inverse Fourier transform: definitions and proofs (link to a math section)

  - representation in basis of wave vector operator $\hat{\mathbf{k}}$, $\hat{\mathbf{p}} = \hbar \hat{\mathbf{k}}$

(quantum-mechanics:intro:non-relativistic:basis:space-momentum)=
#### From position to momentum representation

Momentum and wave vector, $\mathbf{p} = \hbar \mathbf{k}$

$$\begin{aligned}
  \langle \mathbf{p} | \Psi \rangle
  & = \langle \mathbf{p} | \int_{\mathbf{r}'} | \mathbf{r}' \rangle \langle \mathbf{r}' | \Psi\rangle d \mathbf{r}' = \\
  & =   \int_{\mathbf{r}'} \langle \mathbf{p} | \mathbf{r}' \rangle \langle \mathbf{r}' | \Psi\rangle d \mathbf{r}' = \\
  & = \frac{1}{(2\pi)^{3/2}} \int_{\mathbf{r}'} \exp \left[ i \frac{\mathbf{p} \cdot \mathbf{r}}{\hbar} \right] \langle \mathbf{r}' | \Psi\rangle d \mathbf{r}' = \\
\end{aligned}$$

Relation between position and wave-number representation can be represented with a Fourier transform

$$\begin{aligned}
  \langle \mathbf{k} | \Psi \rangle
  & = \langle \mathbf{k} | \int_{\mathbf{r}'} | \mathbf{r}' \rangle \langle \mathbf{r}' | \Psi\rangle d \mathbf{r}' = \\
  & =   \int_{\mathbf{r}'} \langle \mathbf{k} | \mathbf{r}' \rangle \langle \mathbf{r}' | \Psi\rangle d \mathbf{r}' = \\
  & = \frac{1}{(2\pi)^{3/2}} \int_{\mathbf{r}'} \exp \left[ i \mathbf{k} \cdot \mathbf{r}' \right] \langle \mathbf{r}' | \Psi\rangle d \mathbf{r}' = \\
  & = \frac{1}{(2\pi)^{3/2}} \int_{\mathbf{r}'} \exp \left[ i \mathbf{k} \cdot \mathbf{r}' \right] \Psi(\mathbf{r}') d \mathbf{r}' = \\
  & = \mathscr{F}\{ \Psi(\mathbf{r}) \} (\mathbf{k})
\end{aligned}$$


(quantum-mechanics:intro:non-relativistic:schrodinger-equation)=
### Schrodinger Equation

$$i \hbar \dfrac{d}{dt} | \Psi \rangle = \hat{H} | \Psi \rangle $$

being $\hat{H}$ the Hamiltonian operator and $|\Psi\rangle$ the wave function, as a function of time $t$ as an independent variable.

(quantum-mechanics:intro:non-relativistic:schrodinger-equation:hamiltonian)=
#### Stationary States
Eigenspace of the Hamiltonian operator

$$\hat{H} |\Psi_k \rangle = E_k |\Psi_k \rangle \ ,$$

with $E_k$ possible values of energy measurements. *If no eigenstates with the same eigenvalue exists, then...otherwise...*
*Without external influence* **todo** *be more detailed!*, energy values and eigenstates of the systems are constant in time.

Thus, exapnding the state of the system $|\Psi\rangle$ over the stationary states gives $|\Psi_k\rangle$, $|\Psi\rangle = |\Psi_k\rangle c_k(t)$, and inserting in Schrodinger equation

$$i \hbar \dot{c}_k |\Psi_k\rangle = c_k  E_k |\Psi_k\rangle$$

and exploiting orthogonality of eigenstates, a diagonal system for the amplitudes of stationary states ariese,

$$i \hbar \dot{c}_k = c_k E_k \ .$$

whose solution reads

$$c_k(t) = c_{k,0} \exp \left[- i \frac{E_k}{\hbar} t \right]$$

Thus the state of the system evolves like a superposition of monochromatic waves with frequencies $\omega_k = \frac{E_k}{\hbar}$,

$$| \Psi \rangle = | \Psi_k \rangle c_k(t) = | \Psi_k \rangle c_{k,0}\exp\left[-i \frac{E_k}{\hbar} t \right] \ .$$

$$\begin{aligned}
 \dfrac{d}{dt} \bar{A}
 & = \dfrac{d}{dt} \left( \langle \Psi | \hat{A} | \Psi \rangle \right) = \\
 & = \dfrac{d}{dt} \langle \Psi | \hat{A} | \Psi \rangle + \langle \Psi | \frac{d \hat{A}}{dt} | \Psi \rangle + \langle \Psi | \hat{A} \frac{d}{dt} | \Psi \rangle = \\
 & = \langle \Psi | \frac{d \hat{A}}{dt} | \Psi \rangle + \frac{i}{\hbar} \langle \Psi | \hat{H} \hat{A} | \Psi \rangle - \frac{i}{\hbar} \langle \Psi | \hat{A} \hat{H} | \Psi \rangle = \\
 & = \langle \Psi | \left( \frac{i}{\hbar} [ \hat{H}, \hat{A} ] + \frac{d \hat{A}}{dt} \right) | \Psi \rangle \ .
\end{aligned}$$

(quantum-mechanics:intro:non-relativistic:schrodinger-equation:pictures)=
#### Pictures
- Schrodinger
- Heisenberg
- Interaction

(quantum-mechanics:intro:non-relativistic:schrodinger-equation:pictures:schrodinger)=
##### Schrodinger

If $\hat{H}$ not function of time

$$| \Psi \rangle (t) = \exp\left[ - i \frac{\hat{H}}{\hbar} (t-t_0) \right] | \Psi \rangle(t_0) = \hat{U}(t,t_0) | \Psi \rangle(t_0) $$

$$\bar{A} = \langle \Psi | \hat{A} | \Psi \rangle = \langle \Psi_0 | \hat{U}^*(t,t_0) \hat{A} \hat{U}(t,t_0) | \Psi_0 \rangle$$

(quantum-mechanics:intro:non-relativistic:schrodinger-equation:pictures:heisenberg)=
##### Heisenberg

While Schrodinger picture works with (usually) time-independent operators and time-dependent wave functions, Heisenberg picture works with time-dependent operators and time-independent wave functions. The state of a quantum system at two different times is connected by a unitary operator $U_{t,t_0}$,

$$| \Psi_t \rangle = U_{t,t_0} | \Psi_{t_0} \rangle$$

**Expected value.** The expected value of the physical quantity represented by the Hermitian operator $\hat{A}$ reads

$$\begin{aligned}
 \langle \hat{A} \rangle 
 & = \langle \Psi_t | \hat{A} | \Psi_t \rangle = \\
 & = \langle \Psi_{t_0} | U^{\dagger}_{t,t_0} \hat{A} U_{t,t_0} | \Psi_{t_0} \rangle = \\
 & = \langle \Psi_{t_0} | \hat{A}_H(t) | \Psi_{t_0} \rangle \ ,
\end{aligned}$$

having defined the counterpart in Heisenberg picture, $\hat{A}_H(t) = U^{\dagger}_{t,t_0} \hat{A} U_{t,t_0}$ of the operator $\hat{A}$ in Schrodinger picture.

**Hamiltonian operator in Heisenberg picture.** 

$$\hat{H}_H = U^\dagger \hat{H} U  \ .$$

**If** the Hamiltonian operator is **time-independent in Schrodinger picture**, the evolution operator can be written as $U_{t} = \exp\left(-i \frac{\hat{H}}{\hbar} t  \right)$. In this case, $U$ and $\hat{H}$ commute, and the Hamiltonian operator in Heisenberg picture has the same expression as the Hamiltonian operator in Schrodinger equation,

$$\hat{H}_H = U^{\dagger} \hat{H} U = \quad ( \quad \text{if $\partial_t \hat{H} = 0$} \quad ) \quad = U^{\dagger} U \hat{H} = \hat{H} \ .$$

**Time derivative of the operator $\hat{A}_H(t)$.**

$$\begin{aligned}
  \dfrac{d}{dt} \hat{A}_H(t)
  & = \dfrac{d}{dt} \left( U^{\dagger}_{t,t_0} \hat{A} U_{t,t_0} \right) = \\
  & = \partial_t U^{\dagger}_{t,t_0} \hat{A} U_{t,t_0} + U^{\dagger}_{t,t_0} \partial_t \hat{A} U_{t,t_0} + U^{\dagger}_{t,t_0} \hat{A} \partial_t U_{t,t_0} = \\
  & = - \frac{1}{i \hbar} U^{\dagger}_{t,t_0} \hat{H} \hat{A} U_{t,t_0} + U^{\dagger}_{t,t_0} \partial_t \hat{A} U_{t,t_0} +\frac{1}{i \hbar}  U^{\dagger}_{t,t_0} \hat{A} \hat{H} U_{t,t_0} = \\
  & = - \frac{1}{i \hbar} U^{\dagger}_{t,t_0} \hat{H} U_{t,t_0} U^{\dagger}_{t,t_0} \hat{A} U_{t,t_0} + U^{\dagger}_{t,t_0} \partial_t \hat{A} U_{t,t_0} +\frac{1}{i \hbar}  U^{\dagger}_{t,t_0} \hat{A} U_{t,t_0} U^{\dagger}_{t,t_0}  \hat{H} U_{t,t_0} = \\
  & = - \frac{1}{i\hbar} \left[ \hat{H}_H, \hat{A}_H \right] + \left( \partial_t \hat{A} \right)_H  \ ,
\end{aligned}$$

as the relation {eq}`eq:h-u-dtu` gives $\partial_t U_{t,t_0} U^{\dagger}_{t,t_0} = \frac{1}{i \hbar} \hat{H}$, 


<!--
**Commutation of $U$ with $\hat{H}$.**

$$\hat{H} U = \left( i \hbar \partial_t U \,  U^\dagger \right) U = i \hbar \partial_t U$$

$$U^\dagger \hat{H} = U^\dagger \left( i \hbar \partial_t U \,  U^\dagger \right) = - i \hbar U^{\dagger} U \partial_t U^{\dagger} = - i \hbar \partial_t U^\dagger =$$
-->

---

**old** ...
for $\hat{H}$ independent from time $t$,

$$\begin{aligned}
  \dfrac{d}{dt} \bar{\mathbf{r}} & = \overline{\frac{i}{\hbar} \left[ \hat{H}, \hat{\mathbf{r}} \right]} = - \frac{1}{ih} \overline{[ \hat{H}, \hat{\mathbf{r}} ]} \\
  \dfrac{d}{dt} \bar{\mathbf{p}} & = \overline{\frac{i}{\hbar} \left[ \hat{H}, \hat{\mathbf{p}} \right]} = - \frac{1}{ih} \overline{[ \hat{H}, \hat{\mathbf{p}} ]} \\
\end{aligned}$$

```{dropdown} Hamiltonian Mechanics

From Lagrange equations

$$\dfrac{d}{dt} \left( \frac{\partial L}{\partial \dot{q}} \right) - \frac{\partial L}{\partial q} = Q_q$$

$q$ generalized coordinates, $p:= \frac{\partial L}{\partial \dot{q}}$ generalized momenta.

Hamiltonian

$$H(p,q,t) = p \dot{q} - L(\dot{q}, q, t)$$

Increment of the Hamiltonian

$$dH = \partial_p H dp + \partial_q H dq + \partial_t H dt $$

$$\begin{aligned}
  dH & = \dot{q} dp + p d \dot{q} - \partial_{\dot{q}} L d \dot{q} - \partial_{q} L d q - \partial_t L d t = \\
     & = \dot{q} dp - \partial_{q} L d q - \partial_t L d t = \\
     & = \dot{q} dp - \left( \dot{p} + Q_q \right) d q - \partial_t L d t = \\
\end{aligned}$$

$$\begin{cases}
  \frac{\partial H}{\partial p} = \dot{q} \\
  \frac{\partial H}{\partial q} = - \frac{\partial L}{\partial q} = - \dot{p} + Q_q \\
  \frac{\partial H}{\partial t} = - \frac{\partial L}{\partial t}
\end{cases}$$

Physical quantity $f(q(t), p(t), t)$. Its time derivative reads

$$\begin{aligned}
\frac{d f}{dt}
  & = \frac{\partial f}{\partial q} \dot{q} + \frac{\partial f}{\partial p} \dot{p} + \frac{\partial f}{\partial t} = \\
  & = \frac{\partial f}{\partial q} \frac{\partial H}{\partial p} + \frac{\partial f}{\partial p} \left[ - \frac{\partial H}{\partial q} + Q_q \right] + \frac{\partial f}{\partial t} = \\
  & = - \partial_q H \partial_p f + \partial_p H \partial_q f + \partial_t f + Q_q \partial_p f = \\
  & = - \{ H, f \} + \partial_t f + Q_q \partial_p f
\end{aligned}$$

If $Q_q = 0$, the correspondence between quantum mechanics and classical mechanics

$$\frac{d f}{d t} = - \{ H, f \} + \partial_t f \qquad \leftrightarrow \qquad \dfrac{d}{dt} \overline{\hat{f}} = - \frac{1}{i \hbar} \overline{ [ \hat{H}, \hat{f} ]} + \overline{\frac{\partial \hat{f}}{\partial t}}$$

$$\{ H, f \} \qquad \leftrightarrow \qquad \frac{i}{\hbar}[\hat{H}, \hat{f}]$$


```



(quantum-mechanics:intro:non-relativistic:schrodinger-equation:pictures:interaction)=
##### Interaction

### Operators

Commuting operators, $0 = [ \hat{A}, \hat{B} ] = \hat{A} \hat{B} - \hat{B} \hat{A}$. Their eigenvalue problems read

$$\begin{aligned}
  \hat{A} | a \rangle & = a | a \rangle \\
  \hat{B} | b \rangle & = b | b \rangle \\
\end{aligned}$$


$$
  a \hat{B} | a \rangle = \hat{B} \hat{A} | a \rangle = \hat{A} \left( \hat{B} | a \rangle \right) \\
$$

Thus the state $\hat{B} | a \rangle$ is an eigenstate of $\hat{A}$, with the same eigenvalue $a$. If the eigenvalue is non-degenerate, this eigenstate must be proportional to the original eigenstate, and thus $\hat{B} | a \rangle = b | a \rangle$. If the eigenvalue is degenerate, the state $\hat{B} | a \rangle$ can be a linear combination of all the eigenstates $| a_i \rangle$ with eigenvalue $a_i = a$.

### Matrix Mechanics

#### Attualization of 1925 papers

<!--
$$|\Psi\rangle = \sum_k | \Psi_k \rangle c_{k,0}\exp\left[-i \frac{E_k}{\hbar} t \right]$$

$$\langle \Psi | \hat{\mathbf{X}} | \Psi \rangle$$

$$\langle \Psi | \Psi_m \rangle \langle \Psi_m | \hat{\mathbf{X}} | \Psi_n \rangle \langle \Psi_n | \Psi \rangle$$

$$X_{mn} = \langle \Psi_m | \hat{\mathbf{X}} | \Psi_n \rangle $$

$$\langle \Psi | \hat{\mathbf{P}} | \Psi \rangle$$
-->

...to find the canonical commutation relation,

$$[ \hat{\mathbf{r}}, \hat{\mathbf{p}} ] = i \hbar  \mathbb{I} \, \hat{\mathbf{1}} \ .$$

$$\begin{aligned}
\left[ \hat{\mathbf{r}}, \hat{\mathbf{p}} \right]
 & = \hat{\mathbf{r}} \hat{\mathbf{p}} - \hat{\mathbf{p}} \hat{\mathbf{r}} = \\
 & = \hat{\mathbf{r}} \int_{\mathbf{r}} | \mathbf{r} \rangle \langle \mathbf{r} | d \mathbf{r} \hat{\mathbf{p}}
   - \hat{\mathbf{p}} \int_{\mathbf{r}} | \mathbf{r} \rangle \langle \mathbf{r} | d \mathbf{r} \ \hat{\mathbf{r}} \ \int_{\mathbf{r}'} | \mathbf{r}' \rangle \langle \mathbf{r}' | d \mathbf{r}' = \\
 & = - \int_{\mathbf{r}} \mathbf{r} | \mathbf{r} \rangle i \hbar \nabla \langle \mathbf{r} | \, d \mathbf{r} - \hat{\mathbf{p}} \int_{\mathbf{r}} \int_{\mathbf{r}'} | \mathbf{r} \rangle \mathbf{r}' \underbrace{\langle \mathbf{r} |\mathbf{r}' \rangle}_{\delta(\mathbf{r}-\mathbf{r}')} \langle \mathbf{r}' | d \mathbf{r}' = \\
 & = - \int_{\mathbf{r}} \mathbf{r} | \mathbf{r} \rangle i \hbar \nabla \langle \mathbf{r} | \, d \mathbf{r} - \hat{\mathbf{p}} \int_{\mathbf{r}} \mathbf{r} | \mathbf{r} \rangle \langle \mathbf{r} | d \mathbf{r} = \\
 & = - \int_{\mathbf{r}} \mathbf{r} | \mathbf{r} \rangle i \hbar \nabla \langle \mathbf{r} | \, d \mathbf{r} - \int_{\mathbf{r}'} | \mathbf{r} \rangle \langle \mathbf{r} | d \mathbf{r} \ \hat{\mathbf{p}} \ \int_{\mathbf{r}'} \mathbf{r}' | \mathbf{r}' \rangle \langle \mathbf{r}' | d \mathbf{r}' = \\
 & = - \int_{\mathbf{r}} \mathbf{r} | \mathbf{r} \rangle i \hbar \nabla \langle \mathbf{r} | \, d \mathbf{r} + \int_{\mathbf{r}} | \mathbf{r} \rangle i \hbar \nabla \langle \mathbf{r} | d \mathbf{r} \int_{\mathbf{r}'} \mathbf{r}' | \mathbf{r}' \rangle \langle \mathbf{r}' | d \mathbf{r}' = \dots
\end{aligned}$$

$$\begin{aligned}
\left[ \hat{\mathbf{r}}, \hat{\mathbf{p}} \right] | \Psi \rangle 
 & = - \int_{\mathbf{r}} \mathbf{r} | \mathbf{r} \rangle i \hbar \nabla \Psi(\mathbf{r},t) + \int_{\mathbf{r}} | \mathbf{r} \rangle i \hbar \nabla \left( \mathbf{r} \Psi(\mathbf{r},t) \right) = \\
 & = - \int_{\mathbf{r}} | \mathbf{r} \rangle i \hbar \left[ \mathbf{r} \nabla \Psi(\mathbf{r},t) + \mathbb{I} \Psi(\mathbf{r},t) + \mathbf{r} \nabla \Psi(\mathbf{r},t) \right] = \\
 & = i \hbar \underbrace{\int_{\mathbf{r}} | \mathbf{r} \rangle \langle \mathbf{r} | d \mathbf{r}}_{\hat{\mathbf{1}}} \, | \Psi \rangle \ ,
\end{aligned}$$

and since $| \Psi \rangle$ is arbitrary

$$\left[ \hat{\mathbf{r}}, \hat{\mathbf{p}} \right] = i \hbar \mathbb{I} \hat{\mathbf{1}} \ . $$

$$\left[ \hat{r}_a, \hat{p}_b \right] = i \hbar \delta_{ab} \ . $$


(quantum-mechanics:heisenber-uncertainty-relation)=
### Heisenberg Uncertainty relation

Uncertainty principle is a relation that holds for "wave descriptions" as it can be proved in the generic framework of [Fourier transform](https://basics2022.github.io/bbooks-math-miscellanea/ch/complex/fourier-transform.html), see [Fourier transform:Uncertainty relation](https://basics2022.github.io/bbooks-math-miscellanea/ch/complex/fourier-transform.html#uncertainty-relation).

- Heisenberg uncertainty relation is a relation between product of the variance of two physical quantities and their commutator,
- **todo** *relation with measurement process and outcomes. Commutation as a measurement process: first measure $B$ and then $A$, or first measure $A$ and then $B$*

$$\sigma_A \sigma_B \ge \frac{1}{2} \left|\overline{[\hat{A}, \hat{B}]}\right| \ .$$

```{dropdown} Proof of Heisenberg uncertainty "principle"
:open:

$$\begin{aligned}
 \sigma^2_A \sigma^2_B
 & = \langle \Psi | \left(\hat{A} - \bar{A} \right)^2 | \Psi \rangle\langle \Psi | \left(\hat{B} - \bar{B} \right)^2 | \Psi \rangle = \\
 & = \langle (\hat{A} - \bar{A} ) \Psi |  (\hat{A} - \bar{A} ) \Psi \rangle \langle  (\hat{B} - \bar{B} ) \Psi |  (\hat{B} - \bar{B} ) \Psi \rangle = \\
 & = \| ( \hat{A} - \bar{A} ) \Psi \|^2 \| ( \hat{B} - \bar{B} ) \Psi \|^2 = \\
 & \ge \left| \langle ( \hat{A} - \bar{A} ) \Psi | ( \hat{B} - \bar{B} ) \Psi  \rangle \right|^2 = \\
 & = \left| \langle \Psi | (\hat{A} - \bar{A})(\hat{B} - \bar{B}) \Psi \rangle \right|^2 = \\
 & = \left| \langle \Psi | \hat{A}\hat{B} - \hat{A}\bar{B} - \bar{A}\hat{B} + \bar{A}\bar{B} | \Psi \rangle \right|^2 = \\
 & = \left| \langle \Psi | \hat{A}\hat{B} - \bar{A}\bar{B} | \Psi \rangle \right|^2 \ge && \text{(1)} \\
 & = \left| \frac{\langle \Psi | \hat{A}\hat{B} - \hat{B}\hat{A} | \Psi \rangle}{2i} \right|^2 = \\
 & = \frac{ \left|\langle \Psi | [\hat{A}, \hat{B}] | \Psi \rangle \right|^2}{4} = \frac{1}{4} \left| \overline{[\hat{A}, \hat{B}]} \right|^2
\end{aligned}$$

having used Cauchy-Schwartz triangle inequality in (1),

$$|z| \ge | \text{im}(z) | = \frac{z - z^*}{2 i} \ .$$

<!--
$$|z| = \frac{\text{re}\{z\} + \text{re}\{z^*\}}{2} = \frac{\text{im}\{z\} - \text{im}\{z^*\}}{2i}$$
-->

```

Hesienberg uncertainty principles applied to position and momentum reads

$$\sigma_{r_a} \sigma_{p_b} \ge \frac{1}{2} \left|\overline{[\hat{r}_a, \hat{p}_b]}\right| = \frac{\hbar}{2}  \delta_{ab} \ .$$


## Many-body problem
Wave function with symmetries: Fermions and Bosons


