(quantum-mechanics:qft:multi-body)=
# Multi-body quantum mechanics and QFT

In multi-body quantum systems the number of identical particles may change in time, and the interactions may occur as non-smooth dynamics involving creation and destruction of particles. First, the limits of the quantum systems represented with so called first quantization process are discussed: these systems can't represent systems with a variable number of particles and non smooth interactions. Then, the second quantization of the electron field is introduced, along with the Pauli exclusion principle. Eventually, the properties and the formalism for the second quantization of boson and fermion fields are recalled.

(quantum-mechanics:qft:multi-body:first-quantization)=
## First quantization

First quantization moves the description of a particle to a wave process, promoting generalized coordinates and momenta $x$, $p$ to operators $\hat{q}$, $\hat{p}$. The state of a system is described by a wave function $| \Psi \rangle$ belonging to a Hilbert space $\mathcal{H}$, satisfying the Schrodinger equation of the system

$$i \hbar \dot{ | \Psi \rangle } = \hat{H} | \Psi \rangle \ .$$

The wavefunction $| \Psi \rangle$ satisfies the normalization condition $\langle \Psi | \Psi \rangle = 1$.
If the Hamiltonian operator $\hat{H}$ is independent from time, its spectral decomposition provides an orthogonal basis for $\mathcal{H}$ of stationary states $\{ | \psi_n \rangle \}$ and their energy levels $\{ E_n \}$. The wavefunction of the system $| \Psi \rangle$ can be represented in the orthonormal basis as

$$| \Psi(t) \rangle = \sum_n | \psi_n \rangle c_n(t) \ ,$$

with the coefficients $c_n$ that can be linked to the probability $|c_n|^2$ of finding the system whose state is represented by $| \Psi \rangle$ in the state $| \psi_n \rangle$, as from normalization condition it follows

$$1 = \langle \Psi | \Psi \rangle = \sum_{n,m} c_n^* c_m \underbrace{\langle \psi_n | \psi_m \rangle}_{\delta_{nm}} = \sum_n |c_n|^2 \ .$$

The Schrödinger equation makes $c_n(t)$ vary continuously. In energy basis, the coefficients of teh expansion are governed by the ODEs

$$i \hbar \dot{c}_n = E_n c_n \ ,$$

and thus they evolve as $c_n(t) = c_{n,0} \exp\left( - i \frac{E_n}{\hbar} t \right)$.


**But** Interactions between systems may occur as non-smooth dynamics. As an example, EM radiation absorption or emission by an atom occurs in **quantum jumps**. As an example, spontaneous emission of EM radiation from an atom involves:
1. the destruction of a high-energy $e^-$,
2. the creation of a lower-energy $e^-$ + a $\gamma$.

## Second quantization of the electron field

**First quantization.** The wave function describing an electron can be written as a linear combination of the energy eigenstates. In space representation

$$
\psi(\mathbf{r},t)=\sum_k b_k(t)\psi_k(\mathbf{r}) = \sum_k b_{k0} \psi_k(\mathbf{r}) e^{-i\omega_kt} \ .
$$

with $\omega_k = \tfrac{E_k}{\hbar}$. The expected value of the energy is 

$$
\langle\psi|\hat H|\psi\rangle=\sum_{m,n}\langle m|\hat H|n\rangle\,b^*_{m0}b_{n0}\,e^{+i\omega_mt}e^{-i\omega_nt}
=\sum_nE_n|b_{n0}|^2 \ .
$$

**Second quantization:** $b_{k0}\to\hat b_k$ (destruction operator). In analogy with multi-body QM:

$$
\hat H=\sum_kE_k\hat n_k=\sum_kE_k\hat b_k^\dagger\hat b_k
$$


## Hamiltonian and state of the non-interacting $e^-$ and radiation fields

**Electron field.** The state can be represented in the occupation number basis as a linear combination of the basis of the Fock space, namely

$$\left\{ | \mathbf{n} \rangle \right\} = \left\{ |\mathbf{0} \rangle, |1,0,0,\dots \rangle, |0,1,0,\dots \rangle, \dots, |2,0,0,\dots \rangle, |1,1,0,\dots \rangle, \dots \right\} \ .$$

$$
e^-:\ |\phi_e\rangle=|n_{e1},n_{e2},\dots\rangle,\quad \hat H_e=\sum_kE_k\hat b_k^\dagger\hat b_k
$$

Radiation field

$$
\text{rad}:\ |\psi_r\rangle=|n_{k\alpha}\dots\rangle,\quad \hat H_{rad}=\sum_{k,\alpha}\hbar\omega_k\hat a^\dagger_{k\alpha}\hat a_{k\alpha}
$$

These are **non-interacting fields**.

An **interaction is required** to get quantum jumps of $e^-$ associated with creation/annihilation of a $\gamma$.

## Bosons and fermions

*(This page of the notes is written upside-down; the content is transcribed in condensed form.)*

**Bosons** — occupation-number formalism:

- $\hat a^\dagger$ acts on a state by raising it, $|0\rangle\to|1\rangle\to|2\rangle\to\cdots$, and $\hat a$ lowers it.
- Number operator: $\hat n_k=\hat a_k^\dagger\hat a_k$, s.t. $\hat n_k|\dots n_k\dots\rangle=n_k|\dots n_k\dots\rangle$.

$$
\hat a^\dagger_k|\dots n_k\dots\rangle=\sqrt{n_k+1}\,|\dots(n_k+1)\dots\rangle,\qquad
\hat a_k|\dots n_k\dots\rangle=\sqrt{n_k}\,|\dots(n_k-1)\dots\rangle
$$

CCR (canonical commutation relations):

$$
[\hat a_k,\hat a^\dagger_{k'}]=\hat a_k\hat a^\dagger_{k'}-\hat a^\dagger_{k'}\hat a_k=\delta_{kk'}
$$

**Fermions** — with occupation-number formalism (Pauli exclusion principle):

- $\hat b^\dagger\hat b^\dagger|0\rangle=0$, and $\hat b\,\hat b|1\rangle=0$ (a second particle cannot be added to an occupied orbital);
- $\hat b|0\rangle=0$, $\hat b^\dagger|1\rangle=0$;
- thus $\{\hat b,\hat b'\}$ and $\{\hat b^\dagger,\hat b'^\dagger\}$ vanish: **anticommutators**, $\{\hat b,\hat b^\dagger\}=1$ (CCR/anticommutation);
- number operator $\hat n=\hat b^\dagger\hat b$ satisfies $\hat n^2=\hat b^\dagger\hat b\hat b^\dagger\hat b=\hat b^\dagger(1-\hat b^\dagger\hat b)\hat b=\hat n$ ⟹ $n=0$ or $1$.

**[check]** Fermion/boson page: written upside-down and partly hard to read; verify against the original.

---

