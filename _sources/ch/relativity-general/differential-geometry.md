(relativity-general:notes:differential-geometry)=
# Differential Geometry

```{dropdown} References
:open:

* Math basics: **todo** check and complete the chapters about [**tensor calculus**](https://basics2022.github.io/bbooks-math-miscellanea/ch/tensor-algebra-calculus/calculus-euclidean.html) and [**differential geometry**](https://basics2022.github.io/bbooks-math-miscellanea/ch/differential-geometry/intro.html)

```

<!--
(relativity-general:notes:differential-geometry:intro)=
### Basics
-->


```{dropdown} Basics
:open:

Let $\mathbf{X}(q^k)$ a parametrization of points in a $n$-dimensional space, $k = 1:n$.

**Natural basis**, $\mathbf{b}_k := \frac{\partial \mathbf{X}}{\partial q^k}$. Vectors of the natural basis can be used to write vectors and tensor fields as a linear combination of them, or in their components w.r.t. that basis

$$\mathbf{v} = v^k \mathbf{b}_k \quad , \quad \mathbf{A} = A^{kl} \mathbf{b}_k \otimes \mathbf{b}_l \ .$$

**Metric tensor**, The covariant compoenents are $\mathbf{b}_k \cdot \mathbf{b}_l =: g_{kl}$. Some properties: $g_{k}^{\ l} = \delta_{k}^{l}$, $g_{ab} g^{bc} = \delta_{a}^{c}$.

**Contravariant basis**, $\{ \mathbf{b}^k \}$, s.t. $\mathbf{b}_k \cdot \mathbf{b}^l = \delta_k^l$. It's easy to prove that $\mathbf{b}_k = g_{kl} \mathbf{b}^l$ (just scalar product with $\mathbf{b}^j$...), and the law for raising or lower indices holds, $A^{ij} = g^{ik} A_{k}^{\ j}$,...

**Derivatives of the basis vectors.** The components of the derivative $\frac{\partial \mathbf{b}_i}{\partial q^k} = \Gamma_{ik}^l\mathbf{b}_l$ are defined as the Christoffel symbols of the second type. As these are second-order derivatives, for Schwartz theorem about mixed partial derivatives, the symmetry $\Gamma_{ij}^k = \Gamma_{ji}^k$ immediately follows. The derivative of the vectors of the contravariant basis follows from

$$\begin{aligned}
  0
  & = \partial_{k} \left( \mathbf{b}_l \cdot \mathbf{b}^m \right) = \\
  & = \partial_{k} \mathbf{b}_l \cdot \mathbf{b}^m + \mathbf{b}_l \cdot \partial_k \mathbf{b}^m = \\
  & = \Gamma_{kl}^{n} \underbrace{ \mathbf{b}_n \cdot \mathbf{b}^m}_{ = \delta_{n}^m} + \mathbf{b}_l \cdot \partial_k \mathbf{b}^m \ ,
\end{aligned}$$

and thus $\partial_k \mathbf{b}^m = - \Gamma_{kl}^{m} \mathbf{b}^l$.

**Derivatives of the metric tensor.** Using the definition of the covariant components of the metric tensor and the derivatives of the vectors of the natural basis, it's easy to prove

$$\dfrac{\partial q^c}{g_{ab}} = \Gamma_{d}^{ac} g_{db} + \Gamma_{bc}^{d} g_{ad}$$

Using the property $g_{ab} g^{bc} = \delta_{a^c}$, from its derivatives $\partial_d$,

$$\partial_d g_{ab} g^{bc} + g_{ab} \partial_d g^{bc} = 0 \ ,$$

it follows that $\partial_d g^{ec} = - g^{ea} \partial_d g_{ab} g^{bc}$.

```

(relativity-general:notes:differential-geometry:gradient)=
## Gradient, covariant derivative and directional derivative

Gradient of a scalar field

$$\nabla f = \mathbf{b}^k \partial_k f \ .$$

Gradient of a vector field

$$\nabla \mathbf{v} = \mathbf{b}^k \mathbf{b}_i \left( \partial_k v^i + \Gamma_{kl}^{i} v^l  \right) \ .$$

```{dropdown} Proof

$$\begin{aligned}
  \nabla \mathbf{v}
  & = \mathbf{b}^k \dfrac{\partial}{\partial q^k} \left( v^i \mathbf{b}_i \right) = \\
  & = \mathbf{b}^k \mathbf{b}_i \partial_k v^i + \mathbf{b}^k \mathbf{b}_l \Gamma_{ik}^{l} v^i = \\
  & = \mathbf{b}^k \mathbf{b}_i \left( \partial_k v^i + \Gamma_{kl}^{i} v^l \right) \ .
\end{aligned}$$

```

Gradient of a 2-nd order tensor field

$$\nabla \mathbf{A} = \mathbf{b}^k \mathbf{b}_i \mathbf{b}_j \left( \partial_k A^{ij} + \Gamma_{kl}^{i} A^{lj} + \Gamma_{kl}^{j} A^{il}  \right) \ = \mathbf{b}^k \mathbf{b}_i \mathbf{b}_j \nabla_k A^{ij}.$$

```{dropdown} Proof

...

```

(relativity-general:notes:differential-geometry:curvature-tensor)=
## Curvature Tensor

```{dropdown} todo. Meaning of this definition

...

```

Definition through the action on an arbitrary vector field, whose components are

$$\left\{ \mathbf{v} \cdot \mathbf{R} \right\}_{\sigma \eta \nu} = v_{\xi} R^{\xi}_{\ \ \sigma \eta \nu} = \left( \nabla_{\eta} \nabla_{\nu} - \nabla_{\nu} \nabla_{\eta} \right) v_{\sigma}$$

```{dropdown} First term
:open:

$$\begin{aligned}
  \nabla \nabla \mathbf{v} 
  & = \mathbf{b}^{\eta} \partial_{\eta} \left[ \mathbf{b}^{\nu} \partial_{\nu} \left( v_{\sigma} \mathbf{b}^{\sigma} \right) \right] = \\
  & = \mathbf{b}^{\eta} \partial_{\eta} \left[ \mathbf{b}^{\nu} \mathbf{b}^{\sigma} \left( \partial_{\nu} v_{\sigma} - \Gamma_{\nu \sigma}^{\xi} v_{\xi}  \right) \right] = \\
  & = \mathbf{b}^{\eta} \mathbf{b}^{\nu} \mathbf{b}^{\sigma} \left[ - \Gamma_{\eta \nu}^{\mu} (\dots)_{\mu \sigma} - \Gamma_{\eta \sigma}^{\mu} (\dots)_{\nu \mu} + \partial_{\eta \nu} v_{\sigma} - \partial_{\eta} \left( \Gamma_{\nu \sigma}^{\xi} v_{\xi} \right) \right] = \\
  & = \mathbf{b}^{\eta} \mathbf{b}^{\nu} \mathbf{b}^{\sigma} \left[
    - \Gamma_{\eta  \nu}^{\mu} \left( \partial_{\mu} v_{\sigma} - \Gamma_{\mu \sigma}^{\xi} v_{\xi} \right)
    - \Gamma_{\eta \sigma}^{\mu} \left( \partial_{\nu} v_{\mu} - \Gamma_{\mu \nu}^{\xi} v_{\xi} \right)
    + \partial_{\eta \nu} v_{\sigma} - \partial_{\eta} \Gamma_{\nu \sigma}^{\xi} v_{\xi} - \Gamma_{\nu \sigma}^{\xi} \partial_{\eta} v_{\xi} \right] = \\
  & =  \mathbf{b}^{\eta} \mathbf{b}^{\nu} \mathbf{b}^{\sigma} \nabla_{\eta \nu} v_{\sigma} \ .
\end{aligned}$$


```

```{dropdown} $\ \nabla_{\sigma \eta} v_{\nu} - \nabla_{\eta \sigma} v_{\nu} \ $
:open:

Exploiting symmetry properties of Christoffel symbols,

**todo!!!** **change indices to match the definition of the curvature tensor**

$$\begin{aligned}
  \nabla_{\sigma \eta} v_{\nu} - \nabla_{\eta \sigma} v_{\nu}
  & = 
    - \underbrace{\Gamma_{\sigma \eta}^{\xi} \partial_{\xi} v_{\nu}}_{1} + \underbrace{\Gamma_{\sigma \eta}^{\mu} \Gamma_{\mu \nu}^{\xi} v_{\xi}}_{2}
    - \underbrace{\Gamma_{\sigma \nu }^{\xi} \partial_{\eta} v_{\xi}}_{3} + \Gamma_{\sigma \nu }^{\mu} \Gamma_{\mu \eta}^{\xi} v_{\xi}
    + \underbrace{\partial_{\sigma \eta} v_{\nu}}_{4} - \partial_{\sigma} \Gamma_{\eta \nu}^{\xi} v_{\xi} - \underbrace{\Gamma_{\eta \nu}^{\xi} \partial_{\sigma} v_{\xi}}_{5} + \\
  & - \left[ 
    - \underbrace{\Gamma_{\eta \sigma}^{\xi} \partial_{\xi} v_{\nu}}_{1} + \underbrace{\Gamma_{\eta \sigma}^{\mu} \Gamma_{\mu \nu}^{\xi} v_{\xi}}_{2}
    - \underbrace{\Gamma_{\eta   \nu }^{\xi} \partial_{\sigma} v_{\xi}}_{5} + \Gamma_{\eta \nu }^{\mu} \Gamma_{\mu \sigma}^{\xi} v_{\xi} 
    + \underbrace{\partial_{\eta \sigma} v_{\nu}}_{4} - \partial_{\eta} \Gamma_{\sigma \nu}^{\xi} v_{\xi} - \underbrace{\Gamma_{\sigma \nu}^{\xi} \partial_{\eta} v_{\xi} }_{3}
  \right] = \\
  & = \left[ \partial_{\eta} \Gamma_{\sigma \nu}^{\xi} - \partial_{\sigma} \Gamma_{\eta \nu}^{\xi} + \Gamma_{\sigma \nu}^{\mu} \Gamma_{\mu \eta}^{\xi} - \Gamma_{\eta \nu}^{\mu} \Gamma_{\mu \sigma}^{\xi} \right] v_{\xi} \ . 
\end{aligned}$$

```

Thus, it follows that

$$R^{\xi}_{\ \ \sigma \eta \nu} = \partial_{\eta} \Gamma_{\sigma \nu}^{\xi} - \partial_{\nu} \Gamma_{\eta \sigma}^{\xi} + \Gamma_{\sigma \nu}^{\mu} \Gamma_{\mu \eta}^{\xi} - \Gamma_{\eta \sigma}^{\mu} \Gamma_{\mu \nu}^{\xi}$$

$$R_{\phi \sigma \eta \nu} = g_{\phi \xi} R^{\xi}_{\ \ \sigma \eta \nu} = g_{\phi \xi} \left( \partial_{\eta} \Gamma_{\sigma \nu}^{\xi} - \partial_{\nu} \Gamma_{\eta \sigma}^{\xi} + \Gamma_{\sigma \nu}^{\mu} \Gamma_{\mu \eta}^{\xi} - \Gamma_{\eta \sigma}^{\mu} \Gamma_{\mu \nu}^{\xi}\right)$$

(relativity-general:notes:differential-geometry:curvature-tensor:ricci)=
### Ricci's tensor

**todo** Meaning

Ricci's tensor is defined as the contraction of the first and third indices of the curvature tensor with the metric tensor,

$$R_{\sigma \nu} := g^{\alpha \beta} R_{\alpha \sigma \beta \nu} = \underbrace{g^{\alpha \beta} g_{\alpha \gamma}}_{\delta_{\gamma}^{\beta}} R^{\gamma}_{\ \ \sigma \beta \nu} = R^{\mu}_{\ \ \sigma \mu \nu}$$

$$R_{\sigma \nu} = \partial_{\xi} \Gamma^{\xi}_{\sigma \nu} - \partial_{\nu} \Gamma^{\xi}_{\xi \sigma} + \Gamma_{\sigma \nu}^{\mu} \Gamma_{\mu \xi}^{\xi} - \Gamma_{\xi \nu}^{\mu} \Gamma^{\xi}_{\mu \sigma}$$


(relativity-general:notes:differential-geometry:curvature-tensor:curvature-scalar)=
### Curvature scalar

**todo** Meaning

$$R := g^{\sigma \nu} R_{\sigma \nu} = R^{\sigma}_{\ \ \sigma} \ .$$

$$R = g^{\sigma \nu} R_{\sigma \nu} = g^{\sigma \nu} \left( \partial_{\xi} \Gamma^{\xi}_{\sigma \nu} - \partial_{\nu} \Gamma^{\xi}_{\xi \sigma} + \Gamma_{\sigma \nu}^{\mu} \Gamma_{\mu \xi}^{\xi} - \Gamma_{\xi \nu}^{\mu} \Gamma^{\xi}_{\mu \sigma} \right)$$


(relativity-general:notes:differential-geometry:curvature-tensor:properties)=
### Properties

* $R_{abcd} = - R_{abdc}$

```{dropdown} Proof
:open:

By direct inspection of the expression of the components of the curvature tensor,

$$R_{\phi \sigma \eta \nu} = g_{\phi \xi} R^{\xi}_{\ \ \sigma \eta \nu} = g_{\phi \xi} \left( \partial_{\eta} \Gamma_{\sigma \nu}^{\xi} - \partial_{\nu} \Gamma_{\eta \sigma}^{\xi} + \Gamma_{\sigma \nu}^{\mu} \Gamma_{\mu \eta}^{\xi} - \Gamma_{\eta \sigma}^{\mu} \Gamma_{\mu \nu}^{\xi}\right)$$

and the symmetry of the Christoffel symbols, $\Gamma_{ab}^c = \Gamma_{ba}^c$.

```

* $R_{abcd} = - R_{bacd}$
* $R_{abcd} + R_{acdb} + R_{adbc} = 0$
* $R_{abcd} = R_{cdab}$
* $R_{abcd;e} + R_{abde;c} + R_{abec;d} = 0$ (Second Bianchi identity)

```{dropdown} Proof
:open:

$$\begin{aligned}
  R_{\phi \sigma \eta \nu; \chi} 
  & = \left( g_{\phi \xi} R^{\xi}_{\ \ \sigma \eta \nu} \right)_{;\chi} = \\
  & = g_{\phi \xi} \left( \partial_{\eta} \Gamma_{\sigma \nu}^{\xi} - \partial_{\nu} \Gamma_{\eta \sigma}^{\xi} + \Gamma_{\sigma \nu}^{\mu} \Gamma_{\mu \eta}^{\xi} - \Gamma_{\eta \sigma}^{\mu} \Gamma_{\mu \nu}^{\xi}\right)_{; \chi} = \\
  & = 
\end{aligned}$$

**todo**


```

(relativity-general:notes:differential-geometry:curvature-tensor:properties:ricci-divergence)=
#### Divergence of Ricci's tensor

$$
  \nabla_{\mu} R^{\mu}_{\ \ \nu} = \frac{1}{2} \nabla_{\nu} R \ .
$$

```{dropdown} Proof
:open:

$$\begin{aligned}
  R_{\sigma \nu}
  = R^{\xi}_{\ \ \sigma \xi \nu} 
  = \partial_{\xi} \Gamma_{\sigma \nu}^{\xi} - \partial_{\sigma} \Gamma_{\xi \nu}^{\xi} + \Gamma_{\sigma \nu}^{\mu} \Gamma_{\mu \xi}^{\xi} - \Gamma_{\xi \nu}^{\mu} \Gamma_{\mu \sigma}^{\xi} 
\end{aligned}$$

$$R^{\mu}_{\ \ \nu} = g^{\mu \sigma} R_{\sigma \nu}$$

$$\begin{aligned}
  \nabla_{\mu} R^{\mu}_{\ \ \nu}
  & = \partial_\mu R^{\mu}_{\ \ \nu} + \Gamma_{\mu \sigma}^{\mu} R^{\sigma}_{\ \ \nu} - \Gamma_{\sigma \nu}^{\mu} R^{\sigma}_{\ \ \mu} = \\
  & = \\ 
\end{aligned}$$

```



