(general-relativity:geodesics:linearization)=
# Linearization of the geodesic equation

## ...

### 0. Starting point

The geodesic equation for $q^\mu(\lambda)=q^\mu(x(\lambda))$, with $x^\alpha$ the Riemann normal coordinates at $P$, reads

$$
M^\mu{}_\alpha\,\ddot x^\alpha+G^\mu{}_{\alpha\beta}\,\dot x^\alpha\dot x^\beta=0 ,
$$

with $M^\mu{}_\alpha(x):=\partial_{x^\alpha}q^\mu(x)$ and $G^\mu{}_{\alpha\beta}(x):=\partial_\beta M^\mu{}_\alpha(x)+\Gamma^\mu_{\nu\sigma}(q(x))\,M^\nu{}_\alpha(x)\,M^\sigma{}_\beta(x)$.

Multiplying by $(M^{-1}(x))^\gamma{}_\mu$ isolates the second derivative:

$$
\boxed{\;\ddot x^\gamma+(M^{-1}(x))^\gamma{}_\mu\,G^\mu{}_{\alpha\beta}(x)\,\dot x^\alpha\dot x^\beta=0\;}
\qquad\Longleftrightarrow\qquad
\ddot x^\gamma+\tilde\Gamma^\gamma{}_{\alpha\beta}(x)\,\dot x^\alpha\dot x^\beta=0,
\qquad \tilde\Gamma:=M^{-1}G .
$$

The goal is to expand $M^{-1}$ and $G$ in powers of $x$ and multiply the two series.

**Conventions.** $\tilde e^\mu_\alpha$ is the tetrad at $P$ and $b^\alpha_\mu$ its inverse, $b^\alpha_\mu\tilde e^\mu_\beta=\delta^\alpha_\beta$. The Riemann tensor is $R^\alpha{}_{\beta\gamma\delta}=\partial_\gamma\Gamma^\alpha_{\beta\delta}-\partial_\delta\Gamma^\alpha_{\beta\gamma}+\Gamma^\alpha_{\gamma\lambda}\Gamma^\lambda_{\beta\delta}-\Gamma^\alpha_{\delta\lambda}\Gamma^\lambda_{\beta\gamma}$ (independent of the signature). All quantities at $P$ are projected on the local frame, e.g.

$$
\Gamma^\kappa{}_{\alpha\beta}:=b^\kappa_\mu\Gamma^\mu_{\nu\sigma}(P)\tilde e^\nu_\alpha\tilde e^\sigma_\beta,\qquad
\partial_\gamma\Gamma^\kappa{}_{\alpha\beta}:=b^\kappa_\mu\,\partial_\rho\Gamma^\mu_{\nu\sigma}(P)\,\tilde e^\rho_\gamma\tilde e^\nu_\alpha\tilde e^\sigma_\beta ,
$$

and similarly for $R^\alpha{}_{\beta\gamma\delta}$ and its covariant derivatives. These frame components of $\Gamma$ in the global coordinates are *not* tensors, and they all drop out of the final result.

### 1. Counting orders

Rescale $x\to\varepsilon x$ at fixed $\lambda$. Then $x$, $\dot x$ and $\ddot x$ each carry one power of $\varepsilon$. This is consistent because every term of the equation contains exactly two $\lambda$-derivatives, so the counting in amplitude is independent of the counting in derivatives. In the reduced equation,

$$
\ddot x\;\sim\;\varepsilon^1,\qquad \tilde\Gamma_n(x)\,\dot x\dot x\;\sim\;\varepsilon^{n+2},
$$

where $\tilde\Gamma_n$ is the part of $\tilde\Gamma$ homogeneous of degree $n$ in $x$.

Written with the constant projector $b_\mu$ instead of $M^{-1}(x)$, the equation contains cross terms such as $\ddot x^\alpha x^\beta A^\mu{}_{\alpha\beta}$, which look second order. They are an artefact of $b_\mu\neq M^{-1}(x)$. Since $\ddot x$ is itself of order $\ge3$ on shell, these terms are really of order $\ge4$, and they are removed exactly by the factor $M^{-1}(x)$.

### 2. Expansion of the map $q^\mu(x)$

Normal coordinates are defined by the requirement that $x^\alpha=\lambda u^\alpha$ is a geodesic for every constant $u^\alpha$. Then $\ddot x=0$ and $\dot x=u$, so the equation along each ray gives $G^\mu{}_{\alpha\beta}(x)\,x^\alpha x^\beta=0$. With the degree operator $D:=x^\alpha\partial_\alpha$ (so $x^\alpha x^\beta\partial_\alpha\partial_\beta=D(D-1)$ and $x^\alpha M^\mu{}_\alpha=Dq^\mu$), this is

$$
D(D-1)\,q^\mu+\Gamma^\mu_{\nu\sigma}(q)\,Dq^\nu\,Dq^\sigma=0 .
$$

Write $q^\mu=q_P^\mu+\sum_{k\ge1}q^\mu_k$, with $q_k$ homogeneous of degree $k$ (so $Dq_k=k\,q_k$). The degree-$n$ part of the equation is

$$
n(n-1)\,q_n^\mu=-\Big[\Gamma^\mu_{\nu\sigma}(q)\,Dq^\nu Dq^\sigma\Big]_{\deg n},
$$

and the right-hand side involves only $q_k$ with $k\le n-1$. The recursion is therefore triangular. Explicitly,

$$
q^\mu=q^\mu_P+\tilde e^\mu_\alpha x^\alpha+\tfrac12A^\mu{}_{\alpha\beta}x^\alpha x^\beta+\tfrac16B^\mu{}_{\alpha\beta\gamma}x^\alpha x^\beta x^\gamma+\tfrac1{24}D^\mu{}_{\alpha\beta\gamma\delta}x^\alpha x^\beta x^\gamma x^\delta+\dots
$$

$$
A^\kappa{}_{\alpha\beta}=-\Gamma^\kappa{}_{\alpha\beta},\qquad
B^\kappa{}_{\alpha\beta\gamma}=-\partial_{(\gamma}\Gamma^\kappa{}_{\alpha\beta)}+2\,\Gamma^\kappa{}_{\lambda(\alpha}\Gamma^\lambda{}_{\beta\gamma)} ,
$$

where $A,B,D,\dots$ are totally symmetric (Taylor coefficients of one function) and the indices are frame-projected. The next coefficient $D$ follows from $n=4$ of the same recursion. The first coefficient $q_1=\tilde e^\mu_\alpha x^\alpha$ is the free choice of the tetrad.

### 3. Expansion of $M$ and $M^{-1}$

Differentiating $q^\mu(x)$,

$$
M^\mu{}_\alpha=\tilde e^\mu_\alpha+A^\mu{}_{\alpha\beta}x^\beta+\tfrac12B^\mu{}_{\alpha\beta\gamma}x^\beta x^\gamma+\tfrac16D^\mu{}_{\alpha\beta\gamma\delta}x^\beta x^\gamma x^\delta+\dots
$$

Factor out the value at $P$:

$$
M^\mu{}_\alpha=\tilde e^\mu_\beta\big(\delta^\beta_\alpha+N^\beta{}_\alpha(x)\big),\qquad
N=N_1+N_2+\dots,
$$

$$
N_1{}^\beta{}_\alpha=a^\beta{}_{\alpha\gamma}x^\gamma,\qquad
N_2{}^\beta{}_\alpha=\tfrac12\mathsf b^\beta{}_{\alpha\gamma\delta}x^\gamma x^\delta,\qquad
N_3{}^\beta{}_\alpha=\tfrac16\mathsf d^\beta{}_{\alpha\gamma\delta\varepsilon}x^\gamma x^\delta x^\varepsilon,
$$

with $a=bA$, $\mathsf b=bB$, $\mathsf d=bD$ (frame projections). Since $N=O(x)$, the Neumann series converges near $P$:

$$
(M^{-1})^\gamma{}_\mu=\big[(1+N)^{-1}\big]^\gamma{}_\beta\,b^\beta_\mu=\Big[1-N_1+(N_1N_1-N_2)+\big(-N_1N_1N_1+N_1N_2+N_2N_1-N_3\big)+\dots\Big]^\gamma{}_\beta\,b^\beta_\mu .
$$

```{dropdown} Inverse of a polynomial expansion
:open:

$$\begin{aligned}
M^{\mu}_{\ \ \nu} 
& = M^{\mu}_{0 \ \ \nu} + M^{\mu}_{1\ \ \nu \alpha} x^\alpha + \frac{1}{2} M^{\mu}_{2\ \ \nu \alpha \beta} x^\alpha x^\beta + \frac{1}{6} M^{\mu}_{3\ \ \nu \alpha \beta \gamma} x^\alpha x^\beta x^\gamma + \dots = \\
& = M^{\mu}_{0 \ \ \eta} \left\{ \delta^{\eta}_{\ \nu} + \widetilde{M}^{\eta}_{1\ \ \nu \alpha} x^\alpha + \frac{1}{2} \widetilde{M}^{\eta}_{2\ \ \nu \alpha \beta} x^\alpha x^\beta + \frac{1}{6} \widetilde{M}^{\eta}_{3\ \ \nu \alpha \beta \gamma} x^\alpha x^\beta x^\gamma + \dots \right\} \ ,
\end{aligned}$$

with $\widetilde{M}^{\eta}_{i\ \ \nu \alpha \dots} = \left( M^{-1}_{0} \right)^{\eta}_{\ \ \mu} M^{\mu}_{i\ \ \nu \alpha \dots}$. Let $P^{\nu}_{\ \ \sigma}$ s.t. $M^{\mu}_{\ \ \nu} P^{\nu}_{\ \ \sigma} = \delta^{\mu}_{\ \ \sigma}$, with its polynomial expansion

$$\begin{aligned}
P^{\nu}_{\ \ \sigma} 
& = P^{\nu}_{0 \ \ \sigma} + P^{\nu}_{1\ \ \sigma \alpha} x^\alpha + \frac{1}{2} P^{\nu}_{2\ \ \sigma \alpha \beta} x^\alpha x^\beta + \frac{1}{6} P^{\nu}_{3\ \ \sigma \alpha \beta \gamma} x^\alpha x^\beta x^\gamma + \dots = \\
& = P^{\nu}_{0 \ \ \eta} \left\{ \delta^{\eta}_{\ \ \sigma} + \widetilde{P}^{\eta}_{1\ \ \sigma \alpha} x^\alpha + \frac{1}{2} \widetilde{P}^{\eta}_{2\ \ \sigma \alpha \beta} x^\alpha x^\beta + \frac{1}{6} \widetilde{P}^{\eta}_{3\ \ \sigma \alpha \beta \gamma} x^\alpha x^\beta x^\gamma + \dots \right\}
\end{aligned}$$

The unknown coefficients $P^{\nu}_{i \ \ \sigma}$ of the polynomial series are evaluate matching coefficients in the inverse relation.

**Zero-th order.** $\delta^{\mu}_{\ \ \sigma} = M^{\mu}_{0\ \ \nu} P^{\nu}_{0 \ \ \sigma} $ implies $P^{\nu}_{0\ \ \sigma} = \left( M_0^{-1} \right)^{\nu}_{\ \ \sigma}$.

**First order.**

$$
0 = M^{\mu}_{0 \ \ \nu} P^{\nu}_{1 \ \ \sigma \alpha } x^\alpha + M^{\mu}_{1 \ \ \nu \alpha} P^{\nu}_{0 \ \ \sigma} x^\alpha
$$

implies for each $\alpha$ 

$$
P^{\nu}_{1 \ \ \sigma \alpha} 
  = - \left( M^{-1}_0 \right)^{\nu}_{\ \ \xi} M^{\xi}_{1 \ \ \chi \alpha} P^{\chi}_{0 \ \ \sigma} 
  = - \left( M^{-1}_0 \right)^{\nu}_{\ \ \xi} M^{\xi}_{1 \ \ \chi \alpha} \left( M^{-1}_{0} \right)^{\chi}_{\ \ \sigma}
$$

or

$$\widetilde{P}^{\nu}_{1\ \ \sigma \alpha} = - \widetilde{M}^{\nu}_{1\ \ \sigma \alpha} \ .$$

**Second order.**

$$\begin{aligned}
0 
& = x^\alpha x^\beta \left\{ \frac{1}{2} M^{\mu}_{0 \ \ \nu} P^{\nu}_{2 \ \ \sigma \alpha \beta} + M^{\mu}_{1 \ \ \nu \alpha} P^{\nu}_{1 \ \ \sigma\beta} + \frac{1}{2} M^{\mu}_{2 \ \ \nu \alpha \beta} P^{\nu}_{0 \ \ \sigma} \right\} = && \text{(sym.)} \\
& = \frac{1}{2} x^\alpha x^\beta \left\{ M^{\mu}_{0 \ \ \nu} P^{\nu}_{2 \ \ \sigma \alpha \beta} + M^{\mu}_{1 \ \ \nu \alpha} P^{\nu}_{1 \ \ \sigma\beta} + M^{\mu}_{1 \ \ \nu \beta} P^{\nu}_{1 \ \ \sigma\alpha} + M^{\mu}_{2 \ \ \nu \alpha \beta} P^{\nu}_{0 \ \ \sigma} \right\} \ ,
\end{aligned}$$

implies

$$\begin{aligned}
P^{\nu}_{2 \ \ \sigma \alpha \beta} 
  & = - \left( M^{-1}_0 \right)^{\nu}_{\ \ \mu} \left( M^{\mu}_{1 \ \ \xi \alpha} P^{\xi}_{1 \ \ \sigma\beta} + M^{\mu}_{1 \ \ \xi \beta} P^{\xi}_{1 \ \ \sigma\alpha} + M^{\mu}_{2 \ \ \xi \alpha \beta} P^{\xi}_{0 \ \ \sigma} \right) = \\
  & =   \left( M^{-1}_0 \right)^{\nu}_{\ \ \mu} \left( M^{\mu}_{1 \ \ \xi \alpha} \left( M^{-1}_0 \right)^{\xi}_{\ \ \eta} M^{\eta}_{1 \ \ \chi \beta} \left( M^{-1}_{0} \right)^{\chi}_{\ \ \sigma} + M^{\mu}_{1 \ \ \xi \beta} \left( M^{-1}_0 \right)^{\xi}_{\ \ \eta} M^{\eta}_{1 \ \ \chi \alpha} \left( M^{-1}_{0} \right)^{\chi}_{\ \ \sigma} - M^{\mu}_{2 \ \ \xi \alpha \beta} \left( M^{-1}_0 \right)^{\xi}_{\ \ \sigma} \right) = \\
\end{aligned}$$

or

$$\widetilde{P}^{\nu}_{2\ \ \sigma \alpha \beta} = \widetilde{M}^{\nu}_{1 \ \ \xi \alpha} \widetilde{M}^{\xi}_{1 \ \ \sigma \beta} + \widetilde{M}^{\nu}_{1 \ \ \xi \beta} \widetilde{M}^{\xi}_{1 \ \ \sigma \alpha} - \widetilde{M}^{\nu}_{2 \ \ \sigma \alpha \beta} \ .$$

**$n^{\rm th}$-order.** Recursion formula holds

$$\widetilde{P}^{\nu}_{n \ \ \sigma \alpha_1 \dots \alpha_n} = \dots$$

**todo** *Prove it!*

```

````{dropdown} Expansion of $\ \left( M^{-1}(x) \right)^{\gamma}_{\ \ \mu} G^{\mu}_{\ \ \alpha \beta}(x) \dot{x}^\alpha \dot{x}^\beta$
:open:

$$\begin{aligned}
  0 
  & = \ddot{x}^\gamma + \left( M^{-1}(x) \right)^{\gamma}_{\ \ \mu} G^{\mu}_{\ \ \alpha \beta}(x) \dot{x}^\alpha \dot{x}^\beta = \\
  & = \ddot{x}^\gamma + \left( P^{\gamma}_{0\ \ \mu} + P^{\gamma}_{1 \ \ \mu\xi} x^{\xi} + \dots \right) \left( G^{\mu}_{0\ \ \alpha \beta} + G^{\mu}_{1\ \ \xi\alpha\beta} x^{\xi} + \dots \right) \dot{x}^\alpha \dot{x}^\beta \ .
\end{aligned}$$

**Third-order.** Choosing Riemann normal coordinates, $G^{\mu}_{0\ \ \alpha \beta} = 0$, so the third-order contribution reads 

$$\begin{aligned}
  P^{\gamma}_{0\ \ \mu} G^{\mu}_{1\ \ \alpha \beta \xi} \dot{x}^\alpha \dot{x}^\beta x^\xi
  & = e^{\gamma}_{\ \ \mu} \left( B^{\mu}_{\ \alpha \beta \xi} + \partial_{x^{\xi}} \Gamma^{\mu}_{\nu \sigma}(P) \widetilde{e}^{\nu}_{\ \ \alpha} \widetilde{e}^{\sigma}_{\ \ \beta} + \Gamma^{\mu}_{\nu \sigma}(P) A^{\nu}_{\ \ \alpha \xi} \widetilde{e}^{\sigma}_{\ \ \beta} + \Gamma^{\mu}_{\nu \sigma}(P) \widetilde{e}^{\nu}_{\ \ \alpha} A^{\sigma}_{\ \ \beta \xi} \right) \dot{x}^\alpha \dot{x}^\beta x^\xi = \\
\end{aligned}$$

Using

$$\begin{aligned}
  \partial_{x^\xi} \Gamma^{\mu}_{\nu \sigma} & = \partial_{x^\xi} q^{\rho} \partial_{q^{\rho}} \Gamma^{\mu}_{\nu \sigma} = \widetilde{e}^{\rho}_{\xi} \partial_{q^{\rho}} \Gamma^{\mu}_{\nu \sigma} \\
  A^{\lambda}_{\ \ \alpha \beta} & = -\Gamma^{\lambda}_{\phi \zeta}(P) \widetilde{e}^{\phi}_{\ \alpha} \widetilde{e}^{\zeta}_{\ \beta} \\
\end{aligned}$$

and observing that

$$\begin{aligned}
  G^{\mu}_{1\ \ \alpha \beta \xi}
  & = B^{\mu}_{\ \ \alpha \beta \xi} + \left( \partial_{\rho} \Gamma^{\mu}_{\nu \sigma} - \Gamma^{\mu}_{\chi \sigma} \Gamma^{\chi}_{\nu \rho} - \Gamma^{\mu}_{\nu \chi} \Gamma^{\chi}_{\sigma \rho} \right) \widetilde{e}^{\nu}_{\ \alpha} \widetilde{e}^{\sigma}_{\ \beta} \widetilde{e}^{\rho}_{\ \xi} = \\
  & = B^{\mu}_{\ \ \alpha \beta \xi} + \widetilde{K}^{\mu}_{\ \nu \sigma \rho} \widetilde{e}^{\nu}_{\ \alpha} \widetilde{e}^{\sigma}_{\ \beta} \widetilde{e}^{\rho}_{\ \xi} = \\
  & = B^{\mu}_{\ \alpha \beta \xi} + K^{\mu}_{\ \alpha \beta \xi} \\
  & =: T^{\mu}_{\ \alpha \beta \xi}
\end{aligned}$$

Recalling that $T^{\mu}_{\ \alpha \beta \xi} = - \tfrac{1}{3} \left( \bar{R}^{\mu}_{\ \alpha \beta \xi} + \bar{R}^{\mu}_{\ \beta \alpha \xi} \right)$ for Riemann normal coordinates, the polynomial expansion of the geodesics equation up to the third order reads

$$\begin{aligned}
  0 
  & = \ddot{x}^\gamma - \frac{1}{3} e^\gamma_{\ \mu} \left( \bar{R}^{\mu}_{\ \alpha \beta \xi} + \bar{R}^{\mu}_{\ \beta \alpha \xi} \right) \dot{x}^\alpha \dot{x}^\beta x^\xi = \\
  & = \ddot{x}^\gamma - \frac{1}{3} \left( {R'}^{\gamma}_{\ \alpha \beta \xi} + {R'}^{\gamma}_{\ \beta \alpha \xi} \right) \dot{x}^\alpha \dot{x}^\beta x^\xi \ ,
\end{aligned}$$

having projected here also the upper index on the local Minkowski vector basis, and exploiting symmetry of dummy indices

$$
  \ddot{x}^\gamma = \frac{2}{3} {R'}^{\gamma}_{\ \alpha \beta \xi} \dot{x}^\alpha \dot{x}^\beta x^\xi \ .
$$



---

*see [local inertial reference frame](general-relativity:local-inertial-reference-frame) and clean this and those notes* **todo**

* $B^{\mu}_{\ \alpha \lambda \gamma}$ symmetric under any swap of lower indices

* $K^{\mu}_{\ \alpha \lambda \gamma} = \left( \partial_{\chi} \Gamma^{\mu}_{\phi \sigma} - \Gamma^{\mu}_{\phi \xi} \Gamma^{\xi}_{\chi \sigma} - \Gamma^{\mu}_{\sigma \xi} \Gamma^{\xi}_{\phi \chi} \right) \widetilde{e}^{\phi}_{\alpha} \widetilde{e}^{\sigma}_{\lambda} \widetilde{e}^{\chi}_{\gamma}$, is symmetric under $\alpha \leftrightarrow \lambda$

* $T^{\mu}_{\ \alpha \lambda \gamma} = B^{\mu}_{\ \alpha \lambda \gamma} + K^{\mu}_{\ \alpha \lambda \gamma}$, symmetric under $\alpha \leftrightarrow \lambda$

---

<!--
and dropping the argument $(P)$, 

$$\begin{aligned}
  & P^{\gamma}_{0\ \ \mu} G^{\mu}_{1\ \ \alpha \beta \sigma} \dot{x}^\alpha \dot{x}^\beta x^\xi = \\
  & = e^{\gamma}_{\mu} \left[ - \frac{1}{3}( R^{\mu}_{\ \ \nu \rho \sigma} + R^{\mu}_{\ \ \sigma \rho \nu} ) + \partial_{\rho} \Gamma^{\mu}_{\nu \sigma} - \Gamma^{\mu}_{\chi \sigma} \Gamma^{\chi}_{\alpha \xi} - \Gamma^{\mu}_{\nu \chi} \Gamma_{\beta \xi}^\chi \right] 
  \widetilde{e}^{\nu}_{\ \ \alpha} \widetilde{e}^{\sigma}_{\ \ \beta} \widetilde{e}^{\rho}_{\ \ \xi} \dot{x}^\alpha \dot{x}^\beta x^\xi \\
\end{aligned}$$


With $M^\mu{}_\alpha(x):=\partial_{x^\alpha}q^\mu(x)$ and $G^\mu{}_{\alpha\beta}(x):=\partial_\beta M^\mu{}_\alpha(x)+\Gamma^\mu_{\nu\sigma}(q(x))\,M^\nu{}_\alpha(x)\,M^\sigma{}_\beta(x)$.

$$
q^\mu=q^\mu_P+\tilde e^\mu_\alpha x^\alpha+\tfrac12A^\mu{}_{\alpha\beta}x^\alpha x^\beta+\tfrac16B^\mu{}_{\alpha\beta\gamma}x^\alpha x^\beta x^\gamma+\tfrac1{24}C^\mu{}_{\alpha\beta\gamma\delta}x^\alpha x^\beta x^\gamma x^\delta+\dots
$$

$$
M^\mu{}_\alpha=\tilde e^\mu_\alpha+A^\mu{}_{\alpha\beta}x^\beta+\tfrac12B^\mu{}_{\alpha\beta\gamma}x^\beta x^\gamma+\tfrac16C^\mu{}_{\alpha\beta\gamma\delta}x^\beta x^\gamma x^\delta+\dots
$$

$$
\left( M^{-1} \right)^{\gamma}_{\mu} = 
$$

$$
A^\kappa{}_{\alpha\beta}=-\Gamma^\kappa{}_{\alpha\beta},\qquad
B^\kappa{}_{\alpha\beta\gamma}=-\partial_{(\gamma}\Gamma^\kappa{}_{\alpha\beta)}+2\,\Gamma^\kappa{}_{\lambda(\alpha}\Gamma^\lambda{}_{\beta\gamma)} ,
$$
-->

````




### 4. Expansion of $G$

Projecting on the frame, $g^\kappa{}_{\alpha\beta}(x):=b^\kappa_\mu G^\mu{}_{\alpha\beta}(x)=g_0+g_1+g_2+\dots$, with $g_n$ homogeneous of degree $n$. The ingredients are

$$
\partial_\beta M^\mu{}_\alpha=A^\mu{}_{\alpha\beta}+B^\mu{}_{\alpha\beta\gamma}x^\gamma+\tfrac12D^\mu{}_{\alpha\beta\gamma\delta}x^\gamma x^\delta+\dots,
$$

$$
\Gamma^\mu_{\nu\sigma}(q(x))=\Gamma^\mu_{\nu\sigma}+\partial_\rho\Gamma^\mu_{\nu\sigma}\,\Delta q^\rho+\tfrac12\partial_\rho\partial_\tau\Gamma^\mu_{\nu\sigma}\,\Delta q^\rho\Delta q^\tau+\dots,\qquad
\Delta q^\rho=\tilde e^\rho_\alpha x^\alpha+\tfrac12A^\rho{}_{\alpha\beta}x^\alpha x^\beta+\dots
$$

Multiplying the series order by order (all $\Gamma$'s are evaluated at $P$ and projected on the frame):

$$
g_0{}^\kappa{}_{\alpha\beta}=A^\kappa{}_{\alpha\beta}+\Gamma^\kappa{}_{\alpha\beta}=0,
$$

$$
g_1{}^\kappa{}_{\alpha\beta}=\Big[\mathsf b^\kappa{}_{\alpha\beta\gamma}+\partial_\gamma\Gamma^\kappa{}_{\alpha\beta}-\Gamma^\kappa{}_{\lambda\beta}\Gamma^\lambda{}_{\alpha\gamma}-\Gamma^\kappa{}_{\alpha\lambda}\Gamma^\lambda{}_{\beta\gamma}\Big]x^\gamma,
$$

and $g_2$ follows by collecting all products of total degree 2 (it involves $\mathsf d$, $\mathsf b$, $a$, $\Gamma$, $\partial\Gamma$ and $\partial\partial\Gamma$). Here $g_0=0$ is the statement that the quadratic coefficient $A$ cancels the connection at $P$.

### 5. The product $\tilde\Gamma=M^{-1}G$ order by order

From $(1+N)\,\tilde\Gamma=g$ one gets the recursion

$$
\tilde\Gamma_n=g_n-\sum_{k=1}^{n-1}N_k\,\tilde\Gamma_{n-k},\qquad \tilde\Gamma_0=g_0=0,
$$

that is

$$
\tilde\Gamma_1=g_1,\qquad
\tilde\Gamma_2=g_2-N_1\,g_1,\qquad
\tilde\Gamma_3=g_3-N_1\tilde\Gamma_2-N_2\,g_1,\;\dots
$$

Equivalently, the geodesic equation expanded in $\varepsilon$ is

$$
\ddot x^\kappa=-\sum_{n\ge1}\tilde\Gamma_n{}^\kappa{}_{\alpha\beta}(x)\,\dot x^\alpha\dot x^\beta ,\qquad
\text{the term }n\text{ being of order }\varepsilon^{n+2}.
$$

### 6. Results order by order

**Order $\varepsilon^1$.** $\;\ddot x^\alpha=0$.

**Order $\varepsilon^2$.** The only candidate is $\tilde\Gamma_0\dot x\dot x=g_0\dot x\dot x=0$, which vanishes. The second-order information is entirely in $A=-\Gamma\tilde e\tilde e$.

**Order $\varepsilon^3$.** Inserting $\mathsf b$ from Section 2 into $g_1$ and contracting with $(u,u,x)$ for $\alpha,\beta,\gamma$, all quantities combine into

$$
g_1(u,u,x)^\kappa=\tfrac23\Big[\partial_x\Gamma^\kappa_{uu}-\partial_u\Gamma^\kappa_{ux}+\Gamma^\kappa_{\lambda x}\Gamma^\lambda_{uu}-\Gamma^\kappa_{\lambda u}\Gamma^\lambda_{ux}\Big]=\tfrac23R^\kappa{}_{uxu}=-\tfrac23R^\kappa{}_{\beta\gamma\delta}u^\beta u^\gamma x^\delta .
$$

The non-tensorial $\Gamma$ terms cancel against the $\mathsf b$ term of the expansion of $q$. Since $g_1$ is symmetric in $(\alpha\beta)$, this fixes it completely:

$$
\tilde\Gamma^\kappa{}_{\alpha\beta}\Big|_{1}=-\tfrac13\big(R^\kappa{}_{\alpha\beta\gamma}+R^\kappa{}_{\beta\alpha\gamma}\big)x^\gamma ,
\qquad
\boxed{\ddot x^\kappa=\tfrac23\,R^\kappa{}_{\beta\gamma\delta}\,\dot x^\beta\dot x^\gamma x^\delta+O(\varepsilon^4)} .
$$

Check: if $x\parallel\dot x$ (a geodesic through $P$), the right-hand side vanishes by the antisymmetry of $R$ in $\gamma\delta$.

**Order $\varepsilon^4$.** Here $\tilde\Gamma_2=g_2-N_1g_1$ and the non-tensorial pieces again cancel. The result contains only $\nabla R$. It can be obtained either by the explicit multiplication, or from the following two properties:

1. $\tilde\Gamma_2{}^\kappa{}_{\alpha\beta}(x)\,x^\alpha x^\beta=0$ (rays are geodesics).
2. $\nabla_\varepsilon R^\kappa{}_{\alpha\gamma\beta}\,x^\varepsilon=\partial_\gamma\tilde\Gamma_2{}^\kappa{}_{\alpha\beta}-\partial_\beta\tilde\Gamma_2{}^\kappa{}_{\alpha\gamma}$ (the curvature at degree 1; here $\partial R=\nabla R$ at $P$ because $\tilde\Gamma(0)=0$).

Solving these (the totally symmetric part of the coefficient tensor vanishes by 1, and the rest is fixed by 2) gives

$$
\tilde\Gamma_2{}^\kappa{}_{\alpha\beta}=\tfrac1{24}\Big[\,5\big(\nabla_x R^\kappa{}_{\alpha x\beta}+\nabla_x R^\kappa{}_{\beta x\alpha}\big)-\nabla_\beta R^\kappa{}_{x\alpha x}-\nabla_\alpha R^\kappa{}_{x\beta x}\Big],
$$

where a subscript $x$ means contraction with $x^\delta$, e.g. $\nabla_xR^\kappa{}_{\alpha x\beta}=x^\varepsilon x^\delta\nabla_\varepsilon R^\kappa{}_{\alpha\delta\beta}$ and $R^\kappa{}_{x\alpha x}=R^\kappa{}_{\delta\alpha\varepsilon}x^\delta x^\varepsilon$. Hence

$$
\ddot x^\kappa=-\tilde\Gamma_2{}^\kappa{}_{\alpha\beta}\,\dot x^\alpha\dot x^\beta+(\text{order }\varepsilon^5).
$$

Check: tracing over $\kappa=\alpha$ gives $-\tfrac1{12}\big(2\nabla_xR_{\beta x}+\nabla_\beta R_{xx}\big)$ (Ricci tensor $R_{\beta\delta}=R^\kappa{}_{\beta\kappa\delta}$ and the contracted Bianchi identity), which is $\partial_\beta\ln\sqrt{|g|}$ at the corresponding order in normal coordinates.

**Order $\varepsilon^5$ and beyond.** $\tilde\Gamma_3$ contains $\nabla\nabla R$ and $R^2$, and so on. Every $\tilde\Gamma_n$ is a tensor built from $R$ and its covariant derivatives, because the frame components $\Gamma$ cancel at each order.

| order | content | equation |
|---|---|---|
| $\varepsilon^1$ | — | $\ddot x=0$ |
| $\varepsilon^2$ | $\tilde\Gamma_0=0$ | no new term |
| $\varepsilon^3$ | $\tilde\Gamma_1\propto R\,x$ | $\ddot x^\kappa=\tfrac23R^\kappa{}_{\beta\gamma\delta}\dot x^\beta\dot x^\gamma x^\delta$ |
| $\varepsilon^4$ | $\tilde\Gamma_2\propto\nabla R\,xx$ | $\ddot x=-\tilde\Gamma_2\dot x\dot x$ |
| $\varepsilon^5$ | $\tilde\Gamma_3\propto\nabla\nabla R,\;R^2$ | next |

### 7. Solving the expanded equation

Take $x(0)=x_0$ and $\dot x(0)=v$, both of order $\varepsilon$. At leading order $x=x_0+v\lambda$. Inserting it in the $\varepsilon^3$ equation and using $R^\kappa{}_{\beta\gamma\delta}v^\beta v^\gamma v^\delta=0$,

$$
\ddot x^\kappa=\tfrac23R^\kappa{}_{\beta\gamma\delta}v^\beta v^\gamma x_0^\delta,
\qquad
x^\kappa(\lambda)=x_0^\kappa+v^\kappa\lambda+\tfrac13R^\kappa{}_{\beta\gamma\delta}v^\beta v^\gamma x_0^\delta\,\lambda^2+O(\varepsilon^4).
$$

Composing with $q^\mu(x)$ from Section 2 gives $q^\mu(\lambda)$ to the same order.

**Geodesic deviation.** For $x=u\lambda+\xi$, linearizing the $\varepsilon^3$ equation gives
$\ddot\xi^\alpha=\tfrac23\big[R^\alpha{}_{\beta\gamma\delta}u^\beta u^\gamma\xi^\delta+\lambda R^\alpha{}_{\beta\gamma\delta}u^\beta\dot\xi^\gamma u^\delta\big]$.
This is not covariant: the factor $2/3$ and the explicit $\lambda$ term come from $\xi$ being a coordinate difference. With the covariant derivative along $u\lambda$, $\frac{D\xi}{d\lambda}=\dot\xi+\tilde\Gamma_1(u,\xi)$, the extra terms cancel and

$$
\frac{D^2\xi^\alpha}{d\lambda^2}=R^\alpha{}_{\beta\gamma\delta}\,u^\beta u^\gamma\xi^\delta=-R^\alpha{}_{\beta\gamma\delta}\,u^\beta\xi^\gamma u^\delta .
$$



