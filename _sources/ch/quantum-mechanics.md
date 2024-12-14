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
- unitary $1 = \langle \Psi | \Psi \rangle = \left| \Psi \right|^2$, for statistical interpretation of $\left| \Psi \right|^2$ as a density probability function

#### Operators and Observables
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


#### Space Representation

Space operator $\hat{\mathbf{r}}$ has eigenvalues $\mathbf{r}$ identifying the possible measurements of the position

$$\hat{\mathbf{r}} | \Psi \rangle = \mathbf{r} | \Psi \rangle \ ,$$


#### Momentum Representation

### Schrodinger Equation

$$i \hbar \dfrac{d}{dt} | \Psi \rangle = \hat{H} | \Psi \rangle $$

being $\hat{H}$ the Hamiltonian operator and $|\Psi\rangle$ the wave function, as a function of time $t$ as an independent variable.

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

#### Representations
##### Schrodinger
##### Heisenberg
##### ...


### Matrix Mechanics

#### Attualization of 1925 papers

$$|\Psi\rangle = \sum_k | \Psi_k \rangle c_{k,0}\exp\left[-i \frac{E_k}{\hbar} t \right]$$

$$\langle \Psi | \hat{\mathbf{X}} | \Psi \rangle$$

$$\langle \Psi | \Psi_m \rangle \langle \Psi_m | \hat{\mathbf{X}} | \Psi_n \rangle \langle \Psi_n | \Psi \rangle$$

$$X_{mn} = \langle \Psi_m | \hat{\mathbf{X}} | \Psi_n \rangle $$


$$\langle \Psi | \hat{\mathbf{P}} | \Psi \rangle$$

...to find the canonical commutation relation,

$$[ \hat{\mathbf{r}}, \hat{\mathbf{p}} ] = i \hbar \, \hat{\mathbf{1}} \ .$$



## Many-body problem
Wave function with symmetries: Fermions and Bosons


