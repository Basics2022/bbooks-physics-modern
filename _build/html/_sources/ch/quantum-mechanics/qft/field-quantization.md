(quantum-mechanics:qft:field-quantization)=
# Field quantization

First, a [classical system](quantum-mechanics:qft:field-quantization:classical) governed by a wave equation is discussed, along with its mode decomposition: a general solution can be written as the superposition of modes $u(x,t) = \sum_k q_k(t) n_k(x)$ whose contribution is modulated by coefficients $q_k(t)$ satisfying the ODE of a ["single-frequency" harmonic oscillator](quantum-mechanics:qft:harmonic-oscillator). Thus, quantization of the system is performed in the modal basis using the same procedure used for the "single-frequency" harmonic oscillator.

(quantum-mechanics:qft:field-quantization:classical)=
## Classical system

Let a classical field $u(x,t)$ be governed by the wave equation

$$
\partial_t^2u-c^2\partial_{xx}u=f \ ,
$$

supplied with proper initial and boundary conditions. This equation is usually the continuous model (exploiting **continuum hypotesis**, or some equivalent principle) of a macroscopic system, made of a huge number - but **finite** number - of sub-systems at the microscopic level. This is quite a relevant remark, as continuous models have an infinite number of modes, while discrete models with a finite number of sub-systems have a finite number of modes.

The wave equation is a PDE that can be interpreted as the continuous counter-part of a set of ODE for the sub-systems of a discrete model, e.g.

$$
\ddot u_i-c^2\frac{u_{i-1}-2u_i+u_{i+1}}{\Delta x^2}=f_i \ ,
$$

having used centered finite difference for the second-order space derivative.
As done in [mechanics of elastic structures](https://basics2022.github.io/bbooks-physics-continuum-mechanics/ch/solids/intro.html), the solution of the continuous equation can be written in the modal basis, that is computed as all the possible standing waves of the homogeneous problem

$$
\partial_t^2u-c^2\partial_{xx}u=0
$$

supplied with homogeneous boundary conditions $u(0) = u(L) = 0$, using the methods of separation of variables. Modes are the set of functions
$n_k(x) = \sin \left( \frac{k \pi}{L} x \right)$, with $k \in \mathbb{N}^+$. The general solution can be written as a linear combination of the modes

$$
u(x,t)=\sum_k q_k(t)\sin\!\left(\frac{k\pi}{L}x\right) \ ,
$$

with time-dependent coefficients $q_k(t)$ satisfying the harmonic oscillator uncoupled ODEs

$$
\ddot q_k+\underbrace{\frac{c^2k^2\pi^2}{L^2}}_{\omega_k^2}q_k=0 \ .
$$ (eq:field-quantization:classical:mode-ode)

An **energy density** of the system can be defined as

$$e(x,t) :=  \frac{|\partial_t u|^2}{2} + c^2 \frac{|\partial_x u|^2}{2} \ .$$

and the energy in the whole domain is

$$\begin{aligned}
 E 
 & = \int_{x=0}^{L} e(x,t) \, dx = \\
 & = \int_{x=0}^{L} \left\{ \frac{1}{2} \sum_{k, k'} \dot{q}_k \dot{q}_{k'} \sin\left( \frac{k \pi x}{L}\right) \sin\left( \frac{k' \pi x}{L} \right) + \frac{1}{2} \sum_{k,k'} c^2 q_k q_{k'} \frac{k k' \pi^2}{L^2} \cos \left( \frac{k \pi x}{L} \right) \cos \left( \frac{k' \pi x}{L} \right) \right\} \, dx = \\
 & = \frac{L}{2} \left\{ \frac{1}{2} \sum_{k} \dot{q}_k^2 + \frac{1}{2} \sum_{k} c^2 \frac{k^2 \pi^2}{L^2} q_k^2 \right\}  = \\
 & = \frac{L}{2} \sum_{k} \left\{ \frac{1}{2} \dot{q}_k^2 + \frac{1}{2} \omega_k^2 q_k^2 \right\}  = \\
 & = \sum_{k} E_k(q^k, \dot{q}^k) \ ,
\end{aligned}$$

having exploited orthogonality of the modes. The latter expression shows that the total energy can be written as the sum of energy contributions from the different modes. As the amplitudes of the modes satisfy the harmonic oscillator ODE, then they can be written as

$$\begin{aligned}
  q_k(t)       & = Q_k e^{i ( \omega_k t + \varphi_k)} + c.c. = 2 Q_k \cos( \omega_k t + \varphi_k ) \\
  \dot{q}_k(t) & = i \omega_k Q_k e^{i (\omega_k t + \varphi_k)} + c.c. = - 2 \omega_k Q_k \sin( \omega_k t + \varphi_k ) \\
\end{aligned}$$

and the energy in the domain becomes

$$\begin{aligned}
  E
  & = \frac{L}{4} \sum_k \left\{ 4 \omega_k^2 Q_k^2 \sin^2( \omega_k t + \varphi_k ) + \omega_k^2 4 Q_k^2 \cos^2( \omega_k t + \varphi_k ) \right\} = \\
  & = L \sum_k \omega_k^2 Q_k^2 \ ,
\end{aligned}$$

so that the elementary contribution of the $k^{th}$ mode to the energy of the system is $E_k = L \omega^2_k Q_k^2$.


(quantum-mechanics:qft:field-quantization:quantization)=
## From classical to quantum

The amplitude $q_k(t)$ of mode $k$ is governed by the dynamical equation {eq}`eq:field-quantization:classical:mode-ode`, compatible with the Hamiltonian

$$H_k(q^k,p_k) = \frac{p_k^2}{2} + \frac{\omega_k^2 (q^k)^2}{2} \ .$$

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

### Infinite energy

Even if $n_k=0\ \forall k$, then $E=\sum_{k=1}^{\infty}\tfrac12\hbar\omega_k=\infty$.

**But** physical systems are made of a **finite number** (even if huge) of particles $N$, and thus the system has only $N$ modes: so the zero-point energy for mechanical systems is non-$\infty$.

*But* for continuous fields, say $\vec e(\vec r,t)$, we don't have this argument: as it's usually possible to measure only energy differences, zero-point energy "can be declared by fiat", i.e. "the vacuum state has zero energy".

