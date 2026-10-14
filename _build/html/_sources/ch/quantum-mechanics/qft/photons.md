(quantum-mechanics:qft:photons)=
# Photons - EM field quantization

Photons are the quanta of EM fields. After reviewing classical electromagnetism, two different introductions to EM field quantization are presented
* [Quantization of the EM field in an ideal cavity (Fermi, 1931)](quantum-mechanics:qft:photons:em-field-quantization:fermi)
* [Quantization of the EM field in free space](quantum-mechanics:qft:photons:em-field-quantization:free-space)

Then, the [classical limit](quantum-mechanics:qft:photons:em-field-quantization:classical-limit) is discussed, comparing [a field with incoherent states](quantum-mechanics:qft:photons:em-field-quantization:classical-limit:incoherent-states) and [a field with coherent states](quantum-mechanics:qft:photons:em-field-quantization:classical-limit:coherent-states)

(quantum-mechanics:qft:photons:classical-em)=
## Classcal Electromagnetism

Link to [Classical Electromagnetism](https://basics2022.github.io/bbooks-physics-electromagnetism/intro.html).

(quantum-mechanics:qft:photons:em-field-quantization)=
## EM field quantization

(quantum-mechanics:qft:photons:em-field-quantization:fermi)=
### Fermi 1931, Introduction to QFT lessons

(quantum-mechanics:qft:photons:em-field-quantization:free-space)=
### EM Field in free space

#### Field in 1D free space

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

#### In a 3D domain

$$
\hat A=\sum_{\vec k,\mu}\vec e_{\vec k\mu}\frac{1}{\sqrt{2\omega_k}}\left\{\hat a^\dagger_{\vec k,\mu}e^{-i\vec k\cdot\vec r}+\hat a_{\vec k,\mu}e^{i\vec k\cdot\vec r}\right\}
$$

$$
\hat H=\sum_{\vec k,\mu}\left(\hat N_{\vec k,\mu}+\tfrac12\right)\hbar\omega_k,\qquad
|\psi\rangle=|\dots n_{\vec k,\mu}\dots\rangle
$$

(quantum-mechanics:qft:photons:em-field-quantization:classical-limit)=
## Quantum description of the EM field — classical limit

Example: 1D domain, 1 propagating wave.

$$
A(z,t)=u_x\,b\cos(kz-\omega t+\theta)\ \xrightarrow{\text{quant}}\
\hat A=u_x\sqrt{\tfrac1{2\omega}}\left(\hat a e^{ikz}+\hat a^\dagger e^{-ikz}\right)
$$

How to recover the classical limit?

(quantum-mechanics:qft:photons:em-field-quantization:classical-limit:incoherent-states)=
### Try 1 — Incoherent states

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

(quantum-mechanics:qft:photons:em-field-quantization:classical-limit:coherent-states)=
### Try 2 — Coherent states

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
