(quantum-mechanics)=
# Quantum Mechanics

## Mathematical tools for quantum mechanics

```{prf:definition} Operator
```

```{prf:definition} Adjoint operator
Given an operator $\hat{A}: U \rightarrow V$, its self-adjoint $\hat{A}^*: V \rightarrow U$ is the operator s.t.

$$(\mathbf{v}, \ \hat{A} \mathbf{u})_{V} = (\mathbf{u}, \hat{A}^* \mathbf{v} )_{U}$$

holds for $\forall \mathbf{u} \in U, \ \mathbf{v} \in V$.

```

(quantum-mechanics:math:operators:self-adjoint)=
```{prf:definition} Hermitian (self-adjoint) operator
If $\hat{A}: U \rightarrow U$, it is a self-adjoint operator if $\hat{A}^* = \hat{A}$.
```
Self-adjoint operators have real eigenvalues, and orthogonal eigenvectors (at least those associated to different eigenvalues; those associated with the same eigenvalues can be used to build an orthogonal set of vectors with orthogonalization process).


## Postulates of Quantum Mechanics
- ...
- Canonical Commutation Relation (CCR) *and Canonical Anti-Commutation Relation...*

## Non-relativistic Mechanics
### Statistical Interpretation
#### Wave function
The state of a system is described by a wave function $|\Psi\rangle$ 

**todo**
- properties: domain, image,...
- unitary $1 = \langle \Psi | \Psi \rangle$

#### Operators and Observables
Physical **observable** quantities are represented by [Hermitian operators](quantum-mechanics:math:operators:self-adjoint).

Given $\hat{A}$ and the set of its eigenvectors $\{ |A_i \rangle \}_i$ (**todo** *continuous or discrete spectrum..., need to treat this difference quite in details*), with associated eigenvalues $\{ a_i \}_i$

$$\hat{A} |A_i \rangle = a_i |A_i\rangle$$

$$| \Psi \rangle = | A_i \rangle \langle A_i | \Psi \rangle =  | A_i \rangle \Psi_i^A $$

$$1 =\langle \Psi | \Psi \rangle = \Psi_j^{A*} \underbrace{\langle A_j | A_i \rangle}_{\delta_{ij}} \Psi_i^{A} = \left| \Psi_i^A \right|^2$$

$$\begin{aligned}
  \langle A_j| \Psi \rangle = \langle A_j | A_i \rangle \langle A_i | \Psi \rangle 
\end{aligned}$$



#### Space Representation
#### Momentum Representation

### Schrodinger Equation

$$i \hbar \dfrac{d}{dt} | \Psi \rangle = \hat{H} | \Psi \rangle $$

being $\hat{H}$ the Hamiltonian operator and $|\Psi\rangle$ the wave function, as a function of time $t$ as an independent variable.

#### Stationary States
Eigenspace of the Hamiltonian operator

$$\hat{H} |\Psi\rangle_i = E_i |\Psi\rangle_i \ ,$$

with $E_i$ energy. If no eigenstates with the same eigenvalue exists, then

### Matrix Mechanics

## Many-body problem
Wave function with symmetries: Fermions and Bosons


