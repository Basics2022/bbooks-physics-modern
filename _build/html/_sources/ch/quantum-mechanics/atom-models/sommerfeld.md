(quantum-mechanics:atom-models:sommerfeld)=
# Sommerfeld model


In 1913, Niels Bohr proposed a revolutionary model of the atom that successfully explained the spectral lines of hydrogen. Bohr’s model combined classical mechanics with quantum concepts, asserting that electrons revolve around the nucleus in fixed, circular orbits with quantized angular momentum:

$$L = n \hbar = n \frac{h}{2\pi}, \quad n \in \{1, 2, 3, \dots\}$$

While the Bohr model was a monumental step forward, high-resolution spectroscopy soon revealed several limitations:
* **Fine Structure:** Spectral lines that initially appeared singular actually split into closely spaced multiplet lines under high resolution.
* **Complex Atoms:** The model failed to accurately predict the spectra of multi-electron atoms (like helium).
* **Zeeman Effect:** It could not explain the splitting of spectral lines in the presence of a magnetic field.

To resolve these shortcomings, German physicist **Arnold Sommerfeld** extended Bohr's theory in 1916 by:
* relaxing the restriction of purely circular orbits.
* introducing relativistic corrections

## Key Postulates and Mathematical Framework

Sommerfeld generalized Bohr’s circular orbit condition using the **Wilson-Sommerfeld Quantization Rule** for periodic systems:

$$\oint p_i \, dq^i = n_i h$$

where $p_i$ is the generalized momentum corresponding to coordinate $q^i$, $n_i$ is an integer quantum number, and $h$ is Planck's constant.

### Elliptical Orbits
Sommerfeld proposed that electron orbits are generally **elliptical**, with the nucleus residing at one of the foci of the ellipse. To describe an ellipse in polar coordinates $(r, \theta)$, two generalized coordinates are required, leading to two quantization conditions:

1. **Azimuthal Quantization**, 

   $$\oint p_\theta \, d\theta = n_\theta h \implies L = n_\theta \hbar$$

2. **Radial Quantization**, 

   $$\oint p_r \, dr = n_r h \ .$$

Here, $n_\theta$ is the azimuthal quantum number (also denoted as $k$) and $n_r$ is the radial quantum number. The total principal quantum number $n$ is defined as:

$$n = n_r + n_\theta$$

The geometry of the ellipse—specifically the ratio of the semi-minor axis $b$ to the semi-major axis $a$—is governed by these quantum numbers:

$$\frac{b}{a} = \frac{n_\theta}{n} = \frac{n_\theta}{n_r + n_\theta}$$

* When $n_\theta = n$, $b = a$, yielding a circular orbit (Bohr's original case).
* When $n_\theta < n$, $b < a$, producing an elliptical orbit.

### Relativistic Correction and Energy Splitting
In non-relativistic mechanics, the energy of an electron in an elliptical orbit depends **only** on the principal quantum number $n$:

$$E_n = -\frac{m_e e^4}{8 \epsilon_0^2 h^2 n^2}$$

This means all orbits with the same $n$ would have identical energy (degeneracy). 

However, Sommerfeld recognized that an electron moves faster when it passes closer to the nucleus in a highly elliptical orbit. Applying Einstein’s special relativity, the electron's mass $m$ varies with velocity $v$:

$$m = \frac{m_0}{\sqrt{1 - v^2/c^2}}$$

When relativistic effects are accounted for, the ellipse undergoes **precession** (perihelion precession), breaking the energy degeneracy. The modified energy expression becomes dependent on both $n$ and $n_\theta$:

$$E_{n, n_\theta} = -\frac{R_y h c Z^2}{n^2} \left[ 1 + \frac{\alpha^2 Z^2}{n} \left( \frac{1}{n_\theta} - \frac{3}{4n} \right) \right]$$

where:
* $R_y$ is the Rydberg constant,
* $Z$ is the atomic number,
* $\alpha = \dfrac{e^2}{4\pi \epsilon_0 \hbar c} \approx \dfrac{1}{137}$ is the **Fine-Structure Constant**.


## Major Achievements

1. **Explanation of Fine Structure:** The dependence of energy levels on $n_\theta$ alongside $n$ successfully explained the small energy differences responsible for the fine splitting of hydrogen spectral lines.
2. **Introduction of Spatial Quantization:** Sommerfeld added a third quantum number $m$ (magnetic quantum number) to describe the orientation of orbits in 3D space, providing a framework for the Zeeman effect.
3. **Introduction of $\alpha$:** It introduced the fine-structure constant $\alpha$, a fundamental constant in modern physics representing the coupling strength of electromagnetic interactions.


## Limitations and Transition to Quantum Mechanics

Despite its empirical success, the Bohr-Sommerfeld model was a **semi-classical (or "Old Quantum Theory")** construction. Its limitations ultimately spurred the transition to modern quantum mechanics:

* **Ad-hoc Assumptions:** It blended classical electrodynamics (planetary orbits) with arbitrary quantization rules without an underlying wave mechanism.
* **Intensity and Selection Rules:** It could not predict the transition probabilities (intensities of spectral lines) accurately.
* **Failure for Multi-Electron Systems:** Like Bohr's model, it could not be extended reliably to helium or larger atoms.

The model was eventually superseded by [the non-relativistic atomic model using **Schrödinger's Wave Mechanics**](quantum-mechanics:atom-models:schrodinger) (1926) and **Dirac's Relativistic Quantum Mechanics** (1928), where $n_\theta$ was replaced by the orbital angular momentum quantum number $l = n_\theta - 1$.
