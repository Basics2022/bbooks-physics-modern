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

````{dropdown} Details of the spectral decomposition of the Hamiltonian operator

Let $\xi = a x$. Then, as $\frac{d}{dx} = \frac{d \xi}{d x} \frac{d}{d \xi} = a \frac{d}{d \xi}$ the equation can be recast as

$$E_n \psi_n(\xi) = - a^2 \frac{\hbar^2}{2 m} \psi''_n(\xi) + \frac{m \omega^2 \xi^2}{2 a^2} \psi_n(\xi) \ .$$

Defining $a = \sqrt{\frac{m \omega}{\hbar}}$, $\lambda_n = \frac{2 E_n}{\hbar \omega}$, the equation becomes

$$\psi''_n(\xi) + (\lambda_n - \xi^2) \psi_n(\xi) = 0 \ .$$

```{dropdown} Asymptotic behavior

For $|\xi| \rightarrow +\infty$, the elastic term dominates the eigenvalue term, and thus

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

```

```{dropdown} Full solution

Let the solution be $\psi(\xi) = h(\xi) e^{-\xi^2/2}$, with unknown $h(\xi)$. Its derivatives read

$$\begin{aligned}
  \psi'  & = \left( h' - \xi h \right) e^{-\xi^2/2} \\
  \psi'' & = \left( h'' - h - 2 \xi h' + \xi^2 h \right) e^{-\xi^2/2} \\
\end{aligned}$$

Introducing this expression in the differential equation, and removing the term $e^{-\xi^2/2} \ne 0$,

$$\begin{aligned}
  0 
  & = ( \lambda - \xi^2 ) h(\xi) + ( h''(\xi) - h(\xi) - 2 \xi h'(\xi) + \xi^2 h(\xi) ) = \\
  & = \lambda h(\xi) + h''(\xi) - h(\xi) - 2 \xi h'(\xi)  \ .
\end{aligned}$$

Let the power expansion of $h(\xi)$ be

$$h(\xi) = \sum_{k=0}^{+\infty} c_k \xi^k \ ,$$

thus the equation becomes

$$\begin{aligned}
 0 
 & = \lambda \sum_{k=0}^{+\infty} c_k \xi^k + \sum_{k=0}^{+\infty} k (k-1) c_k \xi^{k-2} - \sum_{k=0}^{+\infty} c_k \xi^k - 2 \xi \sum_{k=0}^{+\infty} k \, c_k \xi^{k-1} = \\
 & = \lambda \sum_{k=0}^{+\infty} c_k \xi^k + \sum_{k=0}^{+\infty} (k+2) (k+1) c_{k+2} \xi^{k} - \sum_{k=0}^{+\infty} c_k \xi^k - 2 \sum_{k=0}^{+\infty} k \, c_k \xi^{k} = \\
 & = \sum_{k=0}^{+\infty} \left\{ - \left( - \lambda + 1 + 2k \right) c_k + \left( k + 2 \right) \left( k + 1 \right) c_{k+2} \right\} \xi^k \ .
\end{aligned}$$

This equation implies the a recursion relation between the coefficients of the power expansion

$$c_{k+2} = \frac{2k + 1 - \lambda}{(k+2)(k+1)} c_k \ .$$ (eq:hermite:recurrence)

```

```{dropdown} Symmetry of the solutions

The recurrence relation {eq}`eq:hermite:recurrence` involves coefficients with the same parity, $c_k$ and $c_{k+2}$. Thus it's possible to select:

* even solutions, by setting $c_1 = 0$, that implies $c_3 = c_5 = \dots = 0$
* odd  solutions, by setting $c_0 = 0$, that implies $c_2 = c_4 = \dots = 0$

```

```{dropdown} Asymptotic behavior of the power series

Let's discuss even solution here. The discussion for odd solutions is identical.

**Even solutions.** Let $c_1 = 0$. Then the power series of $h(\xi)$ only contains even powers

$$h(\xi) = \sum_{m=0}^{+\infty} c_{2m} \xi^{2m} \ .$$

For "large" $m$, the recurrence relation becomes

$$c_{2m+2} \sim \frac{2}{2m} c_{2m} = \frac{c_{2m}}{m} \sim \frac{c_{2m}}{m+1} \ ,$$

so that the asymptotic behavior of the **infinite power series** becomes

$$h(\xi) = \dots + \sum_{m=1}^{+\infty} c_{2m} \xi^{2m} = \dots + c_0 \sum_{m=0}^{+\infty} \frac{\xi^{2m}}{m!} = \dots + e^{\xi^2} \ .$$

Thus, the asymptotic behavior of the full solution, $\psi(\xi) = e^{-\xi^2/2} h(\xi)$, is $\psi(\xi) \sim e^{-\xi^2/2} e^{\xi^2} = e^{\xi^2/2}$, for $\xi \rightarrow \mp +\infty$. As the boundary conditions of the original problem implies $\psi(\xi \rightarrow \mp \infty) \rightarrow 0$, this asymptotic behavior is not allowed, and thus the power series can't have an infinite number of terms. Thus the recurrence relation provides a **stopping criterion**.

If $c_{n+2} = 0$ is the first zero coefficient with that parity (i.e. $c_{n+1} = 0$), then the last non-zero term is $c_n$. The recurrence relation provides the condition

$$\lambda_n = 2 n + 1 \ .$$

The following table contains the first solutions (not normalized, not orthogonal **!** )

| $k$ | $\lambda_k$ | $E_k =  \frac{\hbar \omega}{2} \lambda_k = \hbar \omega \left( k + \frac{1}{2} \right)$ | $\psi_k(\xi)$ |
| :---: | :---: | :---: | :--- |
| $0$ | $1$ | $\tfrac{1}{2} \hbar \omega$ | $c_0 e^{-\xi^2/2}$   | 
| $1$ | $3$ | $\tfrac{3}{2} \hbar \omega$ | $c_1 x e^{-\xi^2/2}$ | 
| $2$ | $5$ | $\tfrac{5}{2} \hbar \omega$ | $c_0 \left( 1 - x^2 \right) e^{-\xi^2/2}$ | 
| $3$ | $7$ | $\tfrac{7}{2} \hbar \omega$ | $c_1 \left( x - \tfrac{2}{3} x^3 \right) e^{-\xi^2/2}$ | 


```


````

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

$$\begin{aligned}
  \hat{H}
  & = \frac{\hat{p}^2}{2 m} + \frac{m \omega^2 \hat{x}^2}{2} = \\
  & = \hbar \omega \underbrace{ \sqrt{\frac{m \omega}{2 \hbar}} \left( \hat{x} - i \frac{\hat{p}}{m \omega} \right)}_{= \hat{a}^\dagger} \underbrace{\sqrt{\frac{m\omega}{2 \hbar}} \left( \hat{x} + i \frac{\hat{p}}{m \omega} \right)}_{=\hat{a}} - i \hbar \omega \frac{m \omega}{2 \hbar} \underbrace{\left( \hat{x} \frac{\hat{p}}{m \omega} - \frac{\hat{p}}{m \omega} \hat{x} \right)}_{\frac{1}{m \omega}[\hat{x}, \hat{p}] = \frac{i \hbar}{m \omega}} = \\
  & = \hbar\omega \left( \hat{a}^\dagger \hat{a} + \frac{1}{2} \right) \ . 
\end{aligned}$$

```

```{dropdown} Commutation of annihilation and creation operator

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

The $n$ mode in space basis reads

$$\psi_n(x) = e^{-x^2/2} h_n(x) = e^{-x^2/2} \sum_{k=0}^{n} c_k x^k \ ,$$

with the coefficients of the power series linked by the recurrence relation {eq}`eq:hermite:recurrence`. The application of the position operator gives 

$$x \psi_n(\xi) = \sqrt{\frac{\hbar}{m \omega}} \, \xi \psi_n(\xi) \ ,$$

while the application of the momentum operator (on an even function, with $c_1 = 0$) gives, recalling that $\xi = x \sqrt{\tfrac{m \omega}{\hbar}}$, and thus $\partial_x = \xi'(x) \partial_\xi = \sqrt{\tfrac{m\omega}{\hbar}} \partial_{\xi}$,

$$\begin{aligned}
  \langle x | \hat{p} | \psi_n \rangle 
  & = - i \hbar \partial_x \psi_n(x) = \\
  & = - i \hbar \sqrt{\frac{m \omega}{\hbar}} \left\{ -\xi \sum_{k=0}^{n} c_k \xi^k + \sum_{k=0}^{n} k c_k \xi^{k-1} \right\} e^{-\xi^2/2} = \\
  & = - i \hbar \sqrt{\frac{m \omega}{\hbar}} \left\{ - \sum_{k=0}^{n} c_k \xi^{k+1} + \underbrace{c_1}_{=0} + \sum_{k=0}^{n} ( k + 2) c_{k+2} \xi^{k+1} \right\} e^{-\xi^2/2} = \\
  & = - i \hbar \sqrt{\frac{m \omega}{\hbar}} \left\{ - \sum_{k=0}^{n} \left( c_k - (k+2) c_{k+2} \right) \xi^{k+1} \right\} e^{-\xi^2/2} \ .
\end{aligned}$$

**Creation operator** gives

$$\begin{aligned}
  & \sqrt{\frac{m \omega}{2 \hbar}} \left\langle x \left| \hat{x} - i \frac{\hat{p}}{m \omega} \right| \psi_n \right\rangle = \\
  & \quad = \sqrt{\frac{m \omega}{2 \hbar}} \left\{ \sqrt{\frac{\hbar}{m \omega}} e^{-\xi^2/2} \sum_{k=0}^{n} c_k \xi^{k+1} - \frac{i}{m \omega} \cdot \left( i \hbar \right) \cdot\sqrt{\frac{m\omega}{\hbar}} \sum_{k=0}^{n} \left( c_k - (k+2) c_{k+2} \right) \xi^{k+1} \right\} = \\
  & \quad = \frac{1}{\sqrt{2}} e^{-\xi^2/2} \left\{ \sum_{k=0}^{n} c_k \xi^{k+1} + \sum_{k=0}^{n} \left( c_k - (k+2) c_{k+2} \right) \xi^{k+1} \right\} = \\
  & \quad = \frac{1}{\sqrt{2}} e^{-\xi^2/2} \sum_{k=0}^{n} \left( 2 c_k - (k+2) c_{k+2} \right) \xi^{k+1} = \\
  & \quad = \frac{1}{\sqrt{2}} e^{-\xi^2/2} \sum_{k=0}^{n} c_k \left( 2 - \frac{2k+1-\lambda_n}{k+1} \right) \xi^{k+1} = \\
  & \quad = \frac{1}{\sqrt{2}} e^{-\xi^2/2} \sum_{k=0}^{n} \underbrace{c_k \left( \frac{2 n + 2}{k+1} \right)}_{=:d_{k+1}} \xi^{k+1} \ ,
\end{aligned}$$

with $\lambda_n = 2 n + 1$

$$d_{k+1} = c_k \frac{2n+2}{k+1} \ ,$$

and thus

$$\begin{aligned}
  d_{k+3}
  & = c_{k+2} \frac{2n+2}{k+3} = \\
  & = -2 c_{k} \frac{n-k}{(k+1)(k+2)} \frac{2n+2}{k+3} = \\
  & = -2 \frac{n-k}{(k+2)(k+3)} \left( c_k \frac{2n+2}{k+1} \right) = \\
  & = -2 \frac{(n+1)-(k+1)}{(k+2)(k+3)} d_{k+1} = \\
  & = -2 \frac{(n+1)-(k+1)}{(k+2)(k+3)} d_{k+1} \ ,
\end{aligned}$$

and, recognizing the degree of the expansion $n+1$, it follows 

$$d^{(n+1)}_{k+3} = - 2 \frac{(n+1) - (k+1)}{(k+2)(k+3)} d_{k+1}^{(n+1)} \ ,$$

compatible with the recurrence relation 

$$
 c_{k+2}^{(n)} = \frac{2k+1 - \lambda_n}{(k+1)(k+2)} c_k^{(n)} = - 2 \frac{n-k}{(k+1)(k+2)} c_k^{(n)} \ .
$$

**Annihilation operator.** Algebra is left as an exercise for readers or contributors...


```

(quantum-mechanics:qft:harmonic-oscillator:quantization:number-operator)=
### Number operator

The number operator is defined as $\hat a^\dagger\hat a=:\hat n$, with $\hat n|n\rangle=n|n\rangle$.

$$
\hat H=\hbar\omega\left(\tfrac12+\hat a^\dagger\hat a\right),\qquad [\hat a,\hat a^\dagger]=1
$$

All these results apply to a single particle, in a 1-dim domain, with a single oscillation frequency.

**TODO**: generalization to more complex systems — is it possible?


(quantum-mechanics:qft:harmonic-oscillator:classical-limit)=
## Classical limit

(quantum-mechanics:qft:harmonic-oscillator:classical-limit:coherent-states)=
### Coherent states

* Definition
* Properties:
  * time evolution of a coherent state
  * classical evolution of expected values
  * minimum uncertainty

#### Definition


**Through the action of the displacement operator on the vacuum state.**

$$| \alpha \rangle = \hat{D}(\alpha) | 0 \rangle = \exp\left(  \right) | 0 \rangle$$

```{dropdown} Displacement operator
:open:


```

**Eigen-state of the annihilation operator.** A coherent state $| \alpha \rangle$ is the eigenstate of the annihilation operator $\hat{a}$.

**Schrodinger picture.** In Schrodinger picture, the operator is independent of time,

$$\hat{a} | \alpha \rangle = \alpha | \alpha \rangle \ .$$


````{dropdown} Coherent state as a power series
:open:

$$| \alpha \rangle = \sum_{n=0}^{+\infty} b_n | \phi_n \rangle \ ,$$

with 

$$b_n = \frac{\alpha^n}{\sqrt{n!}} \, b_0 =  \frac{\alpha^n}{\sqrt{n!}} e^{- \frac{|\alpha|^2}{2}} e^{i \varphi}  \ .$$

```{dropdown} Details

$$\begin{aligned}
 \alpha \sum_{n=0}^{+\infty} b_n | n \rangle = \sum_{n=0}^{+\infty} \sqrt{n+1} b_{n+1} | n \rangle \ ,
\end{aligned}$$

and thus

$$\sqrt{n+1} \, b_{n+1} = \alpha b_n \ ,$$

and

$$b_{n} = \frac{\alpha^n}{\sqrt{n!}} b_0$$

Normalization gives

$$1 = \langle \alpha | \alpha \rangle = \sum_{m,n=0}^{+\infty} b_m^* b_n \langle m | n \rangle = |b_0|^2 \sum_{n=0}^{+\infty} \frac{\alpha^{2n}}{n!} = |b_0|^2 \cdot e^{|\alpha|^2} \ ,$$

i.e.

$$b_0 = e^{i \varphi} e^{- \frac{|\alpha|^2}{2}} \ .$$


```

````

**Poisson distribution of probability coefficients in energy basis.** The probabilities $|c_n|^2$ of being in energy states $| \phi_n \rangle$ follows a **Poisson distribution**,

$$| c_n |^2 = \frac{ |\alpha|^{2n} e^{-|\alpha|^2}}{n!} = p^{Poisson} (n; |\alpha|^2) \ ,$$

and thus it has both **expected value** and **variance** equal to $|\alpha|^2$.


**Time evolution of the state of a system, starting in a coherent state $| \Psi \rangle_0 = | \alpha \rangle$.** The evolution of a system governed by the Sschrodinger equation

$$i \hbar \dfrac{d}{dt} | \Psi \rangle_t = \hat{H} | \Psi \rangle_t = \left[ \frac{\hat{p}^2}{2m} + \frac{m \omega^2 \hat{x}^2}{2} \right] | \Psi \rangle_t \ ,$$

can be written as

$$\begin{aligned}
  | \Psi \rangle_t 
  & = \exp\left[ - i \frac{\hat{H}}{\hbar} t \right] | \Psi \rangle_0 = \\
  & = \exp\left[ - i \frac{\hat{H}}{\hbar} t \right] \sum_{n=1}^{+\infty} \frac{\alpha^n}{\sqrt{n!}} e^{- \frac{|\alpha|^2}{2}} e^{i \varphi} | \phi_n \rangle = \\ 
  & = e^{i \varphi} e^{- \frac{|\alpha|^2}{2}} \sum_{n=1}^{+\infty} \frac{\alpha^n}{\sqrt{n!}} e^{-i \frac{E_n}{\hbar} t} | \phi_n \rangle \ .
\end{aligned}$$

For a harmonic oscillator $E_n = \hbar \omega \left( n + \frac{1}{2} \right)$,

$$\begin{aligned}
  | \Psi \rangle_t 
  & = e^{-i \frac{\omega}{2} t} \left[ e^{i \varphi} e^{- \frac{|\alpha|^2}{2}} \sum_{n=1}^{+\infty} \frac{\left( \alpha e^{-i \omega t} \right)^n}{\sqrt{n!}} | \phi_n \rangle \right] \ .
\end{aligned}$$

````{dropdown} In space representation
:open:

The annihilation operator reads

$$\begin{aligned}
  \langle x | \hat{a} 
  & = \sqrt{\frac{m \omega}{2 \hbar}}\langle x | \left( \hat{x} + \frac{i \hat{p}}{m \omega} \right) = \\
  & = \sqrt{\frac{m \omega}{2 \hbar}} \left( x + \frac{\hbar}{m \omega} \partial_x \right)
\end{aligned}$$

and its spectral decomposition

$$\begin{aligned}
  \langle x | \hat{a} | \alpha \rangle & = \alpha \langle x | \alpha \rangle \\
  \sqrt{\frac{m \omega}{2 \hbar}} \left( x + \frac{\hbar}{m \omega} \partial_x \right) \psi_\alpha(x) & = \alpha \psi_\alpha(x)
\end{aligned}$$

whose solution is

$$\psi_\alpha(x) = \left( \frac{m \omega}{\pi \hbar} \right)^{1/4} \exp \left[ -\frac{m \omega}{2 \hbar} \left( x - \sqrt{\frac{2 \hbar}{m \omega}} \text{Re}\{ \alpha \} \right)^2 + i \sqrt{\frac{m \omega}{2 \hbar}} \text{Im}\{ \alpha \} x + i \, \text{Im}\{ C \} \right] \ .$$

```{dropdown} Details

Solution of the equation

$$ x y(x) + a y'(x) = b y(x) $$

with separation of variables,

$$\begin{aligned}
  a y'(x) & = ( x - b ) y(x) \\
  \int \frac{dy}{y} & = \int \frac{1}{a} \left( b - x \right) dx \\
  \ln |y| & = \frac{1}{a} \left( - \frac{x^2}{2} + b x + C \right) \\
  \rightarrow \quad y(x) & = \exp \left[ - \frac{x^2}{2 a} + \frac{b}{a} x + C \right] \\
\end{aligned}$$

The factor $K = \exp(C)$ is determined with the normalization condition, up to an irrelevant phase factor. In the problem $a \in \mathbb{R}$, $b \in \mathbb{C}$, and thus the squared magnitude is

$$\begin{aligned}
  |y(x)|^2 
  & = \exp\left(-\frac{x^2}{a}\right) \cdot \exp\left( \frac{b + b^*}{a} x\right) \cdot \exp\left( C + C^*\right) = \\
  & = \exp\left(-\frac{x^2}{a} + 2 \frac{\text{Re}\{ b \}}{a} x + 2 \text{Re}\{ C \} \right) = \\
  & = \exp\left[ - \frac{1}{a} \left( x - \text{Re}\{ b \} \right)^2 + \frac{\text{Re}\{ b \}^2}{a} + 2 \text{Re}\{ C \} \right] = \\
\end{aligned}$$

and its integral

$$1 = \int_{-\infty}^{+\infty} |y(x)|^2 dx = \int_{-\infty}^{+\infty} \exp\left( - \frac{1}{a} \left( x - \text{Re}\{ b \} \right)^2 \right) \, dx \cdot \exp \left[ \dots \right] = \sqrt{\pi a} \cdot \exp [ \dots ] ,$$

so that the normalization factor reads $\exp[ \dots ] = \frac{1}{\sqrt{2 a}}$, having exploited 

$$I^2 = \left[ \int_{x=-\infty}^{+\infty} e^{-\frac{x^2}{a}} \right]^2 = 2 \pi \cdot \frac{a}{2} \cdot \int_{r = 0}^{+\infty} e^{-\frac{r^2}{a}} d \frac{r^2}{a} = \pi a \ .$$

As $\exp\left[ \frac{\text{Re}\{ b \}^2}{a} + 2 \text{Re}\{ C \} \right] = \frac{1}{\sqrt{2 a}}$, the normalized solution becomes

$$\begin{aligned}
  y(x) 
  & = \exp\left[ - \frac{x^2}{2 a} + \frac{\text{Re}\{b\}}{a} x + i \frac{\text{Im}\{b\}}{a} x + \text{Re}\{ C \} + i \text{Im}\{ C \} \right] = \\
  & = \exp\left[ - \frac{x^2}{2 a} + \frac{\text{Re}\{b\}}{a} x + i \frac{\text{Im}\{b\}}{a} x + i \text{Im}\{ C \} \right] \cdot \exp \left[ - \frac{\text{Re}\{ b \}^2}{2 a} \right] \cdot \frac{1}{(\pi a)^{1/4}} = \\
  & = \exp\left[ - \frac{1}{2 a} \left( x - \text{Re}\{ b \} \right)^2 + i \frac{\text{Im}\{b\}}{a} x + i \text{Im}\{ C \} \right] \cdot \frac{1}{(\pi a)^{1/4}} \ .
\end{aligned}$$

Thus the solution of the eigenproblem of the annihilation operator is readily found with $a = \frac{\hbar}{m \omega}$, $b = \alpha \sqrt{\frac{2 \hbar}{m \omega}}$, and thus $\frac{b}{a} = \alpha \sqrt{\frac{m \omega}{2 \hbar}}$,

$$\psi_\alpha(x) = \left( \frac{m \omega}{\pi \hbar} \right)^{1/4} \exp \left[ -\frac{m \omega}{2 \hbar} \left( x - \sqrt{\frac{2 \hbar}{m \omega}} \text{Re}\{ \alpha \} \right)^2 + i \sqrt{\frac{m \omega}{2 \hbar}} \text{Im}\{ \alpha \} x + i \, \text{Im}\{ C \} \right] \ .$$

```


````


**Heisenberg picture.** Creation operator in Heisenberg picture satisfies Heisenberg dynamical equation,

$$i \hbar \dfrac{d \hat{a}_H}{dt} = [\hat{a}, \hat{H}]_H = \dots = \hbar \omega \hat{a}_H \ ,$$

and thus its evolution is $\hat{a}_H(t) = \hat{a}_H(0) \, e^{-i \omega t}$. Using the relation {} between Heisenberg and Schrodinger pictures of the same operator, $\hat{A}_H = \mathscr{U}_{t,t_0}^\dagger \hat{A}_S \mathscr{U}_{t,t_0}$, with $\mathscr{U}_{t_0,t_0} = \hat{\mathbf{1}}$, it follows that $\hat{a}_H(0) = \hat{a}$, and $\hat{a}_H(t) = \hat{a} \, e^{-i \omega t}$, without explicitly writing the index $S$ for Schrodinger picture.

Thus the spectral decomposition of the annihilation operator in Heisenberg picture, $\hat{a}_H | \alpha \rangle_H = \alpha_H | \alpha \rangle_H$, becomes

$$e^{-i \omega t} \hat{a} | \alpha \rangle_H = \alpha_H | \alpha \rangle_H $$
$$\hat{a} | \alpha \rangle_H = e^{i \omega t} \alpha_H | \alpha \rangle_H $$

and thus

$$| \alpha \rangle_H = $$

...

#### Classical limit

The expected value of the position and the momentum of the system starting in a coherent state is

$$\begin{aligned}
 \langle \hat{x} \rangle & = \sqrt{\frac{\hbar}{2 m \omega}} \left( \alpha^* e^{i \omega t} + \alpha e^{-i \omega t} \right) = \sqrt{\frac{2 \hbar} {m \omega}} \left( \text{Re}\{ \alpha \} \cos(\omega t) + \text{Im}\{ \alpha \} \sin(\omega t) \right) \\
 \langle \hat{p} \rangle & = \sqrt{\frac{m \hbar \omega}{2}} \left( i \alpha^* e^{i \omega t} - i \alpha e^{-i \omega t} \right) = \sqrt{2 m \hbar \omega} \left( - \text{Re}\{ \alpha \} \sin(\omega t) + \text{Im}\{ \alpha \} \cos(\omega t) \right) = m \frac{d}{dt} \langle \hat{x} \rangle \\
\end{aligned}$$


```{dropdown} Details

Using Heisenberg picture, the expected value of the position reads

$$\begin{aligned}
  \langle \hat{x} \rangle
  & = \langle \alpha | \hat{x}_H | \alpha \rangle = \\
  & = \langle \alpha | \sqrt{\frac{\hbar}{2 m \omega}} \left( \hat{a}^\dagger_H + \hat{a}_H \right) | \alpha \rangle = \\
  & = \sqrt{\frac{\hbar}{2 m \omega}} \langle \alpha | \left( \hat{a}^\dagger e^{i \omega t} + \hat{a} e^{-i \omega t} \right) | \alpha \rangle = \\
  & = \sqrt{\frac{\hbar}{2 m \omega}} \left( \alpha^* e^{i \omega t} + \alpha e^{-i \omega t} \right) \ ,
\end{aligned}$$

since $\langle \alpha | \hat{a} | \alpha \rangle = \alpha$, $\langle \alpha | \hat{a}^\dagger | \alpha \rangle = \alpha^*$ (see the section [One-mode coherent state, for the EM field](quantum-mechanics:qft:photons:coulomb:classical-limit:one-mode-coherent)). The expected value of the momentum, $\hat{p} = i \sqrt{\frac{m \hbar \omega}{2}} \left( \hat{a}^{\dagger} - \hat{a} \right)$, reads

$$\begin{aligned}
  \langle \hat{p} \rangle
  & = \langle \alpha | \hat{p}_H | \alpha \rangle = \\
  & = \langle \alpha | i \sqrt{\frac{m \hbar \omega}{2}} \left( \hat{a}^\dagger_H - \hat{a}_H \right) | \alpha \rangle = \\
  & = \sqrt{\frac{m \hbar \omega}{2}} \langle \alpha | i \left( \hat{a}^\dagger e^{i \omega t} - \hat{a} e^{-i \omega t} \right) | \alpha \rangle = \\
  & = \sqrt{\frac{m \hbar \omega}{2}} \left( i \alpha^* e^{i \omega t} - i \alpha e^{-i \omega t} \right) = \\
  & = \sqrt{\frac{m \hbar \omega}{2}} \cdot 2 \cdot \text{Re} \{ i \alpha^* e^{i \omega t} \} = \\
  & = \sqrt{ 2 m \hbar \omega} \left( \text{Im}\{ \alpha \} \cos( \omega t ) - \text{Re} \{ \alpha \} \sin(\omega t) \right) \ ,
\end{aligned}$$


```

Non-spreading wave-packets

```{dropdown}
:open:

```

Minimal uncertainty

```{dropdown}
:open:

```

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
