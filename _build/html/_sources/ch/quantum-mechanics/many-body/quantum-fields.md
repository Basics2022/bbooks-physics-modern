(quantum-mechanics:second-quantizazion:quantum-fields)=
# Quantum fields

In this section, creation and annihilation operators in continuous basis (like space or momentum) are introduced, in terms of creation/annihilation operators in a given (and discrete?) basis $\{ \nu_a \}_a$ 

<!--
Let $\{ | \nu_k \rangle \}_k$ a basis of quantum states of the 1-body system. The 1-body wave function can be represented as a linear combination of the vectors of this basis,

$$| \psi \rangle = \sum_k | \nu_k \rangle c_k = \sum_k | \nu_k \rangle \langle \nu_k | \psi \rangle \ ,$$

and in position representation

$$\psi(\mathbf{r},t) = \langle \mathbf{r} | \psi \rangle = \sum_k \nu_k(\mathbf{r}) c_k(t) \ .$$
-->

## Field creation and annihilation operators

Creation and annihilation operators in space basis can be written using the basis $\{ \nu_a \}$ as

$$\Psi^\dagger(\mathbf{r}) = \sum_a \nu_a^*(\mathbf{r}) \hat{a}^\dagger_{\nu_a}$$ (eq:qft:fields:creation)

$$\Psi        (\mathbf{r}) = \sum_a \nu_a  (\mathbf{r}) \hat{a}_{\nu_a}        $$ (eq:qft:fields:annihilation)

Creation operator $\Psi^\dagger(\mathbf{r})$ *creates a particle* in state $| \mathbf{r} \rangle$, while annihilation operator $\Psi(\mathbf{r})$ *destroys a particle* in state $| \mathbf{r} \rangle$.

The inverse relations hold

$$\begin{aligned}
  \hat{a}^\dagger_{\nu_a} 
  & = \int_{\mathbf{r}} \nu_a(\mathbf{r}) \Psi^\dagger(\mathbf{r}) \, d \mathbf{r} \ .
\end{aligned}$$ (eq:qft:fields:creation:inverse)

$$\begin{aligned}
  \hat{a}_{\nu_a} 
  & = \int_{\mathbf{r}} \nu_a^*(\mathbf{r}) \Psi(\mathbf{r}) \, d \mathbf{r} \ .
\end{aligned}$$ (eq:qft:fields:annihilation:inverse)


```{dropdown} Details. Inverse relations

$$\begin{aligned}
  \hat{a}^\dagger_{\nu_a} 
  & = \sum_b \hat{a}_{\nu_b}^\dagger \langle \nu_b | \nu_a \rangle =  \\
  & = \sum_b \hat{a}_{\nu_b}^\dagger \langle \nu_b | \int_{\mathbf{r}} | \mathbf{r} \rangle \langle \mathbf{r} | \, d \mathbf{r} \, | \nu_a \rangle =  \\
  & = \int_{\mathbf{r}} \nu_a(\mathbf{r}) \sum_b \nu^*_b(\mathbf{r}) \hat{a}_{\nu_b}^\dagger \, d \mathbf{r} = \\
  & = \int_{\mathbf{r}} \nu_a(\mathbf{r}) \Psi^\dagger(\mathbf{r}) \, d \mathbf{r} \ .
\end{aligned}$$

$$\begin{aligned}
  \hat{a}_{\nu_a} 
  & = \sum_b \hat{a}_{\nu_b} \langle \nu_a | \nu_b \rangle =  \\
  & = \sum_b \hat{a}_{\nu_b} \langle \nu_a | \int_{\mathbf{r}} | \mathbf{r} \rangle \langle \mathbf{r} | \, d \mathbf{r} \, | \nu_b \rangle =  \\
  & = \int_{\mathbf{r}} \nu_a^*(\mathbf{r}) \sum_b \nu_b(\mathbf{r}) \hat{a}_{\nu_b} \, d \mathbf{r} = \\
  & = \int_{\mathbf{r}} \nu_a^*(\mathbf{r}) \Psi(\mathbf{r}) \, d \mathbf{r} \ .
\end{aligned}$$

```


**todo** *Need to distinguish between bosons and fermions? Or one can just use the proper set of creation/annihilation operators, without any other major change in the formulas* 

### CCR




### One-particle system

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

### Two-particle system

#### Bosons

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

### Many-body systems


#### Bosons

**Identity operator.**

* Summing over ordered/independent configurations ("occupation representation")

   $$\hat{\mathbf{1}}^{(N)} = \sum_{i_1 \le i_2 \le \dots \le i_N} | \nu_{i_1}, \nu_{i_2}, \dots, \nu_{i_N} \rangle \langle \nu_{i_1}, \nu_{i_2}, \dots, \nu_{i_N} |$$

* Summing over all the indices ("creation operator represetnation")
   
   $$\hat{\mathbf{1}}^{(N)} = \frac{1}{N!} \sum_{i_1, i_2, \dots, i_N} \left( c_{\nu_{i_1}}^{\dagger} \dots c_{\nu_{i_N}}^{\dagger} | 0 \rangle \right) \left( \langle 0 | c_{\nu_{i_1}} \dots c_{\nu_{i_N}} \right)$$


#### Fermions

**Identity operator.**

* Summing over ordered/independent configurations ("occupation representation")

   $$\hat{\mathbf{1}}^{(N)} = \sum_{i_1 < i_2 < \dots < i_N} | \nu_{i_1}, \nu_{i_2}, \dots, \nu_{i_N} \rangle \langle \nu_{i_1}, \nu_{i_2}, \dots, \nu_{i_N} |$$

* Summing over all the indices ("creation operator represetnation")
   
   $$\hat{\mathbf{1}}^{(N)} = \frac{1}{N!} \sum_{i_1, i_2, \dots, i_N} \left( c_{\nu_{i_1}}^{\dagger} \dots c_{\nu_{i_N}}^{\dagger} | 0 \rangle \right) \left( \langle 0 | c_{\nu_{i_1}} \dots c_{\nu_{i_N}} \right)$$

