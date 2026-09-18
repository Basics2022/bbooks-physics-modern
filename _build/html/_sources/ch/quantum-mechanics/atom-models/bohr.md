(quantum-mechanics:atom-models:bohr)=
# Bohr model

Assumption:
* Electron moves on circular orbits
* All the possible orbits are identified by discrete values of the angular momentum, $L = n \hbar$
* Light emission/absorption occurs when an electron transitions between two orbits

Some mathematical details, using the equations of classical mechanics. The problem of determining the orbit of an electron around the positive nucleus is a two-body problem, subject to a force $\vec{F} \propto \frac{\vec{r}}{|\vec{r}|^3}$ (here the assumption of the center of mass in the nucleus; otherwise change of coordinates, and equivalent masses...). For an electrically neutral atom with one electron only ($H$ atom?) the dynamical equation governing the motion of the electron

$$m \ddot{\vec{r}} = - \frac{q^2}{4 \pi \varepsilon} \frac{\vec{r}}{|\vec{r}|^3} \ ,$$

being $q$ the charge of the electron.

* Using polar coordinates, $\vec{r} = r \hat{r}$

* Taking time derivative of the position vector $\vec{r}$ identifying the position of the electron w.r.t. the nucleus

   $$\begin{aligned}
     \dfrac{d}{dt} \left( r \hat{r} \right ) & = \dot{r} \hat{r} + r \dot{\theta} \hat{\theta} \\
     \dfrac{d^2}{dt^2} \left( r \hat{r} \right ) & = \left( \ddot{r} - r \dot{\theta}^2 \right) \hat{r} +  \left( 2 \dot{r} \dot{\theta} + r \ddot{\theta} \right) \hat{\theta} \\
   \end{aligned}$$

* Assuming circular orbits, $\dot{r} = 0$

the radial and angular components of the dynamical equation read

$$\begin{aligned}
  r      & : \quad - m r \dot{\theta}^2 = - \frac{q^2}{4 \pi \varepsilon} \frac{1}{r^2} \\
  \theta & : \quad \ddot{\theta} = 0 \\
\end{aligned}$$

The angular momentum and the energy of the system are

* Angular momentum,

   $$\begin{aligned}
     n \hbar = L_n 
     & = m r_n^2 \dot{\theta}_n =  && \text{(radial component)} \\
     & = m r_n^2 \left( \frac{q^2}{4 \pi \varepsilon r_n^3 m} \right)^{\frac{1}{2}} = \\
     & =  \frac{\sqrt{m} q}{\sqrt{ 4 \pi \varepsilon}} r^{\frac{1}{2}} \\
     \rightarrow \quad r_n & = 4 \pi \varepsilon \frac{n^2 \hbar^2}{m q^2}
   \end{aligned}$$

* Energy, 

  $$\begin{aligned}
    E_n 
    & = \frac{1}{2} m |\dot{\vec{r}}_n|^2 - \frac{q^2}{4 \pi \varepsilon} \frac{1}{r_n} =  && \text{(radial component of the eom)} \\
    & = \frac{q^2}{8 \pi \varepsilon} \frac{1}{r_n} - \frac{q^2}{4 \pi \varepsilon} \frac{1}{r_n} = \\
    & = - \frac{q^2}{8 \pi \varepsilon} \frac{1}{r_n} = && \text{($r_n$ from angular momentum)} \\
    & = - \frac{m q^4}{32 \pi^2 \varepsilon^2 \hbar^2} \frac{1}{n^2} = && \text{($h = 2 \pi \hbar$)} \\
    & = - \frac{m q^4}{8 \varepsilon^2 h^2}\frac{1}{n^2} \ .
  \end{aligned}$$

From the relation $\Delta E = \nu h$, the relation between the frequency of the emitted (if $E_{n} > E_{m}$, $n$ initial state, $m$ final state) or absorbed (if $E_n < E_m$, $n$ initial state, $m$ final state) radiation, follows

$$\nu_{nm} = \frac{E_n - E_m}{h} = - \frac{m q^4}{8 \varepsilon^2 h^3} \left( \frac{1}{n^2} - \frac{1}{m^2} \right)$$

