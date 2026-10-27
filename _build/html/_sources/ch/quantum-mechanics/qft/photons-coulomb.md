(quantum-mechanics:qft:photons:coulomb)=
# Photons - EM field quantization with Coulomb gauge

<!--
Using Coulomb gauge $\nabla \cdot \vec{a} = 0$ the governing equations of the EM potentials read

$$\left\{ \begin{aligned}
  \nabla^2 \varphi & = \frac{\rho}{\varepsilon} \\
  \square \vec{a} & = \mu \vec{j}_{\parallel} \ .
\end{aligned}\right.$$
-->

(quantum-mechanics:qft:photons:coulomb:classical)=
## Classical fields

In free space without charge and current densities, the vector potential satisfies the homogeneous wave equation $\square \vec{a} = \vec{0}$, whose solution can be written as a linear combination of Fourier modes. For finite (or periodic) domains

$$\vec{a}(\vec{r},t) = \sum_{\vec{k}} \vec{a}(\vec{k},t) e^{i \vec{k} \cdot \vec{r}} \ ,$$

with $k_a L_a = n_a 2 \pi$, $n_a \in \mathbb{Z}$. For infinite domains

$$\vec{a}(\vec{r},t) = \dfrac{1}{(2 \pi )^{3/2}} \int_{\vec{k}} \vec{a}(\vec{k},t) e^{i \vec{k} \cdot \vec{r}} \, d \vec{k} \ .$$

**Coulomb gauge.** Exploiting the orthogonality of the base functions $\frac{e^{i \vec{k} \cdot \vec{r}}}{(2\pi)^{3/2}}$, Coulomb gauge $\nabla \cdot \vec{a} = 0$ implies 

$$i \vec{k} \cdot \vec{a}(\vec{k}, t) = 0 \quad , \quad \forall \vec{k} \ .$$

Thus, as each coefficient $\vec{a}(\vec{k},t)$ is orthogonal to its corresponding wave vector $\vec{k}$, it only has 2 independent components (corresponding to **polarization**). Let $\{ \vec{\epsilon}_{\vec{k},\mu} \}_{\mu \in \{1, 2\}}$ an orthogonal basis - with $\vec{\epsilon}_{\vec{k},\mu} \cdot \vec{k} = 0$ - for the coefficient $\vec{a}(\vec{k},t)$, then this coefficient can be written as

$$\vec{a}(\vec{k}, t) = \sum_{\mu} \vec{\epsilon}_{\vec{k}, \mu} a(\vec{k},\mu, t) \ .$$

**Real-valued field, $\vec{a}(\vec{r},t)$.** Since $\vec{a}(\vec{r},t)$ is a real-valued field, then 

$$\vec{a}(\vec{k},t) = \vec{a}^*(-\vec{k},t) \ . $$ (eq:photons:a:real-value)

**Solution of the homogeneous wave equation.** Exploiting the orthogonality of the base functions, and the linearity of the wave equation, each coefficient of the Fourier expansion satisfies a linear second-order equation (simple harmonic oscillator),

$$\frac{1}{c^2}\partial_{tt} \vec{a}(\vec{k}, t) + |\vec{k}|^2 \vec{a}(\vec{k},t) = \vec{0} \ ,$$

whose solution reads

$$\vec{a}(\vec{k},t) = \vec{a}_{-}(\vec{k}) e^{i \omega_{\vec{k}} t} + \vec{a}_{+}(\vec{k}) e^{- i \omega_{\vec{k}} t} \ ,$$

with $\omega_{\vec{k}} = c | \vec{k} |$, and the coefficients to be determined with the initial conditions for the potential governed by the wave equation. The condition {eq}`eq:photons:a:real-value` about real-valued field $\vec{a}(\vec{r},t)$ implies

$$\vec{a}_+(\vec{k},t) = \vec{a}^*_-(-\vec{k},t) \quad , \quad \vec{a}_-(\vec{k},t) = \vec{a}^*_+(-\vec{k},t) \ .$$

```{dropdown} Details

$$\begin{aligned}
  \vec{a}(\vec{k},t) & = \vec{a}_{-}(\vec{k}) e^{i \omega_{\vec{k}} t} + \vec{a}_{+}(\vec{k}) e^{- i \omega_{\vec{k}} t} \\
  \vec{a}^*(-\vec{k},t) & = \left( \vec{a}_{-}(-\vec{k}) e^{i \omega_{-\vec{k}} t} + \vec{a}_{+}(-\vec{k}) e^{- i \omega_{-\vec{k}} t} \right)^* = \\
                        & =        \vec{a}_{-}^*(-\vec{k}) e^{-i \omega_{\vec{k}} t} + \vec{a}^*_{+}(-\vec{k}) e^{i \omega_{\vec{k}} t} \\
\end{aligned}$$


```

**Solution of the wave equation.** Putting everything together, the solution of the wave equation for the vector potential can be written - here in a periodic domain - as

$$\begin{aligned}
  \vec{a}(\vec{r},t) 
  & = \sum_{\vec{k}} \vec{a}(\vec{k},t) e^{i \vec{k} \cdot \vec{r}} = \\
  & = \sum_{\vec{k}} \left[ \vec{a}_{-}(\vec{k}) e^{i \omega_{\vec{k}} t} + \vec{a}_{+}(\vec{k}) e^{- i \omega_{\vec{k}} t}  \right] e^{i \vec{k} \cdot \vec{r}} = && \text{(see re-arrangement)} \\
  & = \sum_{\vec{k}} \left[ \vec{a}_{-}(-\vec{k}) e^{i ( \omega_{\vec{k}} t - \vec{k} \cdot \vec{r} )} + \vec{a}_{+}(\vec{k}) e^{- i ( \omega_{\vec{k}} t - \vec{k} \cdot \vec{r})}  \right] \ .
\end{aligned}$$ (eq:photons-coulomb:vector-potential:fourier)


```{dropdown} Re-arrangement of the summation

For each $\vec{k}$ (except for $\vec{k} = \vec{0}$, to avoid summing twice the same contributions), summing over $\vec{k}$ and $-\vec{k}$ produces 4 terms

$$\begin{aligned}
  & \vec{a}(\vec{k}, t) + \vec{a}(-\vec{k}, t) = \\
  & = \vec{a}_{-}(\vec{k}) e^{i ( \omega_{\vec{k}} t + \vec{k} \cdot \vec{r})} + \vec{a}_{+}(\vec{k}) e^{i( - \omega_{\vec{k}} t + \vec{k} \cdot \vec{r})} 
    +  \vec{a}_{-}(-\vec{k}) e^{i ( \omega_{\vec{k}} t - \vec{k} \cdot \vec{r})} + \vec{a}_{+}(-\vec{k}) e^{i(- \omega_{\vec{k}} t -i \vec{k} \cdot \vec{r})} \\ 
\end{aligned}$$

that can be re-grouped as

$$\begin{aligned}
  & = \underbrace{ \vec{a}_{-}(\vec{k}) e^{i ( \omega_{\vec{k}} t + \vec{k} \cdot \vec{r})} + \vec{a}_{+}(-\vec{k}) e^{-i(\omega_{\vec{k}} t + i \vec{k} \cdot \vec{r})} }
   + \underbrace{ \vec{a}_{+}(\vec{k}) e^{-i(\omega_{\vec{k}} t - \vec{k} \cdot \vec{r})} + \vec{a}_{-}(-\vec{k}) e^{i ( \omega_{\vec{k}} t - \vec{k} \cdot \vec{r})} } \ ,
\end{aligned}$$

s.t. each pair of terms gives a real contribution. Here the sum of the first pair fives a travelling wave in $- \hat{k}$ direction, while the second pair gives a travelling wave in $+ \hat{k}$ direction.


```


**EOMs and solutions as a function of generalized coordinates and momenta.**

...

**Electro-magnetic field.**

...

(quantum-mechanics:qft:photons:coulomb:quantization)=
## Quantization

...**todo** *discuss promotion. Link to classical limit, other quantization procedures,...*

Promotion of the expression {eq}`eq:photons-coulomb:vector-potential:fourier` to operator. In Heisenberg picture

$$
\hat{\vec{a}}(\vec{r},t) = \sum_{\vec{k}, \mu} \left[ e^{i ( \omega_{\vec{k}} t - \vec{k} \cdot \vec{r} )} \vec{\epsilon}_{\vec{k}, \mu} \hat{a}^\dagger_{\vec{k},\mu} + e^{- i ( \omega_{\vec{k}} t - \vec{k} \cdot \vec{r})} \vec{\epsilon}_{\vec{k},\mu} \hat{a}_{\vec{k},\mu} \right]
$$

...

with Heisenberg picture for annihilation and creation operators being $\hat{a}^\dagger_H(t) = \hat{a}^\dagger e^{i \omega t}$ and $\hat{a}_H(t) = \hat{a} e^{-i \omega t}$ respectively.

**todo** *Discuss both Schrodinger and Heisenberg picture.*

```{dropdown} Schrodinger and Heisenberg picture of annihilation/creation operators. Single simple harmonic oscillator

The Hamiltonian operator of a single simple harmonic oscillator reads

$$\hat{H} = \frac{\hat{p}^2}{2} + \frac{\omega^2 \hat{q}^2}{2} = \hbar \omega \left( \hat{a}^{\dagger} \hat{a} + \frac{1}{2} \right) \ .$$

**Annihilation operator.** Heisenberg equations of motion for the annihilation operator reads

$$\begin{aligned}
  i \hbar \dfrac{d \hat{a}_H}{d t}
  & = \left[ \hat{a}, \hat{H} \right]_{H} + \cancelto{0}{\left( \partial_t \hat{a} \right)_H} = \\
  & = \left[ \hat{a}, \left( \hat{a}^\dagger \hat{a} + \frac{1}{2} \right) \hbar \omega \right]_{H} + \cancelto{0}{\left( \partial_t \hat{A} \right)_H} = \\
  & = \left\{ \left( \hat{a} \hat{a}^\dagger \hat{a} - \hat{a}^\dagger \hat{a} \hat{a} \right)  \right\}_H \hbar \omega = \\
  & = \left\{ \left[ \hat{a}, \hat{a}^\dagger \right] \hat{a} \right\}_H \hbar \omega = \\
  & = \hbar \omega  \hat{a}_{H} \ ,
\end{aligned}$$

whose solution provides the relation between the Heisenberg and Schdoringer picture of the annihilation operator,

$$\hat{a}_H(t) = \hat{a}_H(0) e^{-i \omega t} = \hat{a} e^{-i \omega t} \ .$$

**Creation operator.** Heisenberg equations of motion for the creation operator reads

$$\begin{aligned}
  i \hbar \dfrac{d \hat{a}^\dagger_H}{d t}
  & = \left[ \hat{a}^\dagger, \hat{H} \right]_{H} + \cancelto{0}{\left( \partial_t \hat{a}^\dagger \right)_H} = \\
  & = \left[ \hat{a}^\dagger, \left( \hat{a}^\dagger \hat{a} + \frac{1}{2} \right) \hbar \omega \right]_{H} + \cancelto{0}{\left( \partial_t \hat{A} \right)_H} = \\
  & = \left\{ \left( \hat{a}^\dagger \hat{a}^\dagger \hat{a} - \hat{a}^\dagger \hat{a} \hat{a}^\dagger \right)  \right\}_H \hbar \omega = \\
  & = \left\{ \hat{a}^\dagger \left[ \hat{a}^\dagger, \hat{a} \right] \right\}_H \hbar \omega = \\
  & = - \hbar \omega  \hat{a}^\dagger_{H} \ ,
\end{aligned}$$

whose solution provides the relation between the Heisenberg and Schdoringer picture of the creation operator,

$$\hat{a}^\dagger_H(t) = \hat{a}^\dagger_H(0) e^{i \omega t} = \hat{a}^\dagger e^{i \omega t} \ .$$




```

### Energy

### Momentum

### ...

(quantum-mechanics:qft:photons:coulomb:classical-limit)=
## Classical limit

(quantum-mechanics:qft:photons:coulomb:classical-limit:one-mode-coherent)=
### One-mode coherent state

The state of an electromagnetic field can be written as a linear combination of states in the Fock space, with the occupation numbers of each possible modes $| \vec{k}, \mu \rangle$. A one-mode coherent state is defined as the $| \alpha_{\vec{k},\mu} \rangle$ that's an eigenstate of the annihilation operator $\hat{a}_{\vec{k},\mu}$ for the mode $| \vec{k}, \mu \rangle$,

$$\hat{a}_{\vec{k},\mu} | \alpha_{\vec{k},\mu} \rangle = c_{\vec{k}, \mu} | \alpha_{\vec{k},\mu} \rangle \ .$$

The one-mode coherent state is a linear combination of states in the Fock space

$$| \alpha_{\vec{k},\mu} \rangle = \sum_{n} b_n^{\vec{k},\mu} | \dots n_{\vec{k},\mu} \dots \rangle \ ,$$

with zero occupation number of any state different from $|\vec{k}, \mu \rangle$, or dropping the indices,

$$| \alpha \rangle = \sum_{n=0}^{+\infty} b_n | n \rangle \ ,$$

with $b_n = b_0 \frac{c^n}{\sqrt{n!}}$ from the definition and coefficient matching, and $b_0 = e^{-\frac{|c|^2}{2}}$ from the normalization condition $\langle \alpha | \alpha \rangle = 1$.

````{dropdown} Annihilation operator
:open:

Expected value when the system is in state $| \alpha \rangle$,

$$\langle \alpha | \hat{a} | \alpha \rangle = c $$

```{dropdown} Details

$$\begin{aligned}
  \langle \alpha | \hat{a} | \alpha \rangle 
  & = \sum_{n,m=0}^{+\infty} b_m^* b_n \langle m | \hat{a} | n \rangle = \\
  & = \sum_{m=0}^{+\infty} \sum_{n=1}^{+\infty} b_m^* b_n \sqrt{n} \langle m | n - 1 \rangle = \\
  & = \sum_{m=0}^{+\infty} \sum_{n=0}^{+\infty} b_m^* b_{n+1} \sqrt{n+1} \underbrace{\langle m | n \rangle}_{=\delta_{mn}} = \\
  & = \sum_{n=0}^{+\infty} c \cdot |b_n|^2 = \\
  & = c \cdot \sum_{n=0}^{+\infty} \frac{|c|^{2n}}{n!} = \\
  & = c \cdot \underbrace{|b_0|^2 \cdot e^{|c|^2}}_{=1} = c \ ,
\end{aligned}$$

since $\sqrt{n+1} b_{n+1} = c \cdot b_n$.

```
````

````{dropdown} Creation operator
:open:

Expected value when the system is in state $| \alpha \rangle$,

$$\langle \alpha | \hat{a}^\dagger | \alpha \rangle = c^* $$

```{dropdown} Details

$$\begin{aligned}
  \langle \alpha | \hat{a}^\dagger | \alpha \rangle 
  & = \left( \langle \alpha | \hat{a} | \alpha \rangle \right)^* = \\
  & = \left( \sum_{n,m=0}^{+\infty} b_m^* b_n \langle m | \hat{a} | n \rangle \right)^* = \\
  & = \sum_{m=0}^{+\infty} \sum_{n=1}^{+\infty} b_m b_n^* \sqrt{n} \langle m | n - 1 \rangle = \\
  & = \sum_{m=0}^{+\infty} \sum_{n=0}^{+\infty} b_m b_{n+1}^* \sqrt{n+1} \underbrace{\langle m | n \rangle}_{=\delta_{mn}} = \\
  & = \sum_{n=0}^{+\infty} c^* \cdot |b_n|^2 = \\
  & = c^* \cdot \sum_{n=0}^{+\infty} \frac{|c|^{2n}}{n!} = \\
  & = c^* \cdot \underbrace{|b_0|^2 \cdot e^{|c|^2}}_{=1}  = c^* \ .
\end{aligned}$$


```

````

````{dropdown} Number operator
:open:

Expected value of the number operator

$$
  \langle \alpha | \hat{n} | \alpha \rangle = |c|^2
$$

```{dropdown} Details

With $\hat{n} = \hat{a}^\dagger \hat{a}$,

$$\begin{aligned}
  \langle \alpha | \hat{a}^\dagger \hat{a} | \alpha \rangle 
  & = \sum_{m,n=0}^{+\infty} b_m^* b_n \langle m | \hat{a}^\dagger \hat{a} | n \rangle = \\
  & = \sum_{m,n=0}^{+\infty} b_m^* b_n \sqrt{n} \langle m | \hat{a}^\dagger | n - 1 \rangle = \\
  & = \sum_{m,n=0}^{+\infty} b_m^* b_n \sqrt{n} \sqrt{n} \underbrace{\langle m | n \rangle}_{=\delta_{mn}} = \\
  & = \sum_{n=0}^{+\infty} | b_n |^2 \cdot n = \\
  & = |b_0|^2 \sum_{n=1}^{+\infty} n \frac{|c|^{2n}}{n!} = \\
  & = |c|^2 \cdot |b_0|^2 \cdot \underbrace{\sum_{n=0}^{+\infty} \frac{|c|^{2n}}{n!}}_{ = e^{|c|^2} = |b_0|^{-2}} = \\
  & = |c|^2 \ .
\end{aligned}$$

```

````

````{dropdown} Potential vector
:open:

Expected value of the potential vector field operator

$$\begin{aligned}
  \langle \alpha | \hat{\vec{a}}(\vec{r},t) | \alpha \rangle
  & =  e^{i ( \omega_{\vec{k}} t - \vec{k} \cdot \vec{r} )} \vec{\epsilon}_{\vec{k}, \mu} \, c^*_{\vec{k},\mu} + e^{- i ( \omega_{\vec{k}} t - \vec{k} \cdot \vec{r})} \vec{\epsilon}_{\vec{k},\mu} \, c_{\vec{k},\mu} \ .
\end{aligned}$$

```{dropdown} Details

$$\begin{aligned}
  \langle \alpha | \hat{\vec{a}}(\vec{r},t) | \alpha \rangle
  & = \langle \alpha | \sum_{\vec{k}', \mu'} \left[ e^{i ( \omega_{\vec{k}'} t - \vec{k}' \cdot \vec{r} )} \vec{\epsilon}_{\vec{k}', \mu'} \hat{a}^\dagger_{\vec{k}',\mu'} + e^{- i ( \omega_{\vec{k}'} t - \vec{k}' \cdot \vec{r})} \vec{\epsilon}_{\vec{k}',\mu'} \hat{a}_{\vec{k}',\mu'} \right] | \alpha \rangle = \\
  & = \langle \alpha | \left[ e^{i ( \omega_{\vec{k}} t - \vec{k} \cdot \vec{r} )} \vec{\epsilon}_{\vec{k}, \mu} \hat{a}^\dagger_{\vec{k},\mu} + e^{- i ( \omega_{\vec{k}} t - \vec{k} \cdot \vec{r})} \vec{\epsilon}_{\vec{k},\mu} \hat{a}_{\vec{k},\mu} \right] | \alpha \rangle = \\
  & =  e^{i ( \omega_{\vec{k}} t - \vec{k} \cdot \vec{r} )} \vec{\epsilon}_{\vec{k}, \mu} \langle \alpha | \hat{a}^\dagger_{\vec{k},\mu} | \alpha \rangle + e^{- i ( \omega_{\vec{k}} t - \vec{k} \cdot \vec{r})} \vec{\epsilon}_{\vec{k},\mu} \langle \alpha | \hat{a}_{\vec{k},\mu} | \alpha \rangle = \\
  & =  e^{i ( \omega_{\vec{k}} t - \vec{k} \cdot \vec{r} )} \vec{\epsilon}_{\vec{k}, \mu} \, c^* + e^{- i ( \omega_{\vec{k}} t - \vec{k} \cdot \vec{r})} \vec{\epsilon}_{\vec{k},\mu} \, c \ .
\end{aligned}$$

Comparison with {eq}`eq:photons-coulomb:vector-potential:fourier` identifies the coefficients of the Fourier expansion with the eigenvalue of the annihilation operator corresponding to the coherent state,

$$
\vec{a}_+(\vec{k},\mu) \sim c_{\vec{k},\mu}
\quad , \quad
\vec{a}_-(-\vec{k},\mu) \sim c^*_{\vec{k},\mu} \ .
$$

```

````




