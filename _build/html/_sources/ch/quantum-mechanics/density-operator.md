(quantum-mechanics:density-operator)=
# Density Operator

Let's start from an example of the preparation of a system of subsystems in pure states $| \psi_i \rangle$, with probability $p_i$, $\sum_i p_i = 1$. Let $M$ an observable, with the corresponding Hermitian operator $\hat{M}$ with discrete values $m_\mu$ and corresponding states $| m_{\mu} \rangle$.

Now, the probability of measuring the value $m_{\mu}$ for a system in state $| \psi_i \rangle$, i.e. the conditional probability $p(m=m_{\mu} | | \psi \rangle = | \psi_i \rangle)$ reads

$$p(m=m_{\mu} |  | \psi \rangle = | \psi_i \rangle ) = | \langle m_{\mu} | \psi_i \rangle |^2 =  \langle  \psi_i | m_{\mu} \rangle  \langle m_{\mu} | \psi_i \rangle \ .$$

The probability of measuring $m$ from the ensemble is the marginal probability,

$$\begin{aligned}
  p(m = m_{\mu}) 
  & = \sum_i p(m = m_{\mu} | | \psi \rangle = | \psi_i \rangle) \, p( | \psi \rangle = | \psi_i \rangle ) = \\
  & = \sum_i \langle \psi_i | m_{\mu} \rangle \langle m_{\mu} | \psi_i \rangle \, p_i = \\
  & = \sum_i \langle \psi_i | \hat{\Pi}_{m_{\mu}} | \psi_i \rangle \, p_i \ ,
\end{aligned}$$

having introduced the orthogonal projector over the $\mu^{th}$ eigenfunction of the operator $\hat{M}$, i.e. $\hat{\Pi}_{m_{\mu}} = | m_{\mu} \rangle \langle m_{\mu} |$.

Let's define the **density operator** as

$$\hat{\rho} = \sum_i p_i | \psi_i \rangle \langle \psi_i | \ .$$

Using an orthonormal basis $\{ | e_k \rangle \}_k$, it's easy to show that

$$\begin{aligned}
  \text{Tr}\left( \hat{\rho} \hat{\Pi}_{m_{\mu}} \right) 
  & := \sum_k \langle e_k | \hat{\rho} \hat{\Pi}_{m_{\mu}} | e_k \rangle = \\
  & = \sum_{k,i} p_i \langle e_k | \psi_i \rangle \langle \psi_i | \hat{\Pi}_{m_{\mu}} | e_k \rangle = \\
  & = \sum_{i} p_i \langle \psi_i | \hat{\Pi}_{m_{\mu}} \underbrace{\sum_k | e_k \rangle \langle e_k |}_{ = \hat{\mathbf{1}} } \psi_i \rangle = \\
  & = \sum_{i} p_i \langle \psi_i | \hat{\Pi}_{m_{\mu}} | \psi_i \rangle = \\
  & = p(m = m_{\mu}) \ .
\end{aligned}$$

**Expected value.**

$$\begin{aligned}
 \mathbb{E}[ M ]
 & = \sum_{\mu} m_{\mu} p ( m = m_{\mu} ) = \\
 & = \sum_i \sum_{\mu} m_{\mu} p_i \langle \psi_i | m_{\mu} \rangle \langle m_{\mu} | \psi_i \rangle = \\
 & = \sum_i \sum_{\mu} p_i \langle \psi_i | \hat{M} | m_{\mu} \rangle \langle m_{\mu} | \psi_i \rangle = \\
 & = \sum_{\mu} | \langle m_{\mu} \sum_i  p_i| \psi_i \rangle\langle \psi_i | \hat{M} | m_{\mu} \rangle = \\
 & = \sum_{\mu} \langle m_{\mu} | \hat{\rho} \hat{M} | m_{\mu} \rangle = \\
 & = \text{Tr} \left( \hat{\rho} \hat{M} \right) \ .
\end{aligned}$$

```{dropdown} Trace of an operator
:open:

Choosing a set of **orthogonal unit vectors** $| \psi_i \rangle$, the trace of an operator $\hat{A}$ can be defined as

$$\text{Tr}\left( \hat{A} \right) = \sum_{i} \langle \psi_i | \hat{A} | \psi_i \rangle \ .$$

Properties

* 
   $$\text{Tr}\left( \hat{A} | \psi_j \rangle \langle \psi_j | \right) = \sum_{i} \langle \psi_i | \hat{A} | \psi_j \rangle \underbrace{\langle \psi_j | \psi_i \rangle}_{\delta_{ij}} = \langle \psi_j | \hat{A}| \psi_j \rangle \ . $$

*  
   $$\text{Tr}\left( \hat{A}\right) = \text{Tr}\left( \hat{A} \sum_j | \psi_j \rangle \langle \psi_j | \right) = \sum_{i,j} \langle \psi_i | \hat{A} | \psi_j \rangle \underbrace{\langle \psi_j | \psi_i \rangle}_{\delta_{ij}} = \sum_i \langle \psi_i | \hat{A}| \psi_i \rangle \ . $$

Choosing a **generic basis** $\{ | \phi_k \rangle \}_k$, the $k^{th}$ vector of this basis can be written as a linear combination of the vectors of a unit orthogonal basis,

As done in Differential Geometry, a reciprocal basis $\{ | \phi^j \rangle \}_j$ exists s.t. $\langle \phi^j | \phi_k \rangle = \delta^j_k$. Defining the components of the metric tensor $g_{ij} = \langle \phi_i | \phi_j \rangle$, $g^{ij} = \langle \phi^i | \phi^j \rangle$ the relations between the original basis and its reciprocal follows

$$| \phi^i \rangle = g^{ij} | \phi_j \rangle \quad , \quad | \phi_i \rangle = g_{ij} | \phi^j \rangle .$$

The identity operator can be written as $\hat{\mathbf{1}} = \sum_j | \phi_j \rangle \langle \phi^j | =  \sum_j | \phi^j \rangle \langle \phi_j |$, as

$$| v \rangle = \sum_i v^i | \phi_i \rangle = \sum_{i,j} v^i | \phi_j \rangle \underbrace{\langle \phi^j | \phi_i \rangle}_{=\delta^j_i} = \sum_{j} | \phi_j\rangle \langle \phi^j | \, \sum_i v^i | \phi_i \rangle = \hat{\mathbf{1}} | v \rangle \ . $$

The vectors of the basis can be written as a linear combination of the vectors of an orthonormal basis $\{ | \psi_k \rangle \}_k$,

$$| \phi_i \rangle = \sum_{k} T_{i}^{\ \ k} | \psi_k \rangle \ .$$

The dual vectors are written as $| \phi^j \rangle = \sum_l R^{jl} | \psi_l \rangle$. As the dual vectors should be orthogonal to the vectors of the original basis, it follows

$$\delta^{j}_{i} = \langle \phi^j | \phi_i \rangle = \sum_{k,l} \left( R^{jl} \right)^* T_{i}^{\ \ k} \underbrace{\langle \psi_l | \psi_k \rangle}_{= \delta_{lk}} = \sum_{k} \left( R^{jk} \right)^* T_{i}^{\ \ k} \ ,$$

i.e. the transformation matrix $\mathsf{R}$ of the vectors of the reciprocal basis is the inverse of the adjoint of the matrix $\mathsf{T}$, i.e.

$$\begin{aligned}
  \left( \mathsf{T} \right)_{ik} & = T_i^{\ \ k} \\
  \left( \mathsf{R} \right)_{jk} & = R^{ij} \\
  \left( \mathsf{T}^{-1} \right)_{kj} & = \left( R^{jk} \right)^* = \left( \mathsf{R}^H \right)_{kj} \\
\end{aligned}$$

Using matrix formalism, the definition of the inverse matrix gives $\mathsf{I} = \mathsf{T} \mathsf{R}^H = \mathsf{R}^H \mathsf{T}$. (**todo** what happens for infinite dimensional spaces?)

Thus, the relation

$$
  \sum_i \langle \phi^i | \hat{A} | \phi_i \rangle = \sum_{l,k}  \underbrace{\sum_i  \left( R^{il} \right)^* T_{i}^{\ \ k}}_{= \left( \mathsf{R}^H \mathsf{T} \right)_{lk} =\delta^{lk}} \langle \psi_l | \hat{A} | \psi_k \rangle = \sum_k \langle \psi_k | \hat{A} | \psi_k \rangle = \text{Tr}\left( \hat{A} \right) \ .
$$

**todo** *Uncomment or delete (more likely)*

<!--

$$| \phi_k \rangle = c_{ki} | \psi_i \rangle \ .$$

The adjoint vector reads  $\langle \phi_k | = c^*_{ki} \langle \psi_i |$. The unitary condition reads

$$1 = \langle \phi_k | \phi_k \rangle = \sum_{i,j} c^*_{ki} c_{kj} \underbrace{\langle \psi_i | \psi_j \rangle}_{=\delta_{ij}} = \sum_i c^*_{ki} c_{ki} $$

In general, $\langle \phi_k | \phi_l \rangle \ne 0$. If the basis $\{ | \phi_k \rangle \}_k$ is unitary and orthogonal itself, then $\langle \phi_k | \phi_i\rangle = 0$, and thus $\delta_{kl} = \langle \phi_k | \phi_l \rangle = \sum_i c^*_{ki} c_{li}$.

The inverse transformation reads $| \psi_k \rangle = b_{ki} | \phi_i \rangle$. Orthogonality condition reads

$$\delta_{ij} = \langle \psi_i | \psi_j \rangle = \sum_{k,l} b^*_{ik} b_{jl} \langle \phi_k | \phi_l \rangle = $$

Evaluating the sum,

$$\sum_k \langle \phi_k | \hat{A} | \phi_k \rangle = \sum_{k,i,j} c_{ki}^* c_{kj} \langle \psi_i | \hat{A} | \psi_j \rangle$$

-->

```

```{prf:example} Difference between mixed states and pure state in superposition

**Pure state** in superposition of two orthogonal states $| \psi_1 \rangle$, $| \psi_2 \rangle$,

$$| \psi \rangle = a_1 | \psi_1 \rangle + a_2 | \psi_2 \rangle \ ,$$

with $|a_1|^2 + |a_2|^2 = 1$. A system prepared in this pure state with probability $p = 1$ has density operator

$$\hat{\rho} = | \psi \rangle \langle \psi | = |a_1|^2 | \psi_1 \rangle \langle \psi_1 | + a_1 a_2^* | \psi_1 \rangle \langle \psi_2 | + a_2 a_1^* | \psi_2 \rangle \langle \psi_1 | + |a_2|^2 | \psi_2 \rangle \langle \psi_2 | \ . $$

If $a = b = \frac{1}{\sqrt{2}}$, the components of the density operator in the basis $\{ | \psi_1 \rangle, | \psi_2 \rangle \}$ are

$$
\begin{bmatrix} |a_1|^2 & a_1 a_2^* \\ a_1^* a_2 & |a_2|^2 \end{bmatrix} =
\begin{bmatrix} \frac{1}{2} & \frac{1}{2} \\ \frac{1}{2} & \frac{1}{2} \end{bmatrix} \ .
$$

**Mixed state.** An ensamble prepared in state $| \psi_1 \rangle$ with probability $p_1$, $p_2 = 1 - p_1$ has density operator

$$\hat{\rho} = p_1 | \psi_1 \rangle \langle \psi_1 | + p_2 | \psi_2 \rangle \langle \psi_2 | \ ,$$

whose components in the $\{ | \psi_1 \rangle, | \psi_2 \rangle \}$ basis are

$$
\begin{bmatrix} p_1 & 0 \\ 0 & p_2 \end{bmatrix} =
\begin{bmatrix} \frac{1}{2} & 0 \\ 0 & \frac{1}{2} \end{bmatrix}
\ .$$




```
