(quantum-mechanics:qft:interactions:e-em-fields:atom-spectra)=
# Bound electrons - Atom spectra

...

**todo**
* Schrodinger, Heisenberg and interaction pictures
* Time dependence of the interaction Hamiltonian, in order to make energy conservation applear
* ...

## Bound electron

An electron bound to an isolated atom is governed by the Schrodinger equation - here neglecting spin for simplicity; use Pauli equation for non-relativistic approximation, or Dirac equation -

$i \hbar \dot{| \Psi \rangle} = \left( \frac{|\hat{\mathbf{p}}|^2}{2 m} + V(\hat{\mathbf{r}}) \right) | \Psi \rangle \ ,$$

being $V(\hat{\mathbf{r}})$ the potential energy operator, due to Coulomb force from the nucleus.


## The Hamiltonian

The full Hamiltonian is $\hat{H}=\hat{H}_{\rm el}+\hat{H}_{\rm rad}+\hat{H}_1+\hat{H}_2$ with, from §2.3 (second-quantised via §1.5),

$$
\hat{H}_1(t)=\frac{q}{m} \int d^3 \mathbf{r} \hat{\Psi}^\dagger(\mathbf{r}) \mathbf{A}(\mathbf{r},t) \cdot (-i\hbar\nabla) \hat{\Psi}(\mathbf{r})  \quad , \quad
\hat{H}_2(t)=\frac{q^2}{2m} \int d^3 \mathbf{r} \hat{\Psi}^\dagger(\mathbf{r}) |\mathbf{A}(\mathbf{r},t)|^2 \hat{\Psi}(\mathbf{r}) \ .
$$

Now,
* expanding $\mathbf{A}(\mathbf{r},t)$ with

  $$\hat{\mathbf{A}}(\mathbf{r},t) = \sum_{\mathbf{k}, \mu} \sqrt{\frac{\hbar}{2 \varepsilon_0 \omega_{\mathbf{k}} V}} \boldsymbol\epsilon_{\mathbf{k},\mu} \left( \hat{a}_{\mathbf{k}, \mu} e^{-i(\omega_{\mathbf{k}}t - \mathbf{k} \cdot \mathbf{r})} + \hat{a}^\dagger_{\mathbf{k}, \mu} e^{i(\omega_{\mathbf{k}}t - \mathbf{k} \cdot \mathbf{r})} \right) \ ,$$

* writing the electron fields as linear combinations of creation an annihilation operators $\hat{c}^\dagger$, $\hat{c}$ in any basis $\{ |\alpha \rangle \}$ as 

  $$\begin{aligned}
    \hat{\Psi}^\dagger(\mathbf{r}) & = \sum_{\alpha} \alpha^*(\mathbf{r}) \hat{c}^\dagger_{\alpha} && = \sum_{\alpha} \langle \alpha | \mathbf{r} \rangle \hat{c}^\dagger_{\alpha} \\
    \hat{\Psi}        (\mathbf{r}) & = \sum_{\beta} \beta  (\mathbf{r}) \hat{c}_{\beta} && = \sum_{\beta} \langle \mathbf{r} | \beta \rangle \hat{c}_{\beta} \\
  \end{aligned}$$

the $\hat{H}_1$ interaction Hamiltonian becomes

$$
\hat{H}_1(t)=\frac em\sum_{\alpha\beta}\sum_{\mathbf k \mu}N_k\Big[\langle\alpha|e^{i\mathbf k\cdot\hat{\mathbf{r}}}\,\boldsymbol\epsilon_{\mathbf{k} \mu}\!\cdot\!\hat{\mathbf{p}}|\beta\rangle\, e^{-i \omega_{\mathbf{k}} t}\,c_\alpha^\dagger c_\beta\,a_{\mathbf k\lambda} +\langle\alpha|e^{-i\mathbf k\cdot\hat{\mathbf{r}}}\,\boldsymbol\epsilon_{\mathbf{k}\mu}\!\cdot\!\hat{\mathbf{p}}|\beta\rangle\, e^{i \omega_{\mathbf{k}} t}\,c_\alpha^\dagger c_\beta\,a^\dagger_{\mathbf k\lambda}\Big],
$$ (eq:atom-spectra:H1)

<div style="color:red">in Schrodinger picture? In interaction picture, the creation and annihilation operators of the photon fields includes the time-dependent complex exponent?</div>

(the orderings of $e^{\pm i\mathbf k\cdot\mathbf x}$ and $\boldsymbol\varepsilon\!\cdot\!\mathbf p$ do not matter since $\boldsymbol\varepsilon\!\cdot\!\mathbf k=0$).

```{dropdown} Details

$$\begin{aligned}
  \hat{H}_1(t)
  & = \frac{q}{m} \int \hat{\Psi}^\dagger(\mathbf{r}) \mathbf{A}(\mathbf{r},t) \cdot (-i\hbar\nabla) \hat{\Psi}(\mathbf{r}) d^3 \mathbf{r} = \\
  & = \frac{q}{m} \int \left( \sum_{\alpha} \langle \alpha | \mathbf{r} \rangle \hat{c}^\dagger_{\alpha}\right) \left( \sum_{\mathbf{k},\mu} N_{\mathbf{k}} \boldsymbol\epsilon_{\mathbf{k},\mu} \left( \hat{a}_{\mathbf{k}, \mu} e^{-i(\omega_{\mathbf{k}}t - \mathbf{k} \cdot \mathbf{r})} + \hat{a}^\dagger_{\mathbf{k}, \mu} e^{i(\omega_{\mathbf{k}}t - \mathbf{k} \cdot \mathbf{r})} \right) \right) \cdot \left( - i \hbar \nabla \sum_{\beta} \langle \mathbf{r} | \beta \rangle \hat{c}_{\beta} \right) d^3 \mathbf{r} = && (1) \\
  & = \frac{q}{m} \sum_{\alpha, \beta} \sum_{\mathbf{k},\mu} N_k \int \langle \alpha | \mathbf{r} \rangle \langle \mathbf{r} | \boldsymbol\epsilon_{\mathbf{k},\mu} \cdot \hat{\mathbf{p}} | \beta \rangle d^3 \mathbf{r} \, \hat{c}^\dagger_{\alpha} \hat{c}_{\beta} \left( \hat{a}_{\mathbf{k}, \mu}  e^{-i(\omega_{\mathbf{k}}t - \mathbf{k} \cdot \mathbf{r})} + \hat{a}^\dagger_{\mathbf{k}, \mu} e^{i(\omega_{\mathbf{k}}t - \mathbf{k} \cdot \mathbf{r})} \right)  = && (2) \\
  & = \frac{q}{m} \sum_{\alpha, \beta} \sum_{\mathbf{k},\mu} N_k \langle \alpha | e^{i \mathbf{k} \cdot \hat{\mathbf{r}}} \, \boldsymbol\epsilon_{\mathbf{k},\mu} \cdot \hat{\mathbf{p}} | \beta \rangle \, \hat{c}^\dagger_{\alpha} \hat{c}_{\beta} \left( \hat{a}_{\mathbf{k}, \mu}  e^{-i \omega_{\mathbf{k}}t } + \hat{a}^\dagger_{\mathbf{k}, \mu} e^{i\omega_{\mathbf{k}}t } \right) \ ,
\end{aligned}$$

since (1) $\langle \mathbf{r} | \hat{\mathbf{p}} | \beta \rangle = - i \hbar \nabla \langle \mathbf{r} | \beta \rangle$, and (2) 

$$\begin{aligned}
  \int_{\mathbf{r}} \langle \alpha | \mathbf{r} \rangle e^{i \mathbf{k} \cdot \mathbf{r}} \langle \mathbf{r} | \boldsymbol\epsilon_{\mathbf{k},\mu} \cdot \hat{\mathbf{p}} | \beta \rangle d^3 \mathbf{r}
  & = \int_{\mathbf{r}} \langle \alpha | e^{i \mathbf{k} \cdot \hat{\mathbf{r}}} | \mathbf{r} \rangle \langle \mathbf{r} | \boldsymbol\epsilon_{\mathbf{k},\mu} \cdot \hat{\mathbf{p}} | \beta \rangle d^3 \mathbf{r} = \\
  & = \langle \alpha | e^{i \mathbf{k} \cdot \hat{\mathbf{r}}} \, \boldsymbol\epsilon_{\mathbf{k},\mu} \cdot \hat{\mathbf{p}} | \beta \rangle d^3 \mathbf{r} \ ,
\end{aligned}$$

since $e^{i \mathbf{k} \cdot \mathbf{r}} | \mathbf{r} \rangle = e^{i \mathbf{k} \cdot \hat{\mathbf{r}}} | \mathbf{r} \rangle$, following from $\hat{x}^n | \mathbf{r} \rangle = x^n | \mathbf{r} \rangle$, and $e^{i \mathbf{k} \cdot \mathbf{r}} = \sum_{j=0}^{+\infty} \frac{(i \mathbf{k} \cdot \mathbf{r})^n}{n!}$, and $e^{i \mathbf{k} \cdot \hat{\mathbf{r}}} = \sum_{j=0}^{+\infty} \frac{(i \mathbf{k} \cdot \hat{\mathbf{r}})^n}{n!}$, and $\int_{\mathbf{r}} | \mathbf{r} \rangle \langle \mathbf{r} | \, d^2 \mathbf{r} = \hat{\mathbf{1}}$.


```


Reading the structure:

- $c^\dagger_\alpha c_\beta\,a$: the electron goes from $\beta$ to $\alpha$ **absorbing** a photon; $c^\dagger_\alpha c_\beta\,a^\dagger$: it goes from $\beta$ to $\alpha$ **emitting** one. Electron number is conserved (§2.2), photon number changes by $\pm1$.
- $H_2$ contains $a^\dagger a$ (scattering, photon number unchanged) and $aa$, $a^\dagger a^\dagger$ (two photons absorbed or emitted), each with a factor $c^\dagger_\alpha c_\beta$.
- Total momentum $\mathbf P_{\rm el}+\mathbf P_{\rm rad}$ is conserved when $V=0$, and the total angular momentum and parity in general (§2).

## Transition rates

<div style="color:red">In order to get $\hat{H}_{int}$ independent from time, should one use interaction picture?</div>

Perturbation theory allows to evaluate the transition probability between an initial state $| i \rangle$ and a final state $| f \rangle$ of the unperturbed system, with Hamiltonian $\hat{H}_0$.

For $\hat{H}=\hat{H}_0+\hat{H}_I$ with the Hamiltonian $\hat{H}_0=\hat{H}_{\rm el}+\hat{H}_{\rm rad}$ the Hamiltonian of the non-interacting fields. Let the initial and final states be eigenvectors of the unperturbed Hamiltonian, i.e.

$$\begin{aligned}
  \hat{H}_0 | i \rangle & = \left( \hat{H}_{\rm el} + \hat{H}_{\rm rad} \right) | \mathbf{n}^{\rm el}_i \rangle_{\rm el} \otimes | \mathbf{n}^{\rm rad}_i \rangle_{\mathbf{k} \mu} = \left( \sum_{a} n_{a,i}^{\rm el} E_a^{\rm el} + \sum_{\mathbf{k} \mu} n_{\mathbf{k} \mu,i}^{\rm rad} E_{\mathbf{k} \mu} \right) | i \rangle = E_i | i \rangle \\
  \hat{H}_0 | f \rangle & = \left( \hat{H}_{\rm el} + \hat{H}_{\rm rad} \right) | \mathbf{n}^{\rm el}_f \rangle_{\rm el} \otimes | \mathbf{n}^{\rm rad}_f \rangle_{\mathbf{k} \mu} = \left( \sum_{a} n_{a,f}^{\rm el} E_a^{\rm el} + \sum_{\mathbf{k} \mu} n_{\mathbf{k} \mu,f}^{\rm rad} E_{\mathbf{k} \mu} \right) | f \rangle = E_f | f \rangle \\
\end{aligned}$$

<!--
and eigenstates $|i\rangle,|f\rangle$ of $H_0$, time-dependent perturbation theory (Dyson series, long-time limit) gives the **golden rule**
-->

**Fermi golden rule** provides the ratio of transition probabilities from $| i \rangle$ to $| f \rangle$ as 

$$
\Gamma_{i\to f}=\frac{2\pi}{\hbar}\,|T_{fi}|^2\,\delta(E_f-E_i),\qquad
T_{fi}=\langle f|H_I|i\rangle+\sum_m\frac{\langle f|H_I|m\rangle\langle m|H_I|i\rangle}{E_i-E_m+i0}+\dots
$$

where $m$ runs over *all* intermediate states of $H_0$ (including states with extra photons). The sum over final photon modes is $\sum_{\mathbf k}\to V\!\int d^3k/(2\pi)^3=V\!\int\omega^2\,d\omega\,d\Omega\big/\big((2\pi)^3c^3\big)$, using $k=\omega/c$.

Absorbption and emission are first-order processes and the transition probabilities are dominated by the term $\langle f | \hat{H}^{int} | \rangle \sim \langle f | \hat{H}_{\rm 1} | i \rangle$, i.e. using the expression {eq}`eq:atom-spectra:H1`

* Absorption, **assuming** an existing electron in $| \beta \rangle$ and non existing electron in $| \alpha \rangle$ (to avoid unnecessary complications with the notation, at least here),

   $$\begin{aligned}
     & \langle f | \hat{H}^{abs}_{\rm 1} | i \rangle = \\
     & = \langle \mathbf{n}^{\rm el}_f | \otimes \langle \mathbf{n}_f^{\rm rad} | \left( \sum_{\alpha\beta}\sum_{\mathbf k \mu} M_{\alpha \beta \mathbf{k} \mu}^{\rm abs} c_\alpha^\dagger c_\beta\,a_{\mathbf k\lambda}  \right)  | \mathbf{n}^{\rm el}_i \rangle \otimes | \mathbf{n}_i^{\rm rad} \rangle = \\
     & = \langle \mathbf{n}^{\rm el}_f | \otimes \langle \mathbf{n}_f^{\rm rad} | \sum_{\alpha\beta \mathbf{k} \mu} M_{\alpha \beta \mathbf{k} \mu}^{\rm abs} \sqrt{n_{\mathbf{k}\mu}} | \mathbf{n}^{\rm el}_{i+\alpha-\beta} \rangle \otimes | \mathbf{n}^{\rm rad}_i - \mathbf{1}_{\mathbf{k}\mu} \rangle 
   \end{aligned}$$

   Thus in a final state with non-zero transition probability
   * there's one electron more in $| \alpha \rangle$, and one electron less in $| \beta \rangle$ w.r.t. the initial state, and thus $E^{\rm el}_f = E^{\rm el}_i + E_a - E_b$,
   * a photon with $\mathbf{k} \mu$ is annihilated (absorbed), so that the radiation energies of the initial and final states are related by $E_f^{\rm rad} - E_i^{\rm rad} = - \hbar \omega_{\mathbf{k}}$.

   As the delta condition implies $E_f = E_i$, then $E_a - E_b = \hbar \omega_{\mathbf{k}}$ (energy conservation), the transition probability is proportional to

   $$|\langle f | \hat{H}^{\rm abs}_{\rm 1} | i \rangle|^2 = n_{\mathbf{k} \mu} | M^{\rm abs}_{\alpha \beta \mathbf{k} \mu} |^2 \ .$$


* Emission, **assuming** an existing electron in $| \beta \rangle$ and non existing electron in $| \alpha \rangle$ (to avoid unnecessary complications with the notation, at least here),

   $$\begin{aligned}
     & \langle f | \hat{H}^{\rm em}_{\rm 1} | i \rangle = \\
     & = \langle \mathbf{n}^{\rm el}_f | \otimes \langle \mathbf{n}_f^{\rm rad} | \left( \sum_{\alpha\beta}\sum_{\mathbf k \mu} M_{\alpha \beta \mathbf{k} \mu}^{\rm em} c_\alpha^\dagger c_\beta\,a^\dagger_{\mathbf k\lambda}  \right)  | \mathbf{n}^{\rm el}_i \rangle \otimes | \mathbf{n}_i^{\rm rad} \rangle = \\
     & = \langle \mathbf{n}^{\rm el}_f | \otimes \langle \mathbf{n}_f^{\rm rad} | \sum_{\alpha\beta \mathbf{k} \mu} M_{\alpha \beta \mathbf{k} \mu}^{\rm em} \sqrt{n_{\mathbf{k}\mu} + 1} | \mathbf{n}^{\rm el}_{i+\alpha-\beta} \rangle \otimes | \mathbf{n}^{\rm rad}_i - \mathbf{1}_{\mathbf{k}\mu} \rangle 
   \end{aligned}$$

   Thus in a final state with non-zero transition probability
   * there's one electron more in $| \alpha \rangle$, and one electron less in $| \beta \rangle$ w.r.t. the initial state, and thus $E^{\rm el}_f = E^{\rm el}_i + E_a - E_b$,
   * a photon with $\mathbf{k} \mu$ is created (emitted), so that the radiation energies of the initial and final states are related by $E_f^{\rm rad} - E_i^{\rm rad} = \hbar \omega_{\mathbf{k}}$.

   As the delta condition implies $E_f = E_i$, then $E_a = E_b - \hbar \omega_{\mathbf{k}}$ (energy conservation), the transition probability is proportional to

   $$|\langle f | \hat{H}^{\rm em}_{\rm 1} | i \rangle|^2 = ( n_{\mathbf{k} \mu} + 1) | M^{\rm em}_{\alpha \beta \mathbf{k} \mu} |^2 \ .$$

```{admonition} Absorption, and stimulated and spontanteous emission

Absorption is proportional to $n_{\mathbf{k} \mu}$, while emission is proportional to $n_{\mathbf{k} \mu} + 1$, as the sum of the stimulated and the spontaneous emission transition probability.

```


````{admonition} Symmetry of absorption and stimulated emission factors


$$M^{\rm abs}_{\alpha \beta \mathbf{k} \mu} = \left( M^{\rm abs}_{\beta \alpha \mathbf{k} \mu} \right)^* \ .$$

```{dropdown} Proof

$$M^{\rm em }_{\alpha \beta \mathbf{k} \mu} = \langle \alpha | e^{i \mathbf{k} \cdot \hat{\mathbf{r}}} \boldsymbol\epsilon_{\mathbf{k}\mu} \cdot \hat{\mathbf{p}} | \beta \rangle = \dots$$

```

````

```{admonition} Dipole approximation and Einstein coefficients

...


```


## Absorption and emission of light by an atom

```{dropdown} Time dependence and energy conservation
:open:

$$\begin{aligned}
 \hat{a}_{\mathbf{k}, \mu}^\dagger & \sim e^{ i \frac{E_{\mathbf{k},\mu}}{\hbar} t} \\
 \hat{a}_{\mathbf{k}, \mu}         & \sim e^{-i \frac{E_{\mathbf{k},\mu}}{\hbar} t} \\
 \hat{c}_\alpha^\dagger            & \sim e^{ i \frac{E_\alpha}{\hbar} t} \\
 \hat{c}_\beta                     & \sim e^{-i \frac{E_\beta }{\hbar} t} \\
\end{aligned}$$

---

$$ \hat{c}_\alpha^\dagger \hat{c}_\beta \hat{a}_{\mathbf{k},\mu} | n_\alpha n_\beta n_{\mathbf{k}, \mu}\rangle = | (n+1)_\alpha (n-1)_\beta (n-1)_{\mathbf{k}, \mu}\rangle$$

```


**Matrix elements.** Let the atom go from level $a$ to $b$. With $n$ photons in the mode $(\mathbf k,\lambda)$:

$$
\text{absorption}\ (E_b>E_a):\ \langle b;n{-}1|H_1|a;n\rangle=\frac em N_k\sqrt n\,\langle b|e^{i\mathbf k\cdot\mathbf x}\boldsymbol\varepsilon\!\cdot\!\mathbf p|a\rangle,
$$
$$
\text{emission}\ (E_b<E_a):\ \langle b;n{+}1|H_1|a;n\rangle=\frac em N_k\sqrt{n+1}\,\langle b|e^{-i\mathbf k\cdot\mathbf x}\boldsymbol\varepsilon\!\cdot\!\mathbf p|a\rangle,
$$

using $a|n\rangle=\sqrt n|n-1\rangle$ and $a^\dagger|n\rangle=\sqrt{n+1}|n+1\rangle$. The rates are therefore proportional to $n$ for absorption and to $(n+1)$ for emission: the part $\propto n$ is **stimulated emission** (the mirror image of absorption), and the part $\propto1$ is **spontaneous emission**, which survives in the vacuum ($n=0$) and is caused by the zero-point field of §3.3. A classical field acting on quantised matter gives no spontaneous emission at all (cf. Chapter 1, §2.4).

**Dipole approximation.** Over the size of the atom, $\mathbf k\!\cdot\!\mathbf x\sim ka_0$. For the hydrogen Lyman-$\alpha$ line, $\omega a_0/c=\tfrac38\alpha=2.7\times10^{-3}$, so $e^{\pm i\mathbf k\cdot\mathbf x}=1+O(10^{-3})$ and we replace it by $1$. The remaining matrix element is converted using $[\mathbf x,H_0]=i\hbar\mathbf p/m$:

$$
\langle b|[\mathbf x,H_0]|a\rangle=(E_a-E_b)\langle b|\mathbf x|a\rangle=\frac{i\hbar}{m}\langle b|\mathbf p|a\rangle
\;\Longrightarrow\;
\langle b|\mathbf p|a\rangle=-\,i\,m\,\omega\,\langle b|\mathbf x|a\rangle\quad\big(\hbar\omega=E_a-E_b\big),
$$

(for absorption $E_a<E_b$ the same identity holds with a sign change, which drops out of $|\cdot|^2$). With the dipole matrix element $\mathbf d_{ba}=-e\langle b|\mathbf x|a\rangle$ the emission matrix element has modulus

$$
|M|^2=\Big(\frac em\Big)^2N_k^2\,(n+1)\,m^2\omega^2|\boldsymbol\varepsilon\!\cdot\!\langle b|\mathbf x|a\rangle|^2=\frac{\hbar\omega}{2\varepsilon_0V}\,(n+1)\,|\boldsymbol\varepsilon\!\cdot\!\mathbf d_{ba}|^2 .
$$

**Spontaneous emission rate** ($n=0$). Apply the golden rule, with $\delta(E_a-E_b-\hbar\omega)=\delta(\omega-\omega_{ab})/\hbar$ and the sum of §5.2:

$$
\Gamma=\frac{2\pi}{\hbar}\cdot\frac{1}{\hbar}\cdot\frac{V\omega^2}{(2\pi)^3c^3}\cdot\frac{\hbar\omega}{2\varepsilon_0V}\int d\Omega\sum_\lambda|\boldsymbol\varepsilon_\lambda\!\cdot\!\mathbf d_{ba}|^2
=\frac{\omega^3}{8\pi^2\varepsilon_0\hbar c^3}\int d\Omega\sum_\lambda|\boldsymbol\varepsilon_\lambda\!\cdot\!\mathbf d_{ba}|^2 .
$$

By polarisation completeness, $\sum_\lambda|\boldsymbol\varepsilon_\lambda\!\cdot\!\mathbf d|^2=|\mathbf d|^2-|\hat{\mathbf k}\!\cdot\!\mathbf d|^2$, and with $\int d\Omega\,\hat k_i\hat k_j=\tfrac{4\pi}{3}\delta_{ij}$ the angular integral is $4\pi|\mathbf d|^2-\tfrac{4\pi}{3}|\mathbf d|^2=\tfrac{8\pi}{3}|\mathbf d|^2$. The result is

$$
\boxed{\;\Gamma_{a\to b}=\frac{\omega^3\,|\mathbf d_{ba}|^2}{3\pi\varepsilon_0\hbar c^3}\;}\qquad\Big(\text{angular distribution }\propto\sin^2\theta\text{ from }\mathbf d\Big),
$$

the Einstein $A$ coefficient derived from first principles (Dirac, 1927). It is the number quoted in Chapter 1, §2.4.

```{prf:example} **Worked example: hydrogen $2p\to1s$ (Lyman-$\alpha$).** 

The photon energy is $\hbar\omega=\tfrac34\,\text{Ry}=10.204$ eV, i.e. $\lambda=121.5$ nm. With $R_{10}=2e^{-r/a_0}a_0^{-3/2}$, $R_{21}=\frac{1}{2\sqrt6}(r/a_0)\,e^{-r/2a_0}a_0^{-3/2}$, the radial integral is $\int R_{10}\,r\,R_{21}\,r^2dr=1.2903\,a_0$ and the angular factor $\langle00|\cos\theta|10\rangle=1/\sqrt3$, giving

$$
\langle1s|z|2p,m{=}0\rangle=\frac{2^{15/2}}{3^5}\,a_0=0.7449\,a_0 .
$$

(The rate is the same for $m=0,\pm1$ by rotation symmetry.) Then $|\mathbf d_{ba}|^2=e^2(0.7449\,a_0)^2$ and

$$
\Gamma=6.27\times10^{8}\ \text{s}^{-1},\qquad\tau=1/\Gamma=1.60\ \text{ns},\qquad\Delta\nu_{\rm nat}=\Gamma/2\pi\simeq100\ \text{MHz}.
$$

The measured $2p$ lifetime is $1.60$ ns. By contrast, the $2s$ level cannot decay to $1s$ by a one-photon E1 transition (no parity change, $\Delta l=0$, §2.4); in isolated hydrogen it decays by emitting *two* photons at a rate of only $\approx8\ \text{s}^{-1}$ (lifetime $\approx0.12$ s), about eight orders of magnitude slower than the allowed $2p$ decay.

```

**The classical limit of the rate.** A classical electron oscillator (Lorentz model) of angular frequency $\omega$ radiates, by Larmor's formula $P=e^2\omega^4x_0^2/(12\pi\varepsilon_0c^3)$, with energy $\tfrac12m\omega^2x_0^2$, so its energy decays at rate $\gamma_{\rm cl}=e^2\omega^2/(6\pi\varepsilon_0mc^3)$. Define the oscillator strength $f_{ba}=\frac{2m\omega}{3\hbar g_b}\sum_{ab}|\langle a|\mathbf r|b\rangle|^2$ ($g$ = degeneracy; the sum runs over all sublevels). Substituting into $\Gamma$ gives

$$
\Gamma_{a\to b}=3\,\frac{g_b}{g_a}\,f_{ba}\,\gamma_{\rm cl}.
$$

For Lyman-$\alpha$, $f=0.416$, $g_{1s}/g_{2p}=1/3$ (orbital degeneracies) and $\gamma_{\rm cl}=1.51\times10^{9}\ \text{s}^{-1}$, so $\Gamma=f\gamma_{\rm cl}=6.27\times10^8\ \text{s}^{-1}$ again: **the quantum emission rate is the classical radiation-damping rate times the oscillator strength**, the dimensionless measure of "how much of a classical oscillator" the transition is. The factor $\hbar$ has dropped out of the structure, as it must in a correspondence-principle statement.

**Thermal equilibrium and Einstein's relations.** In blackbody radiation each mode has mean occupation $\bar n=1/(e^{\hbar\omega/k_BT}-1)$. Summing the above over modes, the total emission rate from a level $a$ is $A(\bar n+1)$ and the absorption rate of an atom in $b$ is $(g_a/g_b)A\bar n$ (because the double sum $\sum_{ab}|\mathbf d_{ab}|^2$ is common). Balancing the populations, $N_a\,A(\bar n+1)=N_b\,(g_a/g_b)A\bar n$, gives

$$
\frac{N_a}{N_b}=\frac{g_a}{g_b}\frac{\bar n}{\bar n+1}=\frac{g_a}{g_b}\,e^{-\hbar\omega/k_BT},
$$

exactly the Boltzmann distribution. This is Einstein's 1917 argument (Chapter 1, §2.4), where $A$, $B_{12}$, $B_{21}$ were related by consistency, now obtained as a *theorem* of the quantised theory: the "+1" is spontaneous emission.

**Beyond the dipole approximation.** Expanding $e^{i\mathbf k\cdot\mathbf x}=1+i\mathbf k\!\cdot\!\mathbf x+\dots$ gives electric-quadrupole and magnetic-dipole transitions, suppressed by $(ka_0)^2\sim10^{-5}$ in rate: these account for "forbidden" lines.

