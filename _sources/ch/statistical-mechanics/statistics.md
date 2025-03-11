(statistical-mechanics:statistics)=
# Statistical Physics - Statistics Miscellanea

```{dropdown} Information content and Entropy
Given a discrete random variable $X$ with probability mass function $p_X(x)$, the self-information (**todo** *what about mutual information of random variables?*) is defined as the opposite of the logaritm of the mass function $p_X(x)$,

$$I_X(x) := - \ln \left( p_X(x) \right) \ .$$

Information content of indenpendent random variables is additive. Since $p_{X,Y}(x,y) = p_X(x) p_Y(y)$,

$$I_{X,Y}(x,y) = - \ln \left( p_{X,Y}(x,y) \right) = -\ln \left( p_X(x) p_Y(y) \right) = - \ln p_X(x) - \ln p_Y(y) \ .$$

**Shannon entropy.** Shannon entropy of a discrete random variable $X$ is defined as the expected value of the information content,

$$H(X) := \mathbb{E}[ I_X(X)] = \sum p_X(x) I_X(x) = - \sum p_X \ln p_X(x) \ .$$

**Gibbs entropy.** Gibbs entropy was defined by J.W.Gibbs in 1878,

$$S = - k_B \sum_i p_i \ln p_i \ .$$

Additivity holds for independent random variables.

**Boltzmann entropy.** Boltmann entropy holds for uniform distributions over $\Omega$ possible states, $p_i = \frac{1}{\Omega}$. Gibbs' entropy of this uniform distribution becomes

$$S = - k_B \Omega \frac{1}{\Omega} \ln \frac{1}{\Omega} = k_B \ln \Omega \ .$$

**Entropy in Quantum Mechanics.** **todo**

```

```{dropdown} Boltzmann distribution

Given a set of discrete states with probability $p_i$, and the average measure as "macroscopic quantity" $E = \sum_i p_i E_i$, Boltzann distribution maximizes the entropy (**todo** *Link to min info, max uncertainty*)

$$S = - k_B \sum_i p_i \ln p_i \ .$$

The distribution follows from the constrained optimization

$$\widetilde{S} = S - \alpha \left( \sum_i p_i -1  \right) - \beta \left( \sum_i p_i E_i - E \right)$$

$$\begin{aligned}
  0 & = \partial_{\alpha} \widetilde{S} = - \sum_i p_i - 1 \\
  0 & = \partial_{\beta}  \widetilde{S} = - \sum_i p_i E_i - E \\
  0 & = \partial_{p_k}    \widetilde{S} = -k_B \left( \ln p_k + 1 \right) - \alpha - \beta E_k \\
\end{aligned}$$

and thus

$$p_k = e^{- 1 - \frac{\alpha}{k_B} - \frac{\beta}{k_B} E_k} = e^{-\left( 1 + \frac{\alpha}{k_B} \right)} e^{- \frac{\beta}{k_B} E_k} = C e^{-\frac{\beta}{k_B} E_k} \ ,$$

and the normalization constant $C$ is determined by normalization condition

$$1 = \sum_k p_k = C \sum_{k} e^{-\frac{\beta E_k}{k_B}}$$

The inverse $Z = C^{-1}$ is defined as the **partition function**,

$$ Z = C^{-1} = \sum_k e^{-\frac{\beta E_k}{k_B}}\ ,$$

and the probability distribution becomes

$$p_k = \frac{e^{-\frac{\beta E_k}{k_B}}}{Z} =  \frac{e^{-\frac{\beta E_k}{k_B}}}{ \sum_{i} e^{-\frac{\beta E_i}{k_B}}} \ .$$


**Properties.**

$$\frac{p_k}{p_i} = e^{-\frac{\beta}{k_B}(E_k - E_i)} \ .$$



```

```{dropdown} Thermodynamics. Comparison of statistics and classical thermodynamics
:open:

First principle of classical thermodynamics (for a monocomponent gas with no electric charge,...) reads

$$T \, dS = d E + P \, dV$$

**Entropy for Boltzmann distribution** reads

$$\begin{aligned}
  S 
  & = - k_B \sum_i p_i \ln p_i = \\
  & = - k_B \sum_i \left[ p_i \left( - \frac{\beta E_i}{k_B} - \ln Z \right) \right] = \\
  & = \beta \langle E \rangle + k_B \ln Z
\end{aligned}$$

From classical thermodyamics, temperature $T$ can be defined as the partial derivative of the entropy of a system w.r.t. its internal energy keeping constant all the other independent variables,

$$\begin{aligned}
  \frac{1}{T}
  & = \left.\left( \dfrac{\partial S}{\partial E} \right)\right|_X = \\
  & = \dfrac{\partial \beta}{\partial E} E + \beta + k_B \frac{\partial \ln Z}{\partial E} = \\
  & = \dfrac{\partial \beta}{\partial E} E + \beta + k_B \frac{1}{Z} \frac{\partial Z}{\partial E} = \\
  & = \dfrac{\partial \beta}{\partial E} E + \beta + k_B \frac{1}{Z} \frac{\partial Z}{\partial \beta} \frac{\partial \beta}{\partial E} = \\
  & = \dfrac{\partial \beta}{\partial E} E + \beta + k_B \frac{1}{Z} \left( - \sum_i \frac{E_i}{k_B} e^{-\frac{\beta E_i}{k_B}} \right) \frac{\partial \beta}{\partial E} = \\
  & = \dfrac{\partial \beta}{\partial E} E + \beta - \left( \sum_i E_i p_i \right) \frac{\partial \beta}{\partial E} = \\
  & = \dfrac{\partial \beta}{\partial E} E + \beta - E \frac{\partial \beta}{\partial E} = \beta \ .
\end{aligned}$$

**todo** 
- write the derivative above clearly in terms of composite functions
- microscopical/statistical approach to the first principle of thermodynamics

$$d E = d \left( \sum_i p_i E_i \right) = \sum_i E_i \, d p_i + \sum_i p_i d E_i$$

```
