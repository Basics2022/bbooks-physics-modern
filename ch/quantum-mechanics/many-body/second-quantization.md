(quantum-mechanics:second-quantizazion)=
# Second Quantization

```{dropdown} Contents
:open:

* Indistinguishability of identical systems: bosons and fermions
* Second quantization: asking which particle is which state? is meaningless, as particles are indistinguishable. How many particles are in each state? could be a reasonable question

```

## Identical systems

Let a system be composed of $N$ identical indistinguishable sub-systems. The state of the subsystem $k$ is described by a single-system wave function $| \psi_k \rangle$ belonging to the single-system Hilbert space $\mathcal{H}_1$. Thus, the state of the many-body subsystem is described by a wave function $| \Psi \rangle$ belonging to the $N$ tensor product space 

$$\mathcal{H}^{\otimes N} = \underbrace{\mathcal{H}_1 \otimes \dots \otimes \mathcal{H}_1}_{n \text{ times}} \ .$$

Let $\{ | \alpha \rangle \}$ be an orthonormal basis for $\mathcal{H}_1$. A basis for $\mathcal{H}^{\otimes N}$ is 

$$| \alpha_1, \dots, \alpha_N \rangle = | \alpha_1 \rangle \dots | \alpha_N \rangle \ .$$

**Indistinguishability.** Applying a permutation operator once

$$P_{ij} \Psi( \dots, \mathbf{r}_i, \dots, \mathbf{r}_j, \dots ) = \Psi( \dots, \mathbf{r}_j, \dots, \mathbf{r}_i, \dots )$$

Applying it twice

$$P_{ij} P_{ij} \Psi( \dots, \mathbf{r}_i, \dots, \mathbf{r}_j, \dots ) = \Psi( \dots, \mathbf{r}_i, \dots, \mathbf{r}_j, \dots ) \ ,$$

it follows that $P_{ij} P_{ij} = 1$. Thus, two solutions are possible, corresponding to two different nature of the subsystems

* Bosons, $P_{ij} = 1$,

   $$\Psi(\dots, \ \mathbf{r}_j, \dots, \ \mathbf{r}_i, \dots) = \Psi(\dots, \ \mathbf{r}_i, \dots, \ \mathbf{r}_j, \dots)$$

* Fermions, $P_{ij} = -1$,

   $$\Psi(\dots, \ \mathbf{r}_j, \dots, \ \mathbf{r}_i, \dots) = - \Psi(\dots, \ \mathbf{r}_i, \dots, \ \mathbf{r}_j, \dots)$$

### Symmetrization and anti-symmetrization

...

## Second quantization

Let $\{ | \alpha \rangle \}$ a basis of the 1-body system. Let $n_\alpha$ the number of subsystems in the single-body state $| \alpha \rangle$, i.e. the **occupation number** of the state. The sum of the occupation numbers is equal to the number of particles $N$, i.e. $\sum_\alpha n_\alpha = N$. In the second quantization, the state of the system is represented in the occupation number state

$$| \mathbf{n} \rangle := | n_1, n_2, \dots, n_{\alpha}, \dots \rangle \ .$$
 
**Ground state.** $| \mathbf{0} \rangle = | 0_1, 0_2, \dots \rangle$.

### Fock states

**todo** *Properties of Fock states*

## Bosons and Fermions

### Bosons

#### Creation and annihilation operators

**Creation operator, $\hat{b}_i^{\dagger}$.** The notation with the dagger is justified below, as the creation operator is the adjoint of the annihilation operator $\hat{b}_i$.

$$\hat{b}_i^{\dagger} | \dots, n_i, \dots \rangle = \sqrt{n+1} | \dots, (n+1)_i, \dots \rangle \ .$$

**Annihilation operator, $\hat{b}_i$.** 

$$\begin{aligned}
  \hat{b}_i | \dots, n_i, \dots \rangle & = \sqrt{n} | \dots, (n-1)_i, \dots \rangle \ , \qquad \text{if $n_i > 0$} \\
  \hat{b}_i | \dots, n_i, \dots \rangle & = | \mathbf{0} \rangle
\end{aligned}$$

```{tip} 

Annihilation and creation operators are not Hermitian.

```

```{dropdown} Creation operator is the adjoint of the annihilation operator
:open:

The adjoint operator of an operator $\hat{a}: A \rightarrow B$ is defined as the operator $\hat{a}^\dagger: B \rightarrow A$ so that

$$\begin{aligned}
  \langle \phi | \hat{a} | \psi \rangle_B 
  & = \langle \psi | \hat{a}^\dagger | \phi \rangle_A^* = \\
  & = \langle \hat{a}^\dagger \phi | \psi \rangle_A \ .
\end{aligned}$$

for any $| \phi \rangle \in B$, $| \psi \rangle \in  A$. Thus, for the annihilation operator $\hat{b}_i$,

$$\langle \mathbf{m} | \hat{b}_i | \mathbf{n} \rangle = \langle \mathbf{n} | \left( \hat{b}_i \right)^{\dagger} | \mathbf{m} \rangle^* \ .$$

$$\begin{aligned}
  \langle \mathbf{n} | \left( \hat{b}_i \right)^{\dagger} | \mathbf{m} \rangle^*
  & = \langle \mathbf{m} | \hat{b}_i  | \mathbf{n} \rangle = && {\text{(1)}} \\
  & = \sqrt{n_i} \langle \mathbf{m} | \mathbf{n} - \mathbf{1}_i \rangle = && {\text{(2)}} \\
  & = \sqrt{n_i} \, \delta_{\mathbf{m}, \mathbf{n}-\mathbf{1}_i} = && {\text{(3)}} \\
  & = \sqrt{m_i + 1} \, \delta_{\mathbf{m}, \mathbf{n}-\mathbf{1}_i} = && {\text{(4)}} \\
  & = \sqrt{m_i + 1} \, \delta_{\mathbf{m}+\mathbf{1}_i, \mathbf{n}} = && {\text{(5)}} \\
  & = \sqrt{m_i + 1} \langle \mathbf{n} | \mathbf{m} + \mathbf{1}_i \rangle = \\
  & = \langle \mathbf{n} | \left( \sqrt{m_i + 1}  | \mathbf{m} + \mathbf{1}_i \rangle \right) = && {\text{(6)}} \\
  & = \langle \mathbf{n} | \hat{b}_i^\dagger | \mathbf{m} \rangle \ ,
\end{aligned}$$

with the Kronecker's delta acting on all the indices - just as an example, with $\mathbf{a} = (a_1, a_2)$, $\mathbf{b} = (b_1, b_2)$, it follows that $\delta_{\mathbf{a}, \mathbf{b}} = \delta_{a_1, b_1} \delta_{a_2, b_2}$ -, and (1) action of the annihilation operator, (2) orthogonality of Fock states, (3-4) properties of Kronecker's delta, (5) orthogonality of Fock states, (6) recognizing the action of the creation operator $\hat{b}_i^\dagger$ on $| \mathbf{m} \rangle$. As the result of the inner product is real, its complex conjugate is the value itself.


```


**Number operator. $\hat{n}_i = \hat{b}_i^\dagger \, \hat{b}_i$** 

$$\begin{aligned}
  \hat{n}_i | \dots, n_i, \dots \rangle
  & = \hat{b}_i^\dagger \, \hat{b}_i | \dots, n_i, \dots \rangle = \\
  & = \hat{b}_i^\dagger \, \left( \sqrt{n} | \dots, (n-1)_i, \dots \rangle \right) = \\
  & = n | \dots, n_i, \dots \rangle \ .
\end{aligned}$$

```{dropdown} Details - Normalization
:open:

$$n_i = \langle \mathbf{n} | \hat{n}_i | \mathbf{n} \rangle = \langle \mathbf{n} | \hat{b}_i^\dagger \hat{b}_i | \mathbf{n} \rangle $$

```

**Total number operator.** $\hat{n} = \sum_{i} \hat{n}_i$

**CCRs.**

$$[ \hat{b}_i, \hat{b}_j^\dagger ] = \delta_{ij} \ . $$

```{dropdown} Proof
:open:

$$[ \hat{b}_i, \hat{b}_j^\dagger ] | \mathbf{n} \rangle = \left( \sqrt{n_j+1} \sqrt{n_i^{(1)}} - \sqrt{n_i} \sqrt{n_j^{(1)}+1} \right) | \dots, (n-1)_i, \dots, (n+1)_j, \dots \rangle $$

with the $n^{(1)}_j$ the state after the application of the first operator. If $i \ne j$, then $n^{(1)}_{j} = n_j$, and thus the result is zero. If $i = j$, then $n_{i}^{(1)} = n_i + 1$, $n_j^{(1)} = n_j - 1$, and thus the result reads

$$[ \hat{b}_i, \hat{b}_i^\dagger ] | \mathbf{n} \rangle = \left( (n_i + 1) - n_i \right) | \mathbf{n} \rangle = 1 \cdot | \mathbf{n} \rangle \ .$$

and thus

$$[ \hat{b}_i, \hat{b}_j^\dagger ] | \mathbf{n} \rangle = \delta_{ij} | \mathbf{n} \rangle \ .$$

```

$$[ \hat{b}_i, \hat{b}_j ] = 0$$

$$[ \hat{b}_i^\dagger, \hat{b}_j^\dagger ] = 0$$

### Fermions

#### Creation and annihilation operators

## Quantum fields


