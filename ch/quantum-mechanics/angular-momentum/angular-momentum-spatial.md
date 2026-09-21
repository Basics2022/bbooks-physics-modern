(quantum-mechanics:angular-momentum:spatial)=
# Spatial Angular Momentum

Promoting the classical definition of angular momentum $\mathbf{L} = \mathbf{r} \times \mathbf{p}$, the angular momentum operator in quantum mechanics reads

$$\hat{\mathbf{L}} = \hat{\mathbf{r}} \times \hat{\mathbf{p}} = \hat{\mathbf{e}}_a \varepsilon_{abc} \hat{r} \hat{p}_c \ ,$$

and using space basis

$$\langle \mathbf{r} | \hat{\mathbf{L}} = \hat{\mathbf{e}}_a \underbrace{\left( - i \, \hbar \, \varepsilon_{abc}\, r_b \, \partial_c \langle \mathbf{r} | \right) }_{= \langle \mathbf{r} | \hat{L}_a }\ .$$

````{dropdown} Properties
:open:

**Composition of 2 components of the angular momentum operator.** Using Cartesian coordinates

$$\begin{aligned}
  \hat{L}_a \hat{L}_b 
  & = - \hbar^2 r_b \partial_a + \hbar^2 \delta_{ab} r_c \partial_c - \hbar^2 \varepsilon_{acd} \varepsilon_{bef} r_c r_e \partial_{df} = \\
\end{aligned}$$

```{dropdown} Details

$$\begin{aligned}
  \hat{L}_a \hat{L}_b 
  & = - \hbar^2 \varepsilon_{acd} r_c \partial_d \left( \varepsilon_{bef} r_e \partial_f \right) = \\
  & = - \hbar^2 \varepsilon_{acd} \varepsilon_{bef} r_c \left( \delta_{de} \partial_f + r_e \partial_{df} \right) = \\
  & = - \hbar^2 \varepsilon_{acd} \varepsilon_{bdf} r_c \partial_f - \hbar^2 \varepsilon_{acd} \varepsilon_{bdf} r_c r_e \partial_{df} = \\
  & = - \hbar^2 \left( \delta_{af} \delta_{cb} - \delta_{ab} \delta_{cf} \right) r_c \partial_f - \hbar^2 \varepsilon_{acd} \varepsilon_{bef} r_c r_e \partial_{df} = \\
  & = - \hbar^2 r_b \partial_a + \hbar^2 \delta_{ab} r_c \partial_c - \hbar^2 \varepsilon_{acd} \varepsilon_{bef} r_c r_e \partial_{df} = \\
\end{aligned}$$

The last term is symmetric w.r.t. $a$, $b$.

```

**Commutators.**

$$[ \hat{L}_a, \hat{L}_b ] = \hat{L}_a \hat{L}_b -  \hat{L}_b \hat{L}_a = - \hbar^2 ( r_b\partial_a - r_a \partial_b) $$

If $a = b$, the obvious result follows, as an operator commutes with itself. If $a \ne b$, 

$$[\hat{L}_a, \hat{L}_b ] = i \varepsilon_{abc} \hbar \hat{L}_c \ ,$$

or with a compact "vector notation", $\hat{\mathbf{L}} \times \hat{\mathbf{L}} = i \hbar \hat{\mathbf{L}}$.

**Magnitude of the angular momentum, $|\hat{L}|^2$.** Using Cartesian coordinates,

$$\begin{aligned}
  |\hat{L}|^2 
  & = 2 \hbar^2 r_a \partial_a - \hbar^2 r_b r_b \partial_{aa} + \hbar^2 r_a r_b \partial_{ab} \ .
\end{aligned}$$

```{dropdown} Details

$$\begin{aligned}
  |\hat{L}|^2 
  & = \hat{L}_x^2 + \hat{L}_y^2 + \hat{L}_z^2 = \\
  & = \hat{L}_a \hat{L}_a = \\
  & = -\hbar^2 r_a \partial_a + 3 \hbar^2 r_a \partial_a - \hbar^2 ( \delta_{ce} \delta_{df} - \delta_{cf} \delta_{de} ) r_c r_e \partial_{df} = \\
  & = 2 \hbar^2 r_a \partial_a - \hbar^2 r_b r_b \partial_{aa} + \hbar^2 r_a r_b \partial_{ab} \ .
\end{aligned}$$

```

**Commutations with magnitude.**

$$[ \hat{L}^2, \hat{L}_a ] = 0$$

```{dropdown} Details
:open:


```

The same hold for any integer power of $\hat{L}_a$, like $\hat{L}_a^2$, as it can be easily proved

$$\begin{aligned}
  \left[ \hat{L}^2, \hat{L}^2_a \right]
  & = \hat{L}^2 \hat{L}_a^2 - \hat{L}_a^2 \hat{L}^2 = \\
  & = \hat{L}^2 \hat{L}_a \hat{L}_a - \hat{L}_a^2 \hat{L}^2 = \\
  & = \hat{L}_a \hat{L}^2 \hat{L}_a - \hat{L}_a \hat{L}_a \hat{L}^2 = \\
  & = \hat{L}_a [ \hat{L}^2,  \hat{L}_a ] = 0  \ .
\end{aligned}$$

Analogous relations in **classical mechanics**

$$
  [ L_a, L_b ] = i \hbar \varepsilon_{abc} \hat{L}_c \qquad , \qquad \{ L_a, L_b \} = \varepsilon_{abc} L_c \\
$$

provides another example of the relation between Poisson brackets in classical mechanics and commutator in quantum mechanics (**Dirac**)

$$\{ A, B \} \quad \leftrightarrow \quad \frac{1}{i \hbar} [ \hat{A}, \hat{B} ]$$

````

## Eigenproblem of angular momentum operators

In this section, the eigenproblems of $\hat{L}^2$ and $\hat{L}_z$ are discussed. Here, all the operators and state functions are written in components using space basis, without explicitly writing the projection $\langle \mathbf{r} |$. 

* Using spherical coordinates, the $2\pi$-periodicity of the problem in $\phi$ implies quantization in the spectral decomposition of $\hat{L}_z$,
* 

```{dropdown} **$\langle \mathbf{r} | \hat{\mathbf{L}}\  $ using Cartesian coordinates.**

$$\ell \psi = \hat{L}_a \psi = - i \hbar \varepsilon_{abc} r_b \partial_c \psi \ , $$

or $\ell \psi = - i \hbar \mathbf{r} \times \nabla \psi$.

...

```

```{dropdown} **$\langle \mathbf{r} | \hat{\mathbf{L}}\  $ using spherical coordinates.**

With the set of spherical coordinates $\psi(r,\theta,\phi)$

$$\begin{aligned}
  \mathbf{r} \times \nabla \psi 
  & = \mathbf{r} \times \left[ \partial_r \psi \, \hat{\mathbf{r}}  + \frac{1}{r} \partial_\theta \psi \, \hat{\boldsymbol\theta} + \frac{1}{r \sin \theta} \partial_{\phi} \psi \hat{\boldsymbol\phi} \right] = \\
  & = \partial_\theta \psi \, \hat{\boldsymbol\phi} - \frac{1}{\sin \theta} \partial_\phi \psi \, \hat{\boldsymbol\theta} \ .
\end{aligned}$$

Thus the $z$-component, with $\hat{\mathbf{z}} \cdot \hat{\boldsymbol{\theta}} = - \sin \theta$, $\hat{\mathbf{z}} \cdot \hat{\boldsymbol\phi} = 0$, can be written as

$$\hat{\mathbf{z}} \cdot \left( \mathbf{r} \times \nabla \psi \right) = \partial_\phi \psi$$

```

```{dropdown} Spectral decomposition of the $z$-component operator, $\hat{L}_z$
:open:

$$\ell_z \psi_z(r,\theta,\phi) = -i \hbar \partial_\phi \psi_z(r,\theta,\phi)$$

The eigenfunctions read

$$\psi_{z,\ell}(r,\theta,\phi) = A(r,\theta) \, \exp\left( i \frac{\ell_z}{\hbar} \phi \right) \ .$$

Periodic condition $\psi_z(0) = \psi_z(2 \pi)$ implies $\frac{\ell_z}{\hbar} = m_l$, $m_l \in \mathbb{Z}$.

**Remark.** The constraint $m_l \in \mathbb{Z}$ is just **one of the constraints** on $m_l$.

In order to keep the notation as intuitive as possible, the eigenvalue $\ell_z$ and the corresponding eigenstate are denoted as $\{ L_{z}, | L_z \rangle\} = \{ \hbar m_l, | m_l \rangle \}$, s.t. $\hat{L}_z | m_l \rangle = \hbar m_l | m_l \rangle$.

```

```{dropdown} Spectral decomposition of commuting operators
:open:

Let $\hat{A} | a \rangle = a | a \rangle$, and $\hat{B} | b \rangle = b | b \rangle$. If $0 = [ \hat{A}, \hat{B} ] = \hat{A} \hat{B} - \hat{B} \hat{A}$. Pre-multiplying the first one by $\hat{B}$,

$$a \hat{B} | a \rangle = \hat{B} \hat{A} | a \rangle = \hat{A} \hat{B} | a \rangle \ .$$

So that $\hat{B} | a \rangle$ is an eigenstate of $\hat{A}$ with eigenvalue $a$.

* If $a$ is an eigenvalue with algebraic multiplicity equal to $1$, then $\hat{B} | a \rangle$ must be proportional to the only eigenstate $| a \rangle $ of the operator $\hat{A}$ with eigenvalue $a$, i.e.

   $$\hat{B} | a \rangle = \mu | a \rangle \ ,$$

   and thus $| a \rangle$ is also an eigenstate of $\hat{B}$.

* If $a$ has algebraic multiplicity larger than $1$, then $\hat{B} | a_i \rangle$, can be a linear combination of all the eigenvectors $| a_k \rangle$ with eigenvalues $a_k = a$,

   $$\hat{B} | a_i \rangle = c_{ik} | a_k \rangle  \ ,$$

   for $\forall i$.

   ...

<!--
   If $\langle a_i | a_k \rangle = \delta_{ik}$,

   $$c_{il} = \langle a_l | c_{ik} | a_k \rangle = \langle a_l | \hat{B} | a_i \rangle = \frac{1}{a} \langle a_l | \hat{B} | \hat{A} | a_i \rangle$$
-->


```



```{dropdown} Relation between $\ \hat{L}_z\ $ and $\ \hat{L}^2 \$
:open:

$$\hat{L}^2 = \hat{L}_x^2 + \hat{L}_y^2 + \hat{L}_z^2$$

As $\hat{L}^2$ commutes with the Cartesian components $\hat{L}_a$, they share the same eigenvalues.The same holds for $\hat{L}_a^2$

$$\begin{aligned}
  \hat{L}^2 = \hat{L}_x^2 + \hat{L}_y^2 + \hat{L}_z^2  \ ,
\end{aligned}$$

implies

$$\begin{aligned}
  \hat{L}^2 - \hat{L}_z^2 = \hat{L}_x^2 + \hat{L}_y^2  \ .
\end{aligned}$$

Let $\psi$ an eigenstate of $\hat{L}^2$, $\hat{L}_z$ with eigenvalues $\ell^2$, $\ell_z$, it follows

$$\left( \hat{L}_x^2 + \hat{L}_y^2 \right) \psi = \left( \hat{L}^2 - \hat{L}_z^2 \right) \psi = \left( \ell^2 - \ell_z^2 \right) \psi$$

As $( \ell^2 -  \ell_z^2 ) | \psi |^2 = \psi^* \hat{L}^2_x \psi = | \hat{L}_x \psi |^2 \ge 0$, it follows that $\ell^2 - \ell^2_z \ge 0$, and thus $-\ell \le \ell_z \le \ell$.

Combining 

$$\begin{aligned}
  \left[\hat{L}_y, \hat{L}_z \right] & = \hat{L}_y \hat{L}_z - \hat{L}_z \hat{L}_y = i \hbar \hat{L}_x \\
  \left[\hat{L}_z, \hat{L}_x \right] & = \hat{L}_z \hat{L}_x - \hat{L}_x \hat{L}_z = i \hbar \hat{L}_y
\end{aligned}$$

summing and subtracting $i (1)$ and $(2)$ them

$$\begin{aligned}
 0
 & = - \hbar \hat{L}_x \mp i \hbar \hat{L}_y - i \hat{L}_y \hat{L}_z + i \hat{L}_z \hat{L}_y \pm \hat{L}_z \hat{L}_x \mp \hat{L}_x \hat{L}_z = \\
 & = - ( \hat{L}_x \pm i \hat{L}_y ) ( \hbar \pm \hat{L}_z ) + \hat{L}_z ( i \hat{L}_y \pm \hat{L}_x ) \ ,
\end{aligned}$$

and thus

$$\hat{L}_z ( i \hat{L}_y \pm \hat{L}_x ) = ( \hat{L}_x \pm i \hat{L}_y ) ( \hbar \pm \hat{L}_z )$$

or

$$\hat{L}_z ( \hat{L}_x \pm i \hat{L}_x ) = ( \hat{L}_x \pm i \hat{L}_y ) ( \hat{L}_z \pm \hbar )$$

Applying this operator to the eigenstate $\psi$

$$\hat{L}_z ( \hat{L}_x \pm i \hat{L}_y ) \psi = ( \hat{L}_x \pm i \hat{L}_y ) ( \hat{L}_z \pm \hbar ) \psi = ( \ell_z \pm \hbar ) ( \hat{L}_x \pm i \hat{L}_y ) \psi$$ (eq:ang-mom:ladder:application)


Thus, the state functions $\psi^{\pm} = \left( \hat{L}_x \pm i \hat{L}_y \right) \psi$ are eigenstates of the operator $\hat{L}_z$ with eigenvalues $\ell_z \pm \hbar$. As $\ell_z \in [ - \ell, \ell ]$, let's call $\ell_{z,min}$ and $\ell_{z,max}$ the minimum and maximum values of $\ell_z$. It follows that the operator $\hat{L}^-$ has the smallest eigenvalue equal to $\ell_{z,min} - \hbar$ and $\hat{L}^+$ has the largest eigenvalue equal to $\ell_{max,z} + \hbar$.

Thus, for $\ell_{z,min}$, $\ell_z - \hbar$ can't be an eigenvalue of $\hat{L}_z$, and thus the relation 

$$\hat{L}_z \left( \hat{L}_x - i \hat{L}_y \right) \psi = ( \ell_{z,min} - \hbar ) ( \hat{L}_x - i \hat{L}_y ) \psi$$

implies that $( \hat{L}_x - i \hat{L}_y ) \psi$ can't be an eigenfunction of $\hat{L}_z$, and thus it must be in the kernel or $\hat{L}_z$, i.e.

$$0 = \hat{L}_z ( \hat{L}_x - i \hat{L}_y ) \psi_{\ell_z,min} = ( \hat{L}_x - i \hat{L}_y ) ( \hat{L}_z + \hbar ) \psi_{\ell_z,min} = ( \ell_{z,min} + \hbar ) ( \hat{L}_x - i \hat{L}_y ) \psi_{\ell,min}$$

A similar relation holds for the largest eigenvalue

$$0 = \hat{L}_z ( \hat{L}_x + i \hat{L}_y ) \psi_{\ell_z,max} = ( \hat{L}_x + i \hat{L}_y ) ( \hat{L}_z - \hbar ) \psi_{\ell_z,max} = ( \ell_{z,max} - \hbar ) ( \hat{L}_x + i \hat{L}_y ) \psi_{\ell,max}$$

Applying $\hat{L}_x + i \hat{L}_y$ to the first equation, the operator becomes

$$( \hat{L}_x + i \hat{L}_y ) ( \hat{L}_x - i \hat{L}_y ) = \hat{L}_x^2 + \hat{L}_y^2 - i [ \hat{L}_x, \hat{L}_y ]  = \hat{L}^2 - \hat{L}_z^2 + \hbar \hat{L}_z \ .$$

Applying $\hat{L}_x - i \hat{L}_y$ to the second equation, the operator becomes

$$( \hat{L}_x - i \hat{L}_y ) ( \hat{L}_x + i \hat{L}_y ) = \hat{L}_x^2 + \hat{L}_y^2 + i [ \hat{L}_x, \hat{L}_y ]  = \hat{L}^2 - \hat{L}_z^2 - \hbar \hat{L}_z \ .$$

Thus, the 2 equations are, for a given value of $\ell$

$$\begin{aligned}
  0 & = ( \ell_{z,min} + \hbar ) ( \ell^2 - \ell_{z,min}^2 + \hbar \ell_{z,min} ) \\ 
  0 & = ( \ell_{z,max} - \hbar ) ( \ell^2 - \ell_{z,max}^2 - \hbar \ell_{z,max} ) \\ 
\end{aligned}$$

Either $\ell_{z;min,max} = \mp \hbar$, or

$$\begin{aligned}
 0 & = \ell^2 - \ell_{z,min}^2 + \hbar \ell_{z,min}  \\
 0 & = \ell^2 - \ell_{z,max}^2 - \hbar \ell_{z,max} \ ,
\end{aligned}$$

and subtracting $0 = (\ell_{z,max} + \ell_{z,min})(\ell_{z,max} - \ell_{z,min} + \hbar )$. As the content of the second bracket is always positive, then $\ell_{z,min} = - \ell_{z,max}$.

---

Following {eq}`eq:ang-mom:ladder:application`, if $| \psi \rangle$ is the eigenvector of $\hat{L}_z$ with eigenvalue $\ell_z$, the wave functions $\hat{L}^{\mp} | \psi \rangle$ are eigenvectors of $\hat{L}_z$ with eigenvalues $\ell_z \mp \hbar$. Thus, the set 

$$\{ \ell_{z,min}, \ell_{z,min} + \hbar, \ell_{z,min} + 2 \hbar, \dots, \ell_{z,max}-\hbar, \ell_{z,max} \} = \{ - m_{l,max} \hbar, \dots , m_{l,max} \hbar \} $$

contains possible values of the eigenvalues of $\hat{L}_z$.


---

$$\lambda\left(L_z\right) = \hbar m_l \qquad m_l \in $$

Now, for $\ell_{z,min} = -m_{l,max} \hbar$, and $\ell_{z,max} = m_{l,max} \hbar$, the corresponding eigenvalues $\ell^2$ are

$$\begin{aligned}
  \ell^2 = \hbar^2 m_{l,max} \left( m_{l,max} + 1 \right) \ .
\end{aligned}$$


<!--

From the composition,

$$( \hat{L}_x + i \hat{L}_y ) ( \hat{L}_x - i \hat{L}_y ) =$$

it follows that this tha operator $\hat{L}^+ \hat{L}^-$ has eigenvalues $\ell^2 - \ell_z^2 + \hbar \ell_z = \ell^2 - \ell_z ( \ell_z - \hbar )$.

Putting together the relations about the eigenvalues of the operators 

$$\ell_z^2 - \hbar^2 = \ell^2 - \ell_z^2 + \ell_z \hbar \ .$$

-->



```
