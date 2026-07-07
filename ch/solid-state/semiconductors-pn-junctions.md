(semiconductors:pn-junctions)=
# $p$-$n$ Junctions


<!--
(semiconductors:pn-junctions:regimes)=
## Regimes

(semiconductors:pn-junctions:zero-bias)=
## Zero bias

(semiconductors:pn-junctions:fwd-bias)=
## Forward bias

(semiconductors:pn-junctions:reverse-bias)=
## Reverse bias

-->

## Introduction to the pn Junction and its Operational Regimes

When a $p$-type and an $n$-type semiconductor are brought into intimate contact, the immense carrier concentration gradients at the interface drive a transient diffusion process. Mobile electrons and holes annihilate each other at the metallurgical interface, leaving behind uncompensated, fixed dopant ions. This region, stripped of mobile carriers, is known as the **depletion region**. The fixed charges generate an internal electric field that opposes further diffusion, establishing a balance.

Depending on the external voltage $V_a$ applied across the device, the junction operates in one of three primary regimes:

* **Zero Bias (Thermal Equilibrium, $V_a = 0$):** No external voltage is applied. The internal electric field perfectly balances the carrier diffusion gradients. The net current density for both electrons and holes is identically zero ($J_n = 0, J_p = 0$).
* **Forward Bias ($V_a > 0$):** A positive potential is applied to the $p$-side relative to the $n$-side. This external potential opposes the built-in field, lowering the electrostatic barrier and narrowing the depletion width. Diffusion forces win over drift, resulting in an exponential injection of minority carriers across the junction.
* **Reverse Bias ($V_a < 0$):** A negative potential is applied to the $p$-side relative to the $n$-side. The external voltage reinforces the built-in field, widening the depletion region and increasing the potential barrier. Diffusion drops to zero, and the current is limited to a minute reverse saturation current driven by thermal generation.

---

## The Depletion Approximation and Shockley Transport

To derive closed-form analytical expressions for the electrostatics and current-voltage relations, we employ the **Depletion Approximation** (also called the *Abrupt Junction Approximation*). This framework assumes that the transition between doping zones is perfectly sharp and that the depletion region is completely devoid of mobile carriers ($\rho = \text{constant}$ inside the zone, $\rho = 0$ outside).

| Concentration | $p$-bulk     | $p$-interface | $n$-interface | $n$-bulk     |
| :------------ | :------:     | :-----------: | :-----------: | :------:     |
| $N_A^-$       | $\sim N_A$   | $\sim N_A$    |               |              |
| $N_D^+$       |              |               | $\sim N_D$    | $\sim N_D$   |
| $p$           | $\sim N_A^-$ |               |               |              |
| $n$           |              |               |               | $\sim N_D^+$ |
| $\rho$        |              | $-N_A^- q$    | $N_D^+ q$     |              |

### Zero Bias (Thermal Equilibrium)
By applying the depletion approximation, the net space-charge density $\rho(x)$ is treated as piecewise constant:

$$\rho(x) = \begin{cases} 
  0 & x \lt x_p \\
 -q N_A & x_p \le x < 0 \\
  q N_D & 0 \le x \le x_n \\
  0 & x \gt x_n \ .
\end{cases}$$

Integrating Gauss' law, $\partial_x e(x) = \frac{\rho(x)}{\varepsilon}$, with the assumption of electrical neutrality, $0 = q (N_A x_p + N_D x_n)$, and zero field outsied the interface,

$$e(x) = \begin{cases}
  0 & x \lt x_p \\
  -\frac{q N_A}{\varepsilon} \left( x - x_p \right) & x_p \le x < 0 \\
   \frac{q N_D}{\varepsilon} \left( x - x_n \right) & 0 \le x \le x_n \\
  0 & x \gt x_n \ .
\end{cases}$$

Integrating Poisson's equation, $\frac{d^2\psi}{dx^2} = -\frac{\rho}{\varepsilon_s}$, across this profile yields a linear electric field $E(x)$ that peaks at the metallurgical interface ($x=0$), and a quadratic electrostatic potential $\psi(x)$.



The total voltage drop across the region is the **built-in potential** $V_{bi}$, determined by the bulk doping concentrations and the Law of Mass Action ($n_0 p_0 = n_i^2$):

$$V_{bi} = V_t \ln\left(\frac{N_A N_D}{n_i^2}\right)$$

where $V_t = \frac{k_B T}{q}$ is the thermal voltage. Global charge neutrality requires $N_A x_p = N_D x_n$, yielding the equilibrium depletion width $W_0$:

$$W_0 = x_p + x_n = \sqrt{\frac{2\varepsilon_s V_{bi}}{q} \left( \frac{1}{N_A} + \frac{1}{N_D} \right)}$$

### Forward Bias Under Shockley Assumptions
To find the explicit $I\text{-}V$ relationship, we introduce the **Shockley Ideal Conditions**:
1. Low-level injection ($n \ll N_A$ in the $p$-bulk; $p \ll N_D$ in the $n$-bulk).
2. No recombination or generation occurs inside the depletion region.
3. The electric field in the neutral bulk regions is negligible; transport there is purely diffusion-driven.

The applied forward voltage $V_a$ lowers the barrier, modifying the depletion width to:

$$W(V_a) = \sqrt{\frac{2\varepsilon_s (V_{bi} - V_a)}{q} \left( \frac{1}{N_A} + \frac{1}{N_D} \right)}$$

The lower barrier allows carriers to scale the potential wall. The carrier concentrations at the edges of the depletion region follow the **Law of the Junction**:

$$n(-x_p) = n_{p0} \exp\left(\frac{V_a}{V_t}\right), \quad p(x_n) = p_{n0} \exp\left(\frac{V_a}{V_t}\right)$$

In the neutral bulk, these injected minority carriers move via diffusion while continuously recombining with the abundant majority carriers. Solving the steady-state minority carrier diffusion equation, $D_p \frac{d^2\Delta p_n}{dx^2} = \frac{\Delta p_n}{\tau_p}$, reveals an exponentially decaying carrier profile away from the boundaries:

$$\Delta p_n(x) = p_{n0} \left[ \exp\left(\frac{V_a}{V_t}\right) - 1 \right] \exp\left(-\frac{x - x_n}{L_p}\right)$$

Evaluating the diffusion current density ($J_p = -q D_p \frac{d\Delta p_n}{dx}$) at the boundaries and summing both carrier contributions yields the classic **Shockley Diode Equation**:

$$I = I_0 \left[ \exp\left(\frac{V_a}{V_t}\right) - 1 \right] \quad \text{where} \quad I_0 = A_j q n_i^2 \left( \frac{D_n}{L_n N_A} + \frac{D_p}{L_p N_D} \right)$$

### Reverse Bias
Under reverse bias, $V_a$ is negative. The effective potential barrier increases to $V_{bi} + |V_a|$, and the depletion region widens, increasing the internal electric field. Diffusion currents drop to zero. The current is governed by the minority carriers in the bulk wandering near the depletion edge, where they are immediately caught by the strong electric field and swept across. This results in a tiny, voltage-independent current equal to $-I_0$.

---

**todo**

## Advanced Description: Quasi-Fermi Levels and Non-Equilibrium Transport

While the depletion approximation and Shockley models provide excellent analytical insights, they break down when trying to model intermediate zones, high-injection regimes, or continuous spatial profiles. Under non-equilibrium conditions ($V_a \neq 0$), the Law of Mass Action is violated ($n \cdot p \neq n_i^2$), meaning a single Fermi level $E_F$ can no longer describe the system.

To build a rigorous, continuous model, we split the equilibrium Fermi level into two independent parameters: **$E_{Fn}(x)$** (the quasi-Fermi level for electrons) and **$E_{Fp}(x)$** (the quasi-Fermi level for holes).

### 3.1 Carrier Statistics under Non-Equilibrium
We express the continuous free carrier concentrations using these independent variables relative to the intrinsic energy level $E_i(x)$:

$$n(x) = n_i \exp\left(\frac{E_{Fn}(x) - E_i(x)}{k_B T}\right)$$

$$p(x) = n_i \exp\left(\frac{E_i(x) - E_{Fp}(x)}{k_B T}\right)$$

Multiplying these equations demonstrates how the splitting of the quasi-Fermi levels tracks the deviation from thermal equilibrium:

$$n(x) \cdot p(x) = n_i^2 \exp\left(\frac{E_{Fn}(x) - E_{Fp}(x)}{k_B T}\right)$$

* In **Forward Bias**, $E_{Fn} > E_{Fp}$, meaning $n \cdot p > n_i^2$, indicating a net excess of mobile carriers.
* In **Reverse Bias**, $E_{Fn} < E_{Fp}$, meaning $n \cdot p < n_i^2$, representing a net suppression of mobile carriers.

### 3.2 Current Formulations via Quasi-Fermi Gradients
Substituting these non-equilibrium statistics into the classic drift-diffusion current density equations ($J_n = -q\mu_n n \frac{d\psi}{dx} + qD_n \frac{dn}{dx}$) leads to a vital physical simplification:

$$J_n(x) = \mu_n n(x) \frac{dE_{Fn}}{dx}$$

$$J_p(x) = \mu_p p(x) \frac{dE_{Fp}}{dx}$$

This formulation demonstrates that net current flows if and only if there is a spatial gradient in the quasi-Fermi levels.



In the neutral bulk regions under low-level forward injection, the majority carrier quasi-Fermi level remains nearly flat, while the minority carrier quasi-Fermi level slopes sharply, driving the diffusion current. Inside the depletion region, both levels split by an amount exactly equal to the applied electrical bias: $E_{Fn} - E_{Fp} = q V_a$.

This continuous framework forms the mathematical foundation required to solve the coupled drift-diffusion equations numerically without relying on piecewise zone assumptions.

