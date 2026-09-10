(quantum-mechanics:history:dispersion)=
# Light dispersion

## First experiences

(quantum-mechanics:history:dispersion:classical)=
## Classical dispersion

(quantum-mechanics:history:dispersion:classical:drude-lorentz)=
### Drude-Lorentz model

...

$$n(\omega)-1 = \frac{q^2 N}{2 \varepsilon_0 m} \frac{1}{\omega_0^2 - \omega^2 + i \gamVma \omega}$$

**Remark.** The refractive index $n$ is a complex number, with 

$$\begin{aligned}
  \text{re} \{ n \}(\omega) & = 1 + \Delta n_0 \omega^2_0 \frac{\omega_0^2 - \omega^2}{(\omega_0^2 - \omega)^2 + \gamma^2 \omega^2} \\
  \text{im} \{ n \}(\omega) & = - \Delta n_0 \omega^2_0 \frac{\gamma \omega}{(\omega_0^2 - \omega)^2 + \gamma^2 \omega^2} \ \le 0 \ , \quad \forall \omega \ge 0 \\
\end{aligned}$$

Here the condition $\omega \ge 0$ is required by the condition that the incoming wave travels from left to right.

Thus, a travelling wave

$$\varphi(x,t) = e^{i (\omega t - k x)} = e^{i \omega \left( t - \frac{x}{c} \right)} = e^{i \omega \left( t - n \frac{x}{c_0} \right)} \ ,$$

thus contains both a oscillating and a dampening contribution by $n = \text{re}\{ n \} + i \, \text{im}\{ n \}$,

$$\varphi(x,t) = e^{\frac{\omega}{c_0} \text{im}\{ n(\omega) \} x} e^{i \omega \left( t - \text{re}\{ n(\omega) \} \frac{x}{c_0} \right)}$$

As the imaginary part of the refractive index is negative for all the positive frequencies, than the real exponential represents a damping term. The minimum value of $\text{im}\{ n \}(\omega)$ for a slightly damped second-order oscillator occurs approximately at the natural frequency, $\omega_{max damp} \simeq \omega_0$. This represents an **absorption of radiation** by the matter.

**Remark.** Drude-Lorentz model in the form $n - 1 = \delta$ is compatible with empirical formulas in the form $n^2 - 1 = \widetilde{\delta}$, as the correction is "small enough" for a linear approximation

$$n^2 = ( 1 + \delta )^2 \simeq 1 + 2 \delta \ .$$

