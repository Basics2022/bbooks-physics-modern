(general-relativity:local-inertial-reference-frame)=
# Local inertial reference frame and equivalence principle

**Goal.** Starting from *generic* coordinates $q^\mu$ on spacetime, build coordinates $x^\alpha$ around an event $P$ in which the metric is Minkowskian up to second-order terms. Then show:

1. what is arbitrary in this construction (and what is not),
2. that "$\Gamma'(P)=0$" and "$\partial g'(P)=0$" are the same condition,
3. that the first deviation from flatness is the Riemann tensor, which no coordinate choice can remove.

This is the mathematical content of the **equivalence principle**.

```{admonition} Notation, and signature

**Conventions.** Signature $\eta_{\alpha\beta}=\mathrm{diag}(+1,-1,-1,-1)$, so $c^2\,d\tau^2=d\mathbf X\cdot d\mathbf X$. Nothing below depends on the signature. Riemann tensor:

$$R^\gamma{}_{\alpha\beta\delta}=\partial_\beta\Gamma^\gamma{}_{\delta\alpha}-\partial_\delta\Gamma^\gamma{}_{\beta\alpha}+\Gamma^\gamma{}_{\beta\lambda}\Gamma^\lambda{}_{\delta\alpha}-\Gamma^\gamma{}_{\delta\lambda}\Gamma^\lambda{}_{\beta\alpha}\ .$$

```


(general-relativity:local-inertial-reference-frame:introduction)=
## Setting and notation

Events in space time are parametrized with a set of coordinates $\{ q^\mu \}_{\mu=0:3}$ as $\mathbf X(q^\mu)$. The event $P$ has coordinates $q_P^\mu$. The choice of the coordinates $\{ q^\mu \}$ induces

- Coordinate natural basis $\mathbf{b}_\mu=\partial_\mu\mathbf{X}$ and metrics $g_{\mu\nu}=\mathbf{ b}_\mu \cdot \mathbf{ b}_\nu$, and the reciprocal basis $\mathbf{ b}^\mu\cdot\mathbf {b}_\nu=\delta^\mu_\nu$.

- Connection - Christoffel symbols, $\Gamma_{\mu \nu}^{\lambda}$, defined as the components in the natural basis of the derivative of the vectors of the natural basis themselves, i.e. 

   $$\frac{\partial^2\mathbf{X}}{\partial q^{\mu} q^{\nu}} = \partial_{q^{\nu}} \mathbf{b}_{\mu} = \partial_{q^{\mu}} \mathbf{b}_{\nu} = \Gamma_{\mu \nu}^{\lambda} \mathbf{b}_{\lambda} \ .$$

   Exploiting the orthogonality of the vectors of a basis and the vectors of its reciprocal basis,

   $$
   \Gamma^\lambda_{\mu\nu}=\mathbf b^\lambda\cdot\partial_\mu\mathbf b_\nu,\qquad
   \Gamma_{\lambda,\mu\nu}:=g_{\lambda\sigma}\Gamma^\sigma{}_{\mu\nu}=\mathbf b_\lambda\cdot\partial_\mu\mathbf b_\nu .
   $$

   It is symmetric in $\mu\nu$ because $\partial_\mu\mathbf b_\nu=\partial_\nu\mathbf b_\mu$.

<!--
**Metric compatibility.** Differentiating $g_{\mu\nu}=\mathbf b_\mu\cdot\mathbf b_\nu$:

$$
\partial_\rho g_{\mu\nu}=\partial_\rho\mathbf b_\mu\cdot\mathbf b_\nu+\mathbf b_\mu\cdot\partial_\rho\mathbf b_\nu
=\Gamma_{\nu,\rho\mu}+\Gamma_{\mu,\rho\nu}.
$$ (eq-compat)

**Change of coordinates** $q^\mu=q^\mu(x)$. With $\mathbf b'_\alpha=\partial_\alpha q^\mu\,\mathbf b_\mu$:

$$
g'_{\alpha\beta}=\partial_\alpha q^\mu\,\partial_\beta q^\nu\,g_{\mu\nu},
$$ (eq-g-transf)

$$
\Gamma'^\gamma{}_{\alpha\beta}=\frac{\partial x^\gamma}{\partial q^\lambda}\Big[\partial_\alpha q^\mu\,\partial_\beta q^\nu\,\Gamma^\lambda{}_{\mu\nu}+\partial_\alpha\partial_\beta q^\lambda\Big].
$$ (eq-gamma-transf)

The second line follows from $\Gamma'^\gamma{}_{\alpha\beta}=\mathbf b'^\gamma\cdot\partial_\alpha\mathbf b'_\beta$ and
$\partial_\alpha\mathbf b'_\beta=\partial_\alpha\partial_\beta q^\nu\,\mathbf b_\nu+\partial_\beta q^\nu\partial_\alpha q^\mu\,\partial_\mu\mathbf b_\nu$.
The inhomogeneous term $\partial_\alpha\partial_\beta q^\lambda$ is why $\Gamma$ is **not a tensor** and can be switched off at a point.
-->

(general-relativity:local-inertial-reference-frame:local-basis)=
## Local vector basis - first order terms of local coordinates

**Transformation of basis vectors.** As $\mathbf{e}_{\alpha}|_P = \left.\tfrac{\partial \mathbf{X}}{\partial x^\alpha}\right|_{x^\beta = 0}$, and $\mathbf{b}_{\mu}|_P = \left.\tfrac{\partial \mathbf{X}}{\partial q^\mu}\right|_{q^{\nu}=q^{\nu}_P}$, using the rule of differentiation of composite functions on $\mathbf{X}(x^\alpha(q^\mu))$

$$\left.\mathbf{b}_{\mu}\right|_P = \left.\frac{\partial \mathbf{X}}{\partial q^{\mu}}\right|_{q^{\nu}_P} = \left.\frac{\partial x^{\alpha}}{\partial q^{\mu}}\right|_{q^\nu=0} \left.\frac{\partial \mathbf{X}}{\partial x^{\alpha}}\right|_{x^\beta=0} =:\left. e^{\alpha}_{\ \ \mu} \right|_P \left.\mathbf{e}_{\alpha}\right|_P \ ,$$

having defined the matrix of transformation of the vectors of the local bases in $P$, $e^{\alpha}_{\ \ \mu}$. The inverse transformation is defined as

$$\widetilde{e}^{\mu}_{\ \ \alpha} = \left. \frac{\partial q^{\mu}}{\partial x^{\alpha}} \right|_{q^{\nu}_P} \ ,$$ (eq:local-inertial:basis-transformation:inverse)

so that 

$$\widetilde{e}^{\mu}_{\ \ \alpha} e^{\alpha}_{\ \ \nu} = \frac{\partial q^{\mu}}{\partial x^{\alpha}} \frac{\partial x^{\alpha}}{\partial q^{\nu}} = \frac{\partial q^{\mu}}{\partial q^{\nu}} = \delta^{\mu}_{\nu} \ . $$

The vectors $\mathbf e_\alpha=\partial_\alpha\mathbf X|_P=\tilde e^\mu{}_\alpha\,\mathbf b_\mu$ form a **local basis** (tetrad) at $P$. Requiring $g'_{\alpha\beta}(P) = \mathbf{e}_{\alpha} \cdot \mathbf{e}_{\beta} = \eta_{\alpha\beta}$ immediately gives

$$
\eta_{\alpha \beta} = \mathbf{e}_{\alpha} \cdot \mathbf{e}_{\beta} = \widetilde{e}^{\mu}_{\ \ \alpha} \widetilde{e}^{\nu}_{\ \ \beta} \mathbf{b}^{\mu} \cdot \mathbf{b}^{\nu} = \widetilde{e}^{\mu}_{\ \ \alpha} \widetilde{e}^{\nu}_{\ \ \beta} g_{\mu \nu}(P) \ , $$

i.e.

$$\begin{aligned}
  \eta_{\alpha \beta} & = g_{\mu\nu}(P)\,\tilde e^\mu{}_\alpha\tilde e^\nu{}_\beta \\
  g_{\mu\nu}(P) & = e^\alpha{}_\mu\,e^\beta{}_\nu\,\eta_{\alpha\beta} \ .
\end{aligned}$$ (eq-tetrad)

<!--
Definition of a local basis $\mathbf{e}_{\alpha}$, s.t. $\mathbf{e}_{\alpha} \cdot \mathbf{e}_{\beta} = \eta_{\alpha \beta}$.

...

The vectors $\mathbf e_\alpha=\partial_\alpha\mathbf X|_P=\tilde e^\mu{}_\alpha\,\mathbf b_\mu$ form a **local basis** (tetrad) at $P$. Requiring $g'_{\alpha\beta}(P)=\eta_{\alpha\beta}$ gives

$$
g_{\mu\nu}(P)\,\tilde e^\mu{}_\alpha\tilde e^\nu{}_\beta=\eta_{\alpha\beta}\quad\Longleftrightarrow\quad
g_{\mu\nu}(P)=e^\alpha{}_\mu\,e^\beta{}_\nu\,\eta_{\alpha\beta},
$$ (eq-tetrad)

and the reciprocal basis is $\mathbf e^\alpha=e^\alpha{}_\mu\,\mathbf b^\mu$ with $\mathbf e^\alpha\cdot\mathbf e_\beta=\delta^\alpha_\beta$.

-->

```{admonition} How many free parameters?

- **Counting.** $\tilde e^\mu{}_\alpha$ has $16$ components, and the symmetric equation {eq}`eq-tetrad` gives $10$ conditions. So $16-10=\mathbf{6}$ parameters remain: the Lorentz group $SO(1,3)$ (3 boosts + 3 rotations).

- **Counting along an observer's worldline.** Let the observer have worldline $\mathbf X_P(\tau)$ and 4-velocity

   $$
   \mathbf u_P=\frac{d\mathbf X_P}{d\tau}=\frac{dq^\mu}{d\tau}\mathbf b_\mu,\qquad \mathbf u_P\cdot\mathbf u_P=c^2 .
   $$
   
   Choose the time leg
   
   $$
   \mathbf e_0=\frac{\mathbf u_P}{c},\qquad \mathbf e_0\cdot\mathbf e_0=1 .
   $$
   
   Then $\mathbf e_0$ is **fully fixed by the worldline**. The other three vectors must satisfy $\mathbf e_k\cdot\mathbf e_0=0$ and $\mathbf e_k\cdot\mathbf e_l=-\delta_{kl}$, i.e. they form an orthonormal triad of the spacelike 3-plane orthogonal to $\mathbf u_P$ (Gram–Schmidt always works there). The remaining freedom is the choice of this triad, and counting it as
   
   $$
   \underbrace{3}_{\text{choice of }\mathbf u_P\ (\text{boost})}+\underbrace{2}_{\mathbf e_1}+\underbrace{1}_{\mathbf e_2}+\underbrace{0}_{\mathbf e_3}=6 .
   $$
   
   Choosing $\mathbf u_P$ ties the frame to the observer. The $3$ remaining parameters ($SO(3)$) are the orientation of the spatial axes. Different $\mathbf u_P$ give different, equally valid, local inertial frames related by boosts.

```

```{admonition} Result of the first order
$g'_{\alpha\beta}(P)=\eta_{\alpha\beta}$. The residual freedom is exactly the Lorentz group: **6 parameters**.
```

```{dropdown} Christoffel symbols and coordinate transformations
:open:

$$ \dots $$ (eq-gamma-transf)


```

(general-relativity:local-inertial-reference-frame:local-coordinates)=
## Local set of coordinates


Exploiting the inverse transformation {eq}`eq:local-inertial:basis-transformation:inverse`, it's possible to write a polynomial expansion around the event $P$ of the original coordinates $q^\mu$ as a function of the local coordinates $x^{\alpha}$ as

$$q^{\mu} = q^{\mu}_P + \widetilde{e}^{\mu}_{\alpha} x^{\alpha} + \frac{1}{2} A^{\mu}_{\ \ \alpha \beta} x^\alpha x^\beta + \frac{1}{6} B^{\mu}_{\ \ \alpha \beta \gamma} x^{\alpha} x^{\beta} x^\gamma + o\left( \left( x^\lambda \right)^3 \right) \ .$$ (eq-polynomial-expansion)


<!--
## Local set of coordinates
Let the vectors $\mathbf{e}_{\mu}$ of the local basis the derivatives of the events of the spacetime w.r.t. a set of local coordinates $\{ x^\mu \}_{\mu=0:3}$, identifying the event $P$ with $x^{\mu}_P = 0$

$$\mathbf{e}_{\mu} = \left.\frac{\partial \mathbf{X}}{\partial x^{\mu}}\right|_{x^{\nu}=0} \ .$$


A polynomial expansion of the coordinates $q^{\mu}$ as a function of the local coordinates $x^{\alpha}$ around $P$ ($x^\alpha=0$ at $P$) reads

$$
q^\mu=q_P^\mu+\tilde e^\mu{}_\alpha x^\alpha+\tfrac12A^\mu{}_{\alpha\beta}x^\alpha x^\beta+\tfrac16B^\mu{}_{\alpha\beta\gamma}x^\alpha x^\beta x^\gamma+O(x^4),
$$ (eq-polynomial-expansion)

where $A$ and $B$ are totally symmetric in their lower indices. The inverse of $\tilde e$ is $e^\alpha{}_\mu$:

$$
e^\alpha{}_\mu\,\tilde e^\mu{}_\beta=\delta^\alpha_\beta,\qquad \tilde e^\mu{}_\alpha\, e^\alpha{}_\nu=\delta^\mu_\nu .
$$
-->

##  First order: the tetrad

Already discussed in the section about [Local basis](general-relativity:local-inertial-reference-frame:local-coordinates).

## Second order, $\Gamma^{(x) \gamma}_{\alpha \beta} = 0$, and $\partial_{\gamma} g^{(x)}_{\alpha \beta} = 0$

The requirement that $\Gamma^{(x) \gamma}_{\alpha \beta} = 0$ fixes the value of the coefficients $A^{\lambda}_{\alpha \beta}$ in the expansion {eq}`eq-polynomial-expansion`.
From the transformation law {eq}`eq-gamma-transf`, using $\partial_\alpha q^\mu|_P=\tilde e^\mu{}_\alpha$ and $\partial_\alpha\partial_\beta q^\lambda|_P=A^\lambda{}_{\alpha\beta}$:

$$
\Gamma'^\gamma{}_{\alpha\beta}(P)=e^\gamma{}_\lambda\Big[\Gamma^\lambda{}_{\mu\nu}(P)\,\tilde e^\mu{}_\alpha\tilde e^\nu{}_\beta+A^\lambda{}_{\alpha\beta}\Big].
$$

Setting this to zero:

$$
\boxed{\,A^\lambda{}_{\alpha\beta}=-\Gamma^\lambda{}_{\mu\nu}(P)\,\tilde e^\mu{}_\alpha\tilde e^\nu{}_\beta\,}
$$ (eq-A)

The right side is symmetric in $\alpha\beta$, as required. The solution is **unique**: no freedom is left at second order. So the quadratic approximation of the coordinate map is

$$
q^\mu=q_P^\mu+\tilde e^\mu{}_\alpha x^\alpha-\tfrac12\,\Gamma^\mu{}_{\nu\sigma}(P)\,\tilde e^\nu{}_\alpha\tilde e^\sigma{}_\beta\,x^\alpha x^\beta+O(x^3).
$$

````{dropdown} The same $\ A \ $ removes $\ \partial g'$
:open:

A polynomial expansion of the metric tensor $g'_{\alpha \beta}$ in the local coordinates $x^\gamma$ reads

$$g'_{\alpha \beta}(x^\gamma) = \eta_{\alpha \beta} + x^\gamma \left.\frac{\partial g'_{\alpha \beta}}{\partial x^\gamma}\right|_{x^\lambda = 0} + \frac{1}{2} x^\gamma x^\delta \left. \frac{\partial^2 g'_{\alpha \beta}}{\partial x^\gamma \partial x^\delta} \right|_{x^\lambda=0} + O(x^3) \ .$$

being $g'_{\alpha \beta}(x^\lambda = 0) = \eta_{\alpha \beta}$.

---

By direct computation

$$\begin{aligned}
  g'_{\alpha \beta}(x)
  & = \frac{\partial \mathbf{X}}{\partial x^\alpha} \cdot \frac{\partial \mathbf{X}}{\partial x^{\beta}} = \\
  & = \frac{\partial q^{\mu}}{\partial x^\alpha} \frac{\partial q^{\nu}}{\partial x^\beta} \frac{\partial \mathbf{X}}{\partial q^{\mu}} \cdot \frac{\partial \mathbf{X}}{\partial q^{\nu}} = \\
  & = \left( \widetilde{e}^{\mu}_\alpha - \Gamma^{\mu}_{\ \ \xi \sigma}(P) \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\xi}_{\phi} x^\phi + O(x^2) \right) \left( \widetilde{e}^{\nu}_\beta - \Gamma^{\nu}_{\ \ \varphi \psi}(P) \widetilde{e}^{\mu}_{\beta} \widetilde{e}^{\varphi}_{\chi} x^\chi + O(x^2) \right) g_{\mu \nu}(q^\sigma (x^\lambda)) = \\
  & = \left( \widetilde{e}^{\mu}_\alpha + A^{\mu}_{\alpha \phi} x^\phi + O(x^2) \right) \left( \widetilde{e}^{\nu}_\beta +  A^{\nu}_{\beta \chi} x^\chi + O(x^2) \right) g_{\mu \nu}(q^\sigma (x^\lambda))
\end{aligned}$$

so that the first derivative evaluated in $x^\lambda = 0$ is

$$\begin{aligned}
  \left.\frac{\partial g'_{\alpha \beta}}{\partial x^\gamma}\right|_{x^\lambda = 0} 
  & = \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\nu}_{\beta} \partial_{x^\gamma} g_{\mu \nu}|_{q^\sigma_P} + A^{\mu}_{\alpha \gamma} \widetilde{e}^{\nu}_{\beta} g_{\mu \nu}(P) + A^{\nu}_{\beta \gamma} \widetilde{e}^{\mu}_{\alpha} g_{\mu \nu}(P) = \\
  & = \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\sigma}_{\gamma} \partial_{q^\sigma} g_{\mu \nu}|_{q^\sigma_P} + A^{\mu}_{\alpha \gamma} \widetilde{e}^{\nu}_{\beta} g_{\mu \nu}(P) + A^{\nu}_{\beta \gamma} \widetilde{e}^{\mu}_{\alpha} g_{\mu \nu}(P) \ ,
\end{aligned}$$

having used

$$\begin{aligned}
  \left. \dfrac{\partial}{\partial x^\gamma} g_{\mu \nu}(q^\sigma(x^\alpha)) \right|_{x^\beta = 0}
  & = \left. \frac{\partial g_{\mu \nu}}{\partial q^{\sigma}} \right|_{q^{\xi}_P} \left. \frac{\partial q^\sigma}{\partial x^\gamma}\right|_{x^\lambda=0} 
    = \left. \frac{\partial g_{\mu \nu}}{\partial q^{\sigma}} \right|_{q^{\xi}_P} \widetilde{e}^{\sigma}_{\ \gamma} \ .
\end{aligned}$$

Exploiting the relation {eq}`eq-A`, the first derivative of the metric $g'_{\alpha \beta}$ evaluated in $P$ becomes identically zero,

...


```{dropdown} Details

Expand $g_{\mu \nu}(q^\sigma (x^\alpha))$ to first order in $x$. The ingredients are

$$
\partial_\alpha q^\mu=\tilde e^\mu{}_\alpha+A^\mu{}_{\alpha\sigma}x^\sigma+O(x^2),\qquad
g_{\mu\nu}(q(x))=g_{\mu\nu}(P)+\partial_\rho g_{\mu\nu}\,\tilde e^\rho{}_\sigma x^\sigma+O(x^2).
$$

Using {eq}`eq-tetrad` for the zeroth-order term:

$$
g'_{\alpha\beta}(x)=\eta_{\alpha\beta}+x^\sigma\Big[\partial_\rho g_{\mu\nu}\,\tilde e^\rho{}_\sigma\tilde e^\mu{}_\alpha\tilde e^\nu{}_\beta+g_{\mu\nu}A^\mu{}_{\alpha\sigma}\tilde e^\nu{}_\beta+g_{\mu\nu}\tilde e^\mu{}_\alpha A^\nu{}_{\beta\sigma}\Big]+O(x^2).
$$

Insert {eq}`eq-A` and use $g_{\mu\nu}\Gamma^\mu{}_{\kappa\rho}=\Gamma_{\nu,\kappa\rho}$ (and the symmetry in the last two indices):

$$
g'_{\alpha\beta}(x)=\eta_{\alpha\beta}+x^\sigma\,\tilde e^\rho{}_\sigma\tilde e^\mu{}_\alpha\tilde e^\nu{}_\beta\Big[\partial_\rho g_{\mu\nu}-\Gamma_{\mu,\rho\nu}-\Gamma_{\nu,\rho\mu}\Big]+O(x^2).
$$

The bracket vanishes identically by metric compatibility {eq}`eq-compat`. Therefore

$$
\boxed{\,g'_{\alpha\beta}(x)=\eta_{\alpha\beta}+O(x^2)\,}\qquad\Longleftrightarrow\qquad \Gamma'(P)=0\ \Longleftrightarrow\ \partial_\gamma g'_{\alpha\beta}(P)=0 .
$$ (eq-second-order)

```

````

```{note}
The two statements "$\Gamma'(P)=0$" and "$\partial g'(P)=0$" are equivalent *because* of {eq}`eq-compat`. This is the precise sense in which gravity is "transformed away" at a point: $g_{\mu\nu}$ and its first derivatives, which are what the gravitational field is made of in the Newtonian limit, can both be set to their Minkowski values.
```


```{admonition} The term $A\,A\,x^\sigma x^\xi$ is not trustworthy

The product of the two $A$ terms is $O(x^2)$. At that order one also needs $B$ (from $\partial_\alpha q^\mu$) and $\partial\partial g$ (from the expansion of $g_{\mu\nu}(q(x))$). A consistent expansion must therefore be organised by order, which is done in the next section.

```
---

## Third order in $q^{\mu}(x^\alpha)$

The cubic coefficients $B^\lambda{}_{\alpha\beta\gamma}$ are totally symmetric. Differentiate {eq}`eq-gamma-transf` once more and evaluate at $P$, where $\Gamma'(P)=0$:

$$
T^\gamma{}_{\alpha\beta\delta}:=\partial_\delta\Gamma'^\gamma{}_{\alpha\beta}(P)=e^\gamma{}_\lambda B^\lambda{}_{\alpha\beta\delta}+C^\gamma{}_{\alpha\beta\delta},
$$ (eq-T)

where $C$ is built only from $\tilde e$, $A$, $\Gamma(P)$ and $\partial\Gamma(P)$ (it does not depend on $B$). The derivative of the prefactor $\partial x^\gamma/\partial q^\lambda$ does not contribute, because it multiplies the bracket of {eq}`eq-gamma-transf`, which vanishes at $P$. The only place $B$ enters is through $\partial_\delta\partial_\alpha\partial_\beta q^\lambda=B^\lambda{}_{\alpha\beta\delta}$. $T$ is symmetric in $\alpha\beta$.

### 3.1 Decomposition of $T$

Define the totally symmetric part

$$
S^\gamma{}_{\alpha\beta\delta}=\tfrac13\big(T^\gamma{}_{\alpha\beta\delta}+T^\gamma{}_{\beta\delta\alpha}+T^\gamma{}_{\delta\alpha\beta}\big).
$$

The Riemann tensor at $P$ (where the $\Gamma\Gamma$ terms vanish) is

$$
R'^\gamma{}_{\alpha\beta\delta}=T^\gamma{}_{\delta\alpha\beta}-T^\gamma{}_{\beta\alpha\delta}.
$$

Symmetrising in $(\alpha\beta)$ and using the symmetry of $T$ in its first two lower indices:

$$
R'^\gamma{}_{\alpha\beta\delta}+R'^\gamma{}_{\beta\alpha\delta}
=\big(T^\gamma{}_{\alpha\delta\beta}+T^\gamma{}_{\beta\delta\alpha}\big)-2\,T^\gamma{}_{\alpha\beta\delta}
=3S^\gamma{}_{\alpha\beta\delta}-3\,T^\gamma{}_{\alpha\beta\delta}.
$$

Hence, in any coordinate system with $\Gamma'(P)=0$,

$$
\boxed{\,\partial_\delta\Gamma'^\gamma{}_{\alpha\beta}(P)=S^\gamma{}_{\alpha\beta\delta}-\tfrac13\big(R'^\gamma{}_{\alpha\beta\delta}+R'^\gamma{}_{\beta\alpha\delta}\big)\,}
$$ (eq-decomp)

- The **totally symmetric part $S$** is pure gauge: by {eq}`eq-T` it can be shifted at will through $B$.
- The **rest** is fixed by the Riemann tensor, which transforms as a tensor and therefore cannot be changed by any coordinate choice:

   $$
   R'^\gamma{}_{\alpha\beta\delta}(P)=e^\gamma{}_\lambda\,\tilde e^\mu{}_\alpha\tilde e^\nu{}_\beta\tilde e^\kappa{}_\delta\;R^\lambda{}_{\mu\nu\kappa}(P).
   $$

### Riemann normal coordinates

Choose

$$
B^\lambda{}_{\alpha\beta\delta}=-\tilde e^\lambda{}_\gamma\,C^\gamma{}_{(\alpha\beta\delta)}
$$

with a total symmetrisation of $C$. Then $S=0$. The freedom in $B$ is **entirely used up**. This defines **Riemann normal coordinates**, in which

$$
\partial_\delta\Gamma'^\gamma{}_{\alpha\beta}(P)=-\tfrac13\big(R^\gamma{}_{\alpha\beta\delta}+R^\gamma{}_{\beta\alpha\delta}\big).
$$

### The metric to second order

````{dropdown} Metric to the second order
:open:

$$\begin{aligned}
  g'_{\alpha \beta}(x)
  & = \frac{\partial \mathbf{X}}{\partial x^\alpha} \cdot \frac{\partial \mathbf{X}}{\partial x^{\beta}} = \\
  & = \frac{\partial q^{\mu}}{\partial x^\alpha} \frac{\partial q^{\nu}}{\partial x^\beta} \frac{\partial \mathbf{X}}{\partial q^{\mu}} \cdot \frac{\partial \mathbf{X}}{\partial q^{\nu}} = \\
  & = \frac{\partial q^{\mu}}{\partial x^\alpha} \frac{\partial q^{\nu}}{\partial x^\beta} g_{\mu \nu}(q^\sigma(x^\lambda)) \ .
\end{aligned}$$

Need for the second order expansion in $x$ of $\frac{\partial q^{\mu}}{\partial x^\alpha}$, and $g_{\mu \nu}(q^\sigma(x^\lambda))$

$$\frac{\partial q^{\mu}}{\partial x^\alpha} = \widetilde{e}^{\mu}_{\alpha} + A^{\mu}_{\alpha \beta} x^{\beta} + \frac{1}{2} B^{\mu}_{\alpha \beta \gamma} x^{\beta} x^\gamma + o(x^2)$$

$$g_{\mu \nu}(q^\sigma(x^\alpha)) = g_{\mu\nu}(P) + x^\alpha \left.\frac{\partial g_{\mu \nu}}{\partial x^\alpha}\right|_{x^\lambda = 0} + \frac{1}{2} x^\alpha x^\beta \left. \frac{\partial^2 g_{\mu \nu}}{\partial x^\alpha \partial x^\beta} \right|_{x^\lambda=0} + o(x^2) \ ,$$

with the first derivative evaluated for $x^\lambda = 0$ 

$$\frac{\partial g_{\mu \nu}}{\partial x^\alpha} = \frac{\partial q^{\sigma}}{\partial x^{\alpha}} \frac{\partial g_{\mu \nu}}{\partial q^{\sigma}}= \widetilde{e}^{\sigma}_{\ \alpha} \partial_{q^\sigma} g_{\mu \nu}$$

and the second derivative in $x^\lambda = 0$

$$\begin{aligned}
  \frac{\partial^2 g_{\mu \nu}}{\partial x^\beta \partial x^\alpha} 
  & = \frac{\partial}{\partial x^{\beta}} \left( \frac{\partial q^{\sigma}}{\partial x^{\alpha}} \frac{\partial g_{\mu \nu}}{\partial q^{\sigma}} \right) = \\
  & = \frac{\partial^2 q^{\sigma}}{\partial x^\alpha \partial x^\beta} \frac{\partial g_{\mu \nu}}{\partial q^{\sigma}} + \frac{\partial q^{\sigma}}{\partial x^\alpha} \frac{\partial q^{\chi}}{\partial x^\beta} \frac{\partial^2 g_{\mu \nu}}{\partial q^\sigma \partial q^\chi} = \\
  & = A^{\sigma}_{\alpha \beta} \partial_{q^\sigma} g_{\mu \nu} + \widetilde{e}^{\sigma}_{\ \alpha} \widetilde{e}^{\chi}_{\ \beta} \partial_{q^\sigma q^\chi} g_{\mu \nu} 
\end{aligned}$$

---

Now the first terms of the polynomial expansion of the metrics $g'_{\alpha \beta}(x)$ are

* **zero-th order**

   $${g'}_{\alpha \beta}^{(0)} = \widetilde{e}^{\mu}_{\ \alpha} \widetilde{e}^{\nu}_{\ \beta} g_{\mu \nu}(P) = \eta_{\alpha \beta}$$

* **first order**
   
   $$\begin{aligned}
   {g'}_{\alpha \beta}^{(1)} & =
   A^{\mu}_{\alpha \phi} x^\phi \widetilde{e}^{\nu}_{\ \beta} g_{\mu \nu}(P) +
   \widetilde{e}^{\mu}_{\ \alpha} A^{\nu}_{\beta \phi} x^\phi g_{\mu \nu}(P) +
   \widetilde{e}^{\mu}_{\ \alpha} \widetilde{e}^{\nu}_{\ \beta} x^\phi \widetilde{e}^{\sigma}_{\ \phi} \partial_{q^\sigma} g_{\mu \nu} = \\
   & = x^{\phi} \left[ A^{\mu}_{\alpha \phi} \widetilde{e}^{\nu}_{\ \beta} g_{\mu \nu}(P) + A^{\nu}_{\beta \phi} \widetilde{e}^{\mu}_{\ \alpha} g_{\mu \nu}(P) + \widetilde{e}^{\sigma}_{\phi} \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\nu}_{\beta} \partial_{q^\sigma} g_{\mu \nu} \right] = \\
   & = x^{\phi} \widetilde{e}^{\sigma}_{\phi} \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\nu}_{\beta} \left[ \partial_{q^\sigma} g_{\mu \nu} - \Gamma^{\xi}_{\mu \sigma}(P) g_{\xi \nu}(P) - \Gamma^{\xi}_{\nu \sigma}(P) g_{\xi \mu}(P) \right] = \\
   & = 0 \ .
   \end{aligned}$$

* **second order**


```{dropdown} Details
:open:

$$\begin{aligned}
   {g'}_{\alpha \beta}^{(2)} & =
   \frac{1}{2} B^{\mu}_{\ \alpha \lambda \gamma} x^\lambda x^\gamma \widetilde{e}^{\nu}_{\ \beta} g_{\mu \nu}(P) +
   \widetilde{e}^{\mu}_{\ \alpha} \frac{1}{2} B^{\nu}_{\ \beta \lambda \gamma} x^\lambda x^\gamma g_{\mu \nu}(P) + \\
   & + \frac{1}{2} \widetilde{e}^{\mu}_{\ \alpha} \widetilde{e}^{\nu}_{\ \beta} x^\lambda x^\gamma \left( A^{\sigma}_{\lambda \gamma} \partial_{q^\sigma} g_{\mu \nu} + \widetilde{e}^{\sigma}_{\ \lambda} \widetilde{e}^{\chi}_{\ \gamma} \partial_{q^\sigma q^\chi} g_{\mu \nu}  \right) + \\
   & + 
   A^{\mu}_{\alpha \phi} x^\phi A^{\nu}_{\ \beta \chi} x^\chi g_{\mu \nu}(P) +
   A^{\mu}_{\alpha \lambda} x^\lambda \widetilde{e}^{\nu}_{\ \beta} x^\gamma \widetilde{e}^{\sigma}_{\gamma} \partial_{q^\sigma} g_{\mu \nu} + \\
   & + \widetilde{e}^{\mu}_{\ \alpha} A^{\nu}_{\beta \lambda} x^\lambda x^\gamma \widetilde{e}^{\sigma}_{\gamma} \partial_{q^\sigma} g_{\mu \nu} = \\
   & = x^\lambda x^\gamma \left[ \left( \frac{1}{2} B^{\mu}_{\ \alpha \lambda \gamma} \widetilde{e}^{\nu}_{\ \beta} + \frac{1}{2} B^{\nu}_{\ \beta \lambda \gamma} \widetilde{e}^{\mu}_{\ \alpha} + A^{\mu}_{\alpha \lambda} A^{\nu}_{\beta \gamma} \right) g_{\mu \nu}  
   + \frac{1}{2} \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma} \partial_{q^\sigma q^\chi} g_{\mu \nu} \right. + \\ 
   & + \left. \left( 
   \frac{1}{2} \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\nu}_{\beta} A^{\sigma}_{\lambda \gamma} + 
   \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\sigma}_{\gamma} A^{\mu}_{\alpha \lambda} + 
   \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\sigma}_{\gamma} A^{\nu}_{\beta \lambda}   
   \right) \partial_{q^\sigma} g_{\mu \nu} \right] = \\
\end{aligned}$$

With 

* $\partial_{q^\sigma} g_{\mu \nu} = \Gamma^{\xi}_{\mu \sigma} g_{\xi \nu} + \Gamma^{\xi}_{\nu \sigma} g_{\xi \mu}$, 

* and differentiating by $\partial_{q^\chi}$

   $$\begin{aligned}
        \partial_{q^\chi} \partial_{q^\sigma} g_{\mu \nu}
        & = \partial_{q^\chi} \Gamma^{\xi}_{\mu \sigma} g_{\xi \nu} + \Gamma^{\xi}_{\mu \sigma} \partial_{q^\chi} g_{\xi \nu} + \partial_{q^\chi} \Gamma^{\xi}_{\nu \sigma} g_{\xi \mu} + \Gamma^{\xi}_{\nu \sigma} \partial_{q^\chi} g_{\xi \mu} = \\
        & = \partial_{q^\chi} \Gamma^{\xi}_{\mu \sigma} g_{\xi \nu} + \Gamma^{\xi}_{\mu \sigma} \left( \Gamma^{\phi}_{\chi\xi} g_{\phi \nu} + \Gamma^{\phi}_{\chi\nu} g_{\phi \xi} \right) + \partial_{q^\chi} \Gamma^{\xi}_{\nu \sigma} g_{\xi \mu} + \Gamma^{\xi}_{\nu \sigma} \left( \Gamma^{\phi}_{\chi\xi} g_{\phi \mu} + \Gamma^{\phi}_{\chi\mu} g_{\phi \xi} \right) = \\
   \end{aligned}$$

* and the coefficients $A^\lambda{}_{\alpha\beta}=-\Gamma^\lambda{}_{\mu\nu}(P)\,\tilde e^\mu{}_\alpha\tilde e^\nu{}_\beta$

it follows

$$\begin{aligned}
 {g'}^{(2)}_{\alpha \beta} 
 & = x^\lambda x^\gamma g_{\mu \nu}
 \Big\{ \\
  & \qquad \left. \frac{1}{2} \left( B^{\mu}_{\alpha \lambda \gamma} \widetilde{e}^{\nu}_{\ \beta} + B^{\nu}_{\ \beta \lambda \gamma} \widetilde{e}^{\mu}_{\ \alpha} \right) 
 \right. + \\
 & \qquad + \left.
   \frac{1}{2} g_{\mu \nu} x^\lambda x^\gamma
     \left( \widetilde{e}^{\phi}_{\alpha} \widetilde{e}^{\nu}_{\beta} \partial_{q^\chi} \Gamma^{\mu}_{\phi \sigma} 
     + \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\phi}_{\beta}  \partial_{q^\chi} \Gamma^{\nu}_{\phi \sigma}
     \right) \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma} 
  \right. + \\
 & \qquad \left.
   - \frac{1}{2} g_{\mu \nu} x^\lambda x^\gamma \Gamma^{\mu}_{\chi \xi} \Gamma^{\xi}_{\phi \sigma} \left( 
    \widetilde{e}^{\chi}_{\alpha} \widetilde{e}^{\nu}_{\beta}  \widetilde{e}^{\phi}_{\lambda} \widetilde{e}^{\sigma}_{\gamma}  
  + \widetilde{e}^{\phi}_{\alpha } \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma}  \right) 
 \right. + \\
  & \qquad \left.
  - \frac{1}{2} g_{\mu \nu} x^\lambda x^\gamma \Gamma^{\xi}_{\phi \sigma} \Gamma^{\nu}_{\chi \xi} \left( 
     \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\chi}_{\beta}  \widetilde{e}^{\phi}_{\lambda} \widetilde{e}^{\sigma}_{\gamma} + 
     \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\phi}_{\beta  } \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma} \right) 
 \right\} = \\
 & = x^\lambda x^\gamma g_{\mu \nu}
 \Big\{ \\
  & \qquad \left. \frac{1}{2} \left( B^{\mu}_{\alpha \lambda \gamma} \widetilde{e}^{\nu}_{\ \beta} + B^{\nu}_{\ \beta \lambda \gamma} \widetilde{e}^{\mu}_{\ \alpha} \right) 
 \right. + \\
 & \qquad + \left.
   \frac{1}{2} g_{\mu \nu} x^\lambda x^\gamma
     \left( \widetilde{e}^{\phi}_{\alpha} \widetilde{e}^{\nu}_{\beta} \partial_{q^\chi} \Gamma^{\mu}_{\phi \sigma} 
     + \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\phi}_{\beta}  \partial_{q^\chi} \Gamma^{\nu}_{\phi \sigma}
     \right) \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma} 
  \right. + \\
 & \qquad \left.
   - \frac{1}{2} g_{\mu \nu} x^\lambda x^\gamma \left( \widetilde{e}^{\phi}_{\alpha} \widetilde{e}^{\nu}_{\beta} \Gamma^{\mu}_{\phi \xi} \Gamma^{\xi}_{\chi \sigma} + \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\phi}_{\beta} \Gamma^{\xi}_{\chi \sigma} \Gamma^{\nu}_{\phi \xi}
   \right) \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma} \right. + \\
 & \qquad \left.
   - \frac{1}{2} g_{\mu \nu} x^\lambda x^\gamma \left( \widetilde{e}^{\phi}_{\alpha} \widetilde{e}^{\nu}_{\beta} \Gamma^{\mu}_{\chi \xi} \Gamma^{\xi}_{\phi \sigma} + \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\phi}_{\beta} \Gamma^{\xi}_{\phi \sigma} \Gamma^{\nu}_{\chi \xi}
   \right) \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma} 
 \right\} \ .
\end{aligned}$$


```

```{dropdown} Other details
:open:

$$\begin{aligned}
 & \frac{1}{2} \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma} \partial_{q^{\sigma} q^{\chi}} g_{\mu \nu} = \\
 & = \frac{1}{2} \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma} \left[ \partial_{q^\chi} \Gamma^{\xi}_{\mu \sigma} g_{\xi \nu} + \Gamma^{\xi}_{\mu \sigma} \left( \Gamma^{\phi}_{\chi\xi} g_{\phi \nu} + \Gamma^{\phi}_{\chi\nu} g_{\phi \xi} \right) + \partial_{q^\chi} \Gamma^{\xi}_{\nu \sigma} g_{\xi \mu} + \Gamma^{\xi}_{\nu \sigma} \left( \Gamma^{\phi}_{\chi\xi} g_{\phi \mu} + \Gamma^{\phi}_{\chi\mu} g_{\phi \xi} \right) \right] = \\
 & = \frac{1}{2} g_{\mu \nu} \left\{ \widetilde{e}^{\phi}_{\alpha} \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma} \left( \partial_{q^\chi} \Gamma^{\mu}_{\phi \sigma} + \Gamma^{\xi}_{\phi \sigma} \Gamma^{\mu}_{\chi\xi} \right) \right. + \\ 
 & \qquad \qquad + \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\phi}_{\beta} \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma} \left( \partial_{q^\chi} \Gamma^{\nu}_{\phi \sigma} + \Gamma^{\xi}_{\phi \sigma} \Gamma^{\nu}_{\chi\xi} \right) + \\
 & \qquad \qquad + \left. \widetilde{e}^{\phi}_{\alpha} \widetilde{e}^{\xi}_{\beta} \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma}  \left( \Gamma^{\nu}_{\phi \sigma} \Gamma^{\mu}_{\chi \xi} + \Gamma^{\mu}_{\phi \sigma} \Gamma^{\nu}_{\chi \xi} \right) \right\}
\end{aligned}$$

$$\begin{aligned}
 & \left(
   \frac{1}{2}\widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\nu}_{\beta} A^{\sigma}_{\lambda \gamma} + 
   \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\sigma}_{\gamma} A^{\mu}_{\alpha \lambda} +
   \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\sigma}_{\gamma} A^{\nu}_{\beta \lambda}   
   \right) \partial_{q^\sigma} g_{\mu \nu} = \\
 & =  \left(
   \frac{1}{2}\widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\nu}_{\beta} A^{\sigma}_{\lambda \gamma} + 
   \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\sigma}_{\gamma} A^{\mu}_{\alpha \lambda} + 
   \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\sigma}_{\gamma} A^{\nu}_{\beta \lambda}   
   \right) \left( \Gamma^{\xi}_{\mu \sigma} g_{\xi \nu} + \Gamma^{\xi}_{\nu \sigma} g_{\xi \mu} \right) = \\
 & = g_{\mu \nu} \left\{ \Gamma^{\mu}_{\xi \sigma} \left( 
   \frac{1}{2} \widetilde{e}^{\xi}_{\alpha} \widetilde{e}^{\nu}_{\beta} A^{\sigma}_{\lambda \gamma} + 
   \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\sigma}_{\gamma} A^{\xi}_{\alpha \lambda} + 
   \widetilde{e}^{\xi}_{\alpha} \widetilde{e}^{\sigma}_{\gamma} A^{\nu}_{\beta \lambda}   
 \right) + \right. \\
 & \ \qquad + \left. \Gamma^{\nu}_{\xi \sigma} \left( 
   \frac{1}{2} \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\xi}_{\beta} A^{\sigma}_{\lambda \gamma} + 
   \widetilde{e}^{\xi}_{\beta} \widetilde{e}^{\sigma}_{\gamma} A^{\mu}_{\alpha \lambda} + 
   \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\sigma}_{\gamma} A^{\xi}_{\beta \lambda}   
   \right) \right\} = \\
 & = - g_{\mu \nu} \left\{ \Gamma^{\mu}_{\xi \sigma} \left( 
   \frac{1}{2} \widetilde{e}^{\xi}_{\alpha} \widetilde{e}^{\nu}_{\beta}     \widetilde{e}^{\phi}_{\lambda} \widetilde{e}^{\chi}_{\gamma} \Gamma^{\sigma}_{\phi \chi} + 
   \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\sigma}_{\gamma}  \widetilde{e}^{\phi}_{\alpha } \widetilde{e}^{\chi}_{\lambda}\Gamma^{\xi   }_{\phi \chi} + 
   \widetilde{e}^{\xi}_{\alpha} \widetilde{e}^{\sigma}_{\gamma} \widetilde{e}^{\phi}_{\beta  } \widetilde{e}^{\chi}_{\lambda}\Gamma^{\nu   }_{\phi \chi}   
 \right) + \right. \\
 & \quad \ \qquad + \left. \Gamma^{\nu}_{\xi \sigma} \left( 
   \frac{1}{2} \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\xi}_{\beta}    \widetilde{e}^{\phi}_{\lambda} \widetilde{e}^{\chi}_{\gamma}  \Gamma^{\sigma}_{\phi \chi} + 
   \widetilde{e}^{\xi}_{\beta} \widetilde{e}^{\sigma}_{\gamma} \widetilde{e}^{\phi}_{\alpha } \widetilde{e}^{\chi}_{\lambda} \Gamma^{\mu   }_{\phi \chi} + 
   \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\sigma}_{\gamma}\widetilde{e}^{\phi}_{\beta  } \widetilde{e}^{\chi}_{\lambda} \Gamma^{\xi   }_{\phi \chi}   
   \right) \right\} = \\
 & = - g_{\mu \nu} \left\{
                             \Gamma^{\mu}_{\xi \sigma} \Gamma^{\nu}_{\phi \chi} \left(
     \widetilde{e}^{\xi}_{\alpha} \widetilde{e}^{\sigma}_{\gamma} \widetilde{e}^{\phi}_{\beta  } \widetilde{e}^{\chi}_{\lambda} +
     \widetilde{e}^{\xi}_{\beta } \widetilde{e}^{\sigma}_{\gamma} \widetilde{e}^{\phi}_{\alpha } \widetilde{e}^{\chi}_{\lambda}
   \right) \right. + \\
 & \left. \qquad \quad \ \ + \Gamma^{\mu}_{\xi \sigma} \Gamma^{\xi}_{\phi \chi} \left( 
     \frac{1}{2} \widetilde{e}^{\sigma}_{\alpha} \widetilde{e}^{\nu}_{\beta}  \widetilde{e}^{\phi}_{\lambda} \widetilde{e}^{\chi}_{\gamma} +
     \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\sigma}_{\gamma}  \widetilde{e}^{\phi}_{\alpha } \widetilde{e}^{\chi}_{\lambda} 
   \right) \right. + \\
 & \left. \qquad \quad \ \ + \Gamma^{\nu}_{\xi \sigma} \Gamma^{\xi}_{\phi \chi} \left(
     \frac{1}{2} \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\sigma}_{\beta}  \widetilde{e}^{\phi}_{\lambda} \widetilde{e}^{\chi}_{\gamma} + 
     \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\sigma}_{\gamma} \widetilde{e}^{\phi}_{\beta  } \widetilde{e}^{\chi}_{\lambda}
   \right) \right\} = 
\end{aligned}$$


```

```{dropdown} Further details
:open:

Collecting four types of contributions, 1) $\Gamma^{\mu} \Gamma^{\nu}$, 2) $\Gamma^{\mu} \Gamma^{\xi}$, 3) $\Gamma^{\nu} \Gamma^{\xi}$, 4) terms with $\partial \Gamma$,

$$\begin{aligned}
  (1)
  & = g_{\mu \nu} x^\lambda x^\gamma \Gamma^{\mu}_{\sigma \phi} \Gamma^{\nu}_{\chi \xi} \left(
  \widetilde{e}^{\sigma}_{\alpha} \widetilde{e}^{\phi}_{\lambda} \widetilde{e}^{\chi}_{\beta} \widetilde{e}^{\xi}_{\gamma}
  + \frac{1}{2} \widetilde{e}^{\chi}_{\alpha} \widetilde{e}^{\sigma}_{\beta} \widetilde{e}^{\xi}_{\lambda} \widetilde{e}^{\phi}_{\gamma}
  + \frac{1}{2} \widetilde{e}^{\phi}_{\alpha} \widetilde{e}^{\xi}_{\beta} \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma}
  - \widetilde{e}^{\phi}_{\alpha} \widetilde{e}^{\sigma}_{\gamma} \widetilde{e}^{\xi}_{\beta  } \widetilde{e}^{\chi}_{\lambda}
  - \widetilde{e}^{\phi}_{\beta } \widetilde{e}^{\sigma}_{\gamma} \widetilde{e}^{\xi}_{\alpha } \widetilde{e}^{\chi}_{\lambda}
  \right) = 0 \ ,
\end{aligned}$$

by the symmetries of the metric tensor $g_{\mu \nu}$, and Christoffel symbols $\Gamma_{\sigma\phi}^{\mu}$ w.r.t. the lower indeices.

$$\begin{aligned}
  (2)
  & = g_{\mu \nu} x^\lambda x^\gamma \Gamma^{\mu}_{\chi \xi} \Gamma^{\xi}_{\phi \sigma} \left( 
  \frac{1}{2} \widetilde{e}^{\phi}_{\alpha} \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma}
    - \frac{1}{2} \widetilde{e}^{\chi}_{\alpha} \widetilde{e}^{\nu}_{\beta}  \widetilde{e}^{\phi}_{\lambda} \widetilde{e}^{\sigma}_{\gamma}  
    - \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\chi}_{\gamma}  \widetilde{e}^{\phi}_{\alpha } \widetilde{e}^{\sigma}_{\lambda} 
  \right) = \\
  & = -\frac{1}{2} g_{\mu \nu} x^\lambda x^\gamma \Gamma^{\mu}_{\chi \xi} \Gamma^{\xi}_{\phi \sigma} \left( 
    \widetilde{e}^{\chi}_{\alpha} \widetilde{e}^{\nu}_{\beta}  \widetilde{e}^{\phi}_{\lambda} \widetilde{e}^{\sigma}_{\gamma}  
  + \widetilde{e}^{\nu}_{\beta} \widetilde{e}^{\chi}_{\gamma}  \widetilde{e}^{\phi}_{\alpha } \widetilde{e}^{\sigma}_{\lambda} 
  \right) \ .
\end{aligned}$$

$$\begin{aligned}
  (3)
  & = g_{\mu \nu} x^\lambda x^\gamma \Gamma^{\xi}_{\phi \sigma} \Gamma^{\nu}_{\chi \xi} \left( \frac{1}{2} \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\phi}_{\beta} \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma}
     - \frac{1}{2} \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\chi}_{\beta}  \widetilde{e}^{\phi}_{\lambda} \widetilde{e}^{\sigma}_{\gamma} + 
     - \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\chi}_{\gamma} \widetilde{e}^{\phi}_{\beta  } \widetilde{e}^{\sigma}_{\lambda}
  \right) = \\
  & = - \frac{1}{2} g_{\mu \nu} x^\lambda x^\gamma \Gamma^{\xi}_{\phi \sigma} \Gamma^{\nu}_{\chi \xi} \left( 
     \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\chi}_{\beta}  \widetilde{e}^{\phi}_{\lambda} \widetilde{e}^{\sigma}_{\gamma} + 
     \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\chi}_{\gamma} \widetilde{e}^{\phi}_{\beta  } \widetilde{e}^{\sigma}_{\lambda}
  \right) 
\end{aligned}$$

$$\begin{aligned}
  (4)
  & = \frac{1}{2} g_{\mu \nu} x^\lambda x^\gamma
     \left(  \widetilde{e}^{\phi}_{\alpha} \widetilde{e}^{\nu}_{\beta} \partial_{q^\chi} \Gamma^{\mu}_{\phi \sigma} 
     +  \widetilde{e}^{\mu}_{\alpha} \widetilde{e}^{\phi}_{\beta}  \partial_{q^\chi} \Gamma^{\nu}_{\phi \sigma}
     \right) \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma} \ .
\end{aligned}$$

---

$$R^\gamma{}_{\alpha\beta\delta}=\partial_\beta\Gamma^\gamma{}_{\delta\alpha}-\partial_\delta\Gamma^\gamma{}_{\beta\alpha}+\Gamma^\gamma{}_{\beta\lambda}\Gamma^\lambda{}_{\delta\alpha}-\Gamma^\gamma{}_{\delta\lambda}\Gamma^\lambda{}_{\beta\alpha}$$

$$R_{\lambda\alpha\beta\delta}=g_{\lambda \gamma} R^{\gamma}_{\ \alpha\beta\delta} = g_{\lambda \gamma} \partial_\beta\Gamma^\gamma{}_{\delta\alpha}-g_{\lambda \gamma} \partial_\delta\Gamma^\gamma{}_{\beta\alpha}+g_{\lambda \gamma} \Gamma^\gamma{}_{\beta\lambda}\Gamma^\lambda{}_{\delta\alpha}-g_{\lambda \gamma} \Gamma^\gamma{}_{\delta\lambda}\Gamma^\lambda{}_{\beta\alpha}$$

```

````


Differentiate the metric-compatibility relation {eq}`eq-compat` (written in the primed coordinates) once more and evaluate at $P$, where $\Gamma'=0$, so that derivatives of $g'$ drop out:

$$
\partial_\delta\partial_\gamma g'_{\alpha\beta}(P)=\eta_{\alpha\lambda}T^\lambda{}_{\gamma\beta\delta}+\eta_{\beta\lambda}T^\lambda{}_{\gamma\alpha\delta}
=T_{\alpha\gamma\beta\delta}+T_{\beta\gamma\alpha\delta}.
$$

Insert $T_{\alpha\beta\gamma\delta}=-\tfrac13(R_{\alpha\beta\gamma\delta}+R_{\alpha\gamma\beta\delta})$:

$$
\partial_\gamma\partial_\delta g'_{\alpha\beta}=-\tfrac13\Big[R_{\alpha\gamma\beta\delta}+R_{\alpha\beta\gamma\delta}+R_{\beta\gamma\alpha\delta}+R_{\beta\alpha\gamma\delta}\Big].
$$

The terms $R_{\alpha\beta\gamma\delta}+R_{\beta\alpha\gamma\delta}$ cancel by antisymmetry in the first pair, and $R_{\beta\gamma\alpha\delta}=R_{\alpha\delta\beta\gamma}$ by pair symmetry. So

$$
\partial_\gamma\partial_\delta g'_{\alpha\beta}(P)=-\tfrac13\big(R_{\alpha\gamma\beta\delta}+R_{\alpha\delta\beta\gamma}\big),
$$

and the Taylor expansion of the metric is

$$
\boxed{\,g'_{\alpha\beta}(x)=\eta_{\alpha\beta}-\tfrac13\,R_{\alpha\gamma\beta\delta}(P)\,x^\gamma x^\delta+O(x^3)\,}
$$ (eq-rnc)

### Counting check

- Second derivatives $\partial_\gamma\partial_\delta g'_{\alpha\beta}$: $10\times10=100$ numbers.
- Cubic coefficients $B^\lambda{}_{\alpha\beta\delta}$: $4\times20=80$ numbers, all used to set $S=0$.
- Left over: $100-80=\mathbf{20}$, exactly the number of independent components of the Riemann tensor in four dimensions.

### Summary: what each order does

| Order of $q(x)$ | Coefficient | What it fixes | Freedom left |
|---|---|---|---|
| 1 | $\tilde e^\mu{}_\alpha$ | $g'(P)=\eta$ | 6 (Lorentz group) |
| 2 | $A^\mu{}_{\alpha\beta}=-\Gamma^\mu{}_{\nu\sigma}\tilde e^\nu{}_\alpha\tilde e^\sigma{}_\beta$ | $\Gamma'(P)=0\iff\partial g'(P)=0$ | none (unique) |
| 3 | $B^\mu{}_{\alpha\beta\gamma}$ | totally symmetric part $S$ of $\partial\Gamma'(P)$ | all of $S$ (80 numbers). The remaining 20 are $R$ and are **not removable**. |

Each order of the coordinate map controls the same order of the metric: the first removes $g-\eta$, the second removes $\partial g$, and the third can only rearrange $\partial\partial g$, never eliminate it.


## The equivalence principle

In the coordinates $x^\alpha$ built above:

1. **Free fall is inertial motion at $P$.** The geodesic equation

   $$
   \frac{d^2x^\alpha}{d\tau^2}=-\Gamma'^\alpha{}_{\beta\gamma}\frac{dx^\beta}{d\tau}\frac{dx^\gamma}{d\tau}
   $$
   
   has vanishing right-hand side at $P$: free particles move in straight lines, with corrections that grow linearly in $x$ through $\partial\Gamma'\sim R$.

2. **Non-gravitational physics reduces to special relativity at $P$** (*minimal coupling*). Replacing $\eta\to g$ and $\partial\to\nabla$, for example

   $$
   \nabla_\mu T^{\mu\nu}=\partial_\mu T^{\mu\nu}+\Gamma^\mu{}_{\mu\lambda}T^{\lambda\nu}+\Gamma^\nu{}_{\mu\lambda}T^{\mu\lambda}\ \xrightarrow{\ P\ }\ \partial_\mu T^{\mu\nu},
   $$
   
   so all local laws take their special-relativistic form, with relative corrections of order $|R|\,L^2$ in a region of size $L$.

3. **What remains is tidal.** The residual gravitational information is the Riemann tensor, as seen in {eq}`eq-rnc` and in the **geodesic deviation** of two neighbouring free-falling particles with separation $\xi^\mu$ and 4-velocity $u^\mu$:

   $$
   \frac{D^2\xi^\mu}{d\tau^2}=R^\mu{}_{\nu\rho\sigma}\,u^\nu u^\rho\,\xi^\sigma .
   $$
   
   Hence "local" means: the region is small enough that $|R|\,L^2$ is below the precision of the measurement. The equivalence principle is the statement that the metric and its first derivatives can be made to coincide with those of Minkowski at $P$, but the second derivatives cannot.

---

## Example: uniformly accelerated frame in free space - Rindler coordinates in special relativity

See ["Constant" acceleration observer and Rindler coordinates](relativity-special:rindler).

In Rindler coordinates $(T=ct,\xi)$ with $a$ the proper acceleration of the observer at $\xi=0$,

$$
ds^2=\Big(1+\frac{a\xi}{c^2}\Big)^2dT^2-d\xi^2-dy^2-dz^2 .
$$

The Riemann tensor is identically zero (flat spacetime), but the connection is not:

$$
\Gamma^\xi{}_{TT}=\frac{a}{c^2}\Big(1+\frac{a\xi}{c^2}\Big)\ \xrightarrow{\ \xi=0\ }\ \frac{a}{c^2}.
$$

Take $\tilde e=\mathbb 1$ at $P$ (the observer's own frame). Then by {eq}`eq-A`,

$$
A^\xi{}_{TT}=-\frac{a}{c^2}
\qquad\Longrightarrow\qquad
\xi=x^\xi-\frac{a}{2c^2}\,(x^T)^2+O(x^3).
$$

This is exactly the transformation to the freely falling (inertial) frame: a free particle at rest in $x$ has $\xi=\text{const}-\tfrac{a}{2c^2}T^2$, i.e. it "falls" with acceleration $-a$ as seen by the accelerated observer. This is the equivalence between a uniform gravitational field and an accelerated frame: both are removed at $P$ by $A$, and in flat spacetime nothing remains at third order since $R=0$.

In a genuine gravitational field (e.g. a static observer in Schwarzschild) the same quadratic map removes the local acceleration, but the third-order term leaves the tidal tensor $R\neq0$, which distinguishes the two situations.

---

## Extension along a worldline (Fermi normal coordinates)

If the frame is carried along the whole worldline with the tetrad transported (parallel transport for a geodesic, Fermi–Walker transport otherwise), the same construction gives coordinates in which, for a geodesic observer with a non-rotating triad,

$$
g_{00}=1-R_{0i0j}\,x^ix^j+\dots,\qquad g_{0i}=-\tfrac23R_{0jik}\,x^jx^k+\dots,\qquad g_{ij}=-\delta_{ij}-\tfrac13R_{ikjl}\,x^kx^l+\dots
$$

For an accelerated or rotating observer the leading terms also contain the acceleration $a_i$ and the angular velocity $\boldsymbol\omega$:

$$
g_{00}=(1+a_ix^i)^2-(\boldsymbol\omega\times\mathbf x)^2+\dots
$$

In flat spacetime with $a=\text{const}$ and $\boldsymbol\omega=0$ this is exactly the Rindler metric of Section 6.

 

