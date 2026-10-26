(quantum-mechanics:qft:interactions)=
# Interacting Fields 


```{dropdown} Contents
:open:

* [Perturbation theory](quantum-mechanics:qft:interactions:perturbation-theory)
* [Interaction between electron and EM fields](quantum-mechanics:qft:interactions:e-em-fields)

```

A model for interacting electron and electomagnetic fields requires an interaction contribution in the Hamiltonian of the system, namely

$$
\hat H=\hat H_{atom}+\hat H_{rad}+\hat H_{inter}
$$

being 

$$
\hat H_{atom}=\sum E_k\hat b_k^\dagger\hat b_k
\quad , \quad
\hat H_{rad}=\sum E_{k,\alpha}\hat a^\dagger_{k,\alpha}\hat a_{k,\alpha}
$$

the Hamiltonian of the electron bound to the atom, and the Hamiltonian of the EM field. Interaction comes from the coupling of the electron dynamics and the EM field: electron may act as a source of the EM field, and its state is influenced by the EM field, as shown...

```{dropdown} References

**todo** *Add references to*
* *classical electromagnetism*
* *electromagnetism in special relativity*
* *notes about calculus of variations and Lagrangian approach*

```

As an example, minimal coupling for the motion of acharged particle in an EM field is readily obtained replacing the momentum $\mathbf{P}$ with the sum $\mathbf{P} + q \mathbf{A}$, or in classical mechanics $\vec{p} \rightarrow \vec{p} + q \vec{a}$. In classical mechanics the Hamiltonian reads

$$\mathcal{H} = \frac{1}{2}\frac{|\vec{p}- q \vec{a}|^2}{m} + q \varphi \ ,$$

producing two coupling terms, one linear and one quadratic in $\vec{a}$.

* The linear term produces the dominant interaction processes - for EM with low intensity - in the Hamiltonian terms with three creation/annihilation operators: a pair of creation/annihilation operators of the electron field and one creation or annihilation operator of the photon field, represent absorption and emission of light from the atom. As an example

  - **Absorption** process: $\hat b_n^\dagger\hat b_m\hat a_{k,\alpha}$ — atom $|\psi_m\rangle\to|\psi_n\rangle$, photon $|k,\alpha\rangle$ absorbed (destroyed from the EM field).
  - **Emission** process: $\hat b_m^\dagger\hat a^\dagger_{k,\alpha}\hat b_n$ — atom $|\psi_n\rangle\to|\psi_m\rangle$, photon $|k,\alpha\rangle$ emitted (created in the EM field).

* The quadratic term is responsible for scattering...


