(quantum-mechanics:qft:interactions:e-em-fields)=
# Interaction of the electron and electromagnetic field

The behavior of the interactions between electron and electromagnetic fields strongly depends on the characteristic of the electron field:

* [Bound electrons - Atom spectra](quantum-mechanics:qft:interactions:e-em-fields:atom-spectra)
* [Free electrons - Compton scattering](quantum-mechanics:qft:interactions:e-em-fields:compton-scattering)


````{dropdown} Non-relativistic model of the electron field. Schrodinger equation
:open:

For an electron in a potential $V(\mathbf x)$ we impose $\{\psi_\sigma(\mathbf x),\psi_{\sigma'}^\dagger(\mathbf y)\}=\delta_{\sigma\sigma'}\delta^3(\mathbf x-\mathbf y)$ and use the one-body Hamiltonian:

$$
H_{\rm el}=\sum_\sigma\int d^3x\;\psi_\sigma^\dagger(\mathbf x)\Big[-\frac{\hbar^2\nabla^2}{2m}+V(\mathbf x)\Big]\psi_\sigma(\mathbf x).
$$

The Heisenberg equation follows from $[A,BC]=\{A,B\}C-B\{A,C\}$:

$$
[\psi_\sigma(\mathbf x),\,\psi^\dagger_{\sigma'}(\mathbf y)\,h\,\psi_{\sigma'}(\mathbf y)]=\delta(\mathbf x-\mathbf y)\,h\,\psi_\sigma(\mathbf y)-\psi^\dagger(\mathbf y)\,h\,\underbrace{\{\psi_\sigma(\mathbf x),\psi_{\sigma'}(\mathbf y)\}}_{=0},
$$

so, integrating over $\mathbf y$,

$$
i\hbar\,\partial_t\psi_\sigma(\mathbf x,t)=[\psi_\sigma,H_{\rm el}]=\Big[-\frac{\hbar^2\nabla^2}{2m}+V\Big]\psi_\sigma(\mathbf x,t).
$$

The *operator* $\psi$ obeys the *Schrödinger equation*, and the one-particle wave function is recovered as $\Phi(\mathbf x,\sigma)=\langle0|\psi_\sigma(\mathbf x)|\Phi\rangle$. "Second quantisation" is therefore not a second quantisation of the same object: what is quantised is a field whose classical equation of motion happens to be the Schrödinger equation.

Free electrons
---

For $V=0$ in the periodic box use plane waves $\phi_{\mathbf k\sigma}(\mathbf x)=V^{-1/2}e^{i\mathbf k\cdot\mathbf x}\chi_\sigma$:

$$
\psi_\sigma(\mathbf x)=\frac{1}{\sqrt V}\sum_{\mathbf k}e^{i\mathbf k\cdot\mathbf x}c_{\mathbf k\sigma},\qquad
H_{\rm el}=\sum_{\mathbf k\sigma}\frac{\hbar^2k^2}{2m}\,c^\dagger_{\mathbf k\sigma}c_{\mathbf k\sigma},\qquad
\mathbf P=\sum_{\mathbf k\sigma}\hbar\mathbf k\,c^\dagger_{\mathbf k\sigma}c_{\mathbf k\sigma}.
$$

A single free electron is $c^\dagger_{\mathbf k\sigma}|0\rangle$, with energy $\hbar^2k^2/2m$ and momentum $\hbar\mathbf k$. The ground state of $N$ non-interacting electrons fills the $N$ lowest $(\mathbf k,\sigma)$ levels, the Fermi sea (a consequence of $(c^\dagger)^2=0$). The spin label is conserved by $H_{\rm el}$.

Bound electrons
---

For a hydrogen-like atom, $V=-Ze^2/4\pi\varepsilon_0r$, use the orbitals $\phi_{nlm}(\mathbf x)\chi_\sigma$ with $E_n=-Z^2\,\text{Ry}/n^2$:

$$
\psi_\sigma(\mathbf x)=\sum_{nlm}\phi_{nlm}(\mathbf x)\,c_{nlm\sigma}+\int\!d^3k\;\phi^{(+)}_{\mathbf k}(\mathbf x)\,c_{\mathbf k\sigma},\qquad
H_{\rm el}=\sum_{nlm\sigma}E_n\,c^\dagger_{nlm\sigma}c_{nlm\sigma}+\int\!d^3k\,\frac{\hbar^2k^2}{2m}c^\dagger_{\mathbf k\sigma}c_{\mathbf k\sigma}.
$$

The second term, the **Coulomb scattering states** $\phi^{(+)}_{\mathbf k}$, completes the basis: bound and continuum states together span $\mathcal H$. By §1.6 these operators are related to the plane-wave operators of §4.2 by a unitary transformation, $c^{\rm plane}_{\mathbf p}=\sum_b\langle\mathbf p|b\rangle c_b+\int\langle\mathbf p|\mathbf k^{(+)}\rangle c_{\mathbf k}$, with the bound-state momentum distribution $\langle\mathbf p|b\rangle$ spread over $|\mathbf p|\sim\hbar/a_0$. **The Fock space is the same; free and bound electrons differ only by which single-particle basis diagonalises $H_{\rm el}$.** A transition $c^\dagger_{\mathbf k}c_{b}$ is a photoionisation; $c^\dagger_{b'}c_{b}$ is a bound–bound transition; both are matrix elements of the *same* operator. For an atom with several electrons one adds the two-body Coulomb term of §1.5 and, in the single-active-electron approximation, treats the outermost electron in an effective potential; the light–matter formalism below is unchanged.

**Spin.** Besides the orbital coupling, the electron has a Zeeman-type term $H_{\rm spin}=(e\hbar/2m)\,\boldsymbol\sigma\!\cdot\!\mathbf B$ ($g=2$). Compared with $H_1=(e/m)\mathbf A\!\cdot\!\mathbf p$, using $p\sim\hbar/a_0$ and $B\sim kA$, the ratio is $\sim ka_0\sim10^{-3}$ for optical and UV light, so we neglect it; it produces magnetic-dipole transitions. The fully consistent treatment of spin and its relativistic corrections is given by the Dirac field (§5.6).

````

---

````{dropdown} Old - from Via Science - to be cleaned
:open:

**Photon field (Heisenberg picture).** The vector potential field operator and the Hamiltonian read

$$
\hat{\vec{a}}(\vec{r}, t) = \sum_{\vec k,\alpha}\frac{\vec{\epsilon}_{\vec k,\alpha}}{\sqrt{2\omega_k}}\left(\hat a_{\vec k,\alpha}e^{-i\omega_kt}e^{i\vec k\cdot\vec r}+\hat a^\dagger_{\vec k,\alpha}e^{i\omega_kt}e^{-i\vec k\cdot\vec r}\right)
$$

$$
\hat H_r=\sum_{\vec k,\alpha}\hat n_{\vec k,\alpha}\,\hbar\omega_k \ ,
$$

after **energy renormalization**, i.e. zero-point energy set $\equiv0$.

```{dropdown} Expected value of the enerdy of the EM field
:open:

$$
\langle\hat H_r\rangle=\langle\dots n_{\vec k,\alpha}\dots|\hat H_r|\dots n_{\vec k,\alpha}\dots\rangle=\sum_{\vec k,\alpha}n_{\vec k,\alpha}\hbar\omega_k
$$

<!--
Natural units: $c=1$, $\hbar=1$.
-->

```

**Electron field.** Annihilation and creation field operators for the electron read

$$
\hat\psi(\vec{r},t)=\sum_k\hat b_ke^{-i\omega_kt}\varphi_k(\vec r) \quad ,\qquad
\hat\psi^\dagger(\vec r,t)=\sum_k\hat b^\dagger_ke^{i\omega_kt}\varphi^*_k(\vec r)
$$

being $\varphi_k$ the "orbitals" of the atom of interest, solution of the eigenproblem for the Hamiltonian of the system, $\hat{H} | \psi_n \rangle = E_n | \psi_n \rangle$. The Hamiltonian for one electron (assuming no interaction between electrons?) is

$$
\hat H=\frac1{2m_e}\hat p^2+V(\hat x) \ .
$$


```{dropdown} Expected value of $\hat H$
:open:

$$\begin{aligned}
\langle \hat{H} \rangle
 & = \langle \psi | \hat{H} | \psi \rangle = \\
 & = \sum_{m,n} c_m^* c_n \langle m | \hat{H} | n \rangle = \\
 & = \sum_{m,n} c_m^* c_n \, E_n \, \underbrace{\langle m | n \rangle}_{\delta_{mn}} = \\
 & = \sum_{n} | c_n |^2 \, E_n \ .
\end{aligned}$$

<!--
Let the system be in $|\psi\rangle$; then

$$
\langle\hat H\rangle=\langle\psi|\hat H|\psi\rangle=\int_{x,x'}\langle\psi|x\rangle\langle x|\hat H|x'\rangle\langle x'|\psi\rangle\,dx\,dx'
$$

and with $|\psi\rangle=\sum_kc_k|\phi_k\rangle$:

$$\begin{aligned}
 \langle\hat H\rangle
 & = \sum_{k,k'}\int_{\vec{r}, \ \vec{r}'} c_k^*\langle\phi_k|x\rangle\langle x|\hat H|\phi_{k'}\rangle c_{k'} d \vec{r} d \vec{r}'= \\
 & = \sum_{k,k'}\int_{\vec{r}, \ \vec{r}'} c_k^*c_{k'}\langle\phi_k|x\rangle E_{k'}\langle x|\phi_{k'}\rangle d \vec{r} d \vec{r}' = \\
 & = \dots = \\
 & = \sum_k|c_k|^2E_k \ .
\end{aligned}$$
-->

```

```{dropdown} QFT form of the Hamiltonian
:open:

...

**todo** *Check and uncomment*

<!--
Just replacing the wavefunction $\phi_k(\vec r)$ with the field operator, and $\phi_k^*(\vec r)$ with $\hat\psi^\dagger$:

$$
\hat H_e=\int_x\hat\psi^\dagger(x,t)\hat H\hat\psi(x,t)\,dx
=\int_x\sum_{m,m'}\hat b^\dagger_m\psi_m^*(x)\hat H\hat b_{m'}\psi_{m'}(x)\,dx
$$

$$
=\sum_{m,m'}\int_x\psi_m^*(x)\hat H\psi_{m'}(x)dx\ \hat b_m^\dagger\hat b_{m'}
=\sum_{m,m'}E_{m'}\,\delta_{mm'}\,\hat b_m^\dagger\hat b_{m'}
=\sum_mE_m\hat b_m^\dagger\hat b_m=\sum_mE_m\hat n_m
$$
-->

```

### Interaction Hamiltonian

**Minimal coupling.** The Hamiltonian of a particle with mass $m$ and electric charge $q$ in a prescribed EM field is

$$\mathcal{H} = \frac{1}{2} m \left| \dot{\vec{r}} \right|^2 + q \varphi = \frac{|\vec{p} - q \vec{a}|^2}{2 m} + q \varphi \ .$$

If the EM radiation field can be written with the vector EM potential field $\vec{a}$, while the scalar EM potential field fully represents the EM field of the nucleus, the Hamiltonian operator for a electron bound to an atom in an external EM field is obtained by the promotion to operators of the electron position and momentum, and the vector EM field,


$$\begin{aligned}
  \hat{H} 
  & = \frac{\left| \hat{ \mathbf{p} } \right|^2}{2m_e} \underbrace{ - \frac{q}{m_e} \hat{\mathbf{p}} \cdot \hat{\mathbf{a}} + \frac{q^2}{2m_e} \left| \hat{\mathbf{a}} \right|^2}_{\hat{H}_{int}} + V(\hat{\mathbf{r}}) = \\
\end{aligned}$$

---

Do $\hat p$ and $\hat a$ commute? Likely not! Maybe yes, if $\hat p$ only acts on $e^-$ while $\hat a$ acts on $\vec k,\alpha$.

---

To get the interaction Hamiltonian, put the 2 extra terms (due to the e.m. field) into the expectation formula:

$$
\hat H=\int_x\sum_m\hat b_m^\dagger\psi_m^*(x)\,\hat H_{int}\sum_n\hat b_n\psi_n(x)\,dx
$$

---

```{dropdown} One-body operator for a bosonic field
:open:

Let $\hat{o}$, with $\hat{a}^\dagger$ and $\hat{a}$ creation and annihilation operators in the $\{ | \psi_k \rangle \}_k$ basis. Let $o_{\alpha \beta} = \langle \psi_{\alpha} | \hat{o} | \psi_{\beta} \rangle$.

$$\hat{O}_1 = \sum_{\alpha,\beta} o_{\alpha \beta} \hat{a}^\dagger_{\alpha} \hat{a}_{\beta}$$

or in space representation

$$\hat{O}_1 = $$


```

```{dropdown} One-body operator for a fermionic field
:open:


```



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


````
