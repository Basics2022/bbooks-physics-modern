(quantum-mechanics:history:origins)=
# Origins of Matrix and Wave Quantum Mechanics

(quantum-mechanics:history:origins:matrix-mechanics)=
## Origins of Matrix Mechanics

````{dropdown} Quantization of radiation energy.
:open:

* Planck (1900), Einstein photoelectric effect (1905) and heat capacity of the solids: introduction and evidences of $h$, $E = h \nu$

  $$u(\nu, T) = \dots$$ (eq:history:planck-radiation-formula)

````

````{dropdown} Light-matter interaction and light dispersion.
:open:
* First experimental evidences: Cauchy; Sellmeier (1872) proposed an empirical law for the refraction index $n$ taking into account resonances of matter; [Lorentz-Drude](quantum-mechanics:history:dispersion:classical:drude-lorentz) (1900-1905) provided a theoretical model of Sellmeier formula, using Maxwell equations for electromagentism,

  $$n - 1 = \dfrac{q^2 N}{2 \varepsilon m} \dfrac{1}{\omega_0^2 - \omega^2 + i \gamma \omega} \approx \dfrac{q^2 N}{2 \varepsilon m} \dfrac{1}{\omega_0^2 - \omega^2}  \ ,$$ (eq:history:lorenz-drude)

  being $m$ and $q$ the mass and the charge of a particle, $N$ the number density of the charged particles, $\omega_0$ the natural frequency and $\gamma$ a damping coefficient of the dynamical equation governing the dynamics of the particle, $m \ddot{x} + m \gamma \omega \dot{x} + m \omega_0^2 x = q E(t)$.

* Einstein (1916): quantum theory of the radiation interacting with matter.
  * Statistics of the equilibrium of radiation and matter, with the processes of absorption, spontaneous emission and stimulated emissions. He introduced Einstein coefficiens as proportionality constants
  * E. theory connected Bohr's atomic with Planck's radiation formula {eq}`eq:history:planck-radiation-formula`: matching Planck's formula induces relationss between Einstein coefficients,

    $$
    \dfrac{A_{jk}}{B_{kj}} \dfrac{g_j}{g_k} = \dfrac{8 \pi \nu^3}{c^3}
    \qquad , \qquad                        
    \dfrac{B_{jk}}{B_{kj}} \dfrac{g_j}{g_k} = 1 \ .
    $$

    Einstein didn't know how to compute $A_{ik}$, $B_{jk}$, $B_{kj}$, but he was confident that it would have been possible to do so, once a theory of quanta was established.

* Ladenburg (1914-24)
  * a material may have more than one resonance. The generalization of the formula {eq}`eq:history:lorenz-drude` for the refractive index $n$ from Lorentz-Drude model reads

    $$n - 1 = \dfrac{q^2}{2 \varepsilon m} \sum_{k} \dfrac{N_k}{\omega_k^2 - \omega^2} \ ,$$

    with $N_k$ the "number density of particles"[^number-density-nk] with natural frequency $f_k = \dfrac{\omega_k}{2 \pi}$.

  * But what's the meaning of $N_k$? Ladenburg compared the averaged emitted power from [**Larmor's formula**](moving-charge-radiation) {eq}`eq:larmor:quadratic:power-energy` - the classical model - and the emitted power by [**Planck's formula**](), or by [**Einstein quantum theory of interaction of radiation and matter**]() - the quantum model, for a frequency $\nu_{ij}$. The power emitted by $R$ resonators per unit volume is

    ...
    <!--
    $$\begin{aligned}
      \langle P \rangle
      & = R \, \langle \Phi_1 \rangle = \\
      & = R \gamma E = \\
      & = R \gamma \dfrac{c^3}{8 \pi \nu^2} \rho(\nu)
    \end{aligned}$$

    ```{dropdown} Dimensional analysis
   
    $$\begin{aligned}
    [ \langle \Phi_1 \rangle ] & = \dfrac{\text{power}}{\text{n.parts}} \\
    [ R ] & = \dfrac{\text{n.parts}}{\text{length}^3} \\
    [ \langle P \rangle ] & = \dfrac{\text{power}}{\text{length}^3} \\
    \end{aligned}$$

    $$\rho(\nu) = \dots$$

    ```
    -->

[^number-density-nk]: This should be interpreted as a weight representing the contribution of mode $k$. 

````

````{dropdown} Particle-wave duality.
:open:

* Einstein (1909): radiation has wave and particle behavior

````

````{dropdown} Atomic models.
:open:

* Bohr atomic model (1913).

````


