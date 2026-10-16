(quantum-mechanics:second-quantizazion:fermions)=
# Second quantization. Fermions

(quantum-mechanics:second-quantizazion:fermions:creation-annihilation)=
## Creation and annihilation operators

(quantum-mechanics:second-quantizazion:fermions:jordan-wigner)=
### Jordan–Wigner (1928), "On the Pauli exclusion principle"

The state of an atom is described by the occupation numbers of the orbitals: $|n_1\,n_2\dots\rangle$.

* Inconsistency of results if $b_1^\dagger b_2^\dagger|0,0\rangle=-b_2^\dagger b_1^\dagger|0,0\rangle$ ⟹ $|1,1\rangle=-1\times|1,1\rangle$ **(!)** — anticommutation relation.

* Solution of Jordan and Wigner:

$$\begin{aligned}
\hat b^\dagger_k|\dots n_k\dots\rangle & = \theta_k\sqrt{1-n_k}\,|\dots(1-n)_k\dots\rangle \\
\hat b_k|\dots n_k\dots\rangle & = \theta_k\sqrt{n_k}\,|\dots(1-n)_k\dots\rangle
\end{aligned}$$

with $\theta_k=(-1)^{n_1+\dots+n_{k-1}}$.


