(relativity-special:em)=
# Electromagnetism

**From 3-dimensional to 4-dimensional formalism.** In this section the 4-dimensional formalism is introduced, and the 4-dimensional version of governing equations of electromagnetism that naturally suits special relativity theory is derived starting from the governing equations of [classical electromagnetism]().

```{dropdown} Definition of physical quantities
  - 4-potential vector, $\mathbf{A} = \frac{\phi}{c} \mathbf{E}_0 + a^i \mathbf{E}_i$
  - 4-current vector, $\mathbf{J} = c \rho \mathbf{E}_0 + j^i \mathbf{E}_i$
  - EM field tensor,

    $$\begin{aligned}
      \mathbf{F} & = - \mathbf{E}_0 \otimes \mathbf{E}_i \dfrac{e_i}{c} + \dfrac{e_i}{c} \mathbf{E}_i \otimes \mathbf{E}_0 + \varepsilon_{ijk} b_j \mathbf{E}_i \otimes \mathbf{E}_k \\
      \mathbf{D} & = - \mathbf{E}_0 \otimes \mathbf{E}_i c d_i + d_i \mathbf{E}_i \otimes \mathbf{E}_0 + \varepsilon_{ijk} h_j \mathbf{E}_i \otimes \mathbf{E}_k \\
    \end{aligned}$$

    or

    $$\begin{aligned}
      \left[F^{\alpha \beta}\right] = \begin{bmatrix} 0 & - \mathbf{e}^T / c \\ \mathbf{e}/c & \mathbf{b}_{\times}  \end{bmatrix}  \qquad , \qquad
      \left[D^{\alpha \beta}\right] = \begin{bmatrix} 0 & - c \mathbf{d}^T   \\ c \mathbf{d} & \mathbf{h}_{\times}  \end{bmatrix}  \\
    \end{aligned}$$

  - 4-momentum-energy density tensor, $\mathbf{T}$
```

```{dropdown} Definitions, relations and equations

  - Lorentz's gauge, $\nabla \cdot \mathbf{A} = 0$
  - EM field tensor, $\mathbf{F} = \nabla \mathbf{A} - \left( \nabla \mathbf{A} \right)^T$
  - 4-current continuity equation, $\nabla \cdot \mathbf{J} = 0$ 
  - Maxwell's equations

    $$\begin{aligned}
      \mathbf{\nabla} \cdot \mathbf{D} & = \mathbf{J}^f \\
      \nabla \cdot \left( \symbf{\epsilon} : \mathbf{F} \right) & = \mathbf{0}
    \end{aligned}$$

  - Constitutive equations

    $$\mathbf{D} = \dfrac{1}{\mu_0} \mathbf{F} + \mathbf{P}$$

  - Wave equation for the pontential (what about wave equations for the EM field?)

    $$\nabla \cdot \nabla \mathbf{A} = \mu_0 \mathbf{J}$$

  - Energy balance equation

    $$\nabla \cdot \mathbf{T} = - \mathbf{F} \cdot \mathbf{J}$$

  - Equation of motion of a point charge in a EM field,

    $$m \mathbf{X}'' = q \mathbf{F} \cdot \mathbf{X}'$$
```

**Einstein's special relativity and Lorentz's transformations for the EM quantities.** After the equations are derived, Lorentz's transformations are used to discuss special relativity. Low-speed relations, used in classical electromagnetism for systems with charateristic speed $v \ll c$, are derived.

**Lagrangian approach to electromagnetism in special relativity.** Weak form of the equations are derived, and the Lagrangian approach to electromagnetism in special relativity is discussed: both field equations and dynamical equations of charges moving in an electromagnetic field are re-derived with a Lagrangian approach.
