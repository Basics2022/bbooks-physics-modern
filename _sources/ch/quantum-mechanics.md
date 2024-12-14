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
#### Operators and Observables
Physical observable quantities are represented by [Hermitian operators](quantum-mechanics:math:operators:self-adjoint)



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


