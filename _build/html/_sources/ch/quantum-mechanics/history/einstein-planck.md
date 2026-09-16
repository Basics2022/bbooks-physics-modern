(quantum-mehcanics:history:light-matter)=
# Light matter interaction


(quantum-mehcanics:history:light-matter:einstein)=
## Einstein: quantum theory of radiation interacting with matter

Three mechanisms, whose probabilities are

* Spontaneous emission of radiation, for a photon going from level $j$ to level $i$ ($E_j > E_i$),

   $$\left( \frac{d n_{ij}}{d t} \right)_{spont} = A_{ji} n_j \ ,$$

* Stimulated emission of radiation, for a photon going from level $j$ to level $i$ ($E_j > E_i$),

   $$\left( \frac{d n_{ij}}{d t} \right) = B_{ji} n_j \rho(\nu_{ji}) \ ,$$

   with $\nu_{ji} = \frac{E_j - E_i}{h}$, and $\rho(\nu)$ the density of radiation in the system at frequency $\nu$

* Absorption, for a photon going from level $j$ to level $i$ ($E_j > E_i$),

   $$\left( \frac{d n_{ij}}{d t} \right) = - B_{ij} n_i \rho(\nu_{ij}) \ .$$

The overall rate reads

$$\dfrac{d n_i}{d t} = \sum_{j, E_j > E_i} \dfrac{d n_{ij}}{d t} = \sum_{j, E_j > E_i} \left\{ A_{ji} n_j + B_{ji} n_j \rho(\nu_{ij}) - B_{ij} n_i \rho(\nu_{ij}) \right\} $$

At thermodynamic equilibriumm between all the states

$$0 = \dfrac{d n_{ij}}{d t} = A_{ji} n_j + B_{ji} n_j \rho(\nu_{ij}) - B_{ij} n_i \rho(\nu_{ij})$$

Using Boltzmann distribution

$$\frac{n_i}{n} = \frac{g_i e^{-\frac{E_i}{kT}}}{Z} \ ,$$

the expression of the radiation density follows

$$\begin{aligned}
  \rho(\nu_{ij})
  & = \frac{A_{ji} n_j}{n_i B_{ij} - n_j B_{ji}} = \\
  & = \frac{A_{ji} g_j}{B_{ij} g_i} \frac{ \exp(-E_j/kT) }{ \exp(-E_i/kT) - \frac{g_j B_{ji}}{g_i B_{ij}} \exp(-E_j/kT)} = \\
  & = \frac{A_{ji} g_j}{B_{ij} g_i} \frac{ 1 }{ \exp((E_j-E_i)/kT) - \frac{g_j B_{ji}}{g_i B_{ij}}} = \\
  & = \frac{A_{ji} g_j}{B_{ij} g_i} \frac{ 1 }{ \exp(h \nu_{ji}/kT) - \frac{g_j B_{ji}}{g_i B_{ij}}} \ .
\end{aligned}$$

Comparing with Planck's law $\rho(\nu, T) = \frac{2 h \nu^3}{c^2} \frac{1}{\exp(h \nu /kT) - 1}$, the relations between Einstein coefficients $(E_j > E_i)$ follows

$$\frac{g_j A_{ji}}{g_i B_{ij}} = \frac{2 h \nu_{ji}^3}{c^2} \quad , \quad \frac{g_j B_{ji}}{g_i B_{ij}} = 1 \ .$$
