(quantum-mechanics:angular-momentum)=
# Angular momentum

Promoting the classical definition of angular momentum $\mathbf{L} = \mathbf{r} \times \mathbf{p}$, the angular momentum operator in quantum mechanics reads

$$\hat{\mathbf{L}} = \hat{\mathbf{r}} \times \hat{\mathbf{p}} = \hat{\mathbf{e}}_a \varepsilon_{abc} \hat{r} \hat{p}_c \ ,$$

and using space basis

$$\langle \mathbf{r} | \hat{\mathbf{L}} = \hat{\mathbf{e}}_a \underbrace{\left( - i \, \hbar \, \varepsilon_{abc}\, r_b \, \partial_c \langle \mathbf{r} | \right) }_{\hat{L}_a}\ .$$

**Composition of 2 components of the angular momentum operator.**

$$\begin{aligned}
  \hat{L}_a \hat{L}_b 
  & = - \hbar^2 \varepsilon_{acd} r_c \partial_d \left( \varepsilon_{bef} r_e \partial_f \right) = \\
  & = - \hbar^2 \varepsilon_{acd} \varepsilon_{bef} r_c \left( \delta_{de} \partial_f + r_e \partial_{df} \right) = \\
  & = - \hbar^2 \varepsilon_{acd} \varepsilon_{bdf} r_c \partial_f - \hbar^2 \varepsilon_{acd} \varepsilon_{bdf} r_c r_e \partial_{df} = \\
  & = - \hbar^2 \left( \delta_{af} \delta_{cb} - \delta_{ab} \delta_{cf} \right) r_c \partial_f - \hbar^2 \varepsilon_{acd} \varepsilon_{bef} r_c r_e \partial_{df} = \\
  & = - \hbar^2 r_b \partial_a + \hbar^2 \delta_{ab} r_c \partial_c - \hbar^2 \varepsilon_{acd} \varepsilon_{bef} r_c r_e \partial_{df} = \\
\end{aligned}$$

The last term is symmetric w.r.t. $a$, $b$.

**Commutators.**

$$[ \hat{L}_a, \hat{L}_b ] = \hat{L}_a \hat{L}_b -  \hat{L}_b \hat{L}_a = - \hbar^2 ( r_b\partial_a - r_a \partial_b) $$

If $a = b$, the obvious result follows, as an operator commutes with itself. If $a \ne b$, ...

$$[\hat{L}_a, \hat{L}_b ] = i \varepsilon_{abc} \hbar \hat{L}_c \ ,$$

or with a compact "vector notation", $\hat{\mathbf{L}} \times \hat{\mathbf{L}} = i \hbar \hat{\mathbf{L}}$.

**Commutations with magnitude.**

$$[ \hat{L}^2, \hat{L}_a ] = 0$$

Analogous relations in **classical mechanics**

$$
  [ L_a, L_b ] = i \hbar \varepsilon_{abc} \hat{L}_c \qquad , \qquad \{ L_a, L_b \} = \varepsilon_{abc} L_c \\
$$

provides another example of the relation between Poisson brackets in classical mechanics and commutator in quantum mechanics (**Dirac**)

$$\{ A, B \} \quad \leftrightarrow \quad \frac{1}{i \hbar} [ \hat{A}, \hat{B} ]$$

