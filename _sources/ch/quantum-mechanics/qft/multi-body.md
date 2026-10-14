(quantum-mechanics:qft:multi-body)=
# Multi-body quantum mechanics and QFT

## First quantization

particles → waves; $x,p\to\hat x,\hat p$.

$$
i\hbar|\dot\psi\rangle=\hat H|\psi\rangle,\qquad
|\psi\rangle=\sum c_n|\psi_n\rangle\ \ (\text{stationary states}),\qquad
\hat H|\psi_n\rangle=E_n|\psi_n\rangle
$$

$$
1=\langle\psi|\psi\rangle=\sum_n|c_n|^2,\qquad |c_n|^2=\text{probability of being in }|\psi_n\rangle
$$

The Schrödinger equation makes $c_n$ vary continuously. **But** EM radiation occurs in **quantum jumps** ≈

1. destruction of a high-energy $e^-$,
2. creation of a lower-energy $e^-$ + a $\gamma$.

## Second quantization of the electron field

$$
\psi(x,t)=\sum_kb_k(t)\psi_k(x)=\sum_kb_{k0}\psi_k(x)e^{-i\omega_kt}
$$

($\psi_k$ are the energy eigenfunctions.)

$$
\sum_ki\hbar\dot b_k|k\rangle=\hat H\sum_kb_k|k\rangle\ \to\ b_k=b_{k0}\exp\!\left(-i\frac{E_k}{\hbar}t\right)
$$

$$
\langle\psi|\hat H|\psi\rangle=\sum_{mn}\langle m|\hat H|n\rangle\,b^*_{m0}b_{n0}\,e^{+i\omega_mt}e^{-i\omega_nt}
=\sum_nE_n|b_{n0}|^2,\qquad(E_n\langle m|n\rangle=E_n\delta_{mn})
$$

This is the projection of the wavefunction of the $e^-$ onto the energy eigenfunction.

**2nd quantization:** $b_{k0}\to\hat b_k$ (destruction operator). In analogy with multi-body QM:

$$
\hat H=\sum_kE_k\hat n_k=\sum_kE_k\hat b_k^\dagger\hat b_k
$$

### Jordan–Wigner (1928), "On the Pauli exclusion principle"

The state of an atom is described by the occupation numbers of the orbitals: $|n_1\,n_2\dots\rangle$.

* Inconsistency of results if $b_1^\dagger b_2^\dagger|0,0\rangle=-b_2^\dagger b_1^\dagger|0,0\rangle$ ⟹ $|1,1\rangle=-1\times|1,1\rangle$ **(!)** — anticommutation relation.

* Solution of Jordan and Wigner:

$$
\hat b^\dagger_k|\dots n_k\dots\rangle=\theta_k\sqrt{1-n_k}\,|\dots(1-n)_k\dots\rangle,\qquad
\hat b_k|\dots n_k\dots\rangle=\theta_k\sqrt{n_k}\,|\dots(1-n)_k\dots\rangle
$$

with $\theta_k=(-1)^{n_1+\dots+n_{k-1}}$.

## Hamiltonian and state of $e^-$ and radiation fields

$$
e^-:\ |\phi_e\rangle=|n_{e1},n_{e2},\dots\rangle,\quad \hat H_e=\sum_kE_k\hat b_k^\dagger\hat b_k
\qquad\qquad
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

