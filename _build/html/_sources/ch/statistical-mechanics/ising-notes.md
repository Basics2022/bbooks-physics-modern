(statistical-mechanics:ising:notes)=
# Ising model - Notes

(statistical-mechanics:ising:introduction)=
## Introduction




(statistical-mechanics:ising:time-evolution)=
## Time evolution

(statistical-mechanics:ising:time-evolution)=
### Metropolis-Hastings

Metropolis-Hastings algorithm is designed to generate a collection of states according to a desired distribution $p(s)$, using a **Markov process** with a unique **stationary distribution** $\pi(s) = p(s)$.

```{dropdown} Algorithm
:open:

- Initialize state $s_0$ with energy $E_0$
- while **not** terminal condition:
  - flip the spin of a randomly chosen site, to get the possible state $s_\widetilde{n}$
  - calculate the change in energy of the state $\Delta \widetilde{E}_n := \widetilde{E}_n - E_{n-1}$
  - update state:
    - if $\Delta \widetilde{E}_n < 0$ accept the change, $s_n = s_{\widetilde{n}}$
    - if $\Delta \widetilde{E}_n > 0$ accept the change with probability $\exp\left( - \frac{\Delta \widetilde{E}_n}{T} \right)$

```

Starting from the **detailed balance** (sufficient but not necessary condition for the existence of a (unique?) stationary state), $P(s'|s) p(s) = P(s|s') p(s')$, 

$$\frac{P(s'|s)}{P(s|s')} = \frac{p(s')}{p(s)} \ ,$$

each transition is splitted in **two sub-steps**: proposal and acceptance-rejection steps. Transition is written as $P(s'|s) = g(s'|s) A(s',s)$ being $g(s'|s)$ the proposal conditional probability, and $A(s',s)$ the acceptance probability. Acceptance probability is choosen in a way to satisfy the conditions of time-reversal and ergodicity. Metropolis choice reads

$$A(s', s) = \min \left( 1, \frac{p(s')}{p(s)} \frac{g(s|s')}{g(s'|s)} \right) \ .$$

**todo** *check if Metropolis choice fulfills the necessary conditions.*

**Example: Boltmann distribution with uniform proposal.** Let a system have Boltzmann stationary distribution, $p(s) \propto \exp\left( - \beta E(s) \right)$, and uniform proposal conditional probability $g(s'|s) = \frac{1}{N}$, with $N$ the number of accessible states from the state $s$. 

```{prf:example} Ising model on a 2D lattice with 1 flip per update

As an example, for an Ising model on a 2D lattice with dimension $m \times n$ with proposal update with $1$ flip $N = mn$.

```

```{prf:example} Ising model on a 2D lattice with $k$ flips per update

**todo** *Is a probability built with independent successive flips ok? Target states at each flip have the same probability, s.t. the probability of reaching steps $s_k$ after $k$ flips starting from $s_0$ is not uniform.*

<!--
As an example, for an Ising model on a 2D lattice with dimension $m \times n$ with proposal update with $2$ flips, the number of accessible states is given by the number of [combinations with repetitions](https://basics2022.github.io/bbooks-math-miscellanea-hs/ch/statistics/combinatorics.html), $C'_{mn,2} = \left( \begin{matrix} mn + 1 \\ 2 \end{matrix} \right)$.
-->

```

Let $g(s|s') = g(s'|s)$. The acceptance probability of the transition between different states $s' \ne s$ reads

$$A(s',s) = \min \left( 1, e^{ -\beta ( E(s') - E(s) )  } \right) \ ,$$

and the corresponding element of transition matrix is

$$P(s'|s) = \frac{1}{N} \min \left( 1, e^{ -\beta ( E(s') - E(s) )  } \right) \ .$$

The *diagonal elements* of the probability transition matrix - representing no state transition - are evaluated as the probability that makes $\sum_{s'} P(s'|s) = P(s|s) + \sum_{s' \in T(s)} P(s'|s) = 1$, i.e.

$$P(s|s) = \frac{1}{N} \sum_{\begin{aligned} s' & \in T(s) \\ E(s') & > E(s) \end{aligned}} \left( 1 - e^{-\beta (E(s') - E(s))} \right)  \ .$$

```{dropdown} $P(s|s)$

$$\begin{aligned}
  P(s|s) 
  & = 1 - \sum_{s' \in T(s)} P(s'|s) = \\
  & = 1 - \sum_{s' \in T(s)} \frac{1}{N} \min \left( 1, e^{-\beta (E(s') - E(s))} \right) = \\
  & = \frac{1}{N} \sum_{s' \in T(s)} \left[ 1 - \min \left( 1, e^{-\beta (E(s') - E(s))} \right) \right] = \\
  & = \frac{1}{N} \sum_{s' \in T(s)} \max \left( 0, 1 - e^{-\beta (E(s') - E(s))} \right) = \\
  & = \frac{1}{N} \sum_{\begin{aligned} s' & \in T(s) \\ E(s') & > E(s) \end{aligned}} \left( 1 - e^{-\beta (E(s') - E(s))} \right)  \ .
\end{aligned}$$

```

It's easy to prove that this probability functions are related by the detailed balance equations,

$$\frac{P(s'|s)}{P(s|s')} = \frac{\min \left( 1, e^{ -\beta ( E(s') - E(s) )  } \right) }{\min \left( 1, e^{ -\beta ( E(s) - E(s') )  } \right) } = e^{ -\beta ( E(s') - E(s) )  } = \frac{e^{-\beta E(s')}}{e^{-\beta E(s)}} = \frac{p(s')}{p(s)} \ .$$


