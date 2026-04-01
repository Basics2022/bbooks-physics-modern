(statistical-mechanics:entropy)=
# Entropy and arrow of time

(statistical-mechanics:entropy:box-occupation)=
## Box occupation example

A box with two rooms contains $N$ chambers. This balls are numbered so that they are distingushable if you can see their labels.

**Macrostate definition.** A macrostate of the system is defined here by the number of balls in each room, $(N_L, N_R)$. As the total number of balls is given and constant, the number of balls in one chamber, e.g. $N_L$ in the left chamber, is enough to determine the macrostate being $N_R = N - N_L$.

**Microstate counting.** The number of microstates producing the macrostate $N_L$ is the number of combinations, $C_{N, N_L}$

$$\Omega(N_L) = C_{N, N_L} = \left( \begin{matrix} N \\ N_L \end{matrix} \right) = \frac{N!}{(N-N_L)! N_L!} \ .$$

**Entropy of a macrostate.** ...

$$S(n) = \ln \left( \begin{matrix} N \\ n \end{matrix} \right) \ .$$

**Probability transition between macrostates.** Being the probability uniform for any transition of microstates, the probability of transition between macrostates reads

$$\begin{aligned}
  P_{-}(n) := P(n \rightarrow n-1) & = \frac{n}{N} \\
  P_{+}(n) := P(n \rightarrow n+1) & = \frac{N-n}{N} \\
\end{aligned}$$ (eq:entropy:box:trans-prob)

**Expected change of entropy.**

$$\begin{aligned}
  \mathbb{E}\left[ \Delta S(n) \right] 
  & = \sum_{i} P_i(n) \Delta S_i(n) = \\
  & = P_{-}(n) \left( S(n-1) - S(n) \right) + P_{+}(n) \left( S(n+1) - S(n) \right) = \\
  & = \frac{n}{N} \ln \frac{\left( \begin{matrix} N \\ n-1 \end{matrix} \right) }{\left( \begin{matrix} N \\ n \end{matrix} \right) } + \frac{N-n}{N} \ln \frac{\left( \begin{matrix} N \\ n+1 \end{matrix} \right) }{\left( \begin{matrix} N \\ n \end{matrix} \right) } = \\
  & = \frac{n}{N} \ln \frac{N!}{(N-n+1)!(n-1)!} \frac{(N-n)!n!}{N!} + \frac{N-n}{N} \ln \frac{N!}{(N-n-1)!(n+1)!} \frac{(N-n)!n!}{N!} = \\
  & = \frac{n}{N} \ln \frac{(N-n)!n!}{(N-n+1)!(n-1)!} + \frac{N-n}{N} \ln \frac{(N-n)! n!}{(N-n-1)!(n+1)!} = \\
  & = \ln \frac{(N-n)! n!}{(N-n-1)!(n+1)!} + \frac{n}{N} \ln \frac{(N-n-1)!(n+1)!}{(N-n+1)!(n-1)!} = \\
  & = \ln \frac{(N-n)}{n+1} + \frac{n}{N} \ln \frac{n (n+1)}{(N-n)(N-n+1)} = \\
  & = \dots
\end{aligned}$$

**todo** *keep going with the algebra without the limit of large number of particles...*

**In the limit** $N \gg 1$, $n \gg 1$, $N-n \gg 1$,

$$\begin{aligned}
  \mathbb{E}\left[ \Delta S(n) \right] 
  & \simeq \ln \frac{N-n}{n} + \frac{n}{N} \ln \frac{n^2}{(N-n)^2} = \\
  & =      \ln \frac{N-n}{n} - \frac{2n}{N} \ln \frac{N-n}{n} = \\
  & =      \left( 1 - 2 \frac{n}{N} \right) \ln \frac{1 - \frac{n}{N}}{\frac{n}{N}} \ .
\end{aligned}$$

Both factors change sign when $\frac{n}{N} = \frac{1}{2}$. For $\frac{n}{N} < \frac{1}{2}$ both factors are positive, for $\frac{n}{N} > \frac{1}{2}$ both factors are negative. Thus, the expected variation of entropy of this process is non-negative for every value of $n \in [0,N]$ and thus for every transition,

$$\mathbb{E}\left[ \Delta S(n) \right] \ge 0 \ , \quad \forall n \in [0,N] \ .$$

**Markov process of macrostates.** The macrostates and the transition between them can be model as a stationary [Markov process](https://basics2022.github.io/bbooks-math-miscellanea/ch/rl/mdp.html). The probability of the system of being in (macro)state $n$ at time $t$ is $p_n(t)$, and using the transition probability $P(n|m)$ from state $m$ at $t-1$ to state $n$ at $t$, the following holds

$$p_n(t) = \sum_{m} P(n|m) p_m(t-1) \ ,$$

or using matrix formalism, introducing transition probability matrix $\left\{\mathbf{P}\right\}_{mn} := P(n|m)$,

$$\mathbf{p}(t) = \mathbf{p}(t-1) \mathbf{P} \ .$$

The transition probabilities {eq}`eq:entropy:box:trans-prob` define the elements of the transition probability matrix $\mathbf{P}$,

$$\mathbf{P} = \begin{bmatrix}
\cdot       & 1           &               &               &               &             &             \\ 
\frac{1}{N} & \cdot       & 1-\frac{1}{N} &               &               &             &             \\ 
            & \frac{2}{N} & \cdot         & 1-\frac{2}{N} &               &             &             \\ 
            &             & \dots         & \cdot         &         \dots &             &             \\ 
            &             &               & 1-\frac{2}{N} &         \cdot & \frac{2}{N} &             \\ 
            &             &               &               & 1-\frac{1}{N} & \cdot       & \frac{1}{N} \\ 
            &             &               &               &               & 1           & \cdot       \\ 
\end{bmatrix} \ .
$$

**Stationary distribution.** The stationary distribution $\mathbf{p}^*$ is invariant under a transition, i.e. it satisfies $\mathbf{p}^* = \mathbf{p}^* \mathbf{P}$. The stationary distribution of the process is the Binomial distribution

$$p^*_n = \frac{1}{2^N} \left( \begin{matrix} N \\ n \end{matrix} \right) \ .$$

```{dropdown} Proof

This can be proved by direct computation. The first element reads

$$p_0^* = \frac{1}{N} p_1^* \ ,$$

or

$$\frac{1}{2^N} \cdot 1 = \frac{1}{N} \frac{1}{2^N} \frac{1}{N} \ .$$

The $n^{th}$ element ($n \in (1,N-1)$) reads

$$p_n^* = \left( 1-\frac{n-1}{N} \right) p_{n-1}^* + \frac{n+1}{N} p_{n+1}^* \ .$$

or

$$\begin{aligned}
 \frac{1}{2^N} \frac{N!}{(N-n)!n!}
 & = \left( 1 - \frac{n-1}{N} \right) \frac{1}{2^N} \frac{N!}{(N-n+1)! (n-1)!} + \frac{n+1}{N} \frac{1}{2^N} \frac{N!}{(N-n-1)! (n+1)!} = \\
 & = \frac{1}{2^N} \left[ \frac{N-n+1}{N} \frac{N!}{(N-n+1)!(n-1)!} + \frac{n+1}{N} \frac{N!}{(N-n-1)!(n+1)!} \right] = \\
 & = \frac{1}{2^N} \frac{N!}{(N-n)!n!} \left[ \frac{n}{N} + \frac{N-n}{N} \right] = \\
 & = \frac{1}{2^N} \frac{N!}{(N-n)!n!} \ .
\end{aligned}$$

```

**Statistics of the stationary distribution.** 

* Average $\mu = \frac{N}{2}$
* Variance $\sigma^2 = \frac{N}{4}$
* Standard deviation  $\sigma = \frac{\sqrt{N}}{2}$

Thus the relative fluctuation around the average can be estimated with the ratio of the standard deviation and the average value,

$$\frac{\sigma}{\mu} = \frac{1}{\sqrt{N}} \ ,$$

so, the relative fluctuation decreases as $N$ increases.

| $N$     | Relative fluctuation |
| ------  | -------------------- |
| $10^2$  | $10^{-1}$            |
| $10^4$  | $10^{-2}$            |
| $10^6$  | $10^{-3}$            |
| $10^8$  | $10^{-4}$            |

```{dropdown} Average of a binomial distribution

$$\begin{aligned}
  \mathbb{E}[n]
  & = \sum_{n=0}^{N} n \, p_n^* = \\
  & = \frac{1}{2^N} \sum_{n=0}^{N} n \left( \begin{matrix} N \\ n \end{matrix} \right) = \\
  & = \frac{1}{2^N} \sum_{n=1}^{N} N \left( \begin{matrix} N-1 \\ n-1 \end{matrix} \right) = \\
  & = \frac{1}{2^N} N \sum_{n=0}^{N-1} \left( \begin{matrix} N-1 \\ n \end{matrix} \right) = \\
  & = \frac{1}{2^N} N 2^{N-1} = \frac{N}{2} \ .
\end{aligned}$$

```

```{dropdown} Variance of a binomial distribution

$$\sigma^2_n = \mathbb{E}[n^2] - \left( \mathbb{E}[n] \right)^2 $$

Then,

$$\mathbb{E}[n^2] = \mathbb{E}[n(n-1)] + \mathbb{E}[n] \ ,$$

where the first term follows from a similar procedure as the one used for the average, using the identity $n(n-1)\left(\begin{matrix} N \\n \end{matrix}\right) = N(N-1) \left( \begin{matrix} N-2 \\ n-2 \end{matrix} \right)$,

$$\mathbb{E}[n(n-1)] = \frac{N(N-1)}{4} \ .$$

Thus the variance reads

$$\sigma^2_n = \frac{N(N-1)}{4} + \frac{N}{2} - \frac{N^2}{4} = \frac{N}{4} \ .$$

```

**Markov process of microstates.** A microstate is defined by the id of the box of each of the $N$ balls. One-step transition switch the index of one ball. If the transition probability between these microstates is uniform it has probability $\frac{1}{N}$. Not, let's consider two states $i$, $j$. If these states are adjacent, the probabilities $P^{micro}(i \rightarrow j) = P^{micro}(j \rightarrow i) = \frac{1}{N}$, and zero otherwise. Thus, the transition probability matrix $\mathbf{P}^{micro}$ between microstates is symmetric. Since the **transition matrix is symmetric**, the **stationary distribution is uniform**. This is immediately proved using the normalization condition $\mathbf{P} \mathbf{1} = \mathbf{1}$, and the definition of a stationary distribution, $\mathbf{p}^{* T} = \mathbf{p}^{* T} \mathbf{P}$, and the definition of symmetric transition matrix $\mathbf{P} = \mathbf{P}^T$. The transpose of the definition of the stationary distribution, $\mathbf{p}^* = \mathbf{P} \mathbf{p}^*$, compared with the normalization condition, provides the relation $\mathbf{p}^* = \alpha \mathbf{1}$, and normalization condition $1 = |\mathbf{p}^*|_1 = \alpha N$, and $\alpha = \frac{1}{N}$. The stationary distribution for the symmetric Markov process is $\mathbf{p}^* = \frac{1}{N} \mathbf{1}$.


[Combinatorics](https://basics2022.github.io/bbooks-math-miscellanea-hs/ch/statistics/combinatorics.html) naturally links the distribution of microstates and the distribution of the macrostates.

**H-Theorem for symmetric Markov chains.** A discrete version of the Boltzmann's H-Theorem exists for symmetric Markov process, assessing that the entropy $H(\mathbf{p}(t)) := - \sum_k p_k(t) \ln p_k(t)$ is non-decreasing, i.e.

$$H(\mathbf{p}(t+1)) \ge H(\mathbf{p}(t)) \ .$$

```{dropdown} Proof

**Remark.** A generic transition probability matrix $\mathbf{P}$ satisfies the normalization condition $\sum_j P_{ij} = 1$, for every $i$ (row sum). For a symmetric probability matrix $\mathbf{P} = \mathbf{P}^T$, also the column sum holds $\sum_i P_{ij} = 1$.

**Remark.** The function $f(x) = x \ln x$ is convex, i.e. $f''(x) > 0$, for $x > 0$.

$$\begin{aligned}
  f' (x) & = \ln x + 1 \\
  f''(x) & = \frac{1}{x} \ .
\end{aligned}$$

$$\begin{aligned}
  H(t+1) 
  & = - \sum_k p_k(t+1) \ln p_k(t+1) = \\
  & = - \sum_k f( p_k(t+1) ) = \\
  & = - \sum_k f \left( \sum_i p_i(t) P_{ik} \right) \ .
\end{aligned}$$

**Jensen's Inequality.** As $f$ is convex, and $\sum_{i} P_{ik} = 1$, with $P_{ik} \in (0,1)$,

$$f \left( \sum_i p_i P_{ik}  \right) \le \sum_i P_{ik} f( p_i ) \ .$$

Using Jensen's inequality in the expression of $H(t+1)$,

$$\begin{aligned}
H(t+1)
 & \ge - \sum_k \sum_i P_{ik} f(p_i) = \\
 & = - \sum_i f(p_i) \underbrace{\sum_k P_{ik}}_{=1} 
   = H(t) \ ,
\end{aligned}$$

i.e. $H(t+1) \ge H(t)$.


```

