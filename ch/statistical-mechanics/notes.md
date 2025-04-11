(statistical-mechanics:notes)=
# Statistical Physics - Notes

(statistical-mechanics:notes:ensembles)=
## Ensembles

(statistical-mechanics:notes:ensembles)=
## Microcanonical ensemble

(statistical-mechanics:notes:ensembles)=
## Canonical ensemble

(statistical-mechanics:notes:ensembles)=
## Macrocanonical esemble

(statistical-mechanics:notes:distributions)=
## Statistics

Each of the $N$ components of the system is in an **energy level** $i$. Energy level $i$ has $g_i$ sublevels with the same energy level.
- energy levels, $E_i$ of each component
- occupation number $N_i$ of level $i$

- **Central role of energy.** In a system macroscopically at rest, the energy of a system is the only macroscopic meaningful non-zero mechanical quantity, constant for closed and isolated systems
- **Principle of maximum uncertainty**, **maximum entropy**, **minimum information**: given a measurement of a macroscopic variable $V$, describing the macrostate of the system, the feasible un-observed/able microstates of the system are the microstates consistent with it: there's usually a sharp maximum of in the probability density of the micrsotates.

Given a macrostate, what's the number of ways $W(N_i; g_i)$ to get a consistent microstate? Once the expression is found, constrained optimization follows: optimization w.r.t. $N_i$ is usually performed in the limit of $N_i \rightarrow +\infty$ (why in Fermi-Dirac distribution, obeying Pauli exclusion principle?), with the values of the macroscopic variables as constraints usually treated with Lagrange multiplier.

(statistical-mechanics:notes:distributions:mb)=
### Maxwell-Boltzmann

Statistics of distinguishible components.


(statistical-mechanics:notes:distributions:be)=
### Bose-Einstein

Statistics of undistinguishable components that can be in the same (sub)level.
Given the number of elementary components $\sum_{i} N_i = N$ and the energy $\sum_{i} N_i E_i = E$,

$$W_{BE,i} = \frac{(N_i + g_i - 1)!}{N_i! (g_i-1)!} \qquad , \qquad W_{BE} = \prod_i W_{BE,i} \ .$$ (eq:be)

```{dropdown} Counting microstates
**todo** write page *Combinatorics* and add link 
```

**Most likely microstate.** Instead of maximizing {eq}`eq:be`, the objective function is $\ln W_{BE}$, after using Stirling approximation in the limit of large $N_i$ and $g_i$, $N_i! \sim \left(\frac{N_i}{e} \right)^{N_i}$. The approximate occupation number of one of the $G_i$ sublevels of the $i^{th}$ level of the most likely microstate is

$$n_i := \frac{N_i}{G_i} = \frac{1}{e^{\alpha + \beta E_i} - 1} \ .$$

```{dropdown} Optimization
$$\begin{aligned}
  J(N_i, \alpha, \beta)
  & = \ln W_{BE} + \alpha \left( N - \sum_i N_i \right) + \beta \left(E - \sum_i N_i E_i \right) = \\
  & = \sum_i \left\{ \ln(N_i + g_i -1)! - \ln N_i! - \ln (g_i-1)! \right\} + \alpha \left( N - \sum_i N_i \right) + \beta \left(E - \sum_i N_i E_i \right) \simeq \\
  & \simeq \sum_i \left\{ (N_i+g_i-1)\ln(N_i+g_i-1) - N_i\ln N_i - (g_i-1) \ln (g_i-1) + N_i + g_i -1 - N_i - (g_i-1) \right\} + \alpha \left( N - \sum_i N_i \right) + \beta \left(E - \sum_i N_i E_i \right) = \\
  & = \sum_i \left\{ (N_i+g_i-1)\ln(N_i+g_i-1) - N_i\ln N_i - (g_i-1) \ln (g_i-1) \right\} + \alpha \left( N - \sum_i N_i \right) + \beta \left(E - \sum_i N_i E_i \right) \\
\end{aligned}$$

Using $\partial_{n} (n+a) \ln (n+a) = \ln (n+a) + 1$,

$$\begin{aligned}
  0 = \partial_{N_k} J 
  & \simeq \left\{ \ln (N_k+g_k-1) - \ln N_k \right\} - \alpha - \beta E_k \ ,
\end{aligned}$$

and thus

$$\ln \frac{N_k + g_k - 1}{N_k} = \alpha + \beta E_k \ ,$$
$$\frac{N_k + g_k - 1}{N_i} = e^{\alpha + \beta E_k}$$
$$N_k = \frac{g_k - 1}{e^{\alpha + \beta E_k}-1} \simeq \frac{g_k}{e^{\alpha + \beta E_k}-1} \ , $$

Thus, in the limit of $g_k \gg 1$, the  occupation number of the $k$ level is

$$N_k = \frac{G_k}{e^{\alpha + \beta E_k} - 1} \ ,$$

and the average occupation number of one of the $g_k$ sublevels in the $k$ level is

$$n_k := \frac{N_k}{G_k} = \frac{1}{e^{\alpha + \beta E_k} - 1}$$

```

```{dropdown} **Meaning of $\alpha$, $\beta$**
```

````{prf:example} Black-body radiation: Planck, Wien, and Stefan-Boltzmann laws

**Planck's law.** Energy density w.r.t. frequency

$$u_{f}(f, T) = \frac{8 \pi h f^3}{c^3} \frac{1}{e^{\frac{hf}{k_B T}} - 1}$$

```{dropdown} Planck's law in a cubic box
:open:

Planck's law uses:
- relation between pulsation and wave vector, or frequency and wave number and the speed of light $c$ for light waves

  $$c = \frac{\omega}{|\vec{k}|} = \lambda f$$

  $$f = \frac{\omega}{2\pi} = \frac{c |\vec{k}|}{2 \pi}$$

- Planck assumption that the minimum non-zero energy of a mode with frequency $f$ is $E = h f$, and all the possible values of the energy of the mode is

  $$E_m = m h f \quad , \quad m \in \mathbb{N} \ .$$

Taking a cubic box with sides $L_x = L_y = L_z = L$, the possibile modes have (**todo** *why? Which boundary condition? Periodic? Some physical? Just fictitious discretization?*) in each direction wave-lengths $\lambda_n = \frac{L}{|\vec{n}|} = \frac{2 \pi}{|\vec{k}|}$,

$$\vec{k} = \frac{2 \pi}{L} \vec{n} \ .$$

Mode density in $\vec{n}$-domain is 2 mode per each volume of unit length (2 polarization), and thus the number of modes $d N$ in an elementary volume is

$$d N = 2 \, d^3 \vec{n} \ ,$$

Changing variables, it's possible to find the mode density w.r.t. wave vector $\vec{k}$,

$$d N = 2 \, d^3 \vec{n} = 2 \, \frac{L^3}{(2 \pi)^3} \, d^3 \vec{k} \ ,$$

or with its absolute value, exploiting the isotropy of the density function - and writing the elementary volume using "spherical coordinates" $d^3 \vec{k} = 4 \pi \left| \vec{k} \right|^2 d \, \left| \vec{k} \right|$,

$$\begin{aligned}
  d N
  & = \frac{V}{(2 \pi)^3} 8 \pi \left| \vec{k} \right|^2 d \left| \vec{k} \right| = \\
  & = \frac{V}{(2 \pi)^3} 8 \pi \frac{8 \pi^3}{c^3} f^2 d f = \\
  & = V \frac{8 \pi}{c^3} f^2 df =: V g(f) df \ .
\end{aligned}$$


```

```{dropdown} Average energy of a mode
:open:

Using Boltzmann distribution (**why?**) for the energy distribution in a single mode,

$$P(E_r) = \frac{e^{-\beta E_r}}{Z} \ ,$$

with $E_r = r h f$, and the partition function 

$$Z = \sum_{s} e^{- \beta E_s} = \sum_s e^{-\beta h f s} = \frac{1}{1 - e^{-\beta h f}} \ .$$

The average energy of the mode reads

$$\begin{aligned}
  \langle E \rangle
  & = \sum_r E_r P(E_r) = \\
  & = \sum_r r h f \frac{e^{- \beta h f r}}{Z} = \\
  & = h f (1-e^{-\beta h f}) \sum_r r e^{- \beta h f r} = \\
  & = h f (1-e^{-\beta h f}) \frac{e^{- \beta h f}}{(1-e^{-\beta h f})^2} = \\
  & = \frac{h f}{e^{\beta h f} - 1}  \ .
\end{aligned}$$

```

```{dropdown}

Putting together the mode number density and the average energy of a mode, the energy density per unit volume, per frequency reads

$$\begin{aligned}
  u(f, T)
  & = \langle E \rangle(f) \, g(f) = \\
  & = \frac{hf}{e^{\beta h f} - 1} \frac{8 \pi}{c^3} f^2 = \\
  & = \frac{8 \pi h f^3}{c^3} \frac{1}{e^{\beta h f} - 1} \ .
\end{aligned}$$


```

```{dropdown} Property of the series
:open:

$$\sum_{n=0}^{+\infty} n x^n = \frac{x}{(1-x)^2}$$

**Proof.** If the series is convergent (is this the required condition?)

$$\frac{d}{d x} \sum_{n=0}^{+\infty} x^n = \frac{d}{dx} \frac{1}{1 - x} = \frac{1}{(1-x)^2}$$
$$\frac{d}{d x} \sum_{n=0}^{+\infty} x^n = \sum_{n=0}^{+\infty} n x^{n-1}$$
$$x \frac{d}{d x} \sum_{n=0}^{+\infty} x^n = \sum_{n=0}^{+\infty} n x^n = \frac{x}{(1-x)^2}$$

```


**Sperctral radiance**, $B_{f}$, so that an infinitesimal amount of power radiated by a surface ... is $d P = B_f(f,T) \cos \theta \, dA \, d\Omega \, d f$

$$B_{f}(f, T) = \frac{2 h f^3}{c^2}\frac{1}{e^{\frac{hf}{k_B T}} - 1} \ .$$

This expression is obtained[^nano-hub-planck] assuming homogeneous radiation from a small hole cut into a wall of the box. Only half of the energy radiates through the hole - so factor $\frac{1}{2}$ in front of the energy density - through a solid angle $2 \pi$ - and thus this process give the same result as a radiation of all the energy density in all the space directions, just providing the same factor $\frac{1}{4 \pi}$. The flux of energy "has velocity" $c$ and thus

$$B_{f}(f, T) = \frac{1}{4 \pi} u_{f}(f,T) c \ .$$

**Wien's law.** Wien's law tells that the frequency $f^*$ corresponding to the maximum of the spectral radiance of a black-body radiation described by Planck's law is proportional to its temperature.

From direct evaluation of the derivative of the spectral radiance as a function of $f$,

$$\begin{aligned}
  \partial_f B_{f}(f,T)
  & = \frac{2 h}{c^2} \left[ 3 f^2 \frac{1}{e^{\frac{hf}{k_B T}}-1} + f^3 \left(-\frac{\frac{h}{k_B T} e^{\frac{hf}{k_B T}}}{\left( e^{\frac{hf}{k_B T}} - 1 \right)^2}  \right) \right] = \\
  & = \frac{2 h f^2 e^{\frac{hf}{k_B T}}}{c^2 \left( e^{\frac{hf}{k_B T}} - 1 \right)^2} \left[ 3 \left( 1 - e^{-\frac{hf}{k_B T}} \right) - \frac{h f}{k_B T}  \right] \ .
\end{aligned}$$

Now, if $\partial_f B_{f}(f,T) = 0$ the frequency is either $f = 0$, or the solution of the nonlinear algebraic equation

$$0 = 3 \left(1 - e^{-\frac{h f}{k_B T}} \right) - \frac{hf}{k_B T} \ .$$

Defining $x := \frac{h f}{k_B T}$, this equation becomes

$$0 = 3 (1 - e^x) - x \ ,$$

whose solution $x^* \approx 2.82$ can be easily evaluated with an iterative method (or expressed in term of the Lambert's function $W$, so loved at Stanford and on Youtube: they'd probaly like to look at tabulated values, or pose). Once the solution $x^*$ of this non-dimensional equation is found, the frequency where maximum energy density occurs reads

$$f^* = \frac{k_B T}{h} x^* \simeq 2.82 \frac{k_B}{h} T \ .$$


**Stefan-Boltzmann law.**

$$\begin{aligned}
  \frac{P}{A} 
  & = \int B_{f}(f,T) \cos \phi \, df \, d\Omega = \\
  & = \int_{f=0}^{+\infty} \int_{\phi = 0}^{\frac{\pi}{2}} \int_{\theta=0}^{2\pi} B_{f}(f,T) \cos \phi \sin \phi \, df \, d\phi \, d \theta = \\
  & = \pi \int_{f=0}^{+\infty} B_{f}(f,T) \, d f = \\
  & = \frac{2 \pi h}{c^2} \int_{f=0}^{+\infty} \frac{f^3}{e^{\frac{hf}{k_B T}} - 1} \, d f = \\
  & = \frac{2 \pi h}{c^2} \left( \frac{k_B T}{h} \right)^4 \int_{u=0}^{+\infty} \frac{u^3}{e^u - 1} \, d u \ .
\end{aligned}$$

The value of the integral is $\frac{\pi^4}{15}$ and thus

$$\frac{P}{A} = \sigma T^4 \qquad , \qquad \sigma = \frac{2 \pi^5 k_B^4}{15 c^2 h^3} \ .$$

````

[^nano-hub-planck]: [Derivation of Planck's Law](https://nanohub.org/wiki/DerivationofPlancksLaw).

```{prf:example} Energy density and radiance

**Radiance.** The radiance $L_{e,\Omega}$ of a surface is the flux of energy per unit solid angle, per unit projected area of the source.

**Spectral radiance in frequency** is the radiance per unit frequency, $L_{e, \Omega, f} = \frac{\partial L_{e,\Omega}}{\partial f}$.

```

(statistical-mechanics:notes:distributions:fd)=
### Fermi-Dirac

Statistics of undistinguishable components that can't be in the same (sub)level, obeying to the Pauli exclusion principle.
Given the number of elementary components $\sum_{i} N_i = N$ and the energy $\sum_{i} N_i E_i = E$,

$$W_{FD,i} = \frac{G_i!}{(G_i-N_i)! N_i!} \qquad , \qquad W_{FD} = \prod_i W_{FD,i} \ .$$ (eq:fd)

```{dropdown} Counting microstates
**todo** write page *Combinatorics* and add link 
```

**Most likely microstate.** The approximate occupation number of the $i^{th}$ level of the most likely microstate is

$$n_i := \frac{N_i}{G_i} = \frac{1}{1 + e^{\alpha + \beta E_i}} \ .$$

```{dropdown} Optimization

$$\begin{aligned}
  J(N_i, \alpha, \beta)
  & = \ln W_{FD} + \alpha \left( N - \sum_i N_i \right) + \beta \left(E - \sum_i N_i E_i \right) = \\
  & = \sum_i \left\{ \ln G_i! - \ln(G_i - N_i)! - \ln N_i!  \right\} + \alpha \left( N - \sum_i N_i \right) + \beta \left(E - \sum_i N_i E_i \right) = \\
  & = \sum_i \left\{ G_i \ln G_i - (G_i - N_i) \ln(G_i - N_i) - N_i \ln N_i \right\} + \alpha \left( N - \sum_i N_i \right) + \beta \left(E - \sum_i N_i E_i \right) = \\
\end{aligned}$$

Using $\partial_{n} (n+a) \ln (n+a) = \ln (n+a) + 1$,

$$\begin{aligned}
  0 = \partial_{N_k} J 
  & \simeq \left\{ \ln (G_k - N_k) - \ln N_k \right\} - \alpha - \beta E_k \ ,
\end{aligned}$$

and thus

$$\ln \frac{G_k - N_k}{N_k} = \alpha + \beta E_k \ ,$$
$$\frac{G_k}{N_k} - 1 = e^{\alpha + \beta E_k} \ $$

The occupation number of the $k$ level is

$$N_k = \frac{G_k}{1 + e^{\alpha + \beta E_k}} \ .$$

The average occupation of the $G_k$ sublevels of the $k$ level is

$$n_k := \frac{N_k}{G_k} = \frac{1}{1 + e^{\alpha + \beta E_k}} \ .$$


```
```{dropdown} **Meaning of $\alpha$, $\beta$**
```



