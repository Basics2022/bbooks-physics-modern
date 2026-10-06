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

#### Symmetric basis for bosons

Let $| \alpha_1, \dots, \alpha_N \rangle$

$$| \alpha_1, \dots, \alpha_N \rangle_S := \sqrt{ \dfrac{\prod_k n_k!}{N!} } \sum_{\hat{P} \in S_N} \hat{P} | \alpha_1, \dots, \alpha_N \rangle \ ,$$

with $n_k$ the occupation number of the single-body state $k$. The factor before the summation is required for normalization of the symmetric state, as it's the square root of the inverse of the number of permutations with repetitions, see [Combinatorics: Permutations with Repetitions](https://basics2022.github.io/bbooks-math-miscellanea-hs/ch/statistics/combinatorics.html#permutazioni-con-ripetizioni).

```{prf:example} Low-dimensional example

Let a 2-particle system be represented in a Hilbert space thats the product $\mathcal{H}^{\otimes 2} = \mathcal{H}_1 \otimes \mathcal{H}_1$. If the two particles are in the same 1-body state $| a \rangle$, the state of the system is $| a , a \rangle$, equal to the symmetric state. If the two particles are in different and orthogonal states $| a \rangle$, $| b \rangle$, the symmetric representation of the state reads

$$| a, b \rangle_S = \dfrac{1}{\sqrt{2}} \left( | a , b \rangle + | b , a \rangle \right) \ .$$

This state is unit-norm, as

$$\begin{aligned}
  {}_S \langle a , b | a, b \rangle_S 
  & = \frac{1}{\sqrt{2}} \left( \langle a , b | + \langle b , a | \right) \frac{1}{\sqrt{2}} \left( | a , b \rangle + | b , a \rangle  \right) = \\
  & = \frac{1}{2} \left( \underbrace{\langle a , b | a, b \rangle}_{=\langle a | a \rangle \langle b |b \rangle = 1} + \underbrace{\langle b , a | a, b \rangle}_{\langle b | a \rangle \langle a | b \rangle = 0} + \underbrace{\langle a , b | b, a \rangle}_{=0} + \underbrace{\langle b , a | b, a \rangle}_{=1} \right) = 1 \ .
\end{aligned}$$

```

#### Anti-symmetric basis for fermions

Let $| \alpha_1, \dots, \alpha_N \rangle$

$$| \alpha_1, \dots, \alpha_N \rangle_A := \dfrac{1}{\sqrt{N!}} \left| \begin{matrix} | \alpha_1\rangle_1 & \dots & | \alpha_N \rangle_1 \\ \dots & \dots & \dots \\ | \alpha_1\rangle_N & \dots & | \alpha_N \rangle_N \end{matrix} \right| \ .$$

If two bodies were in the same state, two rows of the matrix would be equal and thus the determinant be zero. The factor before the determinant is required for normalization, as it's the square root of the inverse of the number of simple pertumations of $N$ objects without repetitions, see [Combinatorics: Permutations with Repetitions](https://basics2022.github.io/bbooks-math-miscellanea-hs/ch/statistics/combinatorics.html#permutazioni-semplici).

```{prf:example} Low-dimensional example

Let a 2-particle system be represented in a Hilbert space thats the product $\mathcal{H}^{\otimes 2} = \mathcal{H}_1 \otimes \mathcal{H}_1$. If the two particles are in the same 1-body state $| a \rangle$, the state of the system is $| a , a \rangle$,

$$| a , a \rangle_A = \dfrac{1}{\sqrt{2}} \left| \begin{matrix} | a \rangle_1 & | a \rangle_2 \\ | a \rangle_1 & | a \rangle_2 \end{matrix} \right| = 0 \ .$$

If the two particles are in different and orthogonal states $| a \rangle$, $| b \rangle$, the symmetric representation of the state reads

$$| a , b \rangle_A = \dfrac{1}{\sqrt{2}} \left| \begin{matrix} | a \rangle_1 & | b \rangle_1 \\ | a \rangle_2 & | b \rangle_2 \end{matrix} \right| = \frac{1}{\sqrt{2}} \left( | a, b \rangle - | b, a \rangle \right) \ .$$

This state is unit-norm, as

$$\begin{aligned}
  {}_A \langle a , b | a, b \rangle_A 
  & = \frac{1}{\sqrt{2}} \left( \langle a , b | - \langle b , a | \right) \frac{1}{\sqrt{2}} \left( | a , b \rangle - | b , a \rangle  \right) = \\
  & = \frac{1}{2} \left( \underbrace{\langle a , b | a, b \rangle}_{=\langle a | a \rangle \langle b |b \rangle = 1} - \underbrace{\langle b , a | a, b \rangle}_{\langle b | a \rangle \langle a | b \rangle = 0} - \underbrace{\langle a , b | b, a \rangle}_{=0} + \underbrace{\langle b , a | b, a \rangle}_{=1} \right) = 1 \ .
\end{aligned}$$


```


## Second quantization

Let $\{ | \alpha \rangle \}$ a basis of the 1-body system. Let $n_\alpha$ the number of subsystems in the single-body state $| \alpha \rangle$, i.e. the **occupation number** of the state. The sum of the occupation numbers is equal to the number of particles $N$, i.e. $\sum_\alpha n_\alpha = N$. In the second quantization, the state of the system is represented in the occupation number state

$$| \mathbf{n} \rangle := | n_1, n_2, \dots, n_{\alpha}, \dots \rangle \ .$$
 
**Ground state.** $| \mathbf{0} \rangle = | 0_1, 0_2, \dots \rangle$. By definition $\langle 0 | 0 \rangle = 1$.

### Fock states

**todo** *Properties of Fock states*

## Bosons and Fermions

### Bosons

#### Creation and annihilation operators

**Creation operator, $\hat{b}_i^{\dagger}$.** The notation with the dagger is justified below, as the creation operator is the adjoint of the annihilation operator $\hat{b}_i$.

$$\hat{b}_i^{\dagger} | \dots, n_i, \dots \rangle = \sqrt{n+1} | \dots, (n+1)_i, \dots \rangle \ .$$

A state $| n_1, n_2, \dots, n_i, \dots \rangle$ can be obtained from the vacuum equation as

$$| n_1, n_2, \dots, n_i, \dots \rangle = \dfrac{1}{\sqrt{\prod_k n_k!}} \left( \hat{b}_1^{\dagger} \right)^{n_1} \dots \left( \hat{b}_i^\dagger \right)^{n_i} | 0 \rangle \ .$$


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


**Number operator, $\hat{n}_i = \hat{b}_i^\dagger \, \hat{b}_i$.** Number operator is self-adjoint. This is consistent with postulates of quantum mechanics: physical observables are represented by self-adjoint operators.

$$\begin{aligned}
  \hat{n}_i | \dots, n_i, \dots \rangle
  & = \hat{b}_i^\dagger \, \hat{b}_i | \dots, n_i, \dots \rangle = \\
  & = \hat{b}_i^\dagger \, \left( \sqrt{n} | \dots, (n-1)_i, \dots \rangle \right) = \\
  & = n | \dots, n_i, \dots \rangle \ .
\end{aligned}$$

<!--
```{dropdown} Details - Multiplicative factor of creation and annihilation operators
:open:

As the

$$n_i = \langle \mathbf{n} | \hat{n}_i | \mathbf{n} \rangle = \langle \mathbf{n} | \hat{b}_i^\dagger \hat{b}_i | \mathbf{n} \rangle $$

```
-->

**Total number operator.** $\hat{n} = \sum_{i} \hat{n}_i$

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

### Fermions

#### Creation and annihilation operators

## Quantum fields

Let $\{ | \nu_k \rangle \}_k$ a basis of quantum states of the 1-body system. The 1-body wave function can be represented as a linear combination of the vectors of this basis,

$$| \psi \rangle = \sum_k | \nu_k \rangle c_k = \sum_k | \nu_k \rangle \langle \nu_k | \psi \rangle \ ,$$

and in position representation

$$\psi(\mathbf{r},t) = \langle \mathbf{r} | \psi \rangle = \sum_k \nu_k(\mathbf{r}) c_k(t) \ .$$

### Field creation operator

#### One-particle system

**Action of $\hat{\Psi}^\dagger(\mathbf{r})$ on the vacuum state.** The action of the operator $\hat{\Psi}^\dagger(\mathbf{r})$ on the vacuum places a particle in the state $| \mathbf{r} \rangle$, i.e.

$$| \mathbf{r} \rangle = \hat{\Psi}^\dagger(\mathbf{r}) | 0 \rangle \ .$$ (eq:second-quantization:field:r-1)

````{dropdown} Discrete basis
:open:

The state $| \mathbf{r} \rangle$ can be written as a linear combination of the elements of a basis. For a **discrete basis** $\{ | \nu_k \rangle \}_k$,

$$| \mathbf{r} \rangle = \sum_k | \nu_k \rangle \langle \nu_k | \mathbf{r} \rangle \ .$$

A vector of the basis of the 1-body system $| \nu_k \rangle$ can be built with the creation operator acting on the ground state, $| \nu_k \rangle = \hat{a}^\dagger_{\nu_k} | 0 \rangle$, and thus

$$| \mathbf{r} \rangle = \sum_k \langle \nu_k | \mathbf{r} \rangle \, \hat{a}_{\nu_k}^\dagger | 0 \rangle = \sum_k \nu_k^*(\mathbf{r}) \, \hat{a}_{\nu_k}^\dagger | 0 \rangle \ .$$ (eq:second-quantization:field:r-2)

Comparision of {eq}`eq:second-quantization:field:r-1` and {eq}`eq:second-quantization:field:r-2` gives the expression of the field creation operator

$$\hat{\Psi}^\dagger(\mathbf{r}) = \sum_k \nu_k^*(\mathbf{r}) \hat{a}_{\nu_k}^\dagger \ .$$

```{dropdown} Equivalent expression of the single-body wave function
:open:

The single-body wave function in position representation reads

$$\begin{aligned}
  \psi(\mathbf{r}) 
  & = \langle \mathbf{r} | \psi \rangle = \\
  & = \langle 0 | \hat{\Psi}(\mathbf{r}) | \psi \rangle = \\
  & = \sum_k \sum_j \nu_j(\mathbf{r}) \underbrace{\langle 0 | \hat{a}_{\nu_j} | \nu_k \rangle}_{=\delta_{jk} \langle 0 | 0 \rangle = \delta_{jk}} \langle \nu_k | \psi \rangle = \\
  & = \sum_k \nu_k(\mathbf{r}) \langle \nu_k | \psi \rangle = \\ 
  & = \sum_k \langle \mathbf{r} | \nu_k \rangle \langle \nu_k | \psi \rangle \ .
\end{aligned}$$

```

````

````{dropdown} Continuous basis
:open:



````

#### Two-particle system

##### Bosons

Position state can be expressed either with creation operators

$$| \mathbf{r}_1, \mathbf{r}_2 \rangle = \hat{\Psi}^\dagger(\mathbf{r}_2) \hat{\Psi}^\dagger(\mathbf{r}_1) | 0 \rangle \ ,$$

and with as a linear combination of states built with the 1-body basis $\{ \nu_k \}$,

$$| \mathbf{r}_1, \mathbf{r}_2 \rangle = \sum_{i_1 \le i_2} | \nu_{i_1}, \nu_{i_2} \rangle \langle \nu_{i_1}, \nu_{i_2} | \mathbf{r}_1, \mathbf{r}_2 \rangle \ .$$


**Identity operator.**

$$\hat{\mathbf{1}}^{(2)} = \sum_{i_1 \le i_2} | \nu_{i_1}, \nu_{i_2} \rangle \langle \nu_{i_1}, \nu_{i_2} | \ .$$ 

```{dropdown} Proof
:open:

$$\begin{aligned}
  \hat{\mathbf{1}}^{(2)} | \Psi \rangle 
  & = \hat{\mathbf{1}}^{(2)} \sum_{k_1 \le k_2} c_{k_1, k_2} | \nu_{k_1} \nu_{k_2} \rangle = \\
  & = \left( \sum_{i_1 \le i_2} | \nu_{i_1}, \nu_{i_2} \rangle \langle \nu_{i_1}, \nu_{i_2} | \right) \sum_{k_1 \le k_2} c_{k_1, k_2} | \nu_{k_1} , \nu_{k_2} \rangle = \\
  & = \sum_{i_1 \le i_2} \sum_{k_1 \le k_2} | \nu_{i_1}, \nu_{i_2} \rangle \delta_{i_1 k_1} \delta_{i_2 k_2} c_{k_1,k_2} = \\
  & = \sum_{i_1 \le i_2} | \nu_{i_1}, \nu_{i_2} \rangle c_{i_1,i_2} \ .
\end{aligned}$$


```

**Bosons.** The state $| \nu_{i_1}, \nu_{i_2} \rangle$ can be built with creation operators from the vacuum state. If $i_1 \ne i_2$, then

$$| \nu_{i_1}, \nu_{i_2} \rangle = \hat{a}^\dagger_{\nu_{i_1}} \hat{a}^\dagger_{\nu_{i_2}} | 0 \rangle \qquad '=' \qquad | \dots \underbrace{1}_{i_1} \dots \underbrace{1}_{i_2} \dots \rangle \ . $$

If $i_2 = i_1$,

$$| \nu_{i_1}, \nu_{i_1} \rangle = \dfrac{1}{\sqrt{2}} \hat{a}^\dagger_{\nu_{i_1}} \hat{a}^\dagger_{\nu_{i_1}} | 0 \rangle \qquad '=' \qquad | \dots \underbrace{2}_{i_1} \dots \rangle \ , $$

i.e. in general $| \nu_{i_1}, \nu_{i_2} \rangle = f_{i_1 i_2} \hat{a}^\dagger_{i_1} \hat{a}^\dagger_{i_2} | 0 \rangle$, with $f_{i_1 i_2} = \frac{1}{\sqrt{1 + \delta_{i_1 i_2}}}$. Inserting this expression into the formula for $| \mathbf{r}_1, \mathbf{r}_2 \rangle$, the expression for the creator operators follows

$$\begin{aligned}
  | \mathbf{r}_1, \mathbf{r}_2 \rangle
  & = \hat{\Psi}^\dagger(\mathbf{r}_2) \hat{\Psi}^{\dagger}(\mathbf{r}_1) | 0 \rangle = \\
  & = \sum_{i_1 \le i_2} f_{i_1 i_2} \nu_{i_1}^*(\mathbf{r}_1) \nu_{i_2}^*(\mathbf{r}_2) \hat{a}_{\nu_{i_1}}^\dagger \hat{a}_{\nu_{i_2}}^\dagger | 0 \rangle \ ,
\end{aligned}$$

so that

$$\begin{aligned}
  \hat{\Psi}^\dagger(\mathbf{r}_2) \hat{\Psi}^{\dagger}(\mathbf{r}_1) 
  & = \sum_{i_1 \le i_2} f_{i_1 i_2} \nu_{i_1}^*(\mathbf{r}_1) \nu_{i_2}^*(\mathbf{r}_2) \hat{a}_{\nu_{i_1}}^\dagger \hat{a}_{\nu_{i_2}}^\dagger
\end{aligned}$$

The state function of the system in position representation is

$$\begin{aligned}
  \Psi(\mathbf{r}_1, \mathbf{r}_2) 
  & = \langle \mathbf{r}_1 , \mathbf{r}_2 | \Psi \rangle = \\
  & = \langle \mathbf{r}_1 , \mathbf{r}_2 | \sum_{i_1 \le i_2} | \nu_{i_1}, \nu_{i_2} \rangle \langle \nu_{i_1}, \nu_{i_2} | \Psi \rangle = \\
  & = \sum_{i_1 \le i_2} \nu_{i_1}(\mathbf{r}_1) \, \nu_{i_2}(\mathbf{r}_2) \langle \nu_{i_1}, \nu_{i_2} | \Psi \rangle = \\
  & = \langle 0 | \hat{\Psi}(\mathbf{r}_2) \hat{\Psi}(\mathbf{r}_1) | \sum_{i_1 \le i_2} | \nu_{i_1}, \nu_{i_2} \rangle \langle \nu_{i_1}, \nu_{i_2} | \Psi \rangle = \\
\end{aligned}$$

**Fermions.**

#### Many-body systems


##### Bosons

**Identity operator.**

* Summing over ordered/independent configurations ("occupation representation")

   $$\hat{\mathbf{1}}^{(N)} = \sum_{i_1 \le i_2 \le \dots \le i_N} | \nu_{i_1}, \nu_{i_2}, \dots, \nu_{i_N} \rangle \langle \nu_{i_1}, \nu_{i_2}, \dots, \nu_{i_N} |$$

* Summing over all the indices ("creation operator represetnation")
   
   $$\hat{\mathbf{1}}^{(N)} = \frac{1}{N!} \sum_{i_1, i_2, \dots, i_N} \left( c_{\nu_{i_1}}^{\dagger} \dots c_{\nu_{i_N}}^{\dagger} | 0 \rangle \right) \left( \langle 0 | c_{\nu_{i_1}} \dots c_{\nu_{i_N}} \right)$$


##### Fermions

**Identity operator.**

* Summing over ordered/independent configurations ("occupation representation")

   $$\hat{\mathbf{1}}^{(N)} = \sum_{i_1 < i_2 < \dots < i_N} | \nu_{i_1}, \nu_{i_2}, \dots, \nu_{i_N} \rangle \langle \nu_{i_1}, \nu_{i_2}, \dots, \nu_{i_N} |$$

* Summing over all the indices ("creation operator represetnation")
   
   $$\hat{\mathbf{1}}^{(N)} = \frac{1}{N!} \sum_{i_1, i_2, \dots, i_N} \left( c_{\nu_{i_1}}^{\dagger} \dots c_{\nu_{i_N}}^{\dagger} | 0 \rangle \right) \left( \langle 0 | c_{\nu_{i_1}} \dots c_{\nu_{i_N}} \right)$$

