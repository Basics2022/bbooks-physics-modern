(quantum-mechanics:second-quantizazion:fermions)=
# Second quantization. Fermions

The state of a many-body fermionic system is anti-symmetric under the exchange of 2 particles. This is the Pauli exclusion principle, that's represented in the [CARs](quantum-mechanics:second-quantizazion:fermions:car). 

(quantum-mechanics:second-quantizazion:fermions:creation-annihilation)=
## Creation and annihilation operators


$$\begin{aligned}
\hat c^\dagger_k|\dots n_k\dots\rangle & = \theta_k\sqrt{1-n_k}\,|\dots(1-n)_k\dots\rangle \\
\hat c_k|\dots n_k\dots\rangle & = \theta_k\sqrt{n_k}\,|\dots(1-n)_k\dots\rangle
\end{aligned}$$

with $\theta_k=(-1)^{\sum_{j=1}^{k-1} n_j}$.


```{dropdown} Road to the formalization of creation and annihilation operators
:open:

**Pauli exclusion principle.** Pauli exclusion principle implies that the occupation number of a state can be either $0$ or $1$. Creation and annihilation operators should satisfy the following conditions

$$\begin{aligned}
  \hat{c}_i | 0 \rangle & =   0         &&                                \\
  \hat{c}_i | 1 \rangle & = | 0 \rangle && \hat{c}_i^\dagger | 0 \rangle = | 1 \rangle \\
                        &               && \hat{c}_i^\dagger | 1 \rangle = 0 \\
\end{aligned}$$

A first - but wrong, see **Jordan-Wigner** solution - try of the definition of creation $\hat{c}_i^\dagger$ and annihilation operator $\hat{c}_i$ for a fermionic field could be

$$\begin{aligned}
  \hat{c}_k^\dagger | \dots n_k \dots \rangle & = \sqrt{1-n_k} | \dots (1-n)_k \dots \rangle \\
  \hat{c}_k         | \dots n_k \dots \rangle & = \sqrt{  n_k} | \dots (1-n)_k \dots \rangle \\
\end{aligned}$$

This definition would provide an inconsistent behavior with the [canonical anticommuation relations](quantum-mechanics:second-quantizazion:fermions:car). As an example, with $i < j$

$$\hat{c}_i^\dagger \hat{c}_j^\dagger | 0 \rangle = - \hat{c}_j^\dagger \hat{c}_i^\dagger | 0 \rangle \ .$$

Applying the - wrong - expression of the creation and annihilation operators given above, the result would be

$$| 1_i, 1_j \rangle = - | 1_i, 1_j \rangle \ ,$$

that would imply the state is identically zero.

**Jordan-Wigner, "On the Pauli exclusion principle".**[^jordan-wigner]

[^jordan-wigner]: Jordan–Wigner (1928), "On the Pauli exclusion principle"

$$\begin{aligned}
\hat c^\dagger_k|\dots n_k\dots\rangle & = \theta_k\sqrt{1-n_k}\,|\dots(1-n)_k\dots\rangle \\
\hat c_k|\dots n_k\dots\rangle & = \theta_k\sqrt{n_k}\,|\dots(1-n)_k\dots\rangle
\end{aligned}$$

with $\theta_k=(-1)^{\sum_{j=1}^{k-1} n_j}$. With this definition of the creation and annihilation operators the example above, with $i < j$ becomes

$$\begin{aligned}
  \hat{c}_i^\dagger \hat{c}_j^\dagger | 0 \rangle & = (-1)^0 \hat{c}_i^\dagger | 1_j \rangle = (-1)^0 | 1_i, 1_j \rangle =   | 1_i, 1_j \rangle \\
  \hat{c}_j^\dagger \hat{c}_i^\dagger | 0 \rangle & = (-1)^0 \hat{c}_j^\dagger | 1_i \rangle = (-1)^1 | 1_i, 1_j \rangle = - | 1_i, 1_j \rangle
\end{aligned}$$

```

(quantum-mechanics:second-quantizazion:fermions:number)=
## Number operator

(quantum-mechanics:second-quantizazion:fermions:car)=
## Canonical anti-commutation relations

The commutation relation

$$\{ \hat{c}_i^\dagger, \hat{c}_j^\dagger \} = 0$$

implies
* $\hat{c}_i^\dagger \hat{c}_i^\dagger = - \hat{c}_i^\dagger \hat{c}_i^\dagger $, and thus $\left( \hat{c}_i^\dagger \right)^2 = 0$. If $\hat{c}_i^\dagger$ creates the state $| 1_i \rangle$ from the vacuum state $| 0 \rangle$, and a state proportional to $| 2_i \rangle$ when applied to state $| 1_i \rangle$, i.e. with 2 applications to $| 0 \rangle$, then this implies that it's not possible to get $| 2_i \rangle$, and states with larger occupation numbers. Thus, the occupation number of each state can be either $0$ or $1$.

* $\hat{c}_i^\dagger \hat{c}_j^\dagger = - \hat{c}_j^\dagger \hat{c}_i^\dagger $

```{dropdown} Proof
:open:

If $i < j$

$$\begin{aligned}
  & \left( \hat{c}_i^\dagger \hat{c}_j^\dagger + \hat{c}_j^\dagger \hat{c}_i^\dagger \right) | \dots n_i \dots n_j \dots \rangle = \\
  & = \sqrt{n_j - 1} \cdot (-1)^{\sum_{k=1}^{j-1} n_k} \hat{c}_i^\dagger | \dots n_i \dots (n-1)_j \dots \rangle + \sqrt{n_i-1} \cot (-1)^{\sum_{l=1}^{i-1} n_l} \hat{c}_j^\dagger | \dots (n-1)_i \dots n_j \dots \rangle   = \\
  & = \sqrt{n_j - 1} \sqrt{n_i - 1 } \cdot \left\{ (-1)^{\sum_{l=1}^{i-1} n_l} \cdot (-1)^{\sum_{k=1}^{j-1} n_k} + (-1)^{\sum_{k=1, l\ne i}^{k-1} n_l} \cdot (-1)^{n_i-1} \cdot (-1)^{\sum_{l=1}^{i-1} n_l}  \right\} | \dots (n-1)_i \dots (n-1)_j \dots \rangle  = \\
  & = \sqrt{n_j - 1} \sqrt{n_i - 1 } \cdot \left\{ \underbrace{\left( (-1)^{n_i} + (-1)^{n_i-1} \right)}_{=0} (-1)^{\sum_{k=1, l\ne i}^{k-1} n_l} \cdot (-1)^{\sum_{l=1}^{i-1} n_l}  \right\} | \dots (n-1)_i \dots (n-1)_j \dots \rangle  = \\
  & = 0 \ .
\end{aligned}$$

If $j = i$, the equality immediately follows from $\left( c^\dagger_i \right)^2 = 0$.

```


$$\{ \hat{c}_i, \hat{c}_j \} = 0$$

```{dropdown} Proof
:open:

...

```

$$\{ \hat{c}_i, \hat{c}_j^\dagger \} = \delta_{ij} \ . $$

```{dropdown} Proof
:open:

...

```






