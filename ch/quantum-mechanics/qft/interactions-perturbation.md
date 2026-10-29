(quantum-mechanics:qft:interactions:perturbation-theory)=
# Perturbation theory

Other sections dealing with perturbation theory:
* [Perturbation theory for transition probabilities in weak electric fields](quantum-mechanics:history:heisenberg-reinterpretation:transition-perturbation-theory)
* [Interaction picture and perturbation theory](quantum-mechanics:einstein-coeffs-interaction-picture:perturbation)

**todo** *Need for cleaning*

---

Perturbation theory applies to systems governed by a Hamiltonian that can be written as the sum

$$
\hat H = \hat H_0+\hat H_{int} \ ,
$$

with $\hat H_0$ an easy-to-solve (unperturbed) system, whose spectral decomposition is usually known, and $\hat H_{int}$ a "small" perturbation, either time independent or time dependent. Let $| \phi_n \rangle$, and $E_n$ the eigenstates and the eigenvalues of the unperturbed Hamiltonian $\hat{H}_0$, i.e.

$$\hat{H}_0 | \phi_n \rangle = E_n | \phi_n \rangle \ .$$

Now, the perturbation Hamiltonian is explicitly written as the product of a "small" parameter $\lambda$ and a scaled perturbation Hamiltonian $\hat{H}_1$, with the same order of the unperturbed Hamiltonian $\hat{H}_0$, i.e.

$$\hat{H} = \hat{H}_0 + \lambda \hat{H}_1 \ ,$$

and a generic state $| \psi \rangle$ of the system written as a linear combination of the eigenstates $\{ | \phi_n \rangle \}_n$ of the unperturbed system,

$$
|\psi\rangle=\sum_nc_n(t)e^{-i \frac{E_n}{\hbar} t}|\phi_n\rangle \ .
$$

Inserting this expression in the Schrodinger equation $i\hbar|\dot\psi\rangle=(\hat H_0+\hat H_{int})|\psi\rangle$,

$$\begin{aligned}
i\hbar\sum_n\left(\dot c_n-i \frac{E_n}{\hbar} c_n \right)e^{-i \frac{E_n}{\hbar} t}|\phi_n\rangle & = (\hat H_0+\hat H_{int})\sum_nc_ne^{-i \frac{E_n}{\hbar} t}|\phi_n\rangle \\
 \sum_n i\hbar\dot c_ne^{-i \frac{E_n}{\hbar} t}|\phi_n\rangle & = \hat H_{int}\sum_n c_n e^{-i \frac{E_n}{\hbar} t}|\phi_n\rangle \ , 
\end{aligned}$$

since $E_n| \phi_n \rangle = \hat{H}_0 | \phi_n \rangle$. Multiplying by $\langle\phi_m|$, and exploiting orthogonality $\langle \phi_m | \phi_n \rangle = \delta_{mn}$,

$$
i\hbar\dot c_me^{-i\omega_mt}=\sum_nc_ne^{-i\omega_nt}\langle\phi_m|\hat H_{int}|\phi_n\rangle
$$

i.e. the infinite system of equations - $m \in \{0,1,2,\dots\}$ - follows

$$
\dot c_m=\frac1{i\hbar}\sum_nc_ne^{i(\omega_m-\omega_n)t}\langle\phi_m|\hat H_{int}|\phi_n\rangle
$$ (eq:interaction:perturbation)

Perturbation theory looks for a solution writing the coefficients $c_m(t)$ as power expansions in the "small" parameter $\lambda$,

$$
c_m(t)=c_m^{(0)}(t)+\lambda c_m^{(1)}(t)+\lambda^2c_m^{(2)}(t)+\dots
$$

Inserting this expression in {eq}`eq:interaction:perturbation`, 

$$\dot c_m^{(0)}+\lambda\dot c_m^{(1)}+\lambda^2\dot c_m^{(2)}+\dots=\frac1{i\hbar}\sum_n\left(c_n^{(0)}+\lambda c_n^{(1)}+\lambda^2c_n^{(2)}+\dots\right) \lambda H^{(1)}_{mn}e^{i(\omega_m-\omega_n)t} \ ,$$

an (approximate) solution can be found by coefficient matching:

$$\left\{ \begin{aligned}
(0): & \quad \dot{c}_m^{(0)} = 0 \\
(k): & \quad \dot{c}_m^{(k)} = \frac{1}{i\hbar} \sum_n c_n^{(k-1)} H^{(1)}_{mn} e^{i ( \omega_m - \omega_n ) t} \\
\end{aligned} \right.$$


## 0th-order solution

System starting in $| n \rangle$, $c_n(0)=1$, $c_{m \neq n}(0)=0$. As the $0^{th}$-order equations read $\dot{c}^{(0)}_m = 0$, then $0^{th}$-order coefficients are constant in time.

## 1st-order solution

If $c_n^{(0)}(t) = 1$, $c_{m \neq n}(t) = 0$, then infinite set of $1^{st}$ order equations is

$$
\dot c_m^{(1)}(t)= \frac{1}{i\hbar} e^{i\omega_{mn}t} H^{(1)}_{mn}
$$

* coefficient $c_n^{(1)}$

  * if $H_{nn}^{(1)} = 0$, then the dynamical equation reads $\dot{c}^{(1)}_n = 0$, and the constant solution reads $c^{(1)}_n = 0$, as the i.c. for the non-zero order terms are identically zero

  * if $H_{nn}^{(1)} \ne 0$, then the dynamical equation reads $\dot{c}^{(1)}_n = \frac{1}{i\hbar} H^{(1)}_{nn}$, the solution reads $c_n^{(1)} = \frac{H^{(1)}_{nn}}{i\hbar} t$

* coefficients $c_m^{(1)}$, for $m \ne n$,

  * if $H^{(1)}_{mn} = 0$, the dynamical eqaution reads $\dot{c}_m^{(1)} = 0$, and the constant solution reads $c_m^{(1)} = 0$

  * else

     * if $\omega_{mn} := \omega_m - \omega_n \ne 0$, the dynamical equation reads $\dot{c}_m^{(1)} = \frac{e^{i \omega_{mn}t}}{i \hbar} H^{(1)}_{mn}$, then the solution reads

        $$c_m^{(1)}(t) = \left.\left[ - \frac{H^{(1)}_{mn} e^{i \omega_{mn} \tau}}{\hbar \omega_{mn}} \right]\right|_{\tau=0}^{t} = \frac{1 - e^{i \omega_{mn} t}}{\hbar\omega_{mn}} H^{(1)}_{mn}$$ (eq:interactions:perturbations:cm1)
   
     * if $\omega_{mn} := \omega_m - \omega_n = 0$, the dynamical equation reads $\dot{c}_m^{(1)} = \frac{1}{i \hbar} H^{(1)}_{mn}$, and the solution is $c_m^{(1)} = \frac{1}{i \hbar} H^{(1)}_{mn}$.


**Probabilities.** For a system starting in state $| n \rangle$, the power expansion of the coefficients $c_m(t)$ reads

$$
 c_m(t) = \delta_{mn} + \sum_{k=1}^{+\infty} c_m^{(k)} \lambda^k \ .
$$

Thus, 

* the probability $|c_n(t)|^2$ contains zero and first order terms,

   $$\begin{aligned}
     |c_n|^2 
     & = \left( \sum_{k=0}^{+\infty} c_n^{(k)} \lambda^k \right)^* \left( \sum_{j=0}^{+\infty} c_n^{(j)} \lambda^j \right) = \\
     & = \sum_{k=0}^{+\infty} \sum_{j=0}^{+\infty} {c_n^{(k)}}^* c_n^{(j)} \lambda^{k+j} = \\
     & = \sum_{\ell=0}^{+\infty} \sum_{j=0}^{\ell} {c_n^{(\ell-j)}}^* c_n^{(j)} \lambda^{\ell} \ ,
   \end{aligned}$$

   or a bit more explicitly

   $$\begin{aligned}
     | c_n |^2 
     & =  |c_n^{(0)}|^2 + \lambda \left( {c_n^{(0)}}^* c_n^{(1)} + {c_n^{(1)}}^* c_n^{(0)} \right) + \lambda^2 \left( {c_n^{(0)}}^* c_n^{(2)} + | c_n^{(1)} |^2 + {c_n^{(2)}}^* c_n^{(0)}  \right) + \dots = \\
     & =  1 + \lambda \left( c_n^{(1)} + {c_n^{(1)}}^* \right) + \lambda^2 \left( c_n^{(2)} + | c_n^{(1)} |^2 + {c_n^{(2)}}^*  \right) + \dots \ ,
   \end{aligned}$$

* the probabilities $|c_m(t)|^2$ with $m \ne n$ only contains powers larger than or equal to $2$,

   $$\begin{aligned}
     |c_m|^2 
     & = \left( \sum_{k=1}^{+\infty} c_m^{(k)} \lambda^k \right)^* \left( \sum_{j=1}^{+\infty} c_m^{(j)} \lambda^j \right) = \\
     & = \sum_{k=1}^{+\infty} \sum_{j=1}^{+\infty} {c_m^{(k)}}^* c_m^{(j)} \lambda^{k+j} = \\
     & = \sum_{\ell=2}^{+\infty} \sum_{j=1}^{\ell-1} {c_m^{(\ell-j)}}^* c_m^{(j)} \lambda^{\ell} \ ,
   \end{aligned}$$
   
   or a bit more explicitly
   
   $$| c_m |^2 = \lambda^2 |c_m^{(1)}|^2 + \lambda^3 \left( {c_m^{(2)}}^* c_m^{(1)} + {c_m^{(1)}}^* c_m^{(2)} \right) + \dots$$

Here the parameter $\lambda$ is assumed to be real.

If $H^{(1)}_{mn} \ne 0$, and $\omega_{mn} \ne 0$, the coefficient $c_{m}^{(1)}$ is given by {eq}`eq:interactions:perturbations:cm1`, and its square modulus reads

$$\begin{aligned}
  |c_m^{(1)}|^2 
  & = \left( \frac{1 - e^{i \omega_{mn} t}}{\hbar\omega_{mn}} H^{(1)}_{mn} \right)^* \left( \frac{1 - e^{i \omega_{mn} t}}{\hbar\omega_{mn}} H^{(1)}_{mn} \right) = \\
  & = \left| H_{mn}^{(1)} \right|^2 \frac{4 \sin^2 \left( \frac{\omega_{mn} t}{2} \right)}{\hbar^2 \omega_{mn}^2} \ ,
\end{aligned}$$

as $(1 - e^{i a})^* (1- e^{i a}) = 2 - e^{ia} - e^{-ia} = 2 - 2 \cos( a ) = 4 \sin^2 \left( \tfrac{a}{2} \right)$. Thus the leading order of the probability $| c_n(t)|^2$ - this is the probability of finding the state of the system in $| \phi_n \rangle$ at time $t$, as this is the coefficient of $| \phi_n \rangle$ of the state $| \psi \rangle$ except for an irrelevant phase factor $e^{i \omega_{n} t}$ - is

$$
|c_n(t)|^2\sim\lambda^2|H^{(1)}_{mn}|^2\frac{4\sin^2\!\left(\frac{\omega_{mn}t}{2}\right)}{\hbar^2\omega_{mn}^2}
$$

As $t\to+\infty$ this function goes to **Dirac's delta**:

$$
\int_{\omega=-\infty}^{+\infty}\left\{\frac{\sin(\omega t/2)}{\omega}\right\}^2d\omega=\frac\pi2t
$$

so that the transition rate probability between the initial state $m$ and the final state $n$ at the first order is

$$
 \frac{|c_n|^2}{t} \longrightarrow \frac{2\pi}{\hbar^2} \,|H^{int}_{mn}|^2\,\delta(\omega_m-\omega_n) \ .
$$


**todo** *See, update and cross-link* [Math: Dirac delta](https://basics2022.github.io/bbooks-math-miscellanea/ch/functional-analysis/dirac-delta.html).

## Fermi golden rule

```{prf:definition} Fermi golden rule - infinite time
:label: qft:fermi-golden-rule

For $t \rightarrow +\infty$, for a system with unperturbed Hamiltonian $\hat H_0$, with stationary states $|\phi_n\rangle_t=|\phi_n\rangle e^{-i\omega_nt}$, an additive "small" perturbation Hamiltonian $\hat{H}_{int}$ causes the initial state $|i\rangle_t=|\phi_i\rangle e^{-i\omega_it}$ to transition to $|f\rangle=|\phi_f\rangle e^{-i\omega_ft}$ at the rate

$$2\pi\,|H^{int}_{mn}|^2\,\delta(\omega_m-\omega_n)\qquad\text{(to the 1st order)}$$

<span style="color: red;">
* What's the role of the delta here? <br>
* Does it still make sense to set $t \rightarrow +\infty$ at the first order?. <br>
</span>

```

```{prf:definition} Fermi golden rule - finite time
:label: qft:fermi-golden-rule-finite

For a system with unperturbed Hamiltonian $\hat H_0$, with stationary states $|\phi_n\rangle_t=|\phi_n\rangle e^{-i\omega_nt}$, an additive "small" perturbation Hamiltonian $\hat{H}_{int}$ causes the initial state $|i\rangle_t=|\phi_i\rangle e^{-i\omega_it}$ to transition to $|f\rangle=|\phi_f\rangle e^{-i\omega_ft}$ at the rate

$$
|c_n(t)|^2\sim\lambda^2|H^{(1)}_{mn}|^2\frac{4\sin^2\!\left(\frac{\omega_{mn}t}{2}\right)}{\hbar^2\omega_{mn}^2}
$$

<span style="color: red;">
* The non-delta probability reflects the uncertainty principle involving Energy and Time. Without probing a system for an infinite time, it's impossible to get no uncertainty on its energy <br>
</span>

```

## Higher orders

<span style="color: red;">Check it, and provide details about the mutliple interactions involving intermediate states.</span>

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



