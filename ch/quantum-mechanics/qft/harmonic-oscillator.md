(quantum-mechanics:qft:harmonic-oscillator)=
# Harmonic Oscillator

Harmonic oscillator is used as the fundamental element in [field quantization](quantum-mechanics:qft:field-quantization).

(quantum-mechanics:qft:harmonic-oscillator:classical)=
## Classical model

The Hamiltonian function of a harmonic oscillator is

$$
H=\frac{p^2}{2m}+\frac{m\omega^2x^2}{2} \ .
$$

(quantum-mechanics:qft:harmonic-oscillator:quantization)=
## From classical to quantum

Promoting generalized coordinate and momentum to operators, the Hamiltonian operator of the quantum harmonic oscillator reads

$$
\hat{H} = \frac{\hat p^2}{2m}+\frac{m\omega^2\hat x^2}{2} \ .
$$

(quantum-mechanics:qft:harmonic-oscillator:quantization:stationary-states)=
### Stationary states

The **stationary states** are defined as the eigenstates of the Hamiltonian operators, whose energy level is the corresponding eigenvalue

$$E_n|\psi_n\rangle=\left(\frac{\hat p^2}{2m}+\frac{m\omega^2\hat x^2}{2}\right)|\psi_n\rangle \ ,$$

or in position representation, with decaying wave function at infinity,

$$\left\{\begin{aligned}
& E_n\psi_n=-\frac{\hbar^2}{2m}\psi_n''+\frac{m\omega^2x^2}{2}\psi_n \\
& \psi\big|_{\pm\infty} \to 0 \ .
\end{aligned}\right.$$

A solution exists only for a set of **discrete values** of $E_n$, while for all the other values the b.c. are not satisfied. The feasible solutions of the eigenproblem are

$$
\psi_n(x)=c_nH_n(x)e^{-\frac12x^2},\qquad E_n=\left(\tfrac12+n\right)\hbar\omega
$$

| $n$ | $\psi_n(x)$ | $E_n$ |
|---|---|---|
| 0 | $\psi_0=c_0e^{-x^2/2}$ | $\tfrac12\hbar\omega$ |
| 1 | $\psi_1=c_1x\,e^{-x^2/2}$ | $\tfrac32\hbar\omega$ |
| 2 | $\psi_2=c_2(2x^2-1)e^{-x^2/2}$ | $\tfrac52\hbar\omega$ |
|...| $\dots$ | $\dots$ |

:::{important}
The lowest energy is $\neq0$ because of Heisenberg uncertainty, i.e. a particle can't be exactly in $x=0$ with $p=0$!
:::

```{dropdown} Details of the spectral decomposition of the Hamiltonian operator
:open:

```

(quantum-mechanics:qft:harmonic-oscillator:quantization:creation-annihilation-operators)=
### Creator and annihilation operators

Let's call $\psi_n(x)=|n\rangle$. It's possible to prove (**todo** *prove it!*) that there are two operators 

* $\hat a^\dagger|n\rangle\to|n+1\rangle$, **creation operator**, that moves the state $|n\rangle$ to the state $|n+1\rangle$
* $\hat a|n\rangle\to|n-1\rangle$, **annihilation operator**, that moves the state $|n\rangle$ to the state $|n-1\rangle$

These operators are defined with the following proportionality constants - whose reason appears in the definition of the [number operator](quantum-mechanics:qft:harmonic-oscillator:quantization:number-operator) - 

$$\begin{aligned}
\hat a^\dagger|n\rangle & =\sqrt{n+1}\,|n+1\rangle \\
\hat a|n\rangle & =\sqrt{n}\,|n-1\rangle \ ,
\end{aligned}$$

with the condition

$$
\hat a|0\rangle=0 \ .
$$

With $c=\hbar=1$, creation/destruction in terms of $\hat x,\hat p$:

$$
\hat a^\dagger=\sqrt{\tfrac{\omega}{2}}\left(\hat x+\tfrac{i\hat p}{\omega}\right),\qquad
\hat a=\sqrt{\tfrac{\omega}{2}}\left(\hat x-\tfrac{i\hat p}{\omega}\right)
$$

**[check]** the usual convention has the signs the other way round ($\hat a\propto \hat x+i\hat p/\omega$).

```{dropdown} Details about the action of creation and annihilation operators on eigenstates in position basis
:open:


```

(quantum-mechanics:qft:harmonic-oscillator:quantization:number-operator)=
### Number operator

The number operator is defined as $\hat a^\dagger\hat a=:\hat n$, with $\hat n|n\rangle=n|n\rangle$.

$$
\hat H=\hbar\omega\left(\tfrac12+\hat a^\dagger\hat a\right),\qquad [\hat a,\hat a^\dagger]=1
$$

All these results apply to a single particle, in a 1-dim domain, with a single oscillation frequency.

**TODO**: generalization to more complex systems — is it possible?

---

```{dropdown} old version

##  Creation and destruction

### Motivation

- EM energy is quantized. These quanta (photons) have $E=\hbar\omega$, $\vec p=\hbar\vec k$.
- Photons can be created/destroyed. Example, $\gamma$ emission:
  1. destruction of a high-energy $e^-$,
  2. creation of a lower-energy $e^-$ + $\gamma$.
- $e^-$ can be represented by wavefunctions.
- 1917, A. Einstein: re-derived Planck's law; spontaneous and stimulated emission.

### Models for creation and destruction

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
```
