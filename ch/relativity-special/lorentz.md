(relativity-special:lorentz)=
# Inertial reference frames and Lorentz's transformations

Equations of physics as seen by inertial reference frames (**todo** *but what's an inertial reference frame?*) have the same expressions. Change of observer can be related to change of coordinates (and choice of basis vectors, in special relativity) used to describe a physical phenomenon, that is invariant to this change for its very nature: reality doesn't change if observed from different point of view (if observations don't interact with reality itself, at least). Proper mathematical tools for dealing with invariance are vectors and tensors in general.

Using 2 different sets of coordinates associated with constant and uniform basis vectors $\mathbf{E}_{\alpha}$, $\mathbf{E}'_{\beta}$ a vector can be written as

$$\mathbf{V} = V^{\alpha} \mathbf{E}_{\alpha} = V^{'\beta} \mathbf{E}'_{\beta} \ . $$

Lorentz transformation describe the change of description between two inertial reference frames.

(relativity-special:lorentz:transformation)=
## Lorentz's transformations

(relativity-special:lorentz:transformation:std)=
### Lorentz's transformations in standard configuration

Standard configuration is defined for two observers with Cartesian bases for the space components, with the axes aligned, and with relative motion along $x$, $x'$ axes.

...**todo** *derivation...see material for [high school](): [Special Relativity](https://basics2022.github.io/bbooks-physics-hs/ch/modern/einstein-special.html#relativita-speciale):[Relativity and Lorentz's transformations](https://basics2022.github.io/bbooks-physics-hs/ch/modern/einstein-special.html#relativita-e-trasformazioni-di-lorentz)*

$$\begin{aligned}
  ct' & = \gamma ( ct - v x ) \\
   x' & = \gamma ( - v ct + x) \\
   y' & = y         \\
   z' & = z         \\
\end{aligned} \ ,$$

with $\gamma := \dfrac{1}{\sqrt{1 - v^2}}$, so that the coordinates transformations can be written using matrix of change of coordinates

$$\begin{aligned}
  \begin{bmatrix} ct' \\ x' \\ y' \\ z'  \end{bmatrix} & = \begin{bmatrix} \gamma & - \gamma v & 0 & 0 \\ - \gamma v & \gamma & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 1  \end{bmatrix} \begin{bmatrix} ct \\ x \\ y \\ z \end{bmatrix} \\ \\
  X^{'\alpha} & = \Lambda_{\beta}^{\alpha} X^{\beta}  \ .
\end{aligned}$$

This is the same transformation of the components of all the vectors of the 4-dimensional space as seen by two different inertial observers

(relativity-special:lorentz:transformation:general)=
### Lorentz's transformation in general configuration

Beside change of origin of the coordinates, general transformation can be derived composing Lorentz's transformations in stanrdard configuration (the only one derived so far), and rotations of the space coordinates.

As an example, the general expression of Lorentz's transformation between two inertial reference frames with general relative (space) velocity $\vec{v}$ - and aligned axes - can be derived introducing two intermediate inertial reference frames: reference $Otxyz$ and $O't'x'y'z'$ are the two refence frames we'd like to link with a Lorentz transformation; $O_a t_a x_a y_a z_a$ is a reference frame at rest w.r.t. $Otxyz$ with the $x_a$ axis with the same direction of the relative (space) velocity $\vec{v}$, $O_b t_b x_b y_a z_b$ is in standard configuration with $O_a$. The transformation of coordinates reads

$$\begin{aligned}
  \begin{bmatrix} x'_0 \\ \mathbf{r}' \end{bmatrix}
  & = \begin{bmatrix} 1 & \mathbf{0}^T \\ \mathbf{0} & \mathbf{R}^T \end{bmatrix} \begin{bmatrix} x_{b,0} \\ \mathbf{x}_b \end{bmatrix} = \\
  & = \begin{bmatrix} 1 & \mathbf{0}^T \\ \mathbf{0} & \mathbf{R}^T \end{bmatrix} \begin{bmatrix} \gamma & - \gamma v & & \\ - \gamma v & \gamma & & \\ & & 1 & \\ & & & 1 \end{bmatrix} \begin{bmatrix} x_{a,0} \\ \mathbf{x}_a \end{bmatrix}   = \\
  & = \begin{bmatrix} 1 & \mathbf{0}^T \\ \mathbf{0} & \mathbf{R}^T \end{bmatrix} \left(  \begin{bmatrix} \gamma & - \gamma v & & \\ - \gamma v & \gamma - 1 & & \\ & & 0 &  \\ & & &  0 \end{bmatrix} + \begin{bmatrix} 0 & & & \\ & 1 & & \\ & & 1 & \\ & & & 1 \end{bmatrix} \right) \begin{bmatrix} 1 & \mathbf{0}^T \\ \mathbf{0} & \mathbf{R} \end{bmatrix}  \begin{bmatrix} x_{0} \\ \mathbf{x} \end{bmatrix} \ ,
\end{aligned}$$

and the two contributions give

$$\begin{aligned}
 \begin{bmatrix} 1 & \mathbf{0}^T \\ \mathbf{0} & \mathbf{R}^T \end{bmatrix}  \begin{bmatrix} \gamma & - \gamma v & & \\ - \gamma v & \gamma - 1 & & \\ & & 0 &  \\ & & &  0 \end{bmatrix} \begin{bmatrix} 1 & \mathbf{0}^T \\ \mathbf{0} & \mathbf{R} \end{bmatrix}
 & = \begin{bmatrix} 1 & \mathbf{0}^T \\ \mathbf{0} & \mathbf{R}^T \end{bmatrix} \begin{bmatrix} \gamma & - \gamma v \mathbf{R}_{1,:} \\ - \gamma v & (\gamma-1)\mathbf{R}_{1,:} \\ \mathbf{0}_{2,1} & \mathbf{0}_{2,4} \end{bmatrix} = \\
 & = \begin{bmatrix} \gamma & - \gamma v \mathbf{R}_{1,:} \\ - \gamma v \mathbf{R}_{1,:}^T & (\gamma-1)  \mathbf{R}_{1,:}^T \mathbf{R}_{1,:} \end{bmatrix} = \\
 & = \begin{bmatrix} \gamma & - \gamma R_{11} v & - \gamma R_{12} v & - \gamma R_{13} v \\
   - \gamma R_{11} v & (\gamma-1) R_{11} R_{11} &  (\gamma-1) R_{11} R_{12} &  (\gamma-1) R_{11} R_{13} \\
   - \gamma R_{12} v & (\gamma-1) R_{12} R_{11} &  (\gamma-1) R_{12} R_{12} &  (\gamma-1) R_{12} R_{13} \\
   - \gamma R_{13} v & (\gamma-1) R_{13} R_{11} &  (\gamma-1) R_{13} R_{12} &  (\gamma-1) R_{13} R_{13} \\
\end{bmatrix} \ .
\end{aligned}$$

$$\begin{bmatrix} 1 & \mathbf{0}^T \\ \mathbf{0} & \mathbf{R}^T \end{bmatrix}  \begin{bmatrix} 0 & \\ & \mathbf{I}_3  \end{bmatrix} \begin{bmatrix} 1 & \mathbf{0}^T \\ \mathbf{0} & \mathbf{R} \end{bmatrix} = \begin{bmatrix} 0 & \\ & \mathbf{I}_3 \end{bmatrix}$$

Here, components $(R_{11} v, R_{12} v, R_{13} v)$ are the components of velocity $\vec{v}$ as seen by observer $O$, and thus the matrix for coordinate transformation reads

$$\begin{aligned}
  \symbf{\Lambda}
  & = \begin{bmatrix} 0 & \\ & \mathbf{I}_3 \end{bmatrix} + \begin{bmatrix} \gamma & - \gamma \mathbf{v}^T \\ -\gamma \mathbf{v} & (\gamma-1) \mathbf{\hat{v}}\mathbf{\hat{v}}^T \end{bmatrix} = \\
  & = \begin{bmatrix} \gamma & - \gamma \mathbf{v}^T \\ -\gamma \mathbf{v} & \mathbf{I}_3 + (\gamma-1) \mathbf{\hat{v}}\mathbf{\hat{v}}^T  \end{bmatrix}
\end{aligned}$$ (lorentz:transformations:general:matrix)

and the transformation of coordinates can be written as

$$\begin{cases} 
  c t'     & = \gamma ( ct - \vec{v} \cdot \vec{r} )  \\
  \vec{r}' & = - \gamma c t \vec{v} + (\gamma-1) \, \hat{v} \otimes \hat{v} \cdot \vec{r} + \vec{r} = \\
           & = - \gamma c t \vec{v} + \underbrace{\left[ \mathbb{I} - \hat{v} \otimes \hat{v} \right]}_{\mathbb{P}_{\perp\hat{v}}} \cdot \vec{r} + \gamma \, \underbrace{\hat{v} \otimes \hat{v}}_{\mathbb{P}_{\parallel\hat{v}}}  \cdot \vec{r} \ ,
\end{cases}$$ (lorentz:transformations:general:time-space)

having introduced the two orthogonal projectors in directions parallel and orthogonal to the direction of the velocity, $\hat{v}$.

```{prf:example} Standard configuration, as a special case.

If $\vec{v} = v \hat{x}$, Lorentz's transformation for two inertial observers in starndard configuration is retrieved from the general expression of Lorentz's transformation

$$\begin{cases}
  c t' & = \gamma(ct - v x) \\
  \vec{r}' & = -\gamma v ct \hat{x} + y \hat{y} + z \hat{z} + \gamma v x \hat{x}
\end{cases}$$

```

## Transformation of vector components and vectors of the bases

$$\mathbf{V} = V^{\alpha} \mathbf{E}_{\alpha} = V^{'\beta} \mathbf{E}'_{\beta}$$

$$V^{'\beta} = \Lambda_{\alpha}^{\beta} V^{\alpha} \ ,$$

being $\alpha$ and $\beta$ the indice of columns and rows of matrix $\symbf{\Lambda}$ of change of coordinates of the general Lorentz's transformation {eq}`lorentz:transformations:general:matrix`. In order to keep invariance, vectors of the bases transform with the transpose transformation, namely

$$\mathbf{V} = V^{\alpha} \mathbf{E}_{\alpha} = V^{'\beta} \mathbf{E}'_{\beta} =  V^{\alpha} \underbrace{\Lambda_{\alpha}^{\beta}  \mathbf{E}'_{\beta}}_{\mathbf{E}_{\alpha}}$$

$$\mathbf{E}_{\alpha} = \Lambda_{\alpha}^{\beta}  \mathbf{E}'_{\beta} \ .$$ (vector:transformation:bases)

$$\begin{aligned}
  \left[ \Lambda^{-1} \right]^{\alpha}_{\phi}\mathbf{E}_{\alpha} = \underbrace{[\Lambda^{-1}]^{\alpha}_{\phi} \Lambda_{\alpha}^{\beta}}_{= \delta_{\phi}^{\beta}}  \mathbf{E}'_{\beta} \\
\end{aligned}$$

## Transformation of tensor components

$$\mathbf{D} = D^{\alpha \beta} \mathbf{E}_{\alpha} \mathbf{E}_{\beta} = D^{'\phi \eta} \mathbf{E}'_{\phi} \mathbf{E}'_{\eta} = $$

and using the rule of transformation of vectors of the bases {eq}`vector:transformation:bases`

$$D^{' \phi \eta} = D^{\alpha \beta} \Lambda^{\phi}_{\alpha} \Lambda^{\eta}_{\beta} \ ,$$

or using matrix notation (**todo** *avoid abuse of notation! Use underline for arrays of coomponents, bold for vectors and tensors*)

$$\mathbf{D}' = \symbf{\Lambda} \mathbf{D} \symbf{\Lambda}^T$$

```{prf:example} Electromagnetic field tensor

Contravariant components of the electromagnetic field tensor

$$\begin{aligned}
  \begin{bmatrix} 0 & - c \mathbf{d}'^T \\ c \mathbf{d}' & \mathbf{h}'_{\times} \end{bmatrix} 
  & = \begin{bmatrix} \gamma & - \gamma \mathbf{v}^T \\ -\gamma \mathbf{v} & \mathbf{I}_3 + (\gamma-1) \mathbf{\hat{v}}\mathbf{\hat{v}}^T  \end{bmatrix} \begin{bmatrix} 0 & - c \mathbf{d}^T \\ c \mathbf{d} & \mathbf{h}_{\times}\end{bmatrix} \begin{bmatrix} \gamma & - \gamma \mathbf{v}^T \\ -\gamma \mathbf{v} & \mathbf{I}_3 + (\gamma-1) \mathbf{\hat{v}}\mathbf{\hat{v}}^T \end{bmatrix}^T = \\
  & = \begin{bmatrix} \gamma & - \gamma \mathbf{v}^T \\ -\gamma \mathbf{v} & \mathbf{I}_3 + (\gamma-1) \mathbf{\hat{v}}\mathbf{\hat{v}}^T  \end{bmatrix} \begin{bmatrix} \gamma c v d_v & - c \mathbf{d}^T - (\gamma-1) c d_v \hat{\mathbf{v}}^T \\ \gamma c \mathbf{d} - \gamma \mathbf{h}_\times \mathbf{v} & -\gamma c \mathbf{d} \mathbf{v}^T + \mathbf{h}_\times + (\gamma-1) \mathbf{h}_\times \mathbf{\hat{v}} \mathbf{\hat{v}}^T \end{bmatrix} = \\
  & = \begin{bmatrix} 0 & \text{anti-sym} \\ c \mathbf{d}' & \mathbf{h}'_{\times} \end{bmatrix} = \\
\end{aligned}$$

with

$$\begin{aligned}
  c \mathbf{d}'
  & = - \gamma^2 c v^2 \mathbf{\hat{v}} d_v + \gamma c \mathbf{d} - \gamma \mathbf{h}_\times \mathbf{v} + \gamma(\gamma-1) c \hat{\mathbf{v}}d_v
  = \\
  & = c \gamma^2 \hat{\mathbf{v}} d_v \underbrace{(1 - v^2)}_{= \gamma^{-2}} + \gamma c \mathbf{d} - \gamma \mathbf{h} \times \mathbf{v} - \gamma c \hat{\mathbf{v}} d_v = \\
  & = \gamma c \mathbf{d} - \gamma \mathbf{h} \times \mathbf{v} + ( 1 - \gamma ) c \hat{\mathbf{v}} \hat{\mathbf{v}} \cdot \mathbf{d} \ ,
\end{aligned}$$

and

$$\begin{aligned}
  \mathbf{h}'_{\times} & = && (1) \\
  & = \gamma c v \hat{\mathbf{v}} \mathbf{d}^T + \gamma (\gamma - 1) c v d_v \hat{\mathbf{v}} \hat{\mathbf{v}}^T + \\
  & - \gamma c v \mathbf{d} \hat{\mathbf{v}} + \mathbf{h}_{\times} + (\gamma - 1) (\mathbf{h} \times \hat{\mathbf{v}}) \hat{\mathbf{v}}^T - \gamma (\gamma - 1) c v d_v \hat{\mathbf{v}} \hat{\mathbf{v}}^T + (\gamma-1) \hat{\mathbf{v}} \mathbf{v}^T \mathbf{h}_{\times} + \mathbf{0} = && (2) \\
  & = \gamma c v \left( \hat{\mathbf{v}} \mathbf{d}^T - \mathbf{d} \hat{\mathbf{v}}^T \right) + \mathbf{h}_{\times} + (\gamma-1) \left( \left( \mathbf{h}_\times \hat{\mathbf{v}}  \right) \hat{\mathbf{v}}^T  - \hat{\mathbf{v}} \left( \mathbf{h}_\times \hat{\mathbf{v}}\right)^T \right) = && (3) \\
  & = \gamma c v \left( \mathbf{d} \times \hat{\mathbf{v}} \right)_{\times} + \mathbf{h}_{\times} + (\gamma-1) \left( \hat{\mathbf{v}} \times (\mathbf{h} \times \hat{\mathbf{v}}) \right)_{\times}
\end{aligned}$$

having (1) recognized that $\hat{\mathbf{v}} \hat{\mathbf{v}}^T \mathbf{h}_\times \hat{\mathbf{v}} \hat{\mathbf{v}}^T = \hat{\mathbf{v}}( \hat{\mathbf{v}} \cdot ( \mathbf{h} \times \hat{\mathbf{v}}) ) \hat{\mathbf{v}} = \mathbf{0}$, (2) $\{ \mathbf{v}^T \mathbf{h}_{\times} \}_k = v_i \varepsilon_{ijk} h_j = - \{ \mathbf{h}\times \hat{\mathbf{v}} \}_k$ and (3)

$$\begin{aligned}
  \left[ \left(\mathbf{a}_{\times} \mathbf{b} \right)_{\times} \right]_{ij} 
  & = \varepsilon_{ikj} \varepsilon_{klm} a_l b_m = \\
  & = \left( \delta_{jl} \delta_{im} - \delta_{jm} \delta_{il} \right) a_l b_m = \\
  & = a_j b_i - a_i b_j = \left[ \mathbf{b} \mathbf{a}^T - \mathbf{a} \mathbf{b}^T \right]_{ij} \ . 
\end{aligned}$$

Thus 

$$\begin{aligned}
\mathbf{h}' 
  & = \mathbf{h} - \gamma c \mathbf{v} \times \mathbf{d} + (1 -\gamma) (\mathbf{h} \times \hat{\mathbf{v}}) \times \hat{\mathbf{v}} = \\
  & = \mathbf{h} - \gamma c \mathbf{v} \times \mathbf{d} + (1 -\gamma) \left( \hat{\mathbf{v}} \hat{\mathbf{v}} \cdot \mathbf{h} - \mathbf{h}  \right) = \\
  & = \gamma \mathbf{h} - \gamma c \mathbf{v} \times \mathbf{d} + (1 -\gamma) \hat{\mathbf{v}} \hat{\mathbf{v}} \cdot \mathbf{h} \ .
\end{aligned}$$

Going back from non dimensional velocity to dimensional velocity $c \mathbf{v} \rightarrow \mathbf{v}$,

$$\begin{aligned}
  \mathbf{d}' & = \gamma \left( \mathbf{d} - \dfrac{\mathbf{h} \times \mathbf{v}}{c^2} \right) + (1-\gamma) \hat{\mathbf{v}} \, \hat{\mathbf{v}} \cdot \mathbf{d} \\
  \mathbf{h}' & = \gamma \left( \mathbf{h} - \mathbf{v} \times \mathbf{d} \right) + (1 - \gamma) \hat{\mathbf{v}} \, \hat{\mathbf{v}} \cdot \mathbf{h} \\
\end{aligned}$$

Repeating the same process for the electromagnetic field tensor

$$\begin{aligned}
  \left[\mathbf{F}\right]^{\alpha \beta} = \begin{bmatrix} 0 & - \dfrac{\mathbf{e}^T}{c} \\ \dfrac{\mathbf{e}}{c} & \mathbf{b}_{\times} \end{bmatrix} 
\end{aligned}$$

$$\begin{aligned}
  \mathbf{e}' & = \gamma \left( \mathbf{e} -        \mathbf{b} \times \mathbf{v}       \right) + (1-\gamma) \hat{\mathbf{v}} \, \hat{\mathbf{v}} \cdot \mathbf{e} \\
  \mathbf{b}' & = \gamma \left( \mathbf{b} - \dfrac{\mathbf{v} \times \mathbf{e}}{c^2} \right) + (1 - \gamma) \hat{\mathbf{v}} \, \hat{\mathbf{v}} \cdot \mathbf{b} \\
\end{aligned}$$



```

```{prf:example} 4-Current

$$\mathbf{J}' = \symbf{\Lambda} \mathbf{J}$$

$$\begin{aligned}
  c \rho' & = \gamma c \rho - \gamma v \mathbf{j} \\
  \mathbf{j}' & = - \gamma v c \rho + \gamma \mathbf{j} 
\end{aligned}$$

```

```{prf:example} Constitutive equations

Linear isotropic medium

$$\begin{aligned}
  \mathbf{d} & = \varepsilon_0 \mathbf{e} + \mathbf{p} \\
  \mathbf{b} & = \mu_0 \mathbf{h} + \mu_0 \mathbf{m} \\
\end{aligned}$$

with $c^2 = \dfrac{1}{\varepsilon_0 \mu_0}$


$$\begin{aligned}
  c \mathbf{d} & = \varepsilon_0 c^2 \dfrac{\mathbf{e}}{c} + c \mathbf{p} = \dfrac{1}{\mu_0} \dfrac{\mathbf{e}}{c} + c \mathbf{p} \\
  \mathbf{h} & = \dfrac{1}{ \mu_0} \mathbf{b} - \mathbf{m} \\
\end{aligned}$$

the constitutive equations can be written in 4-dimensional form as

$$\mathbf{D} = \dfrac{1}{\mu_0} \mathbf{F} + \mathbf{P}$$

$$
                 \begin{bmatrix} 0 & - c \mathbf{d}^T  \\ c \mathbf{d} &  \mathbf{h}_{\times} \end{bmatrix} = 
\dfrac{1}{\mu_0} \begin{bmatrix} 0 & -\mathbf{e}^T / c \\ \mathbf{e}/c &  \mathbf{b}_{\times} \end{bmatrix} + 
                 \begin{bmatrix} 0 & - c \mathbf{p}^T  \\ c \mathbf{p} & -\mathbf{m}_{\times} \end{bmatrix}
$$


```
