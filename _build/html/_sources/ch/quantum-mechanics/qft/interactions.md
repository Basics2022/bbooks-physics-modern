(quantum-mechanics:qft:interactions)=
# Interacting Fields 

$$
\hat H=\hat H_{atom}+\hat H_{rad}+\hat H_{inter},\qquad
\hat H_{atom}=\sum E_k\hat b_k^\dagger\hat b_k,\quad
\hat H_{rad}=\sum E_{k,\alpha}\hat a^\dagger_{k,\alpha}\hat a_{k,\alpha}
$$

Examples (space–time diagrams in the notes): all these processes should be weighted by some probability.

- **Absorption** process: $\hat b_n^\dagger\hat b_m\hat a_{k,\alpha}$ — atom $|\psi_m\rangle\to|\psi_n\rangle$, photon $|k,\alpha\rangle$ absorbed.
- **Emission** process: $\hat b_m^\dagger\hat a^\dagger_{k,\alpha}\hat b_n$ — atom $|\psi_n\rangle\to|\psi_m\rangle$, photon $|k,\alpha\rangle$ emitted.

## Perturbation theory

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


## Interaction between electron and electromagnetic fields


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


## Selection rules

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

### Linear momentum

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

...

## Photon–$e^-$ scattering

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

