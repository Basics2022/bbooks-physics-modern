(quantum-mechanics:qft:notes)=
# Introduction to QFT (Via Science) — Lecture Notes

*Natural units $c=\hbar=1$ are used where indicated in the notes.*

:::{note}
Transcription of handwritten notes. Points where the handwriting was ambiguous, or where a sign convention looks inconsistent, are marked with **[check]**.
:::

---

## 1. Creation and destruction

### 1.a Motivation

- EM energy is quantized. These quanta (photons) have $E=\hbar\omega$, $\vec p=\hbar\vec k$.
- Photons can be created/destroyed. Example, $\gamma$ emission:
  1. destruction of a high-energy $e^-$,
  2. creation of a lower-energy $e^-$ + $\gamma$.
- $e^-$ can be represented by wavefunctions.
- 1917, A. Einstein: re-derived Planck's law; spontaneous and stimulated emission.

### 1.b Models for creation and destruction

**Single-frequency oscillators at frequency $\nu$**

- creation → 1 more photon → $\Delta E = h\nu$
- destruction → 1 photon less → $\Delta E = -h\nu$

**Classical oscillator**

$$
H=\frac{p^2}{2m}+\frac{m\omega^2x^2}{2}\quad\longrightarrow\quad
\text{Quantum: }\hat H=\frac{\hat p^2}{2m}+\frac{m\omega^2\hat x^2}{2}
$$

Eigenproblem $E_n|\psi_n\rangle=\left(\frac{\hat p^2}{2m}+\frac{m\omega^2\hat x^2}{2}\right)|\psi_n\rangle$. In position representation:

$$
E_n\psi_n=-\frac{\hbar^2}{2m}\psi_n''+\frac{m\omega^2x^2}{2}\psi_n
\quad\text{+ b.c. s.t. } \psi\big|_{\pm\infty}\to0
$$

A solution exists only for a set of discrete values of $E_n$; for all the other values the b.c. are not satisfied.

$$
\psi_n(x)=c_nH_n(x)e^{-\frac12x^2},\qquad E_n=\left(\tfrac12+n\right)\hbar\omega
$$

| $n$ | $\psi_n(x)$ | $E_n$ |
|---|---|---|
| 0 | $\psi_0=c_0e^{-x^2/2}$ | $\tfrac12\hbar\omega$ |
| 1 | $\psi_1=c_1x\,e^{-x^2/2}$ | $\tfrac32\hbar\omega$ |
| 2 | $\psi_2=c_2(2x^2-1)e^{-x^2/2}$ | $\tfrac52\hbar\omega$ |

:::{important}
The lowest energy is $\neq0$ because of Heisenberg uncertainty, i.e. a particle can't be exactly in $x=0$ with $p=0$!
:::

**Creation / destruction operators**

Let's call $\psi_n(x)=|n\rangle$.

- $\hat a^\dagger|n\rangle\to|n+1\rangle$: moves from the state $|n\rangle$ to the state $|n+1\rangle$
- $\hat a|n\rangle\to|n-1\rangle$

The right proportionality constants give:

$$
\hat a^\dagger|n\rangle=\sqrt{n+1}\,|n+1\rangle,\qquad
\hat a|n\rangle=\sqrt{n}\,|n-1\rangle,\qquad
\hat a|0\rangle=0
$$

With $c=\hbar=1$, creation/destruction in terms of $\hat x,\hat p$:

$$
\hat a^\dagger=\sqrt{\tfrac{\omega}{2}}\left(\hat x+\tfrac{i\hat p}{\omega}\right),\qquad
\hat a=\sqrt{\tfrac{\omega}{2}}\left(\hat x-\tfrac{i\hat p}{\omega}\right)
$$

**[check]** the usual convention has the signs the other way round ($\hat a\propto \hat x+i\hat p/\omega$).

**Number operator**: $\hat a^\dagger\hat a=:\hat n$, with $\hat n|n\rangle=n|n\rangle$.

$$
\hat H=\hbar\omega\left(\tfrac12+\hat a^\dagger\hat a\right),\qquad [\hat a,\hat a^\dagger]=1
$$

All these results apply to a single particle, in a 1-dim domain, with a single oscillation frequency.

**TODO**: generalization to more complex systems — is it possible?

---

## 2. Field quantization

### 2.a Classical system — discretization

$$
\partial_t^2u-c^2\partial_{xx}u=f
\quad\longrightarrow\quad
\ddot u_i-c^2\frac{u_{i-1}-2u_i+u_{i+1}}{\Delta x^2}=f_i
$$

### 2.b Modes

$$
\partial_t^2u-c^2\partial_{xx}u=0,\qquad
u(x,t)=\sum_k q_k(t)\sin\!\left(\frac{k\pi}{L}x\right)\quad\text{(exploiting b.c.)}
$$

In the wave equation, using the orthogonality of the modes:

$$
\ddot q_k+\underbrace{\frac{c^2k^2\pi^2}{L^2}}_{\omega_k^2}q_k=0
$$

### From classical to quantum

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

→ Zero-point energy "can be declared by fiat that this state has zero energy" (as one usually can only measure energy differences!).

---

## 3. Photons

Photons are the quanta of EM fields.

- 3.a Classical EM
- 3.b Towards quantization of the EM field
- 3.c EM cavity (Fermi '31) …

### 3.b Field in 1D free space

Travelling wave along $z$:

$$
\vec A(\vec r,t)=\hat u_x\,b\cos(kz-\omega t+\theta)
$$

$$
b\cos(kz-\omega t+\theta)=b\cos(kz)\cos(\omega t-\theta)+b\sin(kz)\sin(\omega t-\theta)
$$

i.e. a linear combination of 2 standing waves.

**Definitions**

$$
q(t)=b\cos(\omega t-\theta)\ \ (\text{gen. coord.}),\qquad
\dot q(t)=-b\omega\sin(\omega t-\theta)=:p\ \ (\text{gen. mom.}),\qquad
\ddot q=-\omega^2q
$$

$$
\vec A=\hat u_x\left[q\cos(kz)-\frac{p}{\omega}\sin(kz)\right]
$$

In Coulomb gauge:

$$
\vec E=-\partial_t\vec A=-\hat u_x\left[p\cos kz+\omega q\sin kz\right],\qquad
\vec B=\nabla\times\vec A=-\hat u_y\left[kq\sin(kz)+\frac{k}{\omega}p\cos(kz)\right]
$$

**[check]** the $\vec E$ expression above is re-derived from $\dot q=p,\ \dot p=-\omega^2q$; the handwriting is hard to read.

with $\dot q=p$, $\dot p=-\omega^2q$.

**Energy**

$$
H=\tfrac12\left(|\vec E|^2+|\vec B|^2\right)
=\tfrac12\left\{2p^2\cos^2(kz)+2\omega^2q^2\sin^2(kz)+4\omega pq\sin(kz)\cos(kz)\right\}
$$

(using $k^2/\omega^2=1$ as normalization). Averaging over a domain with $L=n\lambda=n\frac{2\pi}{k}$, $n\in\mathbb N$:

$$
\langle H\rangle_L=\tfrac12\left(p^2+\omega^2q^2\right)
$$

**Quantization**: from $q,p$ to $\hat q,\hat p$:

$$
\hat H=\tfrac12\left(\hat p^2+\omega^2\hat q^2\right),\qquad
\hat q=\sqrt{\tfrac{1}{2\omega}}\left(\hat a+\hat a^\dagger\right),\qquad
\hat p=-i\sqrt{\tfrac{\omega}{2}}\left(\hat a-\hat a^\dagger\right)
$$

(**[check]** sign of $\hat p$, chosen to be consistent with the final result below.)

$$
\hat A=\hat u_x\left[\hat q\cos(kz)-\frac{\hat p}{\omega}\sin(kz)\right]
=\hat u_x\sqrt{\tfrac1{2\omega}}\Big\{\cos(kz)(\hat a+\hat a^\dagger)+i\sin(kz)(\hat a-\hat a^\dagger)\Big\}
=\hat u_x\sqrt{\tfrac1{2\omega}}\Big\{\hat a^\dagger e^{-ikz}+\hat a\,e^{ikz}\Big\}
$$

### In a 3D domain

$$
\hat A=\sum_{\vec k,\mu}\vec e_{\vec k\mu}\frac{1}{\sqrt{2\omega_k}}\left\{\hat a^\dagger_{\vec k,\mu}e^{-i\vec k\cdot\vec r}+\hat a_{\vec k,\mu}e^{i\vec k\cdot\vec r}\right\}
$$

$$
\hat H=\sum_{\vec k,\mu}\left(\hat N_{\vec k,\mu}+\tfrac12\right)\hbar\omega_k,\qquad
|\psi\rangle=|\dots n_{\vec k,\mu}\dots\rangle
$$

### 3.c Quantum description of the EM field — classical limit

Example: 1D domain, 1 propagating wave.

$$
A(z,t)=u_x\,b\cos(kz-\omega t+\theta)\ \xrightarrow{\text{quant}}\
\hat A=u_x\sqrt{\tfrac1{2\omega}}\left(\hat a e^{ikz}+\hat a^\dagger e^{-ikz}\right)
$$

How to recover the classical limit?

#### Try 1 — Incoherent states

Let $|\psi\rangle(t)$ be the state with $n$ photons, $|n\rangle$. Time-dependent Schrödinger: $i\hbar|\dot\psi\rangle=\hat H|\psi\rangle$.

$$
|\psi\rangle(t)=c_n(t)|n\rangle,\qquad i\hbar\dot c_n=E_nc_n\ \to\ c_n(t)=c_{n0}\exp\!\left(-\frac{iE_n}{\hbar}t\right)
$$

with $E_n=(n+\tfrac12)\hbar\omega$. For the system in state $|n\rangle$, with $|\psi\rangle_0\equiv|n\rangle\to c_{n0}=1$: $|\psi\rangle_t=\exp(-iE_nt/\hbar)|n\rangle$.

The expected value of the operator $\hat A$ reads

$$
\langle\hat A\rangle=\langle\psi|\hat A|\psi\rangle
=\langle n|\sqrt{\tfrac1{2\omega}}\left(\hat ae^{ikz}+\hat a^\dagger e^{-ikz}\right)|n\rangle
=\frac{e^{ikz}}{\sqrt{2\omega}}\sqrt n\underbrace{\langle n|n-1\rangle}_{=0}+\frac{e^{-ikz}}{\sqrt{2\omega}}\sqrt{n+1}\underbrace{\langle n|n+1\rangle}_{=0}
$$

$$
\Rightarrow\quad\langle\hat A\rangle\equiv0
$$

- At a given time and place, the expected value of $\hat A$ is zero (this is the case of **incoherent light**, random phase).
- The expected value is zero, but the field can be $\neq0$!!

#### Try 2 — Coherent states

Particular superposition of energy states [Glauber '63, "Photon Correlations"].

**Definition**: $\hat a|\psi\rangle=c|\psi\rangle$, with $|\psi\rangle=\sum_{n=0}^{\infty}b_n|n\rangle$. It follows

$$
\hat a|\psi\rangle=\sum_{n=1}^{\infty}b_n\sqrt n\,|n-1\rangle=\sum_{n=0}^{\infty}b_{n+1}\sqrt{n+1}\,|n\rangle=c|\psi\rangle
$$

Exploiting orthogonality of $\{|n\rangle\}$: $c\,b_n=b_{n+1}\sqrt{n+1}$.

**Recursive relation for the coefficients $b_n$:**

$$
\boxed{b_{n+1}=c\,\frac{b_n}{\sqrt{n+1}}}\qquad(\circledast)
$$

If $b_0\neq0$: $b_1=c\,b_0/\sqrt1$, $\ b_2=c\,b_1/\sqrt2=c^2b_0/\sqrt{1\cdot2}$, $\ \dots\ b_n=c^n b_0/\sqrt{n!}$.

Normalization $1=\langle\psi|\psi\rangle=\sum_n|b_n|^2$ gives, using $e^x=\sum_n x^n/n!$:

$$
1=|b_0|^2\sum_{n=0}^{\infty}\frac{|c|^{2n}}{n!}=|b_0|^2e^{|c|^2}\ \Rightarrow\ b_0=e^{-|c|^2/2}\ \ (\text{if } b_0\ \text{is real})
$$

Thus, for a given value of $c$:

$$
|\psi\rangle=\sum_{n=0}^{+\infty}e^{-\frac{|c|^2}{2}}\frac{c^n}{\sqrt{n!}}\,|n\rangle
$$

**Number of photons.** Using the probability $|b_n|^2$ of the system being in state $|n\rangle$:

- expected value of $\hat n$ (~ *signal*):

$$
\langle n\rangle=\sum_{n=0}^{\infty}n|b_n|^2=\sum_{n=0}^{\infty}n\,e^{-|c|^2}\frac{|c|^{2n}}{n!}
=|c|^2\sum_{n=1}^{\infty}e^{-|c|^2}\frac{|c|^{2(n-1)}}{(n-1)!}=|c|^2
$$

- standard deviation / variance $\sigma_n^2$ (~ *quantum noise*):

$$
\sigma_n=\sqrt{\langle(n-\langle n\rangle)^2\rangle}=\dots=\sqrt{\langle n\rangle}=|c|
$$

(The distribution $|b_n|^2$ is a bell-shaped curve centred at $|c|^2$.)

**Expected values of the fields**

*Expected value of $\hat a$:*

$$
\langle\psi|\hat a|\psi\rangle=\sum_{m,n}b^*_{m0}b_{n0}\langle m|\hat a|n\rangle e^{-i(n-m)\omega t}
=\sum_{m,n}b^*_{m0}b_{n0}\sqrt n\,\underbrace{\langle m|n-1\rangle}_{\delta_{m,n-1}}e^{-i\omega t}
=\sum_m b^*_{m0}b_{m+1,0}\sqrt{m+1}\,e^{-i\omega t}
$$

and using the recursion $(\circledast)$:

$$
=\sum_n c\,|b_{n0}|^2e^{-i\omega t}=c\,e^{-i\omega t}
$$

*Expected value of $\hat a^\dagger$:* $\langle\psi|\hat a^\dagger|\psi\rangle=\dots=\sum_nc^*|b_{n0}|^2e^{+i\omega t}=c^*e^{i\omega t}$.

Thus the **expected value of $\hat A$**:

$$
\langle\psi|\hat A|\psi\rangle=u_x\sqrt{\tfrac1{2\omega}}\left\langle\hat a e^{ikz}+\hat a^\dagger e^{-ikz}\right\rangle
=u_x\sqrt{\tfrac1{2\omega}}\left(c\,e^{-i\omega t}e^{ikz}+c^*e^{i\omega t}e^{-ikz}\right)
=u_x\sqrt{\tfrac1{2\omega}}\;2|c|\cos(kz-\omega t+\theta)
$$

with $c=|c|e^{i\theta}$ ≈ **classical electromagnetic wave**.

*Obs.* Time evolution of the state: $|\psi\rangle=\sum_nb_n(t)|n\rangle$. Substituting in $i\hbar|\dot\psi\rangle=\hat H|\psi\rangle$ and using orthogonality: $i\hbar\dot b_n=E_nb_n\to b_n(t)=b_{n0}\exp(-iE_nt/\hbar)$, i.e. $|\psi\rangle=\sum_n\exp(-i\omega_nt)\,b_{n0}|n\rangle$.

*Obs.* With $E_n=\hbar\omega(n+\tfrac12)$: $\omega_m-\omega_n=\omega(m-n)$ — **without the ½ factor!!**

**Summary**

- The expected value of $\hat A$ ~ classical wave.
- The field is a random field whose variance reads:

$$
\sigma_A=\sqrt{\langle\psi|\hat A^2|\psi\rangle-\langle\psi|\hat A|\psi\rangle^2}=\sqrt{\tfrac1{2\omega}}
$$

- *Obs.* The variance is independent of $\vec r,t$ and independent of the number of photons ($|c|^2$). Thus the quantum noise is constant while the signal grows with the field amplitude: **classical limit** — quantum noise → 0 (relative to the signal) as the signal power increases.
- But as the field amplitude goes to zero ($|c|\to0$, # photons → 0), only **quantum fluctuations** remain.

**Heisenberg vs Schrödinger pictures**

- *Heisenberg*: time dependence appears in the operator $\hat A(\vec r,t)$ — **quite convenient!!**
- *Schrödinger*: only space dependence appears in $\hat A$, while $t$ appears in $|\psi\rangle$.

---

## 4. QFT

### 4.a First quantization

particles → waves; $x,p\to\hat x,\hat p$.

$$
i\hbar|\dot\psi\rangle=\hat H|\psi\rangle,\qquad
|\psi\rangle=\sum c_n|\psi_n\rangle\ \ (\text{stationary states}),\qquad
\hat H|\psi_n\rangle=E_n|\psi_n\rangle
$$

$$
1=\langle\psi|\psi\rangle=\sum_n|c_n|^2,\qquad |c_n|^2=\text{probability of being in }|\psi_n\rangle
$$

The Schrödinger equation makes $c_n$ vary continuously. **But** EM radiation occurs in **quantum jumps** ≈

1. destruction of a high-energy $e^-$,
2. creation of a lower-energy $e^-$ + a $\gamma$.

### 2nd quantization of the $e^-$

$$
\psi(x,t)=\sum_kb_k(t)\psi_k(x)=\sum_kb_{k0}\psi_k(x)e^{-i\omega_kt}
$$

($\psi_k$ are the energy eigenfunctions.)

$$
\sum_ki\hbar\dot b_k|k\rangle=\hat H\sum_kb_k|k\rangle\ \to\ b_k=b_{k0}\exp\!\left(-i\frac{E_k}{\hbar}t\right)
$$

$$
\langle\psi|\hat H|\psi\rangle=\sum_{mn}\langle m|\hat H|n\rangle\,b^*_{m0}b_{n0}\,e^{+i\omega_mt}e^{-i\omega_nt}
=\sum_nE_n|b_{n0}|^2,\qquad(E_n\langle m|n\rangle=E_n\delta_{mn})
$$

This is the projection of the wavefunction of the $e^-$ onto the energy eigenfunction.

**2nd quantization:** $b_{k0}\to\hat b_k$ (destruction operator). In analogy with multi-body QM:

$$
\hat H=\sum_kE_k\hat n_k=\sum_kE_k\hat b_k^\dagger\hat b_k
$$

### Jordan–Wigner (1928), "On the Pauli exclusion principle"

The state of an atom is described by the occupation numbers of the orbitals: $|n_1\,n_2\dots\rangle$.

→ Inconsistency of results if $b_1^\dagger b_2^\dagger|0,0\rangle=-b_2^\dagger b_1^\dagger|0,0\rangle$ ⟹ $|1,1\rangle=-1\times|1,1\rangle$ **(!)** — anticommutation relation.

→ Solution of Jordan and Wigner:

$$
\hat b^\dagger_k|\dots n_k\dots\rangle=\theta_k\sqrt{1-n_k}\,|\dots(1-n)_k\dots\rangle,\qquad
\hat b_k|\dots n_k\dots\rangle=\theta_k\sqrt{n_k}\,|\dots(1-n)_k\dots\rangle
$$

with $\theta_k=(-1)^{n_1+\dots+n_{k-1}}$.

### Hamiltonian and state of $e^-$ and radiation fields

$$
e^-:\ |\phi_e\rangle=|n_{e1},n_{e2},\dots\rangle,\quad \hat H_e=\sum_kE_k\hat b_k^\dagger\hat b_k
\qquad\qquad
\text{rad}:\ |\psi_r\rangle=|n_{k\alpha}\dots\rangle,\quad \hat H_{rad}=\sum_{k,\alpha}\hbar\omega_k\hat a^\dagger_{k\alpha}\hat a_{k\alpha}
$$

These are **non-interacting fields**.

An **interaction is required** to get quantum jumps of $e^-$ associated with creation/annihilation of a $\gamma$.

### Bosons and fermions

*(This page of the notes is written upside-down; the content is transcribed in condensed form.)*

**Bosons** — occupation-number formalism:

- $\hat a^\dagger$ acts on a state by raising it, $|0\rangle\to|1\rangle\to|2\rangle\to\cdots$, and $\hat a$ lowers it.
- Number operator: $\hat n_k=\hat a_k^\dagger\hat a_k$, s.t. $\hat n_k|\dots n_k\dots\rangle=n_k|\dots n_k\dots\rangle$.

$$
\hat a^\dagger_k|\dots n_k\dots\rangle=\sqrt{n_k+1}\,|\dots(n_k+1)\dots\rangle,\qquad
\hat a_k|\dots n_k\dots\rangle=\sqrt{n_k}\,|\dots(n_k-1)\dots\rangle
$$

CCR (canonical commutation relations):

$$
[\hat a_k,\hat a^\dagger_{k'}]=\hat a_k\hat a^\dagger_{k'}-\hat a^\dagger_{k'}\hat a_k=\delta_{kk'}
$$

**Fermions** — with occupation-number formalism (Pauli exclusion principle):

- $\hat b^\dagger\hat b^\dagger|0\rangle=0$, and $\hat b\,\hat b|1\rangle=0$ (a second particle cannot be added to an occupied orbital);
- $\hat b|0\rangle=0$, $\hat b^\dagger|1\rangle=0$;
- thus $\{\hat b,\hat b'\}$ and $\{\hat b^\dagger,\hat b'^\dagger\}$ vanish: **anticommutators**, $\{\hat b,\hat b^\dagger\}=1$ (CCR/anticommutation);
- number operator $\hat n=\hat b^\dagger\hat b$ satisfies $\hat n^2=\hat b^\dagger\hat b\hat b^\dagger\hat b=\hat b^\dagger(1-\hat b^\dagger\hat b)\hat b=\hat n$ ⟹ $n=0$ or $1$.

**[check]** Fermion/boson page: written upside-down and partly hard to read; verify against the original.

---

## 5. Interaction and perturbation theory

### Interaction

$$
\hat H=\hat H_{atom}+\hat H_{rad}+\hat H_{inter},\qquad
\hat H_{atom}=\sum E_k\hat b_k^\dagger\hat b_k,\quad
\hat H_{rad}=\sum E_{k,\alpha}\hat a^\dagger_{k,\alpha}\hat a_{k,\alpha}
$$

Examples (space–time diagrams in the notes): all these processes should be weighted by some probability.

- **Absorption** process: $\hat b_n^\dagger\hat b_m\hat a_{k,\alpha}$ — atom $|\psi_m\rangle\to|\psi_n\rangle$, photon $|k,\alpha\rangle$ absorbed.
- **Emission** process: $\hat b_m^\dagger\hat a^\dagger_{k,\alpha}\hat b_n$ — atom $|\psi_n\rangle\to|\psi_m\rangle$, photon $|k,\alpha\rangle$ emitted.

### Perturbation theory

$$
\hat H=\hat H_0+\hat H_{int}
$$

($\hat H_0$: easy-to-solve unperturbed system; $\hat H_{int}$: "small interaction".)

$$
i\hbar|\dot\psi\rangle=(\hat H_0+\hat H_{int})|\psi\rangle,\qquad
|\psi\rangle=\sum_nc_n(t)e^{-i\omega_nt}|\phi_n\rangle
$$

Then

$$
i\hbar\sum_n\left(\dot c_n-i\omega_nc_n\right)e^{-i\omega_nt}|\phi_n\rangle=(\hat H_0+\hat H_{int})\sum_nc_ne^{-i\omega_nt}|\phi_n\rangle
$$

With $\hat H_0|\phi_n\rangle=E_n|\phi_n\rangle$ the $E_n$ terms cancel:

$$
0=\sum_n\left\{i\hbar\dot c_ne^{-i\omega_nt}|\phi_n\rangle-\hat H_{int}c_ne^{-i\omega_nt}|\phi_n\rangle\right\}
$$

Multiplying by $\langle\phi_m|$:

$$
i\hbar\dot c_me^{-i\omega_mt}=\sum_nc_ne^{-i\omega_nt}\langle\phi_m|\hat H_{int}|\phi_n\rangle
\ \Rightarrow\
\dot c_m=\frac1{i\hbar}\sum_nc_ne^{i(\omega_m-\omega_n)t}\langle\phi_m|\hat H_{int}|\phi_n\rangle
$$

an infinite set of equations. Power expansion in a small parameter $\lambda$:

$$
c_m(t)=c_m^{(0)}(t)+\lambda c_m^{(1)}(t)+\lambda^2c_m^{(2)}(t)+\dots
$$

### 0th-order solution

System starting in $|i\rangle$: $c_i(0)=1$, $c_{j\neq i}(0)=0$. Here $H^{int}_{mn}\propto\lambda H^{int}_{mn}$:

$$
\dot c_m^{(0)}+\lambda\dot c_m^{(1)}+\lambda^2\dot c_m^{(2)}+\dots=\frac1{i\hbar}\sum_n\left(c_n^{(0)}+\lambda c_n^{(1)}+\lambda^2c_n^{(2)}+\dots\right)\lambda H^{int}_{mn}e^{i(\omega_m-\omega_n)t}
$$

Check the 0th-order solution (the right way to represent the solution: $c^{(0)}_{n\neq m}(t)\equiv0$, $c_n(t)=\lambda c_n^{(1)}+\lambda^2c_n^{(2)}+\dots$):

- $n=m$: $\dot c^{(0)}_m(t)=\frac1{i\hbar}c^{(0)}_mH^{int}_{mm}$
- $n\neq m$: $\dot c^{(0)}_n(t)=\frac1{i\hbar}c_m^{(0)}(t)H^{int}_{mn}e^{i\omega_{mn}t}$ (with $c^{(0)}_m=1$)

$$
c_m^{(0)}(t)=\begin{cases}\exp\!\left(-\dfrac{iH^{int}_{mm}}{\hbar}t\right)&\text{if i.c. } c^{(0)}_m(0)=1,\ H^{int}_{mm}\neq0\\[2mm] 1&\text{if } H^{int}_{mm}\equiv0\end{cases}
$$

### 1st-order solution

If $H_{mm}=0$, $c_m^{(0)}(t)=1$:

$$
\dot c_n^{(1)}(t)=\frac1{i\hbar}e^{i\omega_{mn}t}H^{int}_{mn}
$$

If $\omega_{mn}\neq0$:

$$
c_n^{(1)}(t)=-\frac1{\hbar\omega_{mn}}e^{i\omega_{mn}t}\Big|_0^tH^{int}_{mn}=\frac{1-e^{i\omega_{mn}t}}{\hbar\omega_{mn}}H^{int}_{mn}
$$

Probabilities (with $c_n^{(0)}\equiv0$ for $n\neq m$):

$$
|c_n(t)|^2=\lambda^2|c_n^{(1)}(t)|^2+\lambda^3\{\dots\}+\dots
$$

Using $(1-e^{i\alpha})^*(1-e^{i\alpha})=2-2\cos\alpha=4\sin^2\frac\alpha2$:

$$
|c_n(t)|^2\sim\lambda^2|H^{int}_{mn}|^2\frac{4\sin^2\!\left(\frac{\omega_{mn}t}{2}\right)}{\hbar^2\omega_{mn}^2}
$$

As $t\to+\infty$ this function goes to **Dirac's delta**:

$$
\int_{\omega=-\infty}^{+\infty}\left\{\frac{\sin(\omega t/2)}{\omega}\right\}^2d\omega=\frac\pi2t
\qquad\text{and}\qquad
|c_n|^2\longrightarrow2\pi t\,|H^{int}_{mn}|^2\,\delta(\omega_m-\omega_n)
$$

(natural units, $\hbar=1$.)

### Fermi golden rule

:::{admonition} Fermi golden rule
- $\hat H_0$ with stationary states $|\phi_n\rangle_t=|\phi_n\rangle e^{-i\omega_nt}$.
- $\hat H_{int}$ causes the state $|i\rangle_t=|\phi_i\rangle e^{-i\omega_it}$ to transition to $|f\rangle=|\phi_f\rangle e^{-i\omega_ft}$ at the rate
$$2\pi\,|M_{mn}|^2\,\delta(\omega_m-\omega_n)\qquad\text{(to the 1st order)}$$
:::

### Higher orders

$$
\dot c_f^{(p+1)}(t)=\frac1{i\hbar}\sum_nc_n^{(p)}(t)\langle f|\hat H^{int}|n\rangle e^{i(\omega_f-\omega_n)t}
$$

E.g. 2nd order: $c_n^{(1)}\propto\langle n|\hat H^{int}|m\rangle\times\frac{1-e^{i\omega_{mn}t}}{\hbar\omega_{mn}}$, so

$$
\dot c_f^{(2)}(t)=\frac1{i\hbar}\sum_n\langle f|\hat H^{int}|n\rangle\langle n|\hat H^{int}|m\rangle\times\frac{1-e^{-i\omega_{mn}t}}{\hbar\omega_{mn}}\,e^{i\omega_{fn}t}
$$

(Diagram in the notes: states $|1\rangle,|2\rangle,|i\rangle,\dots,|I_1\rangle,\dots,|I_2\rangle,\dots,|f\rangle$.)

- 1st order: direct jump $|i\rangle\to|f\rangle$.
- 2nd order: $|i\rangle\to|I\rangle\to|f\rangle$ — need to sum over all possible intermediate states.
- 3rd order: $|i\rangle\to|I_1\rangle\to|I_2\rangle\to|f\rangle$ — need to sum over all possible combinations of intermediate states.

---

## 6. Interacting fields

### 6.a Interacting fields

**Photon field (Heisenberg picture)**

$$
\hat A=\sum_{\vec k,\alpha}\frac{\vec u_{\vec k,\alpha}}{\sqrt{2\omega_k}}\left(\hat a_{\vec k,\alpha}e^{-i\omega_kt}e^{i\vec k\cdot\vec r}+\hat a^\dagger_{\vec k,\alpha}e^{i\omega_kt}e^{-i\vec k\cdot\vec r}\right)
$$

$$
\hat H_r=\sum_{\vec k,\alpha}\hat n_{\vec k,\alpha}\,\hbar\omega_k
$$

(Energy **renormalization**: zero-point energy set $\equiv0$.)

$$
\langle\hat H_r\rangle=\langle\dots n_{\vec k,\alpha}\dots|\hat H_r|\dots n_{\vec k,\alpha}\dots\rangle=\sum_{\vec k,\alpha}n_{\vec k,\alpha}\hbar\omega_k
$$

Natural units: $c=1$, $\hbar=1$.

**Electron field**

$$
\hat\psi(\vec x,t)=\sum_k\hat b_ke^{-i\omega_kt}\varphi_k(\vec r),\qquad
\hat\psi^\dagger(\vec r,t)=\sum_k\hat b^\dagger_ke^{i\omega_kt}\varphi^*_k(\vec r)
$$

($\varphi_k$ are the "orbitals" of the atom.)

$$
\hat H=\frac1{2m_e}\hat p^2+V(\hat x)\quad\text{(Hamiltonian of the electron in the atom)},\qquad
\hat H|\psi_k\rangle=E_k|\psi_k\rangle
$$

**Expected value of $\hat H$.** Let the system be in $|\psi\rangle$; then

$$
\langle\hat H\rangle=\langle\psi|\hat H|\psi\rangle=\int_{x,x'}\langle\psi|x\rangle\langle x|\hat H|x'\rangle\langle x'|\psi\rangle\,dx\,dx'
$$

and with $|\psi\rangle=\sum_kc_k|\phi_k\rangle$:

$$
\langle\hat H\rangle=\sum_{k,k'}\int_xc_k^*\langle\phi_k|x\rangle\langle x|\hat H|\phi_{k'}\rangle c_{k'}\,dx
=\sum_{k,k'}\int_xc_k^*c_{k'}\langle\phi_k|x\rangle E_{k'}\langle x|\phi_{k'}\rangle dx=\dots=\sum_k|c_k|^2E_k
$$

**QFT form of the Hamiltonian**: just replacing the wavefunction $\phi_k(\vec r)$ with the field operator, and $\phi_k^*(\vec r)$ with $\hat\psi^\dagger$:

$$
\hat H_e=\int_x\hat\psi^\dagger(x,t)\hat H\hat\psi(x,t)\,dx
=\int_x\sum_{m,m'}\hat b^\dagger_m\psi_m^*(x)\hat H\hat b_{m'}\psi_{m'}(x)\,dx
$$

$$
=\sum_{m,m'}\int_x\psi_m^*(x)\hat H\psi_{m'}(x)dx\ \hat b_m^\dagger\hat b_{m'}
=\sum_{m,m'}E_{m'}\,\delta_{mm'}\,\hat b_m^\dagger\hat b_{m'}
=\sum_mE_m\hat b_m^\dagger\hat b_m=\sum_mE_m\hat n_m
$$

### Interaction Hamiltonian

Classical mechanics: $\vec p\to\vec p-q\vec a$ (without e.m. field → with e.m. field). Quantum: $\hat p\to\hat p-q\hat a$.

$$
\hat H=\frac{\hat p^2}{2m_e}+V(\hat x)\ \longrightarrow\
\frac{\hat p^2}{2m_e}+\underbrace{\frac{q^2}{2m_e}\left(\hat a_x^2+\hat a_y^2+\hat a_z^2\right)-\frac{q}{m_e}\,\hat p\cdot\hat a}_{\hat H_{int}}+V(\hat x)
$$

Do $\hat p$ and $\hat a$ commute? Likely not! Maybe yes, if $\hat p$ only acts on $e^-$ while $\hat a$ acts on $\vec k,\alpha$.

To get the interaction Hamiltonian, put the 2 extra terms (due to the e.m. field) into the expectation formula:

$$
\hat H=\int_x\sum_m\hat b_m^\dagger\psi_m^*(x)\,\hat H_{int}\sum_n\hat b_n\psi_n(x)\,dx
$$

#### (1) $\vec p\cdot\vec a$ term

$$
\hat H^{(1)}=\int_x\sum_m\dots\frac{q}{m_e}\left(\hat A_x\hat p_x+\hat A_y\hat p_y+\hat A_z\hat p_z\right)\sum_n\dots\,dx
$$

with

$$
\hat A_x=\sum_{\vec k,\alpha}\frac{\{\vec e_{k\alpha}\}_x}{\sqrt{2\omega_k}}\left(\hat a_{\vec k\alpha}e^{i\vec k\cdot\vec x}+\hat a^\dagger_{\vec k\alpha}e^{-i\vec k\cdot\vec x}\right)
$$

- first part: **absorption** (destruction of a $\gamma$),
- second part: **emission** (creation of a $\gamma$),

and $\hat p_x=-i\hbar\partial_x$. For the absorption part along $x$:

$$
\hat H^{(1)}_{abs,x}=-i\hbar\int_x\sum_m\hat b_m^\dagger\psi_m^*(x)\sum_{\vec k,\alpha}\frac{\{\vec e_{k\alpha}\}_x}{\sqrt{2\omega_k}}\hat a_{\vec k\alpha}e^{i\vec k\cdot\vec x}\,\partial_x\sum_n\hat b_n\psi_n(x)\,dx
$$

$$
=-i\hbar\sum_m\sum_n\sum_{\vec k,\alpha}\left[\int_x\psi_m^*(x)\frac{\{\vec e_{k\alpha}\}_x}{\sqrt{2\omega_k}}e^{i\vec k\cdot\vec x}\partial_x\psi_n(x)dx\right]\hat b_m^\dagger\hat a_{\vec k\alpha}\hat b_n
=\sum_m\sum_n\sum_{\vec k,\alpha}M_{abs,x}(m,n,\vec k,\alpha)\,\hat b^\dagger_m\hat b_n\hat a_{\vec k,\alpha}
$$

Collecting all the terms for $x,y,z$, and doing so for the emission part:

$$
\hat H^{(1)}_{abs}=\sum_{m,n,\vec k,\alpha}M_{abs}(m,n,\vec k,\alpha)\,\hat b_m^\dagger\hat b_n\hat a_{\vec k,\alpha}
$$

$$
\hat H^{(1)}_{em}=\sum_{m,n,\vec k,\alpha}M_{em}(m,n,\vec k,\alpha)\,\hat b_m^\dagger\hat b_n\hat a^\dagger_{\vec k,\alpha}
$$

$$
\hat H^{(1)}=\hat H^{(1)}_{abs}+\hat H^{(1)}_{em}
$$

These coefficients determine the probability of the events $\hat b^\dagger_m\hat b_n\hat a^{(\dagger)}_{\vec k,\alpha}$ — **quantum jumps**.

**Energy conservation.** Time-dependent factors have been absorbed in the creation/annihilation operators. It follows that:

- ABS: $\omega_m-\omega_n-\omega_k=0$
- EM: $\omega_m-\omega_n+\omega_k=0$

give the "relevant processes", i.e. those with constant time dependence, as $e^{-i(\dots)t}=1$:

$$
\text{ABS: }\ \omega_k+\omega_n=\omega_m,\qquad\text{EM: }\ \omega_k=\omega_n-\omega_m\qquad(\text{cons. of energy})
$$

#### (2) $a^2$ terms

$$
\hat H^{(2)}=\sum_{m,n}\int_x\hat b_m^\dagger\psi^*_m(x)\,\frac{q^2}{2m_e}\left(\hat a_x^2+\hat a_y^2+\hat a_z^2\right)\sum_n\hat b_n\psi_n(x)\,dx
$$

with $\hat a_x=\sum_{\vec k,\alpha}\frac{\{\vec e_{k\alpha}\}_x}{\sqrt{2\omega_k}}\left(\hat a_{\vec k\alpha}e^{i\vec k\cdot\vec x}+\hat a^\dagger_{\vec k\alpha}e^{-i\vec k\cdot\vec x}\right)$, hence

$$
\hat a_x^2=\sum_{\vec k,\alpha}\sum_{\vec l,\beta}\frac{\{\vec e_{k\alpha}\}_x\{\vec e_{l\beta}\}_x}{\sqrt{2\omega_k}\sqrt{2\omega_l}}\left(\hat a_{k\alpha}e^{i\vec k\cdot\vec x}+\hat a^\dagger_{k\alpha}e^{-i\vec k\cdot\vec x}\right)\left(\hat a_{l\beta}e^{i\vec l\cdot\vec x}+\hat a^\dagger_{l\beta}e^{-i\vec l\cdot\vec x}\right)
$$

**4 types of terms (3 types):**

- 2 destructions
- 2 creations
- 1 destruction & 1 creation (two orderings, counted as one type)

→ **2-photon processes**, much weaker than the 1-photon processes. (Space–time diagrams with two photon lines are drawn in the notes.)

\* Conservation of energy just provides **one** constraint → there's a *continuum* of possible interactions.

$$
\hat H_{int}=\hat H^{(1)}_{int}+\hat H^{(2)}_{int}=\hat H^{(1)}_{abs}+\hat H^{(1)}_{em}+\hat H^{(2)}_{int}
$$

### Dipole approximation

Usually the size of the atom (e.g. $H_2$) orbitals $\propto10^{-9}$ m, while $\lambda_{EM,\,jump}\propto10^{-7}$ m. Thus $\vec k\cdot\vec x$ is small within the atom:

$$
e^{i\vec k\cdot\vec x}=1+i\vec k\cdot\vec x+\dots\sim1\qquad\Rightarrow\qquad\textbf{DIPOLE APPROXIMATION}
$$

In the dipole approximation the ABS and EM coefficients are identical.

---

## 7. Selection rules

### Interesting physical interpretation using angular momentum

Quantum numbers $n,\ell,m_\ell,m_s$.

- $E\propto\frac1{n^2}$ (energy)
- $L=\sqrt{\ell(\ell+1)}\,\hbar$: $|\vec L|$ is known, but not the direction in space.
  - $\ell=0\to L=0$ (s orbital)
  - $\ell=1\to L=\sqrt2\,\hbar$ (p orbital)
- $m_\ell\to$ $z$-component of orbital angular momentum
- $m_s\to$ $z$-component of spin

**Photon angular momentum:** $\sqrt2\,\hbar$.

**Angular momentum conservation** (feasible jumps):

$$
\gamma+s\to p,\qquad p\to\gamma+s
$$

---

## 8. Linear momentum

*Smells like Compton effect.*

**Before:** atom at rest; photon momentum

$$
p=\hbar k=\hbar\omega\frac k\omega=\frac Ec
$$

**After:** atom moving with $V_{atom}$:

$$
p_\gamma=p_{atom}\simeq m\,V_{atom}\ \ (\sim m_{proton}V_{atom})
\ \ \to\ \ V_{atom}\simeq\frac{E}{m_pc}\ \ \left(\sim3\ \mathrm{m/s}\ \text{for a }1s\to2p\text{ transition}\right)
$$

The **nucleus** absorbs the $\gamma$ linear momentum.

### Example 1: $1s+\gamma\to2p$ (absorption)

$$
|i\rangle=|1,0,\dots\rangle_a\,|0\dots n_{\vec k\alpha}\dots0\rangle_r=|1_1\rangle_a|n_{\vec k\alpha}\rangle_r
$$

$$
|f\rangle=|0,0,1,0,\dots\rangle_a\,|0\dots(n-1)_{\vec k\alpha}\dots0\rangle_r=|1_3\rangle_a|(n-1)_{\vec k\alpha}\rangle_r
$$

1-photon interaction: absorption of $\gamma$ ∝ $\hat b_3^\dagger\hat b_1\hat a_{\vec k\alpha}$, modulated by $M(3,1,\vec k,\alpha)$.

$$
|M_{fi}|^2=|\langle f|\hat H_{int}|i\rangle|^2
=\Big|\langle1_3|_a\langle(n-1)_{\vec k\alpha}|_r\ M(3,1,\vec k,\alpha)\,\hat b_3^\dagger\hat b_1\hat a_{\vec k\alpha}\,|1_1\rangle_a|n_{\vec k\alpha}\rangle_r\Big|^2
$$

$$
=\left|\sqrt{n_{\vec k,\alpha}}\,M(3,1,\vec k,\alpha)\right|^2=n_{\vec k,\alpha}\,|M(3,1,\vec k,\alpha)|^2
$$

(here $\hat a_{\vec k\alpha}|n\rangle=\sqrt n|n-1\rangle$ and $\hat b_3^\dagger\hat b_1|1_1\rangle=|1_3\rangle$.)

:::{important}
The transition rate ∝ the **number of photons in the state $\vec k,\alpha$**.
:::

This can be used in the Fermi golden rule.

### Example 2: emission process $2p\to1s+\gamma$

$$
|i\rangle=|1_3\rangle_a|n_{\vec k\alpha}\rangle_r,\qquad|f\rangle=|1_1\rangle_a|(n+1)_{\vec k\alpha}\rangle_r
$$

$$
|M_{fi}|^2=|\langle f|\hat H_{int}|i\rangle|^2=\left|\langle f|M_e(1,3,\vec k,\alpha)\,\hat b_1^\dagger\hat b_3\hat a^\dagger_{\vec k\alpha}|i\rangle\right|^2
=\underbrace{(n_{\vec k,\alpha}+1)}_{\substack{n:\ \text{stimulated emission}\\1:\ \text{spontaneous emission}}}\ \underbrace{|M(1,3,\vec k,\alpha)|^2}_{\text{symmetry properties}}
$$

### Revisiting Einstein coefficients (1917)

---

## 9. Photon–$e^-$ scattering

A free $e^-$ can't absorb a $\gamma$ (conditions about conservation of $E$ and $\vec p$ cannot be met simultaneously).

→ no $\hat H^{(1)}$ processes
→ $\hat H^{(2)}$ is the **dominant interaction**!

→ a free $e^-$ with given momentum is completely **not-localized**
→ Feynman diagrams are not to be taken literally.

→ Conditions about **conservation of momentum** in scattering!
→ Conditions about **conservation of energy**.
→ Alignment of the photon polarization.

**Transition rate** …

$$
2\pi\left(\frac{q^2}{2m_e}\right)^2\frac{\left(\vec e_{k\alpha}\cdot\vec e_{l\beta}\right)^2}{\omega_k\omega_l}\ M_{e,p}\ \big(n_{\vec k\alpha}\ \ ,\ +1\big)
$$

Annotations in the notes: $n_{\vec k\alpha}$ = "photon in initial state"; the $(+1)$ term = "spontaneous + stimulated scattering"; $(\vec e_{k\alpha}\cdot\vec e_{l\beta})^2$ = "alignment of the photon polarization".

**[check]** Final formula: the exact placement of the factors $n_{\vec k\alpha}$ and $(n_{\vec l\beta}+1)$, and the $M_{e,p}$ term, are hard to read; verify against the original.

(In the notes, a small diagram shows the initial state $|\vec p\rangle$ + photon $|\vec k,\alpha\rangle$ → final state $|\vec p'\rangle$ + photon $|\vec l,\beta\rangle$ in a space–time plot.)
