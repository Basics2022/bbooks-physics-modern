(quantum-mechanics:qft:interactions:perturbation-theory)=
# Perturbation theory

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



