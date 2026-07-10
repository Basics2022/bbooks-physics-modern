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

(semiconductors:pn-junctions:regimes)=
## Introduction to the pn Junction and its Operational Regimes

When a $p$-type and an $n$-type semiconductor are brought into intimate contact, the immense carrier concentration gradients at the interface drive a transient diffusion process. Mobile electrons and holes annihilate each other at the metallurgical interface, leaving behind uncompensated, fixed dopant ions. This region, stripped of mobile carriers, is known as the **depletion region**. The fixed charges generate an internal electric field that opposes further diffusion, establishing a balance.

Depending on the external voltage $V_a$ applied across the device, the junction operates in one of three primary regimes:

* **Zero Bias (Thermal Equilibrium, $V_a = 0$):** No external voltage is applied. The internal electric field perfectly balances the carrier diffusion gradients. The net current density for both electrons and holes is identically zero ($J_n = 0, J_p = 0$).
* **Forward Bias ($V_a > 0$):** A positive potential is applied to the $p$-side relative to the $n$-side. This external potential opposes the built-in field, lowering the electrostatic barrier and narrowing the depletion width. Diffusion forces win over drift, resulting in an exponential injection of minority carriers across the junction.
* **Reverse Bias ($V_a < 0$):** A negative potential is applied to the $p$-side relative to the $n$-side. The external voltage reinforces the built-in field, widening the depletion region and increasing the potential barrier. Diffusion drops to zero, and the current is limited to a minute reverse saturation current driven by thermal generation.

---

(semiconductors:pn-junctions:depletion-approximation)=
## The Depletion Approximation and Shockley Transport

To derive closed-form analytical expressions for the electrostatics and current-voltage relations, we employ the **Depletion Approximation** (also called the *Abrupt Junction Approximation*). This framework assumes that the transition between doping zones is perfectly sharp and that the depletion region is completely devoid of mobile carriers ($\rho = \text{constant}$ inside the zone, $\rho = 0$ outside).

| Concentration | $p$-bulk     | $p$-interface | $n$-interface | $n$-bulk     |
| :------------ | :------:     | :-----------: | :-----------: | :------:     |
| $N_A^-$       | $\sim N_A$   | $\sim N_A$    |               |              |
| $N_D^+$       |              |               | $\sim N_D$    | $\sim N_D$   |
| $p$           | $\sim N_A^-$ |               |               |              |
| $n$           |              |               |               | $\sim N_D^+$ |
| $\rho$        |              | $-N_A^- q$    | $N_D^+ q$     |              |

(semiconductors:pn-junctions:depletion-approximation:zero-bias)=
### Zero Bias (Thermal Equilibrium)
By applying the depletion approximation, the net space-charge density $\rho(x)$ is treated as piecewise constant:

$$\rho(x) = \begin{cases} 
  0 & x \lt x_p \\
 -q N_A & x_p \le x < 0 \\
  q N_D & 0 \le x \le x_n \\
  0 & x \gt x_n \ .
\end{cases}$$

Integrating Gauss' law, $\partial_x e(x) = \frac{\rho(x)}{\varepsilon}$, with the assumption of electrical neutrality, $0 = q (N_A x_p + N_D x_n)$, and zero field outside the interface,

$$e(x) = \begin{cases}
  0 & x \lt x_p \\
  -\frac{q N_A}{\varepsilon} \left( x - x_p \right) & x_p \le x < 0 \\
   \frac{q N_D}{\varepsilon} \left( x - x_n \right) & 0 \le x \le x_n \\
  0 & x \gt x_n \ .
\end{cases}$$

Integrating the relation between the electric field and the electric potential, $e(x) = - \partial_x \phi(x)$, with the reference $\phi(x) = 0$ in the $p$-bulk, $x < x_p$,

$$\phi(x) = \begin{cases}
  0 & x \lt x_p \\
  \frac{q N_A}{2 \varepsilon} \left( x - x_p \right)^2 & x_p \le x < 0 \\
  \frac{q N_D}{2 \varepsilon} \left( x - x_n  \right)^2 + \frac{q N_A}{2 \varepsilon} x_p^2 - \frac{q N_D}{2 \varepsilon} x_n^2 & 0 \le x \le x_n \\
  \frac{q}{2 \varepsilon} \left( N_A x_p^2 - N_D x_n^2 \right) =: V_{bi} & x \gt x_n \ .
\end{cases}$$

Global charge neutrality requires $-N_A x_p = N_D x_n$, yielding the equilibrium depletion width $W_0$:

$$W_0 = x_p + x_n = \sqrt{\frac{2\varepsilon_s V_{bi}}{q} \left( \frac{1}{N_A} + \frac{1}{N_D} \right)}$$


```{dropdown} Details

For the continuity of the potential, for $0 \le x \le x_n$, 

$$\begin{aligned}
  \phi(x) 
  & = - \frac{q N_D}{\varepsilon} \left[ \frac{x^2}{2} - x_n x \right] + \phi(0) = \\
  & = - \frac{q N_D}{\varepsilon} \left[ \frac{x^2}{2} - x_n x \right] + \frac{q N_A}{2 \varepsilon} x_p^2 = \\
  & = - \frac{q N_D}{2 \varepsilon} \left( x - x_n  \right)^2 + \frac{q N_A}{2 \varepsilon} x_p^2 + \frac{q N_D}{2 \varepsilon} x_n^2
\end{aligned}$$

Thus the potential difference across the depletion region $V_{bi}$ reads,

$$\begin{aligned}
  \phi(x_n) = \frac{q}{2 \varepsilon} \left( N_A x_p^2 + N_D x_n^2 \right) =: V_{bi} \ .
\end{aligned}$$

The width of the depletion region be $w$ can be written as

$$\begin{aligned}
  w 
  & = x_n - x_p = \\ 
  & = x_n \left( 1 + \frac{N_D}{N_A} \right)
    = x_n N_D \left( \frac{1}{N_D} + \frac{1}{N_A} \right) = \\
  & = - x_p \left( \frac{N_A}{N_D} + 1 \right) 
    = - x_p N_A \left( \frac{1}{N_D} + \frac{1}{N_A} \right) \ ,
\end{aligned}$$

then the potential can be written as

$$\begin{aligned}
  V_{bi}
  & = \frac{q}{2 \varepsilon} \left( \frac{N_A^2 x_p^2}{N_A} + \frac{N_D^2 x_n^2}{N_D} \right) = \\
  & = \frac{q}{2 \varepsilon} N_A^2 x_p^2 \left( \frac{1}{N_A} + \frac{1}{N_D} \right) = \\
  & = \frac{q}{2 \varepsilon} w^2 \left( \frac{1}{N_A} + \frac{1}{N_D} \right)^{-1} \ .
\end{aligned}$$

Thus the width of the depletion region can be written as a function of the built-in potential as

$$w = \sqrt{\frac{2 \varepsilon V_{bi}}{q} \left( \frac{1}{N_A} + \frac{1}{N_D} \right)} \ .$$

```

---

**todo** *Deal with some statistical mechanics to show this*

The total voltage drop across the region is the **built-in potential** $V_{bi}$, determined by the bulk doping concentrations and the Law of Mass Action ($n_0 p_0 = n_i^2$):

$$V_{bi} = V_t \ln\left(\frac{N_A N_D}{n_i^2}\right)$$

where $V_t = \frac{k_B T}{q}$ is the thermal voltage. 


(semiconductors:pn-junctions:depletion-approximation:fwd-bias)=
### Forward Bias Under Shockley Assumptions
To find the explicit $I\text{-}V$ relationship, we introduce the **Shockley Ideal Conditions**:
1. Low-level injection ($n \ll N_A$ in the $p$-bulk; $p \ll N_D$ in the $n$-bulk).
2. No recombination or generation occurs inside the depletion region.
3. The electric field in the neutral bulk regions is negligible; transport there is purely diffusion-driven.

**Width of the depletion region.**
The applied forward voltage $V_a$ lowers the barrier, modifying the depletion width to:

$$W(V_a) = \sqrt{\frac{2\varepsilon_s (V_{bi} - V_a)}{q} \left( \frac{1}{N_A} + \frac{1}{N_D} \right)}$$

**Minority charge injection.** Lowering the barrier causes minority charge injection at the boundaries of the depletion region. Compared to the equilibrium condition with no external voltage,

$$\begin{aligned}
  \Delta n(x_p) & = n_{p0} \left[ \exp\left( \frac{V_a}{V_t} \right) - 1 \right] \\
  \Delta p(x_n) & = p_{n0} \left[ \exp\left( \frac{V_a}{V_t} \right) - 1 \right] \\
\end{aligned}$$

**Charge transport dynamics.** If Shockley conditions hold, no recombination in the depletion region occurs; recombination occurs in the bulk of $p$- and $n$- sections: in bulk regions, the electric field $\vec{e}$ is negligible, and thus the current is driven by diffusion only.

Governing equation of the holes in the $n$-bulk immediately follows from equation {eq}`eq:semi:num-balance`, with the assumption of no drift current in {eq}`eq:semi:charge-current-p`,

$$\begin{aligned}
  \partial_t \Delta p_n  
  & = - \nabla \cdot \left( \frac{j_{p,diff}}{q} \right) + \Delta ( G - R ) = \\
  & = - \nabla \cdot \left( - D \Delta p_n \nabla n \right) + \Delta ( G - R ) \ ,
\end{aligned}$$

or in 1-dimensional problems with constant coefficients

$$\partial_t \Delta p_n = D \partial_{xx} \Delta p_n + \Delta ( G - R )$$

Assuming *steady-state diffusion equation* (**todo** *justify this limit*) governs the diffusion of the minority charge carriers in the bulk, and using **the law of mass action** to write the source term (see box below), the governing equation becomes

$$D_p \Delta p_n'' = \frac{1}{\tau_p} \Delta p_n \ ,$$

with $\tau_p = \frac{1}{k_r n_{n0}}$.


```{dropdown} Law of mass action for $\ G - R$
:open:

In the $n$-bulk region, 
* $n_{n0} \gg p_{n0}$, 
* $\Delta n = \Delta p$ if the electrical charge remains zero
* $\Delta p_n \gg p_{n0}$
* $\Delta n_n \ll n_{n0}$

Thus the source term becomes

$$\begin{aligned}
R - G 
& = k_r p n - k_r p_0 n_0 = \\
& = k_r ( p_{n0} + \Delta p_n ) ( n_{n0} + \Delta n_n ) - k_r p_{n0} n_{n0} = \\
& = k_r ( p_{n0} \Delta n_n + n_{n0} \Delta p_n + \Delta n_n \Delta p_n ) = \\
& \simeq k_r n_{n0} \Delta p_n
\end{aligned}$$

as:
* $G \sim G_0 = R_0$ at equilibrium. **todo** *Find some time/space to justify all these sentences about equilibrium*
* the conditions at the beginning of the box give:
  * $n_{n0} \Delta p_n \gg p_{n0} \Delta n_n$ (because the deltas are equal, and $n_{n0} \gg p_{n0}$)
  * $n_{n0} \Delta p_n \gg \Delta p_n \Delta n_n$ (because the deltas are equal, and $n_{n0} \gg \Delta n_{n}$


```

The differential porblem supplied with proper boundary conditions becomes

$$\left\{ \begin{aligned}
  & \frac{\Delta p_n(x)}{\tau_p} = D_p \Delta p''_n(x) \\
  & p(x_n) = p_{n0} \left[  \exp\left( \frac{V_a}{V_t} \right) - 1 \right] \\
  & p(x \rightarrow +\infty) = 0 \\
\end{aligned} \right.$$

and its solution reads

$$\Delta p_n(x) = p_{n0} \left[ \exp \left( \frac{V_a}{V_t} \right) - 1 \right] \exp\left( - \frac{x - x_n}{L_p} \right) \ ,$$

with $L_p = \sqrt{ \tau_p D_p }$ for the holes in the $n$-bulk, $x > x_n$ 

$$\Delta n_p(x) = n_{p0} \left[ \exp \left( \frac{V_a}{V_t} \right) - 1 \right] \exp\left( \frac{x - x_p}{L_n} \right) \ ,$$

with $L_n = \sqrt{ \tau_n D_n }$ for the electrons in the $p$-bulk, $x < x_p$.[^diffusion-n-bc][^order-of-magnitudes-charges] 

[^diffusion-n-bc]: The boundary conditions of the diffusion of $n$ in the $p$-bulk are $n(x \rightarrow -\infty) = 0$, $n(x_p) = n_{p0} [ \dots ]$.

[^order-of-magnitudes-charges]: Usually $n_0 \ll \Delta n \ll N_A$.

**Current under steady conditions.**

* Depletion region $x \in [x_n, x_p]$. Under steady conditions, no charge accumulation occurs along the $p$-$n$ junction and thus the current must be constant. There's no recombination or generation inside the depletion region $x \in [x_p, x_n]$, thus the following conditions hold for holes and free electrons

   $$\begin{aligned}
     \text{const} & = A J_p(x) = A J_p(x_p) = A J_p(x_n)  \quad \forall x \in [x_p, x_n] \\
     \text{const} & = A J_n(x) = A J_n(x_p) = A J_n(x_n) \ ,
   \end{aligned}$$
   
   and thus
   
   $$\text{const} = A J(x) \quad \forall x \in [x_p, x_n] \ .$$

   Evaluating the current at the boundary of the depletion region (in the model, just ouside that, so that the electric field is zero and the current is driven only by diffusion)

   $$\begin{aligned}
     I = A J(x)
     & = A J_n(x) + A J_p(x) = \\
     & = A J_n(x_p) + A J_p(x_n) = \\
     & = - A (-q) D_n n_p'(x_p) - A q D_p p_n'(x_n) = \\
     & = A q D_n \frac{1}{L_n} n_{p0} \left[ \exp \left( \frac{V_a}{V_t} \right) - 1 \right] + A q D_p \frac{1}{L_p} p_{n0} \left[ \exp \left( \frac{V_a}{V_t} \right) - 1 \right] = \\
     & = q A \left( \frac{D_n n_{p0}}{L_n} + \frac{D_p p_{n0}}{L_p} \right) \left[ \exp \left( \frac{V_a}{V_t} \right) - 1 \right] \ .
   \end{aligned}$$

   This equation readily gives the $V(I)$ relation for an ideal $p$-$n$ junction,

    $$ I(V) = I_0 \left[ \exp \left( \frac{V}{V_t} \right) - 1  \right] \ , $$ (eq:semiconductors:pn-junction:iv)

   with $I_0 = q A \left( \dots \right) = q A n_i^2 \left( \frac{D_n}{L_n N_A} + \frac{D_p}{L_p N_D} \right)$.

* $n$-bulk, $x \in [ x_n, +\infty)$. In this region, the electric field is assumed to be negligible, and thus only diffusion drives the current of the charge carriers. For the holes,

   $$\begin{aligned}
     J_p(x) 
     & = - D_p p'_n(x) = \\
     & = \frac{D_p}{L_p} p_{n0} \exp\left( \frac{V_a}{V_t} \right) \exp \left( - \frac{x-x_n}{L_p} \right) = \\
     & = J_p(x_n) \exp \left( - \frac{x-x_n}{L_p} \right)  \ .
   \end{aligned}$$

   and thus $J_n(x) = J - J_p(x)$.

* $p$-bulk, $x \in (-\infty, x_p]$...

---

<!--
The lower barrier allows carriers to scale the potential wall. The carrier concentrations at the edges of the depletion region follow the **Law of the Junction**:

$$n(-x_p) = n_{p0} \exp\left(\frac{V_a}{V_t}\right), \quad p(x_n) = p_{n0} \exp\left(\frac{V_a}{V_t}\right)$$

In the neutral bulk, these injected minority carriers move via diffusion while continuously recombining with the abundant majority carriers. Solving the steady-state minority carrier diffusion equation, $D_p \frac{d^2\Delta p_n}{dx^2} = \frac{\Delta p_n}{\tau_p}$, reveals an exponentially decaying carrier profile away from the boundaries:

$$\Delta p_n(x) = p_{n0} \left[ \exp\left(\frac{V_a}{V_t}\right) - 1 \right] \exp\left(-\frac{x - x_n}{L_p}\right)$$

Evaluating the diffusion current density ($J_p = -q D_p \frac{d\Delta p_n}{dx}$) at the boundaries and summing both carrier contributions yields the classic **Shockley Diode Equation**:

$$I = I_0 \left[ \exp\left(\frac{V_a}{V_t}\right) - 1 \right] \quad \text{where} \quad I_0 = A_j q n_i^2 \left( \frac{D_n}{L_n N_A} + \frac{D_p}{L_p N_D} \right)$$

(semiconductors:pn-junctions:depletion-approximation:rev-bias)=
### Reverse Bias
Under reverse bias, $V_a$ is negative. The effective potential barrier increases to $V_{bi} + |V_a|$, and the depletion region widens, increasing the internal electric field. Diffusion currents drop to zero. The current is governed by the minority carriers in the bulk wandering near the depletion edge, where they are immediately caught by the strong electric field and swept across. This results in a tiny, voltage-independent current equal to $-I_0$.

-->



## Advanced Description: Quasi-Fermi Levels and Non-Equilibrium Transport

**todo** *Uncomment*

<!--

While the depletion approximation and Shockley models provide excellent analytical insights, they break down when trying to model intermediate zones, high-injection regimes, or continuous spatial profiles. Under non-equilibrium conditions ($V_a \neq 0$), the Law of Mass Action is violated ($n \cdot p \neq n_i^2$), meaning a single Fermi level $E_F$ can no longer describe the system.

To build a rigorous, continuous model, we split the equilibrium Fermi level into two independent parameters: **$E_{Fn}(x)$** (the quasi-Fermi level for electrons) and **$E_{Fp}(x)$** (the quasi-Fermi level for holes).

### Carrier Statistics under Non-Equilibrium
We express the continuous free carrier concentrations using these independent variables relative to the intrinsic energy level $E_i(x)$:

$$n(x) = n_i \exp\left(\frac{E_{Fn}(x) - E_i(x)}{k_B T}\right)$$

$$p(x) = n_i \exp\left(\frac{E_i(x) - E_{Fp}(x)}{k_B T}\right)$$

Multiplying these equations demonstrates how the splitting of the quasi-Fermi levels tracks the deviation from thermal equilibrium:

$$n(x) \cdot p(x) = n_i^2 \exp\left(\frac{E_{Fn}(x) - E_{Fp}(x)}{k_B T}\right)$$

* In **Forward Bias**, $E_{Fn} > E_{Fp}$, meaning $n \cdot p > n_i^2$, indicating a net excess of mobile carriers.
* In **Reverse Bias**, $E_{Fn} < E_{Fp}$, meaning $n \cdot p < n_i^2$, representing a net suppression of mobile carriers.

### Current Formulations via Quasi-Fermi Gradients
Substituting these non-equilibrium statistics into the classic drift-diffusion current density equations ($J_n = -q\mu_n n \frac{d\psi}{dx} + qD_n \frac{dn}{dx}$) leads to a vital physical simplification:

$$J_n(x) = \mu_n n(x) \frac{dE_{Fn}}{dx}$$

$$J_p(x) = \mu_p p(x) \frac{dE_{Fp}}{dx}$$

This formulation demonstrates that net current flows if and only if there is a spatial gradient in the quasi-Fermi levels.



In the neutral bulk regions under low-level forward injection, the majority carrier quasi-Fermi level remains nearly flat, while the minority carrier quasi-Fermi level slopes sharply, driving the diffusion current. Inside the depletion region, both levels split by an amount exactly equal to the applied electrical bias: $E_{Fn} - E_{Fp} = q V_a$.

This continuous framework forms the mathematical foundation required to solve the coupled drift-diffusion equations numerically without relying on piecewise zone assumptions.

-->

