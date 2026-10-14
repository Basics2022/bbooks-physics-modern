(quantum-mechanics:qft:field-quantization)=
# Field quantization

First, a [classical system](quantum-mechanics:qft:field-quantization:classical) governed by a wave equation is discussed, along with its mode decomposition: a general solution can be written as the superposition of modes $u(x,t) = \sum_k q_k(t) n_k(x)$ whose contribution is modulated by coefficients $q_k(t)$ satisfying the ODE of a [harmonic oscillator](quantum-mechanics:qft:harmonic-oscillator).

(quantum-mechanics:qft:field-quantization:classical)=
## Classical system


### Discretization

$$
\partial_t^2u-c^2\partial_{xx}u=f
\quad\longrightarrow\quad
\ddot u_i-c^2\frac{u_{i-1}-2u_i+u_{i+1}}{\Delta x^2}=f_i
$$

### Modes

$$
\partial_t^2u-c^2\partial_{xx}u=0,\qquad
u(x,t)=\sum_k q_k(t)\sin\!\left(\frac{k\pi}{L}x\right)\quad\text{(exploiting b.c.)}
$$

In the wave equation, using the orthogonality of the modes:

$$
\ddot q_k+\underbrace{\frac{c^2k^2\pi^2}{L^2}}_{\omega_k^2}q_k=0
$$

## From classical to quantum

Wavefunction of the mode $k$:

$$
\psi_{n_k}(q^k)\propto H_{n_k}(\cdot)\,e^{-\frac12 (q^k)^2},\qquad E_k=\left(n_k+\tfrac12\right)\hbar\omega_k
$$

Wavefunction of the system of oscillators:

$$
\Psi(q^1,q^2,\dots)=\psi_1(q^1)\,\psi_2(q^2)\cdots
$$

or, using the occupation-number representation: $|n_1,n_2,\dots\rangle=|n_1\rangle|n_2\rangle\cdots$

- creation/destruction and number operators for each individual mode;
- for independent modes: energy $E=\sum_kE_k$, with $E_k=\hbar\omega_k\left(n_k+\tfrac12\right)$.

:::{warning}
But hey! Even if $n_k=0\ \forall k$, then $E=\sum_{k=1}^{\infty}\tfrac12\hbar\omega_k=\infty$ !!!
:::

*But*: physical systems are made of a finite (even if huge) number of particles $N$, and thus the system has only $N$ modes → so the zero-point energy for mechanical systems is non-$\infty$.

*But* for continuous fields, say $\vec e(\vec r,t)$, we don't have this argument!!

$\rightarrow$ Zero-point energy "can be declared by fiat that this state has zero energy" (as one usually can only measure energy differences!).

