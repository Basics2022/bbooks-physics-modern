(quantum-mechanics:second-quantizazion:operators)=
# Operators in QFT

One-body operators act on individual particles. Let $\hat{o}$ the operator acting on the single-particle wave function $| \psi \rangle \in \mathcal{H}$, and $o_{ab} = \langle \phi_a | \hat{o} | \phi_b \rangle$ its matrix components w.r.t. the vectors of the basis of $\{ \psi_a \}_a$ of $\mathcal{H}$, or in **position representation**

$$
o_{ab} = \langle \psi_a | \hat{o} | \psi_b \rangle = \langle \psi_a |\int_{\mathbf{r}} | \mathbf{r} \rangle \langle \mathbf{r} | \hat{o} | \psi_b \rangle \, d \mathbf{r} = \int_{\mathbf{r}} \psi_a^*(\mathbf{r}) \, o \psi_b(\mathbf{r}) \, d \mathbf{r} \ ,
$$

being $o$ the linear (tipically differential) operator in space representation, and $o \psi_b(\mathbf{r})$ its action of $| \psi_b \rangle$ in space representation. Just as an example, the space representation of the action of the $x$-component of the momentum operator $\hat{p}_x$ on vector $| \psi_b \rangle$ reads

$$\langle \mathbf{r} | \hat{p}_x | \psi_b \rangle = -i \hbar \partial_x \langle \mathbf{r} | \psi_b \rangle = - i \hbar \partial_x \psi_b(\mathbf{r}) \ ,$$

so that the linear differential operator in space representation acting on the space representation of the wave vector reads $p_x = - i \hbar \partial_x$, and $p_x \psi_b(\mathbf{r}) = - i \hbar \partial_x \psi_b(\mathbf{r})$.


(quantum-mechanics:second-quantizazion:operators:one-body)=
## One-body operators

**First quantization.** The operator $\hat{O}_1$ is the sum of the 1-particle operators $\hat{o}$, each one acting on the corresponding particle,

$$\hat{O}_1 = \sum_{i=1}^{N} \hat{o}(q^i, p_i) \ .$$ (eq:qft:operator:one-body:first-quantization)

Let the state of the system $| \Psi \rangle$ be represented in the basis $\{ | \psi_{i_1}, \psi_{i_2}, \dots \rangle \}$, with the vectors $|\psi_i \rangle$ being the eigenvectors of the operator $\hat{o}$, with eigenvalues $o_k$. Let the system be in state $| \Psi \rangle = | \psi_{i_1}, \psi_{i_2}, \dots \rangle$. Then the action of the one-body operator on the state of the system reads

$$\hat{O}_1 | \Psi \rangle = \sum_{k=1}^{N} \hat{o}^{(k)} | \Psi \rangle = \sum_{k=1}^N o_{i_k} | \Psi \rangle \ ,$$ (eq:qft:operator:one-body:first-quantization:eig)

i.e. the state $| \psi_{i_1}, \psi_{i_2}, \dots \rangle$ is an eigenstate of the one-body operator $\hat{O}_1$, with eigenvalue $\sum_{k=1}^{N} o_{i_k}$.

```{dropdown} Examples for a 2-particle system.

Let the state a two-particle system be represented by the wave vector $| \Psi \rangle = | \psi_1, \psi_2 \rangle$. Its space representation reads

$$\psi(\mathbf{r}_1, \mathbf{r}_2) = \langle \mathbf{r}_1, \mathbf{r}_2 | \Psi \rangle = \psi_1(\mathbf{r}_1) \psi_2(\mathbf{r}_2) \ .$$

**todo** *Discuss statistical independence...*

Some examples of one-body operators acting on a two-particle system are:

* **Momentum** (1-dimensional domain), $\hat{P}_x = \hat{p}_x^{(1)} + \hat{p}_x^{(2)}$, or $ = \hat{p}_x \otimes \hat{1} + \hat{1} \otimes \hat{p}_x$

  $$\begin{aligned}
    \hat{P} | \Psi \rangle
    & = \hat{P} | \Psi \rangle     
      = | \hat{p} \psi_1, \psi_2 \rangle + | \psi_1, \hat{p}\psi_2 \rangle \ ,
  \end{aligned}$$

  or in space representation

  $$\langle \mathbf{r}_1, \mathbf{r}_2 | \hat{P} | \Psi \rangle = -i \hbar \partial_{x_1} \psi_1(\mathbf{r}_1) \psi_2(\mathbf{r}_2) - i \hbar \psi_1(\mathbf{r}_1) \partial_{x_2} \psi_2(\mathbf{r}_2) \ .$$

* **Kinetic energy**, $\hat{T} = \hat{t}^{(1)} + \hat{t}^{(2)}$

   $$\dots$$

* **External potential energy**, $\hat{V} = \hat{v}^{(1)} + \hat{v}^{(2)}$
   
   $$\dots$$

* **Total energy** (kinetic + external potential energy), $\hat{H} = \hat{h}^{(1)} + \hat{h}^{(2)}$. 
  If the state of the system $| \psi_1, \psi_2 \rangle$ is in $| \psi_a, \psi_b \rangle$, with $| \psi_a \rangle$ a stationary state of the 1-particle system, with energy $E_a$, then it follows that the action of the total energy operator is

  $$\begin{aligned}
    \hat{H} | \Psi \rangle
    & = \left( \hat{h}^{(1)} + \hat{h}^{(2)} \right) | \psi_1, \psi_2 \rangle = \\
    & = \left( \hat{h}^{(1)} + \hat{h}^{(2)} \right) | \psi_1, \psi_2 \rangle = \\
    & = \left( \hat{h}^{(1)} + \hat{h}^{(2)} \right) | \psi_a, \psi_b \rangle = \\
    & = | \hat{h} \psi_a, \psi_b \rangle +  | \psi_a, \hat{h} \psi_b \rangle = \\
    & = \left( E_a + E_b \right) | \psi_a, \psi_b \rangle = \left( E_a + E_b \right) | \Psi \rangle \ .
  \end{aligned}$$

```

**Second quantization.**

$$\begin{aligned}
  \hat{O}_1
  & = \sum_{\alpha, \beta} o_{\alpha \beta} \hat{a}_{\alpha}^\dagger \hat{a}_\beta \ , 
\end{aligned}$$ (eq:qft:operator:one-body:second-quantization)

with $\hat{a}^\dagger_{\alpha}$, $\hat{a}_{\beta}$ the creation and annihilation operators for one particle in states $| \psi_a \rangle$, and $| \psi_b \rangle$ respectively, and $o_{\alpha \beta} = \langle \psi_a | \hat{o} | \psi_b \rangle$, with $\{ | \psi_a \rangle \}$ vectors of a basis of the 1-particle space. The summations in $\alpha$, and $\beta$ here occur on all the 1-particle eigenstates.

If the operator is built using the 1-particle eigenstates of the operator $\hat{o}$, then the matrix $o_{\alpha \beta}$ is diagonal, and the operator can be written as

$$\hat{O}_1 = \sum_{\alpha} o_{\alpha} \hat{a}_{\alpha}^\dagger \hat{a}_{\alpha}  = \sum_{\alpha} o_{\alpha} \hat{n}_{\alpha} \ ,$$

with $o_{\alpha}$ the eigenvalues of the 1-particle operator $\hat{o}$ and $\hat{n}_{\alpha} = \hat{a}^{\dagger}_{\alpha} \hat{a}_{\alpha}$ the number operator of the state $\alpha$. The action of the operator $\hat{O}_1$ on the state of the system, represented in the occupation number basis $| \Psi \rangle = | n_{o_1}, n_{o_2}, \dots \rangle$ built on the 1-particle eigenstates of the operator $\hat{o}$,

$$\begin{aligned}
  \hat{O}_1 | \Psi \rangle 
  & = \left( \sum_{\alpha} o_{\alpha \beta} \hat{a}_{\alpha}^\dagger \hat{a}_{\alpha} \right) | \Psi \rangle 
    = \left( \sum_{\alpha} o_{\alpha \beta} \hat{n}_{\alpha} \right) | \Psi \rangle \ .
\end{aligned}$$

If the system is in an eigenstate of the operator $\hat{O}$, represented by only one vector $| \Psi \rangle = | \mathbf{n} \rangle = | n_{1}, n_{2}, \dots \rangle$, then

$$\begin{aligned}
  \hat{O}_1 | \mathbf{n} \rangle 
  & = \left( \sum_{\alpha} o_{\alpha} \hat{n}_{\alpha} \right) | \mathbf{n} \rangle = \\
  & = \left( \sum_{\alpha} o_{\alpha} \hat{n}_{\alpha} \right) | \dots n_\alpha \dots \rangle = \\
  & = \left( \sum_{\alpha} o_{\alpha} \, {n}_{\alpha} \right) | \dots n_\alpha \dots \rangle = \\
  & = \underbrace{\left( \sum_{\alpha} {n}_{\alpha} o_{\alpha} \right)}_{=:o_{\mathbf{n}}} | \mathbf{n} \rangle \ ,
\end{aligned}$$ (eq:qft:operator:one-body:second-quantization:eig)

i.e. the state $| \mathbf{n} \rangle$ of the occupation numbers of the eigenstates of $\hat{o}$ is an eigenvector of the operator $\hat{O}$ with eigenvalue $o_{\mathbf{n}} := \sum_{\alpha} o_{\alpha} n_{\alpha}$.

```{admonition} Operators in first and second quantization

The action of the operator $\hat{O}_1$ can be expressed using second quantization formalism with {eq}`eq:qft:operator:one-body:second-quantization:eig` or using the analogous first quantization formalism with {eq}`eq:qft:operator:one-body:first-quantization:eig`: while summation in second quantization runs over the eigenstates, the summation runs over "particles" in first quantization. These two different points of view provide the same result, with the eigenvalue of the eigenstate $| \mathbf{n} \rangle = | \psi_{i_1}, \psi_{i_2}, \dots \rangle$ (with $n_1$ of the $\psi_{i_k}$ in eigenstate $\psi_{1}$,...) equal to 

$$o_{\mathbf{n}} = \sum_{\alpha} n_a o_a = \sum_{k} o_{i_k} \ .$$

This analogy also provides a justification for the expressions {eq}`eq:qft:operator:one-body:first-quantization` and {eq}`eq:qft:operator:one-body:second-quantization` of the one-body operator $\hat{O}_1$.

```

### Space representation

Using the relations {eq}`eq:qft:fields:creation:inverse` and {eq}`eq:qft:fields:annihilation:inverse`,

$$\begin{aligned}
  \hat{a}^\dagger_{a} 
  & = \int_{\mathbf{r}} \psi_a(\mathbf{r}) \Psi^\dagger(\mathbf{r}) \, d \mathbf{r} \ .
\end{aligned}$$

$$\begin{aligned}
  \hat{a}_{a} 
  & = \int_{\mathbf{r}} \psi_a^*(\mathbf{r}) \Psi(\mathbf{r}) \, d \mathbf{r} \ .
\end{aligned}$$

it's possible to find another equivalent expression of the expression {eq}`eq:qft:operator:one-body:second-quantization` of the $\hat{O}_1$ operator,

**todo** *Review these steps. There's too much free-style in swapping operators...*

$$\begin{aligned}
\hat{O}_1
& = \sum_{\alpha, \beta} o_{\alpha \beta} \hat{a}_{\alpha}^{\dagger} \hat{a}_{\beta} = \\
& = \sum_{\alpha, \beta} o_{\alpha \beta} \left( \int_{\mathbf{r}} \psi_a(\mathbf{r}) \Psi^\dagger(\mathbf{r}) \, d \mathbf{r} \right) \left( \int_{\mathbf{r}'} \psi_\beta^*(\mathbf{r}') \Psi(\mathbf{r}') \, d \mathbf{r}' \right) = \\
& = \sum_{\alpha, \beta}  \int_{\mathbf{r}} \int_{\mathbf{r}'} o_{\alpha \beta}  \psi_a(\mathbf{r}) \Psi^\dagger(\mathbf{r})  \psi_\beta^*(\mathbf{r}') \Psi(\mathbf{r}') \, d \mathbf{r} \, d \mathbf{r}' = \\
& = \sum_{\alpha, \beta}  \int_{\mathbf{r}} \int_{\mathbf{r}'}  \psi_a(\mathbf{r}) o_{\alpha \beta} \psi_\beta^*(\mathbf{r}')  \Psi^\dagger(\mathbf{r}) \Psi(\mathbf{r}') \, d \mathbf{r} \, d \mathbf{r}' = && (1) \\
& = \int_{\mathbf{r}} \int_{\mathbf{r}'} \sum_{\alpha, \beta}  \langle \mathbf{r} | \psi_a \rangle \langle \psi_a | \hat{o} | \psi_\beta \rangle \langle \psi_\beta | \mathbf{r}' \rangle  \Psi^\dagger(\mathbf{r}) \Psi(\mathbf{r}') \, d \mathbf{r} \, d \mathbf{r}' = \\
& = \int_{\mathbf{r}} \int_{\mathbf{r}'} \sum_{\alpha, \beta}  \langle \mathbf{r} | \hat{o} | \mathbf{r}' \rangle  \Psi^\dagger(\mathbf{r}) \Psi(\mathbf{r}') \, d \mathbf{r} \, d \mathbf{r}' = && (2) \\
& = \int_{\mathbf{r}} \int_{\mathbf{r}'} \sum_{\alpha, \beta}  o_{\mathbf{r}; \partial_{\mathbf{r}}}  \underbrace{\langle \mathbf{r} | \mathbf{r}' \rangle}_{\delta(\mathbf{r}-\mathbf{r}')}  \Psi^\dagger(\mathbf{r}) \Psi(\mathbf{r}') \, d \mathbf{r} \, d \mathbf{r}' = \\
& = \int_{\mathbf{r}} \sum_{\alpha, \beta}  \Psi^\dagger(\mathbf{r}) o_{\mathbf{r}; \partial_{\mathbf{r}}}  \Psi(\mathbf{r}') \, d \mathbf{r} \ ,
\end{aligned}$$

```{prf:example} Kinetic energy

$$\begin{aligned}
 \hat{T}
 & = \int_{\mathbf{r}} \hat{\Psi}^\dagger(\mathbf{r}) \langle \mathbf{r} | \hat{t} \hat{\Psi}(\mathbf{r}) = \\
 & = \dots = \\
 & = \int_{\mathbf{r}} \hat{\Psi}^\dagger(\mathbf{r}) \left( - \frac{\hbar^2}{2m} \nabla^2 \right) \hat{\Psi}(\mathbf{r}) = \\
 & = \int_{\mathbf{r}} \frac{\hbar^2}{2m} \nabla \hat{\Psi}^\dagger(\mathbf{r}) \cdot \nabla \hat{\Psi}(\mathbf{r}) \ ,
\end{aligned}$$

with integration by parts and vanishing operators for $|\mathbf{r}| \rightarrow + \infty$.


```



(quantum-mechanics:second-quantizazion:operators:two-body)=
## Two-body operators

