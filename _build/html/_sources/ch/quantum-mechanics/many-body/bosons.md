(quantum-mechanics:second-quantizazion:bosons)=
# Second quantization. Bosons

The state of a many-body bosonic system is symmetric under the echange of 2 particles. This condition is represented in the [CCRs](quantum-mechanics:second-quantizazion:bosons:ccr).

<!--
$$| \Psi \rangle ( \dots, i, \dots, j, \dots ) = | \Psi \rangle (\dots , j , \dots , i , \dots ) \ .$$

[Canonical commutation relations](quantum-mechanics:second-quantizazion:bosons:ccr) for the [creation and annihilation operators](quantum-mechanics:second-quantizazion:bosons:creation-annihilation) represent this symmetry. As an example, the CCRs

$$[ \hat{b}_i, \hat{b}_j ] = [ \hat{b}^\dagger_i, \hat{b}^\dagger_j ] = 0 \ ,$$

imply that the succcessive annihilation (or the creation) of two particles is independent from the order of the operation, $\hat{b}_i \hat{b}_j = \hat{b}_j \hat{b}_i$. The CCR

$$[ \hat{b}_i, \hat{b}^\dagger_j ] = \delta_{ij} \ ,$$

implies that the creation and annihilation of 2 particles in different states $i \ne j$, i.e. $\hat{b}_i \hat{b}_j^\dagger = \hat{b}_j^\dagger \hat{b}_i$, 

-->

(quantum-mechanics:second-quantizazion:bosons:creation-annihilation)=
## Creation and annihilation operators

**Creation operator, $\hat{b}_i^{\dagger}$.** The notation with the dagger is justified below, as the creation operator is the adjoint of the annihilation operator $\hat{b}_i$.

$$\hat{b}_i^{\dagger} | \dots, n_i, \dots \rangle = \sqrt{n+1} | \dots, (n+1)_i, \dots \rangle \ .$$

A state $| \mathbf{n} \rangle = | n_1, n_2, \dots, n_i, \dots \rangle$ can be obtained from the vacuum equation as

$$| \mathbf{n} \rangle = | n_1, n_2, \dots, n_i, \dots \rangle = \dfrac{1}{\sqrt{\prod_k n_k!}} \left( \hat{b}_1^{\dagger} \right)^{n_1} \dots \left( \hat{b}_i^\dagger \right)^{n_i} \dots | \mathbf{0} \rangle \ .$$


**Annihilation operator, $\hat{b}_i$.** 

$$\begin{aligned}
  \hat{b}_i | \dots, n_i, \dots \rangle & = \sqrt{n} | \dots, (n-1)_i, \dots \rangle \ , \qquad \text{if $n_i > 0$} \\
  \hat{b}_i | \dots, 0_i, \dots \rangle & = 0 \ .
\end{aligned}$$

```{tip} 

Annihilation and creation operators are not Hermitian.

```

```{dropdown} Creation operator is the adjoint of the annihilation operator

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


**Number operator, $\hat{n}_i = \hat{b}_i^\dagger \, \hat{b}_i$.** Number operator is self-adjoint. This is consistent with postulates of quantum mechanics: physical observables are represented by self-adjoint operators.

$$\begin{aligned}
  \hat{n}_i | \mathbf{n} \rangle
  & = \hat{n}_i | \dots, n_i, \dots \rangle = \\
  & = \hat{b}_i^\dagger \, \hat{b}_i | \dots, n_i, \dots \rangle = \\
  & = \hat{b}_i^\dagger \, \left( \sqrt{n} | \dots, (n-1)_i, \dots \rangle \right) = \\
  & = n_i | \dots, n_i, \dots \rangle = \\
  & = n_i | \mathbf{n} \rangle \ .
\end{aligned}$$

<!--
```{dropdown} Details - Multiplicative factor of creation and annihilation operators
:open:

As the

$$n_i = \langle \mathbf{n} | \hat{n}_i | \mathbf{n} \rangle = \langle \mathbf{n} | \hat{b}_i^\dagger \hat{b}_i | \mathbf{n} \rangle $$

```
-->


(quantum-mechanics:second-quantizazion:bosons:number)=
## Number operator

**Total number operator.** $\hat{n} = \sum_{i} \hat{n}_i$


(quantum-mechanics:second-quantizazion:bosons:ccr)=
## Canonical commutation relations

**CCRs.**

$$[ \hat{b}_i, \hat{b}_j^\dagger ] = \delta_{ij} \ . $$

```{dropdown} Proof

$$[ \hat{b}_i, \hat{b}_j^\dagger ] | \mathbf{n} \rangle = \left( \sqrt{n_j+1} \sqrt{n_i^{(1)}} - \sqrt{n_i} \sqrt{n_j^{(1)}+1} \right) | \dots, (n-1)_i, \dots, (n+1)_j, \dots \rangle $$

with the $n^{(1)}_j$ the state after the application of the first operator. If $i \ne j$, then $n^{(1)}_{j} = n_j$, and thus the result is zero. If $i = j$, then $n_{i}^{(1)} = n_i + 1$, $n_j^{(1)} = n_j - 1$, and thus the result reads

$$[ \hat{b}_i, \hat{b}_i^\dagger ] | \mathbf{n} \rangle = \left( (n_i + 1) - n_i \right) | \mathbf{n} \rangle = 1 \cdot | \mathbf{n} \rangle \ .$$

and thus

$$[ \hat{b}_i, \hat{b}_j^\dagger ] | \mathbf{n} \rangle = \delta_{ij} | \mathbf{n} \rangle \ .$$

```

$$[ \hat{b}_i, \hat{b}_j ] = 0$$

$$[ \hat{b}_i^\dagger, \hat{b}_j^\dagger ] = 0$$

