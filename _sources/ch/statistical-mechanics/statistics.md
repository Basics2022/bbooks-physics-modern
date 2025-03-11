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

**Boltzmann entropy.** Boltmann entropy holds for uniform distributions over $\Omega$ possible states, $p_i = \frac{1}{\Omega}$. Gibbs' entropy of this uniform distribution becomes

$$S = - k_B \Omega \frac{1}{\Omega} \ln \frac{1}{\Omega} = k_B \ln \Omega \ .$$

**Entropy in Quantum Mechanics.** **todo**

```

```{dropdown} Boltzmann distribution

```

```{dropdown} 
```
