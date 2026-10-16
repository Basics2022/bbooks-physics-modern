(quantum-mechanics:second-quantizazion:identical)=
# Identical systems

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

(quantum-mechanics:second-quantizazion:identical:symmetrization)=
## Symmetrization and anti-symmetrization

(quantum-mechanics:second-quantizazion:identical:symmetrization:bosons)=
### Symmetric basis for bosons

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

(quantum-mechanics:second-quantizazion:identical:symmetrization:fermions)=
### Anti-symmetric basis for fermions

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


