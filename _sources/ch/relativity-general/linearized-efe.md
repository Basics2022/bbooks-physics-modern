(relativity-general:notes:einstein-equation:linearization)=
# Linearization of Einstein's equation

In this section, linearization of Einstein field equation {eq}`eq:einstein:equation`

$$R^{\mu \sigma} - \frac{1}{2} g^{\mu \sigma} R = \kappa T^{\mu \sigma} \ ,$$

is performed in the limit of weak gravitational field, inducing a metric that only slightly deviates from Minkowski metric $\eta_{\mu \nu} = \text{diag}\{ 1, -1, -1, -1\}$,

$$g_{\mu \nu} = \eta_{\mu \nu} + h_{\mu \nu} \ .$$

Using *harmonic gauge condition*, the linearized Einstein field equation reduces to a wave equation for $\overline{h}^{\mu \sigma} := h^{\mu \sigma} - \frac{1}{2} \eta^{\mu \sigma} h$,

$$\square \overline{h}^{\mu \sigma} = - 2 \kappa T^{\mu \sigma} \ .$$ (eq:efe-linearization:linearized-efe)

First the inverse of the metric and Christoffel symbols are linearized, and then they're used to find the linearized expression of Riemann tensor, Ricci tensor, and scalar curvature, to find the expression of the linearized Einstein equation.

```{dropdown} Linearized Christoffel symbols
:open:

Christoffel symbols can be written in terms of the metric tensor and its derivatives with {eq}`eqn:differential-geometry:gamma:g`

$$\Gamma_{ac}^{b} = \frac{1}{2} g^{bd} \left( \partial_c g_{ad} + \partial_a g_{dc} - \partial_{d} g_{ac} \right) \ .$$ 

The derivatives are first-order contributions, thus linearization only involves zero-order term of $g^{bd}$. Thus linearized Christoffel symbols are

$$\Gamma_{ac}^{b} \sim \frac{1}{2} \eta^{bd} \left( \partial_c h_{ad} + \partial_a h_{dc} - \partial_{d} h_{ac} \right) \ .$$

```

```{dropdown} Linearized inverse metric
:open:

Linearization of the inverse metric

$$\delta_{\mu}^{\xi} = g_{\mu \nu} g^{\nu \xi} = ( \eta_{\mu \nu} + h_{\mu \nu} ) ( \eta^{\nu \xi} + h^{\nu \xi} ) = \delta_{\mu}^{\xi} + h_{\mu \nu} \eta^{\nu \xi} + \eta_{\mu \nu} h^{\nu \xi} + h_{\mu \nu} h^{\nu \xi} \ , $$

implies $0 = h_{\mu \nu} \eta^{\nu \xi} + \eta_{\mu \nu} h^{\nu \xi}$, so that the linear correction to the Minkowski metric is

$$h^{\mu \nu} = - h_{\xi \chi} \eta^{\mu \xi} \eta^{\nu \chi} \ ,$$

and the linearized inverse metric is

$$g^{\mu \nu} = \eta^{\mu \nu} + h^{\mu \nu} = \eta^{\mu \nu} - \eta^{\mu \xi} \eta^{\nu \chi} h_{\xi \chi} \ .$$

```

```{dropdown} Linearization of Riemann tensor
:open:

Riemann tensor,

$$\begin{aligned}
  R^{\xi}_{\ \ \sigma \chi \nu}
  & = \partial_{\chi} \Gamma_{\sigma \nu}^{\xi} - \partial_{\nu} \Gamma_{\chi \sigma}^{\xi} + \Gamma_{\sigma \nu}^{\mu} \Gamma_{\mu \chi}^{\xi} - \Gamma_{\chi \sigma}^{\mu} \Gamma_{\mu \nu}^{\xi} = \\
  & \sim \partial_{\chi} \Gamma_{\sigma \nu}^{\xi} - \partial_{\nu} \Gamma_{\chi \sigma}^{\xi} = \\
  & = \frac{1}{2} \partial_{\chi} \left\{ \eta^{\xi \phi} \left( \partial_\nu h_{\sigma \phi} + \partial_\sigma h_{\phi \nu} - \partial_{\phi} h_{\sigma \nu} \right) \right\}
    - \frac{1}{2} \partial_{\nu } \left\{ \eta^{\xi \phi} \left( \partial_\chi h_{\sigma \phi} + \partial_\sigma h_{\phi \chi} - \partial_{\phi} h_{\sigma \chi} \right) \right\} = \\
  & = \frac{1}{2} \eta^{\xi \phi} \left( \partial_{\chi \sigma} h_{\phi \nu} - \partial_{\chi \phi} h_{\sigma \nu} - \partial_{\nu \sigma} h_{\phi \chi} + \partial_{\nu \phi} h_{\sigma \chi} \right) \ .
\end{aligned}$$

```

```{dropdown} Linearization of Ricci tensor
:open:

Ricci tensor, $R_{\sigma \nu} = R^{\mu}_{\ \ \sigma \mu \nu}$

$$\begin{aligned}
  R_{\sigma \nu} = R^{\xi}_{\ \ \sigma \xi \nu}
  & \sim \frac{1}{2} \eta^{\xi \phi} \left( \partial_{\xi \sigma} h_{\phi \nu} - \partial_{\xi \phi} h_{\sigma \nu} - \partial_{\nu \sigma} h_{\phi \xi} + \partial_{\nu \phi} h_{\sigma \xi} \right) = R_{\sigma \nu}^{(1)} \ ,
\end{aligned}$$

and the contravariant components read

$$R^{\mu \nu (1)} = \eta^{\mu \chi} \eta^{\nu \xi} R_{\chi \xi}^{(1)} \ .$$ (eq:linearize-efe:ricci)

or, explicitly

$$\begin{aligned}
  R^{\mu \chi (1)}
  & = \eta^{\mu \sigma} \eta^{\chi \nu} R_{\sigma \nu}^{(1)} = \\
  & = \eta^{\mu \sigma} \eta^{\chi \nu} \left\{ \frac{1}{2} \eta^{\xi \phi} \left( \partial_{\xi \sigma} h_{\phi \nu} - \partial_{\xi \phi} h_{\sigma \nu} - \partial_{\nu \sigma} h_{\phi \xi} + \partial_{\nu \phi} h_{\sigma \xi} \right) \right\} = \\
  & = \frac{1}{2} \left\{ \partial^{\mu} \partial_{\xi} h^{\xi \chi} - \square h^{\mu \chi} - \partial^{\mu \chi} h + \partial^{\chi} \partial_{\phi} h^{\phi \mu} \right\} \ .
\end{aligned}$$

<!--
  & = \frac{1}{2} \left\{ \eta^{\chi \nu} \partial^{\mu \phi} h_{\phi \nu} - \eta^{\mu \sigma} \eta^{\chi \nu} \square h_{\sigma \nu} - \eta^{\xi \phi} \partial^{\mu \chi} h_{\phi \xi} + \eta^{\mu \sigma} \partial^{\chi \xi} h_{\sigma \xi} \right\}
-->


```

```{dropdown} Linearization of the term $\ -\frac{1}{2} g^{\mu \sigma} R$
:open:

$$\begin{aligned}
  R 
  & := g^{\sigma \nu} R_{\sigma \nu} = \\
  & \sim \frac{1}{2} \eta^{\sigma \nu} \eta^{\xi \phi} \left( \partial_{\xi \sigma} h_{\phi \nu} - \partial_{\xi \phi} h_{\sigma \nu} - \partial_{\nu \sigma} h_{\phi \xi} + \partial_{\nu \phi} h_{\sigma \xi} \right) = \\
  & = \partial^{\nu \phi} h_{\nu \phi} - \square h = R^{(1)} \ ,
\end{aligned}$$

with 

$$\begin{aligned}
 \eta^{\sigma \nu} \partial_{\sigma} & = \partial^{\nu} \\
 \eta^{\xi \phi} \partial_{\xi \phi} & = \square \\
 \eta^{\sigma \nu} h_{\sigma \nu} & =: h
\end{aligned}$$

Linearization of the term $-\frac{1}{2} g^{\mu \sigma} R$ only involves the constant contribution of the metric, i.e.

$$- \frac{1}{2} g^{\mu \sigma} R \sim - \frac{1}{2} \eta^{\mu \sigma} R^{(1)}$$ (eq:linearize-efe:gR)

```

```{dropdown} Linearized Einstein field equation
:open:

Putting together {eq}`eq:linearize-efe:ricci` and {eq}`eq:linearize-efe:gR`, the linearized Einstein equation becomes

$$\begin{aligned}
 \kappa T^{\mu \sigma}
 & = R^{\mu \sigma} - \frac{1}{2} g^{\mu \sigma} R = \\
 & \sim R^{\mu \sigma (1)} - \frac{1}{2} \eta^{\mu \sigma} R^{(1)} = \\
 & = \frac{1}{2} \left\{ \partial^{\mu} \partial_{\xi} h^{\xi \sigma} - \square h^{\mu \sigma} - \partial^{\mu \sigma} h + \partial^{\sigma} \partial_{\phi} h^{\phi \mu} \right\} - \frac{1}{2} \eta^{\mu \sigma} \left\{ \partial^{\nu \phi} h_{\nu \phi} - \square h \right\} = \\
 & = \frac{1}{2} \left\{ \partial^{\mu} \partial_{\xi} h^{\xi \sigma} - \square h^{\mu \sigma} - \partial^{\mu \sigma} h + \partial^{\sigma} \partial_{\phi} h^{\phi \mu} - \eta^{\mu \sigma} \partial^{\nu \phi} h_{\nu \phi} + \eta^{\mu \sigma} \square h \right\} = \\
\end{aligned}$$

Now, defining

$$\overline{h}_{\mu \nu} := h_{\mu \nu} - \frac{1}{2} \eta_{\mu \nu} h \ ,$$

$$\overline{h} = \eta^{\mu \nu} \overline{h}_{\mu \nu} = \eta^{\mu \nu} \left( h_{\mu \nu} - \frac{1}{2} \eta_{\mu \nu} h \right) = h - 2 h = - h \ ,$$ 

so that

$$h_{\mu \nu} = \overline{h}_{\mu \nu} + \frac{1}{2} \eta_{\mu \nu} h = \overline{h}_{\mu \nu} - \frac{1}{2} \eta_{\mu \nu} \overline{h} $$

Thus, exploiting the the expression {eq}`eq:efe-linearization:non-laplacian` in the box, the equation becomes

$$\begin{aligned}
  \kappa T^{\mu \sigma}
  & = \frac{1}{2} \square \left( - h^{\mu \sigma} + \frac{1}{2} \eta^{\mu \sigma} h + \frac{1}{2} \eta^{\mu \sigma} h \right) + \frac{1}{2} \left\{ \partial^{\mu} \partial_{\xi} h^{\xi \sigma} - \partial^{\mu \sigma} h + \partial^{\sigma} \partial_{\phi} h^{\phi \mu} - \eta^{\mu \sigma} \partial^{\nu \phi} h_{\nu \phi} \right\} = \\
  & = \frac{1}{2} \square \left( - h^{\mu \sigma} + \frac{1}{2} \eta^{\mu \sigma} h + \frac{1}{2} \eta^{\mu \sigma} h \right) + \frac{1}{2} \left\{  \partial^{\mu} \partial_{\xi} \overline{h}^{\xi \sigma} + \partial^{\sigma} \partial_{\xi} \overline{h}^{\xi \mu} - \eta^{\mu \sigma} \partial_{\nu \xi} \overline{h}^{\nu \xi} + \frac{1}{2} \eta^{\mu \sigma} \square \overline{h} \right\}  \\
  & = - \frac{1}{2} \square \overline{h}^{\mu \sigma} + \frac{1}{2} \left\{  \partial^{\mu} \partial_{\xi} \overline{h}^{\xi \sigma} + \partial^{\sigma} \partial_{\xi} \overline{h}^{\xi \mu} - \eta^{\mu \sigma} \partial_{\nu \xi} \overline{h}^{\nu \xi}  \right\} \ .
\end{aligned}$$

Prescribing harmonic gauge condition (de Donder), $\partial_{\xi} \overline{h}^{\xi \mu} = 0$, linearized Einstein equation becomes a wave equation for $\overline{h}^{\mu \sigma}$,

$$\square \overline{h}^{\mu \sigma} = - 2 \kappa T^{\mu \sigma} \ .$$

```

```{dropdown} $\partial^{\mu} \partial_{\xi} h^{\xi \sigma} - \partial^{\mu \sigma} h + \partial^{\sigma} \partial_{\phi} h^{\phi \mu} - \eta^{\mu \sigma} \partial^{\nu \phi} h_{\nu \phi}$

$$\begin{aligned}
  & \partial^{\mu} \partial_{\xi} h^{\xi \sigma} - \partial^{\mu \sigma} h + \partial^{\sigma} \partial_{\xi} h^{\xi \mu} - \eta^{\mu \sigma} \partial^{\nu \xi} h_{\nu \xi} = \\
  & = \partial^{\mu} \partial_{\xi} \overline{h}^{\xi \sigma} - \underbrace{ \frac{1}{2} \eta^{\xi \sigma} \partial^{\mu} \partial_{\xi} \overline{h}}_{} + \underbrace{ \partial^{\mu \sigma} \overline{h} }_{} + \partial^{\sigma} \partial_{\xi} \overline{h}^{\xi \mu} - \underbrace{ \frac{1}{2} \eta^{\xi \mu} \partial^{\sigma} \partial_{\xi} \overline{h} }_{} - \eta^{\mu \sigma} \partial_{\nu \xi} \overline{h}^{\nu \xi} + \underbrace{ \frac{1}{2} \eta^{\mu \sigma} \eta^{\nu \xi} \partial_{\nu \xi} \overline{h} }_{ \frac{1}{2} \eta^{\mu \sigma} \square \overline{h} } =  \\
  & = \partial^{\mu} \partial_{\xi} \overline{h}^{\xi \sigma} + \partial^{\sigma} \partial_{\xi} \overline{h}^{\xi \mu} - \eta^{\mu \sigma} \partial_{\nu \xi} \overline{h}^{\nu \xi} + \frac{1}{2} \eta^{\mu \sigma} \square \overline{h} \ .
\end{aligned}$$ (eq:efe-linearization:non-laplacian)

```


