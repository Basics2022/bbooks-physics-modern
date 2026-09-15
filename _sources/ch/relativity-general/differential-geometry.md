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

$$\left\{ \mathbf{v} \cdot \mathbf{R} \right\}_{\sigma \eta \nu} = v_{\xi} R^{\xi}_{\ \ \sigma \eta \nu} = \left( \nabla_{\sigma} \nabla_{\eta} - \nabla_{\eta} \nabla_{\sigma} \right) v_{\nu}$$

```{dropdown} First term
:open:

$$\begin{aligned}
  \nabla \nabla \mathbf{v} 
  & = \mathbf{b}^{\sigma} \partial_{\sigma} \left[ \mathbf{b}^{\eta} \partial_{\eta} \left( v_{\nu} \mathbf{b}^{\nu} \right) \right] = \\
  & = \mathbf{b}^{\sigma} \partial_{\sigma} \left[ \mathbf{b}^{\eta} \mathbf{b}^{\nu} \left( \partial_{\eta} v_{\nu} - \Gamma_{\eta \nu}^{\xi} v_{\xi}  \right) \right] = \\
  & = \mathbf{b}^{\sigma} \mathbf{b}^{\eta} \mathbf{b}^{\nu} \left[ - \Gamma_{\sigma \eta}^{\mu} (\dots)_{\mu \nu} - \Gamma_{\sigma \nu}^{\mu} (\dots)_{\eta \mu} + \partial_{\sigma \eta} v_{\nu} - \partial_{\sigma} \left( \Gamma_{\eta \nu}^{\xi} v_{\xi} \right) \right] = \\
  & = \mathbf{b}^{\sigma} \mathbf{b}^{\eta} \mathbf{b}^{\nu} \left[
    - \Gamma_{\sigma \eta}^{\mu} \left( \partial_{\mu} v_{\nu} - \Gamma_{\mu \nu}^{\xi} v_{\xi} \right)
    - \Gamma_{\sigma \nu }^{\mu} \left( \partial_{\eta} v_{\mu} - \Gamma_{\mu \eta}^{\xi} v_{\xi} \right)
    + \partial_{\sigma \eta} v_{\nu} - \partial_{\sigma} \Gamma_{\eta \nu}^{\xi} v_{\xi} - \Gamma_{\eta \nu}^{\xi} \partial_{\sigma} v_{\xi} \right] = \\
  & =  \mathbf{b}^{\sigma} \mathbf{b}^{\eta} \mathbf{b}^{\nu} \nabla_{\sigma \eta} v_{\nu} \ .
\end{aligned}$$


```

```{dropdown} $\ \nabla_{\sigma \eta} v_{\nu} - \nabla_{\eta \sigma} v_{\nu} \ $
:open:

Exploiting symmetry properties of Christoffel symbols,

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

$$R^{\xi}_{\ \ \sigma \eta \nu} = \partial_{\eta} \Gamma_{\sigma \nu}^{\xi} - \partial_{\sigma} \Gamma_{\eta \nu}^{\xi} + \Gamma_{\sigma \nu}^{\mu} \Gamma_{\mu \eta}^{\xi} - \Gamma_{\eta \nu}^{\mu} \Gamma_{\mu \sigma}^{\xi}$$

(relativity-general:notes:differential-geometry:curvature-tensor:ricci)=
### Ricci's tensor

**todo** Meaning

Ricci's tensor is defined as the contraction of the first and third indices of the curvature tensor with the metric tensor,

$$R_{\nu \sigma} := g^{\alpha \beta} R_{\alpha \sigma \beta \nu} = \underbrace{g^{\alpha \beta} g_{\alpha \gamma}}_{\delta_{\gamma}^{\beta}} R^{\gamma}_{\ \ \sigma \beta \nu} = R^{\mu}_{\ \ \sigma \mu \nu}$$


(relativity-general:notes:differential-geometry:curvature-tensor:curvature-scalar)=
### Curvature scalar

**todo** Meaning

$$R := g^{\nu \sigma} R_{\nu \sigma} \ .$$

