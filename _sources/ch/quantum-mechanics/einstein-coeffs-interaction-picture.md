(quantum-mechanics:einstein-coeffs-interaction-picture)=
# Interaction picture, perturbation theory and Einstein coefficients

(quantum-mechanics:einstein-coeffs-interaction-picture:interaction)=
## Interaction picture

Interaction picture is a common and useful description of a system whose Hamiltonian cna be written as the sum of a term $\hat{H}_0$ that's well known and solvable, and $\hat{H}_1$ that's a perturbation to the system $0$, and it's usually either time-dependent and/or hard to solve analytically,

$$\hat{H} = \hat{H}_0 + \hat{H}_1 \ .$$

As $\hat{H}_0$ is time-independent, the corresponding unitary evolution operator is $U^{(0)} = \exp\left[ i \dfrac{\hat{H}_0}\hbar t \right]$.

A state vector in interaction picture, $| \Psi_I(t) \rangle$ is defined as

$$| \Psi_{I} (t) \rangle = U^{(0) \, \dagger} | \Psi_S(t) \rangle \ ,$$

with $| \Psi_S(t) \rangle$ the state vector in Schrodinger picture.

If one requires that the expectation value of operators is the same using different pictures,

$$\begin{aligned}
  \langle \hat{A}_I \rangle
  & = \langle \Psi_I | \hat{A}_I | \Psi_I \rangle = \\
  & = \langle \Psi_S | \underbrace{U^{(0)} \hat{A}_I U^{(0) \, \dagger}}_{=\hat{A}_S} | \Psi_S \rangle \ ,
\end{aligned}$$

it follows that $\hat{A}_I(t) = U^{(0) \, \dagger}(t,t_0) \hat{A}_S U^{(0)}(t,t_0)$. From the commutation of $\hat{H}_0$ with $U^{(0)}$, it follows that it has the same expression in Schrodinger and interaction picture, $H^{(0)}_I = H^{(0)}_S$.

**Time evolutions.**

````{dropdown} Time evolution of a state $\ | \Psi_I(t) \rangle$
:open:

$$\begin{aligned}
  i \hbar \dfrac{d}{dt} | \Psi_I \rangle 
  & = \hat{H}^{(1)}_I | \Psi_I \rangle \ .
\end{aligned}$$


```{dropdown} Details

$$\begin{aligned}
  i \hbar \dfrac{d}{dt} | \Psi_I \rangle 
  & = i \hbar \dfrac{d}{dt} \left[ U^{(0) \, \dagger}(t,t_0) | \Psi_S \rangle  \right] = \\
  & = i \hbar \left[ \partial_t U^{(0) \, \dagger}(t,t_0) | \Psi_S \rangle + U^{(0) \, \dagger} \dfrac{d}{dt} | \Psi_S \rangle  \right] = \\
  & = - U^{(0) \, \dagger} \hat{H}_0 | \Psi_S \rangle + U^{(0) \, \dagger} \left( \hat{H}^{(0)} + \hat{H}^{(1)} \right) | \Psi_S \rangle = \\
  & = \underbrace{U^{(0) \, \dagger} \hat{H}^{(1)} U^{(0)}}_{\hat{H}^{(1)}_I} \, \underbrace{U^{(0) \, \dagger} | \Psi_S \rangle}_{| \Psi_I \rangle} = \\
  & = \hat{H}^{(1)}_I | \Psi_I \rangle \ .
\end{aligned}$$

recalling that $\hat{H}^{(0)} = i \hbar \, \partial_t U^{(0)} U^{(0) \, \dagger} = - i \hbar U^{(0)} \partial_t U^{(0) \, \dagger}$, and that the Hamiltonian operator is Hermitian, $\hat{H} = \hat{H}^{\dagger}$.

```

````

````{dropdown} Time evolution of an operator $\hat{A}_I(t)$
:open:

```{dropdown} Details
:open:

```

````



(quantum-mechanics:einstein-coeffs-interaction-picture:perturbation)=
## Perturbation theory

 For an isolated system with time-independent Hamiltonian operator $\hat{H}_0$, the state of the system can be written as a linear combination of the eigenstates of the Hamiltonian operator

$$| \Psi(t) \rangle = | n \rangle a_n(t) \ ,$$

with $a_n(t) = a_n(0) \exp\left( - i \frac{E_n}{\hbar} t \right) = \langle n | \Psi(0) \rangle \exp\left( - i \frac{E_n}{\hbar} t \right) $.

**Time varying perturbation theory.** The state of the perturbed system is can be written as a linear combination of the eigenstates of the unperturbed Hamiltonian as well - here explicitly writing a factor $e^{-i E_n t / \hbar}$ in the coefficient,

$$| \Psi(t) \rangle = | n \rangle c_n(t) e^{-i E_n t / \hbar} \ ,$$

so that for unperturbed systems $c_n(t) = a_{n,0}$ constant. Inserting this expression in the Schrodinger equation of the system provides dynamical equations for the coefficients $c_n(t)$, i.e.

$$\begin{aligned}
 0
 & = - i \hbar \dfrac{d}{dt} | \Psi \rangle + \left( \hat{H}_0 + \hat{H}_1(t) \right) | \Psi \rangle = \\
 & = \sum_n \left[ \left( - i \hbar \dot{c}_n - c_n \, E_n + c_n \, E_n \right) | n \rangle + \hat{H}_1 | n \rangle c_n \right] e^{-i E_n t/\hbar} \\
 & = \sum_n \left[ - i \hbar \dot{c}_n |  n \rangle + \hat{H}_1 | n \rangle c_n \right] e^{-i E_n t/\hbar} \ .
\end{aligned}$$

Projecting on $\langle m |$, a system of an infinite number of equations follows

$$\dot{c}_m = - \frac{i}{\hbar} \sum_{n} \langle m | \hat{H}_1 | n \rangle c_n \, e^{i \frac{E_m - E_n}{\hbar} t} \ .$$

(quantum-mechanics:einstein-coeffs-interaction-picture:einstein-coeffs)=
## Einstein coefficients

Perturbation theory is applied to an electron around a steady positive nucleus, subject to time-varying electric field. The classical counterpart of the governing equation of a point charge subject to Coulomb potential and a travelling wave in the electric field 

$$\mathbf{e}(\mathbf{r},t) = 2 \mathbf{E}_0 \cos( \omega t - \mathbf{k} \cdot \mathbf{r} ) = q \mathbf{E}_0 ( e^{i(\omega t - \mathbf{k}\cdot \mathbf{r})} + c.c. ) \ , $$

reads

$$m \ddot{\mathbf{r}} + \dfrac{q^2}{4 \pi \varepsilon} \dfrac{\mathbf{r}}{|\mathbf{r}|^3} = 2 q \mathbf{E}_0 \cos(\omega t - \mathbf{k} \cdot \mathbf{r}) \ .$$


**Dipole approximation** assumes that the displacement of the charged particle is small compared to the wave-length of the radiation, $\mathbf{k} \cdot \mathbf{r} = \frac{ \hat{\mathbf{k}} \cdot \mathbf{r} }{2 \pi \lambda} \ll 1$, and thus the dynamic equation becomes

$$m \ddot{\mathbf{r}} + \dfrac{q^2}{4 \pi \varepsilon} \dfrac{\mathbf{r}}{|\mathbf{r}|^3} = 2 q \mathbf{E}_0 \cos(\omega t) \ .$$

The total force is the sum of the Coulomb force and the force due to the incoming electric field. This sum can be written as a gradient of a scalar function, a potential $V$,

$$\begin{aligned}
  \mathbf{F} 
  & = - \dfrac{q^2}{4 \pi \varepsilon} \dfrac{\mathbf{r}}{|\mathbf{r}|^3} + 2 q \mathbf{E}_0 \cos(2 \pi \, \nu \, t) = \\
  & = \nabla_{\mathbf{r}} \left[ \dfrac{q^2}{4 \pi \varepsilon}\dfrac{1}{|\mathbf{r}|} + 2 q \mathbf{r} \cdot \mathbf{E}_0 \cos(2 \pi \, \nu \, t) \right] = \\
  & = - \nabla_{\mathbf{r}} \left( V_0(\mathbf{r}) + V_1(\mathbf{r},t) \right) \ .
\end{aligned}$$

that can be written as the stationary potential $V_0$ from Coulomb force and the time-varying perturbation $V_1(\mathbf{r},t)$. The vector $q \mathbf{r}$ is usually defined as the **electric dipole**.

Schrodinger equation follows from the promotion of the Hamiltonian function $H = K + V$ to the Hamiltonian operator

$$\hat{H} = \hat{H}_0 + \hat{H}_1(t) = \hat{H}_0 + 2 \mathbf{E}_0 \cdot q \hat{\mathbf{r}} \, \cos(2 \pi \nu t ) \ .$$

<!--
Multiplying by $\dot{\mathbf{r}}$

$$\dfrac{d}{dt} \left[ \dfrac{1}{2} m |\dot{\mathbf{r}}|^2 - \dfrac{q^2}{4 \pi \varepsilon}\dfrac{1}{|\mathbf{r}|} \right] = 2 \dot{\mathbf{r}} \cdot \mathbf{E}_0 \cos(\omega t) \ .$$
-->



