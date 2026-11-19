(relativity-general:intro)=
# General Relativity



````{dropdown} Draft of the introduction
:open:

**What's general relativity?** A geometric theory of gravitation: gravitation is an evidence of bending of spacetime.

```{admonition} GR in summary

GR can be viewed as a geometric theory of gravitation, describing the coupling between mass-energy and spacetime:
* how mass (and energy-momentum in general) deforms the spacetime, summarized in [Einstein field equations](relativity-general:notes:einstein-equation)
* how bodies and radiation (both massive and mass-less entities) move in a non-flat spacetime, along [geodesics](general-relativity:geodesics)

```

**What's not ok with Newton gravitation model?** From the mathematical point of view, Newton gravitation is modeled as an instantaneous action at distance, and this is incompatible with the principles of special relativity: no information can travel in space faster than the speed of light $c$ in vacuum - or, there's a finite maximum velocity of information through space.

```{admonition} Instantaneous action at distance in classical mechanics

In classical mechanics,[^basics-cm-gravitation] the force at distance can be written as the spatial gradient of the gravitational potential $\phi(\vec{r}, t)$, governed by Poisson equation

$$-\nabla^2 \phi(\vec{r},t) = 4 \pi G \rho( \vec{r}, t) \ ,$$

being $G$ the universal constant of gravitation, and $\rho( \vec{r}, t)$ the mass density in space. This equation, and the resulting gravitational force acting on a point mass $P$ with mass $m_P$, $\vec{F}_P(t) = m_P \nabla \phi( \vec{r}_P, t)$ shows no time delay between the causes and the effects, being everything at time $t$. The absence of a time differential operator or a time delay - and the presence of the Laplacian operator - is the mathematical manifestation of instantaneouos action at distance: a change in $\rho(\vec{r},t)$ in $\vec{r}_0$ causes an immediate change in $\phi(\vec{r},t)$ in all the points of the domain, and it's measurable at least in a neighborhood of th point $\vec{r}_0$.

GR model: the geometric counterpart of the gravitational potential is forced by  mass-energy-momentum (tensor). The equations must not contain any instantaneous action at distance, and must be compatible with the principles of special relativity. This can be observed in the [linearized Einstein field equation](relativity-general:notes:einstein-equation:linearization), a wave function for the perturbation of the metric tensor, forced by perturbation in the mass-energy-momentum tensor, with the light speed $c$ as the characteristic speed.

```

**What Newton gravitation can't model accurately?** The first experimental verifications of GR were an accurate description of the bending of a light ray around a massive object (Eddington, 1919), the precession of the perihelion of Mercury. Other experimental tests followed: the effect of gravitation on proper-time, the existence of black holes, the existence of gravitational waves,..., *cosmology*,...

**Einstein thought experiments.**[^einstein-thought-wikipedia][^equivalence-classical-mechanics]

[^basics-cm-gravitation]: [Basics: Classical Mechanics: Gravitation in classical mechanics](https://basics2022.github.io/bbooks-physics-mechanics/ch/actions-examples.html?highlight=gravitation#gravitation).

[^einstein-thought-wikipedia]: [List of some Einstein thought experiments on Wikipedia](https://en.wikipedia.org/wiki/Einstein%27s_thought_experiments).

[^equivalence-classical-mechanics]: [Equivalence principle in classical mechanics](https://basics2022.github.io/bbooks-physics-mechanics/ch/dynamics-equivalence-principle.html). Short discussion about elevator thought experiment and free fall in a gravitational field as the natural state of motion (indistinguishible from uniform linear motion w.r.t. an inertial reference frame).

````
