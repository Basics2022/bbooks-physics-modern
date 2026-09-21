(quantum-mechanics:angular-momentum:total)=
# Total Angular Momentum

State function

$$| \Psi \rangle = | \psi \rangle \otimes | \sigma \rangle \quad  \in \quad \mathcal{H} = \mathcal{H}_{space} \otimes \mathcal{H}_{spin} \ .$$

Total angular momentum operator

$$\hat{\mathbf{J}} = \hat{\mathbf{L}} + \hat{\mathbf{S}} = \hat{\mathbf{L}} \otimes \hat{\mathbf{1}}_{spin} + \hat{\mathbf{1}}_{space} \otimes \hat{\mathbf{S}}$$

Dot product of $\hat{\mathbf{L}}$ and $\hat{\mathbf{S}}$,

$$\hat{\mathbf{L}} \cdot \hat{\mathbf{S}} = L_x \otimes S_x +  L_y \otimes S_y +  L_z \otimes S_z \ .$$

Magnitude square of $\hat{\mathbf{J}}$, $\hat{J}^2$,

$$\begin{aligned}
  \hat{J}^2 
  & = ( \hat{\mathbf{L}} + \hat{\mathbf{S}} ) \cdot ( \hat{\mathbf{L}} + \hat{\mathbf{S}} ) = \\
  & = \hat{L}^2 \otimes \hat{\mathbf{1}} + 2 \hat{\mathbf{L}} \cdot \hat{\mathbf{S}} + \hat{\mathbf{1}} \otimes \hat{S}^2 \ .
\end{aligned}$$


**Orbital angular momentum.**

$$\begin{aligned}
  \hat{L}^2 | \ell, m_l \rangle & = \hbar^2 \ell (\ell+1) | \ell, m_l \rangle && , \quad \ell \in \{ 0, 1, 2, \dots \} \\
  \hat{L}_z | \ell, m_l \rangle & = \hbar m_l             | \ell, m_l \rangle && , \quad m_l  \in \{ - \ell, - \ell+1, \dots, \ell-1, \ell \}
\end{aligned}$$

**Spin angular momentum.**

$$\begin{aligned}
  \hat{S}^2 |   s, m_s \rangle & = \hbar^2 s    (s   +1) | s, m_s \rangle && , \quad s   \in \left\{ 0, \frac{1}{2}, 1, \dots \right\} \\
  \hat{S}_z |   s, m_s \rangle & = \hbar m_s             | s, m_s \rangle && , \quad m_s \in \{ - s, - s+1, \dots, s-1, s \}
\end{aligned}$$

For an electron $s = \frac{1}{2}$, so that $m_s \in \left\{ - \frac{1}{2}, \frac{1}{2} \right\}$, and thus, without explicitly writing $s$ in the eigenvectors - being that a given parameter -,

$$\begin{aligned}
  \hat{S}^2 | m_s \rangle & = \frac{3}{4}\hbar^2 | m_s \rangle && \\
  \hat{S}_z | m_s \rangle & = \hbar m_s          | m_s \rangle && , \quad m_s \in \left\{ -\frac{1}{2}, \frac{1}{2} \right\}
\end{aligned}$$

**Total angular momentum.** The $z$-component of the total angular momentum, and its magnitude squared are defined as

$$\begin{aligned}
  \hat{J}^2 |   j, m_j \rangle & = \hbar^2 j    (j   +1) | j, m_j \rangle && , \quad   j \in \left\{ 0, \frac{1}{2}, 1, \dots \right\} \\
  \hat{J}_z |   j, m_j \rangle & = \hbar m_j             | j, m_j \rangle && , \quad m_j \in \{ - j, - j+1, \dots, j-1, j \}
\end{aligned}$$


## Eigenvalue problem of the total angular momentum for an electron

**Commutation of operators.** The operators $\hat{J}^2$, $\hat{J}_z$, $\hat{L}^2$, $\hat{S}^2$ commute, and thus they share common eigenvectors

$$| j, m_j, \ell, s \rangle \ .$$

The operator $\hat{J}_z$ commutes with $\hat{L}^2$ and $\hat{S}^2$, $\left[ \hat{J}_z, \hat{L}^2 \right] = 0$, $\left[ \hat{J}_z, \hat{S}^2 \right] = 0$.

```{dropdown} Proof

$$\begin{aligned}
  \left[ \hat{J}_z, \hat{L}^2 \right]
  & = \hat{J}_z \hat{L}^2 - \hat{L}^2 \hat{J}_z = \\
  & = \hat{L}_z \hat{L}^2 + \hat{S}_z \hat{L}^2 - \hat{L}^2 \hat{L}_z - \hat{L}^2 \hat{S}_z = \\
  & = \underbrace{\left[ \hat{L}_z,  \hat{L}^2 \right]}_{ = 0 } + \underbrace{\left[ \hat{S}_z, \hat{L}^2 \right]}_{ = 0} = 0 \ .
\end{aligned}$$

The last term holds because $\hat{S}_z$ and $\hat{L}^2$ acts on two different sub-spaces, or explicitly for any $| \Psi \rangle = | \psi \rangle \otimes | \sigma \rangle$,

$$\begin{aligned}
  \hat{S}_z \hat{L}^2 | \Psi \rangle
  & = ( \hat{\mathbf{1}} \otimes \hat{S}_z ) ( \hat{L}^2 \otimes \hat{\mathbf{1}} ) | \psi \rangle \otimes | \sigma \rangle = \\ 
  & = ( \hat{\mathbf{1}} \otimes \hat{S}_z ) ( \hat{L}^2 | \psi \rangle \otimes | \sigma \rangle ) = \\ 
  & = \hat{L}^2 | \psi \rangle \otimes \hat{S}_z | \sigma \rangle \ ,
\end{aligned}$$

and $\hat{L}^2 \hat{S}_z | \Psi \rangle$ provides the same result for any $| \Psi \rangle = | \psi \rangle \otimes | \sigma \rangle$.


```

The operator $\hat{L}_z$ doesn't commute with $\hat{J}^2$, $\left[ \hat{L}_z, \hat{J}^2 \right] = - 2 i \hbar \, \hat{\mathbf{z}} \cdot \hat{\mathbf{L}} \times \hat{\mathbf{S}}$.

```{dropdown} Proof

$$\begin{aligned}
  \left[ \hat{L}_z, \hat{J}^2 \right]
  & = \hat{L}_z \hat{J}^2 - \hat{J}^2 \hat{L}_z = \\
  & = \hat{L}_z \left( \hat{L}^2 + \hat{S}^2 + 2 \hat{\mathbf{L}} \cdot \hat{\mathbf{S}} \right) - \left( \hat{L}^2 + \hat{S}^2 + 2 \hat{\mathbf{L}} \cdot \hat{\mathbf{S}}\right) \hat{L}_z = \\
  & = \underbrace{\left[ \hat{L}_z,  \hat{L}^2 \right]}_{ = 0 } + \underbrace{\left[ \hat{L}_z, \hat{S}^2 \right]}_{ = 0} + 2 [\hat{L}_z, \hat{L}_a] \hat{S}_a = \\
  & = 2 i \hbar \hat{L}_y \hat{S}_x - 2 i \hbar \hat{L}_x \hat{S}_y = \\
  & = - 2 i \hbar \, \hat{\mathbf{z}} \cdot \hat{\mathbf{L}} \times \hat{\mathbf{S}} \ ,
\end{aligned}$$

as $[\hat{L}_z, \hat{L}_x] = i \hbar \hat{L}_y$, $[\hat{L}_y, \hat{L}_z] = i \hbar \hat{L}_x$, $[\hat{L}_z, \hat{L}_z] = 0$,

```

**$z$-component operators.**

$$\begin{aligned}
  \hat{J}_z | \Psi_{m_\ell, m_s} \rangle
  & = ( \hat{L}_z + \hat{S}_z ) | m_\ell \rangle \otimes | m_s \rangle = \\
  & = \hat{L}_z | m_\ell \rangle \otimes | m_s \rangle + \hat{S}_z | m_\ell \rangle \otimes | m_s \rangle = \\
  & = \hbar m_\ell | m_\ell \rangle \otimes | m_s \rangle + \hbar m_s | m_\ell \rangle \otimes | m_s \rangle = \\
  & = \hbar \left( m_\ell + m_s \right) | m_\ell \rangle \otimes | m_s \rangle = \\
  & = \hbar \, m_j \, | m_\ell \rangle \otimes | m_s \rangle \ ,
\end{aligned}$$

and thus the relation $m_j = m_{\ell} + m_s$ for every pair of eigenvectors $| m_{\ell} \rangle$ and $| m_s \rangle$ of the operators $\hat{L}_z$, and $\hat{S}_z$. It also follows, that the extreme values of $m_j$ are $-j$ and $j = \ell + s$.




<!--
Calling $| \ell, m_\ell, m_s \rangle = | \ell, m_\ell \rangle \otimes | m_s \rangle$,

$$\begin{aligned}
  \hat{J}^2 | \ell, m_\ell, m_s \rangle 
  & = \hat{L}^2 | \ell, m_\ell \rangle \otimes \hat{S}^2 | m_s \rangle = \\
  & = \hbar^2 \ell (\ell+1) | \ell, m_\ell \rangle \otimes \frac{\hbar^2}{2} | m_s \rangle = \\
  & = \hbar^2 \left( \ell (\ell+1) + \frac{1}{2} \right) | \ell, m_\ell, m_s \rangle && \ell \in \{ 0, 1, 2, \dots \} \\
  \hat{J}_z | \ell, m_\ell, m_s \rangle 
  & = \hat{L}_z | \ell, m_\ell \rangle \otimes \hat{S}_z | m_s \rangle = \\
  & = \hbar m_\ell | \ell, m_\ell \rangle \otimes \hbar m_s | m_s \rangle = \\
  & = \hbar \left( m_\ell + m_s \right) | \ell, m_\ell, m_s \rangle && m_\ell \in \{ -\ell, \dots, \ell \dots \} , \, \quad m_s \in \left\{ -\frac{1}{2} , \frac{1}{2} \right\} \\
\end{aligned}$$
-->
