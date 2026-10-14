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

Let $\xi = a x$. Then, as $\frac{d}{dx} = \frac{d \xi}{d x} \frac{d}{d \xi} = a \frac{d}{d \xi}$ the equation can be recast as

$$E_n \psi_n(\xi) = - a^2 \frac{\hbar^2}{2 m} \psi''_n(\xi) + \frac{m \omega^2 \xi^2}{2 a^2} \psi_n(\xi) \ .$$

Defining

$$a = \sqrt{\frac{m \omega}{\hbar}} \quad , \quad \lambda_n = \frac{E_n}{\hbar \omega} \ ,$$

the equation becomes

$$\psi''_n(\xi) + (\lambda_n - \xi^2) \psi_n(\xi) = 0 \ .$$

**Asymptotic behavior.** For $|\xi| \rightarrow +\infty$, the elastic term dominates the eigenvalue term, and thus

$$\begin{aligned}
 0 
 & \simeq - \psi'' + \xi^2 \psi \ .
\end{aligned}$$

The asymptotic behavior reads $\psi_{n,\infty}(\xi) = e^{-\xi^2/2}$. This can be checked evaluating the first two derivatives

$$\begin{aligned}
  \frac{d}{d\xi} e^{-\xi^2/2} & = - \xi e^{-\xi^2/2} \\
  \frac{d^2}{d\xi^2} e^{-\xi^2/2} & = \left( -1 + \xi^2 \right) e^{-\xi^2/2} \ .
\end{aligned}$$

and comparing the leading order contributions $O(\xi^2 e^{-\xi^2/2})$.

**Full solution.** Let the solution be $\psi(\xi) = h(\xi) e^{-\xi^2/2}$, with unknown $h(\xi)$. Its derivatives read

$$\begin{aligned}
  \dfrac{d}{d \xi} \psi & = \left( h' - \xi h \right) e^{-\xi^2/2} \\
  \dfrac{d^2}{d \xi^2} \psi & = \left( h'' - h - 2 \xi h' + \xi^2 h \right) e^{-\xi^2/2} \\
\end{aligned}$$



Introducing this expression in the differential equation

$$\begin{aligned}
  0 & = ( \lambda - \xi^2 ) h(\xi) + ( h''(\xi) - h(\xi) - 2 \xi h'(\xi) + \xi^2 h(\xi) )  \ .
\end{aligned}$$

Let the power expansion of $h(\xi)$ be

$$h(\xi) = \sum_{k=0}^{+\infty} c_k \xi^k \ ,$$

thus the equation becomes

$$\begin{aligned}
 0 
 & = (\lambda - \xi^2) \sum_{k=0}^{+\infty} c_k \xi^k + \sum_{k=0}^{+\infty} k (k-1) c_k \xi^{k-2} - \sum_{k=0}^{+\infty} c_k \xi^k - 2 \xi \sum_{k=0}^{+\infty} k \, c_k \xi^{k} + \xi^2 \sum_{k=0}^{+\infty} c_k \xi^k = \\
 & = (\lambda - \xi^2) \sum_{k=0}^{+\infty} c_k \xi^k + \sum_{k=2}^{+\infty} k (k-1) c_k \xi^{k-2} - \sum_{k=0}^{+\infty} c_k \xi^k - 2 \xi \sum_{k=1}^{+\infty} k \, c_k \xi^{k-1} + \xi^2 \sum_{k=0}^{+\infty} c_k \xi^k = \\
 & = (\lambda - \xi^2) \sum_{k=0}^{+\infty} c_k \xi^k + \sum_{k=0}^{+\infty} (k+2) (k+1) c_{k+2} \xi^{k} - \sum_{k=0}^{+\infty} c_k \xi^k - 2 \xi \sum_{k=0}^{+\infty} (k+1) \, c_{k+1} \xi^{k} + \xi^2 \sum_{k=0}^{+\infty} c_k \xi^k = \\
 & = \dots \\
\end{aligned}$$




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
\hat a^\dagger=\sqrt{\tfrac{m\omega}{2\hbar}}\left(\hat x-\tfrac{i\hat p}{m\omega}\right),\qquad
\hat a=\sqrt{\tfrac{m\omega}{2\hbar}}\left(\hat x+\tfrac{i\hat p}{m\omega}\right)
$$


```{dropdown} Creation and annihilation operators, and the Hamiltonian
:open:

$$\begin{aligned}
  \hat{H}
  & = \frac{\hat{p}^2}{2 m} + \frac{m \omega^2 \hat{x}^2}{2} = \\
  & = \hbar \omega \underbrace{ \sqrt{\frac{m \omega}{2 \hbar}} \left( \hat{x} - i \frac{\hat{p}}{m \omega} \right)}_{= \hat{a}^\dagger} \underbrace{\sqrt{\frac{m\omega}{2 \hbar}} \left( \hat{x} + i \frac{\hat{p}}{m \omega} \right)}_{=\hat{a}} - i \hbar \omega \frac{m \omega}{2 \hbar} \underbrace{\left( \hat{x} \frac{\hat{p}}{m \omega} - \frac{\hat{p}}{m \omega} \hat{x} \right)}_{\frac{1}{m \omega}[\hat{x}, \hat{p}] = \frac{i \hbar}{m \omega}} = \\
  & = \hbar\omega \left( \hat{a}^\dagger \hat{a} + \frac{1}{2} \right) \ . 
\end{aligned}$$

```

```{dropdown} Commutation of annihilation and creation operator
:open:

$$\begin{aligned}
  \left[ \hat{a}, \hat{a}^\dagger \right]
  & = \frac{m\omega}{2\hbar} \left[ \hat{x} + i \frac{\hat{p}}{m\omega}, \hat{x} - i \frac{\hat{p}}{m\omega}\right] = \\
  & = \frac{m\omega}{2\hbar} \left\{ -\frac{i}{m\omega} [ \hat{x}, \hat{p} ] + \frac{i}{m\omega} [ \hat{p}, \hat{x} ] \right\} = \\
  & = - i \frac{1}{2\hbar} \left\{ [ \hat{x}, \hat{p} ] + [ \hat{x}, \hat{p} ] \right\} = \\
  & = - i \frac{1}{2\hbar} \cdot 2 i \hbar = \\
  & = 1 \ .
\end{aligned}$$

```

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
