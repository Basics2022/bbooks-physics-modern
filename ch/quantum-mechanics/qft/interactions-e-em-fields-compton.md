(quantum-mechanics:qft:interactions:e-em-fields:compton-scattering)=
# Free electrons - Compton scattering

**Setup.** Take $V=0$ and an electron initially at rest with spin $\sigma$:

$$
|i\rangle=c^\dagger_{\mathbf 0\sigma}\,a^\dagger_{\mathbf k\lambda}|0\rangle,\qquad|f\rangle=c^\dagger_{\mathbf p'\sigma'}\,a^\dagger_{\mathbf k'\lambda'}|0\rangle,\qquad\mathbf p'=\hbar(\mathbf k-\mathbf k')\ \ \text{(momentum conservation)}.
$$

There are three contributions at order $e^2$, the time-ordered diagrams: (a) the seagull $H_2$ acting once; (b) $H_1$ twice, absorbing $\mathbf k$ first then emitting $\mathbf k'$; (c) $H_1$ twice, emitting $\mathbf k'$ first then absorbing $\mathbf k$.

**The $H_1H_1$ terms vanish.** In (b) the first vertex is $\langle\hbar\mathbf k|e^{i\mathbf k\cdot\mathbf x}\boldsymbol\varepsilon\!\cdot\!\mathbf p|\mathbf 0\rangle\propto\boldsymbol\varepsilon\!\cdot\!\mathbf p_i=0$ because $\mathbf p$ acts on the initial state, which has $\mathbf p_i=0$. In (c) the first vertex is $\propto\boldsymbol\varepsilon'\!\cdot\!\mathbf p_i=0$ for the same reason. (This is exact in Coulomb gauge: $\boldsymbol\varepsilon\!\cdot\!\mathbf p$ acts *before* the intermediate momentum appears.) For a moving electron these terms are of relative order $p/mc$, producing the Doppler broadening of the Compton line.

**The seagull term.** The matrix element of $\mathbf A^2$ between $|\mathbf k\lambda\rangle$ and $|\mathbf k'\lambda'\rangle$ has two contributions ($q=\mathbf k,q'=\mathbf k'$ and the swap), so

$$
\langle f|H_2|i\rangle=\frac{e^2}{2m}\cdot2N_kN_{k'}\,(\boldsymbol\varepsilon\!\cdot\!\boldsymbol\varepsilon')\;\underbrace{\frac1V\!\int d^3x\,e^{i(\mathbf k-\mathbf k')\cdot\mathbf x}\,e^{-i\mathbf p'\cdot\mathbf x/\hbar}}_{\delta_{\mathbf p',\hbar(\mathbf k-\mathbf k')}}
=\frac{e^2\hbar}{2m\varepsilon_0V\sqrt{\omega\omega'}}\,(\boldsymbol\varepsilon\!\cdot\!\boldsymbol\varepsilon')\,\delta_{\mathbf p',\hbar(\mathbf k-\mathbf k')},
$$

(using $N_kN_{k'}=\hbar/(2\varepsilon_0V\sqrt{\omega\omega'})$; the electron plane waves $V^{-1/2}e^{i\mathbf p\cdot\mathbf x/\hbar}$ supply the $1/V$, and $\mathbf p_i=0$). 

**Cross-section.** The golden rule with the final photon density of states $V\omega'^2d\Omega/\big((2\pi)^3c^3\hbar\big)$ (we neglect the electron recoil in the Jacobian $dE_f/d\omega'=\hbar(1+O(\hbar\omega/mc^2))$) gives

$$
\frac{d\Gamma}{d\Omega}=\frac{2\pi}{\hbar}\Big(\frac{e^2\hbar}{2m\varepsilon_0V\sqrt{\omega\omega'}}\Big)^2|\boldsymbol\varepsilon\!\cdot\!\boldsymbol\varepsilon'|^2\frac{V\omega'^2}{8\pi^3c^3\hbar}
=\frac{e^4}{16\pi^2m^2\varepsilon_0^2c^3V}\,\frac{\omega'}{\omega}\,|\boldsymbol\varepsilon\!\cdot\!\boldsymbol\varepsilon'|^2 .
$$

The incident flux is one photon per volume $V$ at speed $c$, i.e. $c/V$. Dividing,

$$
\boxed{\;\frac{d\sigma}{d\Omega}=r_e^2\,\frac{\omega'}{\omega}\,|\boldsymbol\varepsilon\!\cdot\!\boldsymbol\varepsilon'|^2,\qquad r_e=\frac{e^2}{4\pi\varepsilon_0mc^2}=2.818\ \text{fm}\;}
$$

(using $e^4/(16\pi^2m^2\varepsilon_0^2c^4)=r_e^2$). This is **Thomson scattering**, derived here from the quantised theory, with a polarisation dependence $|\boldsymbol\varepsilon\!\cdot\!\boldsymbol\varepsilon'|^2$ (the scattered photon keeps the projected polarisation of the incident one).

**Unpolarised light.** Summing over the final polarisations with completeness, $\sum_{\lambda'}|\boldsymbol\varepsilon\!\cdot\!\boldsymbol\varepsilon'_{\lambda'}|^2=1-(\boldsymbol\varepsilon\!\cdot\!\hat{\mathbf k}')^2$, and averaging over the two incident polarisations, $\tfrac12\sum_\lambda(\boldsymbol\varepsilon_\lambda\!\cdot\!\hat{\mathbf k}')^2=\tfrac12\sin^2\theta$ (the two polarisations transverse to $\hat{\mathbf k}$ together project onto $\hat{\mathbf k}'$ with weight $1-\cos^2\theta$). The polarisation-averaged factor is thus $1-\tfrac12\sin^2\theta=\tfrac12(1+\cos^2\theta)$. Hence

$$
\frac{d\sigma}{d\Omega}\Big|_{\rm unpol}=\frac{r_e^2}{2}\,\frac{\omega'}{\omega}\,(1+\cos^2\theta),\qquad
\sigma_{\rm T}=\frac{8\pi}{3}r_e^2=6.652\times10^{-29}\ \text{m}^2=0.665\ \text{b},
$$

using $\int(1+\cos^2\theta)\,d\Omega=16\pi/3$ and $\omega'/\omega\to1$. The cross-section is independent of the frequency and of $\hbar$: it is the classical result of an electron driven by the wave and radiating as a Hertzian dipole, recovered as the leading term of a quantum calculation.

Two physical consequences follow from the factor $|\boldsymbol\varepsilon\!\cdot\!\boldsymbol\varepsilon'|^2$:

- The component of the incident polarisation perpendicular to the scattering plane scatters with weight $1$, the in-plane component with weight $\cos^2\theta$. At $\theta=90^\circ$ the scattered light is therefore **100% linearly polarised** (perpendicular to the plane), with degree of polarisation $(1-\cos^2\theta)/(1+\cos^2\theta)$ in general. This is why scattered light, in the sky and in the cosmic microwave background, is polarised.
- Where electrons are free, mean free paths are set by $\ell=1/(n_e\sigma_{\rm T})$: in the solar core ($n_e\approx6\times10^{31}\,\text{m}^{-3}$) this is $\approx0.25$ mm.

**Kinematics: the Compton shift from energy conservation.** The delta function enforces $\hbar\omega=\hbar\omega'+\hbar^2|\mathbf k-\mathbf k'|^2/2m$. Write $|\mathbf k-\mathbf k'|^2=(k-k')^2+2kk'(1-\cos\theta)$. The first term is second order in the small shift, so to leading order in $\hbar\omega/mc^2$,

$$
c\,(k-k')=\frac{\hbar k^2(1-\cos\theta)}{m}\quad\Longrightarrow\quad\frac1{k'}-\frac1k=\frac{k-k'}{kk'}\simeq\frac{\hbar(1-\cos\theta)}{mc},
$$

and with $\lambda=2\pi/k$,

$$
\lambda'-\lambda=\frac{h}{mc}\,(1-\cos\theta),
$$

the Compton formula of Chapter 1, now as the energy conservation of the Fock-space matrix element above. (The exact *relativistic* kinematics gives the same formula without approximation.)

**Where the non-relativistic theory fails.** We can quantify the neglected corrections by comparing the scattered-photon energy at $90^\circ$ from exact relativistic kinematics, $E'=E/(1+E/mc^2)$, with that from the non-relativistic energy balance used above (computed numerically):

| Incident $E$ | Exact $E'$ ($90^\circ$) | Non-relativistic $E'$ | Error |
|:--|:--|:--|:--|
| 17.44 keV (Mo K$\alpha$) | 16.8644 keV | 16.8641 keV | $2\times10^{-5}$ |
| 100 keV | 83.63 keV | 83.41 keV | 0.27% |
| 661.66 keV ($^{137}$Cs) | 288.3 keV | 195.8 keV | 32% |

(For the Mo line, the wavelength shift is $2.4263$ pm exactly, against $2.4277$ pm from the non-relativistic balance.) The relativistic theory (quoted: **Klein–Nishina**, 1929, requiring the Dirac field) gives for unpolarised light

$$
\frac{d\sigma}{d\Omega}=\frac{r_e^2}{2}\Big(\frac{\omega'}{\omega}\Big)^2\Big[\frac{\omega'}{\omega}+\frac{\omega}{\omega'}-\sin^2\theta\Big],
$$

which reduces to our result when $\omega'\to\omega$: $\tfrac12(2-\sin^2\theta)=\tfrac12(1+\cos^2\theta)$. Integrated over angles, the total cross-section relative to Thomson is $\sigma_{\rm KN}/\sigma_{\rm T}=0.937$ at 17.44 keV, $0.741$ at 100 keV, $0.385$ at 662 keV and $0.125$ at 5 MeV: the forward-peaked, energy-dependent suppression that makes high-energy photons penetrating.

**Gauge invariance and the seagull.** In the calculation above only $H_2$ contributed. Had we dropped it as "a second-order nuisance", the amplitude for a free electron at rest would vanish and scattering would be absent, which contradicts the classical (and experimental) Thomson result. The coefficient of $H_2$ is tied to that of $H_1$ by gauge invariance (§2.3), and the amplitude at $\omega\to0$, $-r_e\,\boldsymbol\varepsilon\!\cdot\!\boldsymbol\varepsilon'$, is fixed by the charge and mass alone (a *low-energy theorem*).

**Scattering by a bound electron (quoted).** For an atomic electron initially in $|a\rangle$ and finally in $|b\rangle$, with the same ingredients (the three diagrams and the dipole approximation), the amplitude is

$$
T_{ba}\propto\frac{e^2}{m}\Big[\boldsymbol\varepsilon\!\cdot\!\boldsymbol\varepsilon'\,\delta_{ba}+\frac1m\sum_m\Big(\frac{\langle b|\boldsymbol\varepsilon'\!\cdot\!\mathbf p|m\rangle\langle m|\boldsymbol\varepsilon\!\cdot\!\mathbf p|a\rangle}{E_a+\hbar\omega-E_m}+\frac{\langle b|\boldsymbol\varepsilon\!\cdot\!\mathbf p|m\rangle\langle m|\boldsymbol\varepsilon'\!\cdot\!\mathbf p|a\rangle}{E_a-\hbar\omega'-E_m}\Big)\Big],
$$

the **Kramers–Heisenberg formula** (1925), with the intermediate states $m$ of the atom (including the continuum). The three regimes are all contained in it: for $\hbar\omega\gg$ binding energies the denominators are large, the second term is negligible and one recovers free-electron **Thomson** scattering; for $\hbar\omega\ll E_m-E_a$ the $\omega$-independent terms cancel against the seagull by the Thomas–Reiche–Kuhn sum rule $\sum_m(E_m-E_a)|\langle m|x|a\rangle|^2=\hbar^2/2m$, leaving the **Rayleigh** law $\sigma\propto\omega^4$ (blue sky); and for $\hbar\omega\to E_m-E_a$ the denominators vanish and the amplitude has a **resonance** (resonance fluorescence), regulated by the natural linewidth $\Gamma$ of §5.3.

