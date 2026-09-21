(quantum-mechanics:angular-momentum)=
# Angular Momentum

Before going into details, an introduction is likely to be required. 

**[Spatial (orbital) angular momentum, $\hat{\mathbf{L}}$](quantum-mechanics:angular-momentum:spatial).** Spatial angular motion is the quantum mechanical counterpart of the angular momentum in classical mechanics, $\hat{L} = \mathbf{r} \times \mathbf{p}$, due to the spatial motion of the system w.r.t. a point. The angular momentum operator in quantum mechanics can be defined promoting the classical space and momentum variables to the corresponding operators,

$$\mathbf{L} = \mathbf{r} \times \mathbf{p} \qquad \rightarrow \qquad \hat{\mathbf{L}} = \hat{\mathbf{r}} \times \hat{\mathbf{p}} \ ,$$

whose representation using spatial basis reads

$$\langle \mathbf{r} | \hat{\mathbf{L}} = -i \hbar \mathbf{r} \times \nabla_{\mathbf{r}} \langle \mathbf{r} | \ .$$

This operator has several properties that will be investigated in details in the dedicated section. This operator applies to a wave function representing the position, momentum, and physical quantities with classical analogous, here called $| \psi \rangle$.

**[Spin (intrinsic) angular momentum, $\hat{\mathbf{S}}$](quantum-mechanics:angular-momentum:spin).** Quantum systems may have intrinsic properties, with no classical counterpart. Spin momentum is one of these variables. Spin angular momentum $\hat{\mathbf{S}}$ is defined in analogy with the spatial orbital momentum, with the same properties and acts on a spin state vector $| s \rangle$.

Thus, the full state of the system belongs to a space state that is a tensor product of a space and a spin state space, 

$$\mathcal{H} = \mathcal{H}_{space} \otimes \mathcal{H}_{spin} \ ,$$

defined as the tensor product of a spatial state vector and a spin state vector,

$$| \Psi \rangle = | \psi \rangle \otimes | s \rangle \ .$$

**[Total angular momentum $\hat{\mathbf{J}}$](quantum-mechanics:angular-momentum:total).** Total angular momentum can be defined as the sum of the spatial and the spin angular momentum,

$$\hat{\mathbf{J}} = \left( \hat{\mathbf{L}} \otimes \hat{\mathbf{1}} \right) + \left( \hat{\mathbf{1}} \otimes \hat{\mathbf{S}} \right) \ ,$$

or, remembering that $\hat{\mathbf{L}}$ only acts on $| \psi \rangle$ and $\hat{\mathbf{S}}$ onlt acts on $| s \rangle$, it's usually written as $\hat{\mathbf{J}} = \hat{\mathbf{L}} + \hat{\mathbf{S}}$.



