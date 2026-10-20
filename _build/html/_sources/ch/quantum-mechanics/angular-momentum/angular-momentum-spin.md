(quantum-mechanics:angular-momentum:spin)=
# Spin

* Properties of spin angular momentum operators
* Pauli matrices
* Pauli equation

(quantum-mechanics:angular-momentum:spin:operator)=
## Properties of spin angular momentum operators $\hat{S}^2$, $\hat{S}_z$

In analogy with the spatial angular momentum, and using Cartesian coordinates

$$\begin{aligned}
  \left[ S_a, S_b \right] & = i \hbar \, \varepsilon_{abc} S_c \\
  \left[ S_a, S^2 \right] & = 0 \ . \\
\end{aligned}$$

As the operators $S_z$ and $S^2$ commute, they share the same eigenvectors $| s, m_s \rangle$ (all the eigvecs?) and their eigenproblems read

$$\begin{aligned}
  S_z | s, m_s \rangle & = \hbar m_s | s, m_s \rangle \\
  S^2 | s, m_s \rangle & = \hbar^2 s ( s + 1 ) | s, m_s \rangle \ , 
\end{aligned}$$


The value of $s$ depends on the system of interest: for an electron $s = \frac{1}{2}$. The value of the spin projection quantum number $m_s$ belongs to $m_s \in \{ -s, -s+1, \dots, s-1, s \}$. For an electron, $m_s \in \left\{ - \frac{1}{2}, \frac{1}{2} \right\}$.

(quantum-mechanics:angular-momentum:spin:pauli-matrices)=
## Pauli matrices

$$\begin{aligned}
 \sigma_x & = \begin{bmatrix} 0 &  1 \\ 1 &  0 \end{bmatrix} \\
 \sigma_y & = \begin{bmatrix} 0 & -i \\ i &  0 \end{bmatrix} \\
 \sigma_z & = \begin{bmatrix} 1 &  0 \\ 0 & -1 \end{bmatrix} \\
\end{aligned}$$

### Properties


### Pauli vectors

Using a Cartesian basis, a Pauli vector is defined as

$$\boldsymbol\sigma := \sum_k \sigma_k \hat{\mathbf{x}}_k$$

and the dot product with a vector $\mathbf{a} = \sum_k a_k \hat{\mathbf{x}}_k$ is defined as

$$\begin{aligned}
 \mathbf{a} \cdot \boldsymbol\sigma 
 & = \sum_{l,k} a_l \underbrace{\hat{\mathbf{x}}_l \cdot \hat{\mathbf{x}}_k}_{\delta_{kl}} \sigma_k = \sum_k a_k \, \sigma_k
   = \begin{bmatrix} a_3 & a_1 - i a_2 \\ a_1 + i a_2 & - a_3 \end{bmatrix} \ .
\end{aligned}$$

#### Properties


