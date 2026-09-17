(quantum-mechanics:decoherence)=
# Decoherence

(quantum-mechanics:decoherence:example)=
## Example: two-dimensional system interacting with a large-dimensional environment

(quantum-mechanics:decoherence:example:state)=
### State of the system

A 2-dimensional system is interacting with a large-dimensional environment. The state of the 2-dimensional system is identified by the wave function

$$| \Psi_S \rangle = c_0 | 0 \rangle + c_1 | 1 \rangle \ ,$$

the state of the environment by the wave function $| \Psi_E \rangle$, and the state of the whole system (S+E) by the tensor product of the two,

$$| \Psi_{S+E} \rangle = | \Psi_S \rangle \otimes | \Psi_E \rangle \ .$$

(quantum-mechanics:decoherence:example:evolution)=
### Evolution of the system

The evolution of the system is governed by the Schrodinger equation, with the Hamiltonian of the whole system

$$i \hbar \dfrac{d}{dt} | \Psi_{S+E} \rangle = \hat{H}_{S+E} | \Psi_{S+E} \rangle \ ,$$

whose evolution can be represented by an unitary operator $\hat{U}_{S+E; t,0}$,

$$| \Psi_{S+E} \rangle_t = U_{S+E; t,0} | \Psi_{S+E} \rangle_0  = \dots = \alpha | 0 \rangle \otimes | \Psi_{E;0} \rangle + \beta | 1 \rangle \otimes | \Psi_{E;1} \rangle$$

Density operator reads

$$\hat{\rho} := | \Psi_{S+E} \rangle \langle \Psi_{S+E} | \ .$$

Tracing out the environment states,

$$\begin{aligned}
  \hat{\rho}_E 
  & = \text{Tr}_E \left( \hat{\rho} \right) = \\
  & = \sum_{k} \left( \alpha | 0 \rangle \langle \phi_k | \Psi_{E;0} \rangle + \beta | 1 \rangle \langle \phi_k | \Psi_{E;1} \rangle \right)  \left( \alpha^* \langle 0 | \langle \Psi_{E;0} | \phi_k  \rangle + \beta^* \langle 1 | \langle \phi_k | \Psi_{E;1} \rangle  \right) = \\
  & = |\alpha|^2 | 0 \rangle \langle 0 | \langle \Psi_{E;0} | \underbrace{\sum_k | \phi_k \rangle \langle \phi_k}_{= \hat{\mathbf{1}}} | \Psi_{E;0} \rangle + 
      \alpha \beta^* | 0 \rangle \langle 1 | \langle \Psi_{E;0} | \underbrace{\sum_k | \phi_k \rangle \langle \phi_k |}_{= \hat{\mathbf{1}} } \Psi_{E;1} \rangle + \\
  & \quad + 
      \alpha^* \beta | 1 \rangle \langle 0 | \langle \Psi_{E;1} | \underbrace{\sum_k | \phi_k \rangle \langle \phi_k}_{= \hat{\mathbf{1}}} | \Psi_{E;0} \rangle + 
      |\beta|^2 | 1 \rangle \langle 1 | \langle \Psi_{E;1} | \underbrace{\sum_k | \phi_k \rangle \langle \phi_k |}_{= \hat{\mathbf{1}} } \Psi_{E;1} \rangle = \\
  & = |\alpha|^2 | 0 \rangle \langle 0 | + \alpha \beta^* \langle \Psi_{E;0} | \Psi_{E;1} \rangle | 0 \rangle \langle 1 | + 
    + \alpha^* \beta \langle \Psi_{E;1} | \Psi_{E;0} \rangle | 1 \rangle \langle 0 | + |\beta|^2 | 1 \rangle \langle 1 | \ . 
\end{aligned}$$

The components of the reduced density operator in the system basis are

$$\begin{bmatrix} |\alpha|^2  & \alpha \beta^* \langle \Psi_{E;0} | \Psi_{E;1} \rangle \\ \alpha^* \beta \langle \Psi_{E;1} | \Psi_{E;0} \rangle & |\beta|^2 \end{bmatrix} \ .$$

### Decoherence time

**todo** *check and uncomment*

<!--
$$\begin{aligned}
  | \Psi_{E;0} \rangle & = \bigotimes_k | e_{0,k} \rangle \\
  | \Psi_{E;1} \rangle & = \bigotimes_k | e_{1,k} \rangle \\
\end{aligned}$$

$$\begin{aligned}
  \langle \Psi_{E;1} | \Psi_{E;0} \rangle = \bigotimes_k \langle e_{1,k} | e_{0,k} \rangle = \prod_k r_k e^{i \phi_k}  \ ,
\end{aligned}$$

with $r_k \in \mathbb{R}$, and $r \le 1$. Thus, for short time approximations, $e^x \sim 1 + x$

$$\begin{aligned}
  r_k(t) & \sim r_{k,0}( 1 + \gamma_k t ) \sim r_{k,0} e^{ \gamma_k t } \\
  \phi_k(t) & \sim \phi_{k,0} + \omega_k t \\
\end{aligned}$$

$$\begin{aligned}
  \langle \Psi_{E;1} | \Psi_{E;0} \rangle
  & = \prod_k r_k e^{i \phi_k} = \\
  & \sim \prod_k r_{k,0} e^{i \phi_{k,0}} e^{\left( \gamma_k + i \omega_k \right) t} = \\
  & = \underbrace
\end{aligned}$$
-->

