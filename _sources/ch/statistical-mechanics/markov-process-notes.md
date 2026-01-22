(statistical-mechanics:markov-process)=
# Markov processes

[**Markov Process.**](https://basics2022.github.io/bbooks-math-miscellanea/ch/rl/mdp.html) Let $S$ a finite set of state $s$ that can be indexed with integer indices $i$, $P$ the transition probability between two states at consecutive time-steps, $P_{ss'} = P(s'|s)$, and $p_0$ the initial probability. A Markox process is uniquely defined by the triple

$$\langle S, P, p_0 \rangle \ .$$

If the Markov process is **time-homogeneous**, state transition matrix $P$ is independent from the time-step.


(statistical-mechanics:markov-process:transition-matrix)=
## State transition matrix

Given the finite set of states with integer indices, their probabilities at time $n$ can be collected in the $|S|$-dimensional vector $\mathbf{p}_n$. Transition from time $n-1$ to $n$ can be represented as

$$p_n(s') = \sum_s P (s'|s) p_{n-1}(s) = \sum_s P_{ss'} p_{n-1}(s)  \ ,$$

or using matrix formalism

$$\mathbf{p}^T_{n} = \mathbf{p}^T_{n-1} \mathbf{P} \ .$$

As $\mathbf{p}_n$ and $\mathbf{P}$ represents probability, their elements are non-negative. As the $i^{th}$ element of $\mathbf{p}_n$ represents the probability of the system of being in state $i$ at time $n$, it follows

$$\sum_i \left\{ \mathbf{p}_n \right\}_i = \sum_i p_n(i) = 1 \ .$$

As the element $P_{ij} = P(i|j)$ represents the conditional probability of reaching $j$ from state $i$ in one step, it follows

$$\sum_{j} \left\{ \mathbf{P} \right\}_{ij} = \sum_j P(j|i) = 1 \ .$$


(statistical-mechanics:markov-process:properties)=
## Properties

### Eigenvalue $s = 1$, and stationary state $\ \boldsymbol\pi$

The sum of the elements of each row of $\mathbf{P}$ is equal to $1$, as $\sum_{s'} P_{ss'} = \sum_{s'} P(s' | s) = 1$. Equivalently, state transition matrix $\mathbf{P}$ has an eigenvalue $\lambda = 1$, with the uniform right eigenvector $\mathbf{1}$, i.e. $\mathbf{P} \mathbf{1} = \mathbf{1}$.

The corresponding left eigenvector is a stationary state $\boldsymbol\pi$,

$$\boldsymbol\pi^T \mathbf{P} = \boldsymbol\pi^T \ .$$

### Spectrum of the transition matrix and asymptotic behavior of the system

**todo** *Are all the transition matrices diagonalizable?*

Assuming the transition matrix can be diagonalized, the evolution of the system from the initial probability $\mathbf{p}_0$ can be easily represented. The initial probabbility is written as $\mathbf{p}_0 = c_k \mathbf{w}_k$, being $\mathbf{w}_k$ the left eigenvectors of the transition matrix, and

$$\begin{aligned}
  \mathbf{p}^T_n
  =\mathbf{p}^T_{n-1} \mathbf{P}
  =\mathbf{p}^T_{0} \underbrace{\mathbf{P} \dots \mathbf{P}}_{ n \text{ times} }
  =a_k \underbrace{\mathbf{w}^T_k \mathbf{P}}_{= \lambda_k \mathbf{w}_k^T} \dots \mathbf{P}
  =a_k \lambda_k^n \mathbf{w}_k^T \ .
\end{aligned}$$

As $n \rightarrow +\infty$ only the contributions of the eigenvectors with $|\lambda_k| = 1$ survive. If there's only one of these eigenvalues, $\lambda_1 = 1$, the system converges to $\mathbf{1}$. If there are many eigenvalues with $\lambda_i = 1$, there system converges with probability $a_i$ to those stationary states, being $a_i$ the component of the initial state of the system along the $i^{th}$ eigenvector,

$$\mathbf{p}_n \sim a_k \mathbf{w}_k \ .$$

Components $a_i$ can be evaluated as the dot product between the **dual basis** $\{ \mathbf{v}_i \}_i$ w.r.t. the left eigenvectors and the initial state $\mathbf{p}_0$, as

$$ \mathbf{p}_0^T \mathbf{v}_i = a_k \underbrace{\mathbf{w}_k^T \mathbf{v}_i}_{ = \delta_{ik} \text{, def. of dual basis} } = a_i \ . $$

<!--
, defined as $\mathbf{w}_k^T \mathbf{v}_i := \delta_{ki}$, so tha
-->

Existence of eigenvalues $|s_j| = 1$, $s_j = e^{i \theta_j}$ makes limit cycles possible as

$$\mathbf{p}_n \sim \mathbf{w}_j e^{i n \theta_j} \text{ + c.c.} = 2 \left( \text{re}\{ \mathbf{w}_j \} \cos \theta_j - \text{im}\{ \mathbf{w}_j \} \cos \theta_j \right) \ .$$

**todo** *Discuss the possibility (?) of negative components. What's a negative probability?*

(statistical-mechanics:markov-process:properties:detailed-balance)=
### Detailed balance

 By definition, a **reversible Markov chain** has a positive stationary distribution $\boldsymbol\pi$ that satisfies the detailed balance equations

$$\pi_i P_{ij} = \pi_j P_{ji} \ ,$$

i.e. the flow between each pair of states $i$, $j$ is individaully balanced. Reversibility is a sufficient - even not necessary - condition for the existence of a stationary state.

Let $\pi_i \ne 0$ for $\forall i$, it's possible to define a symmetric matrix via a similarity transformation, as

$$\begin{aligned}
  \sqrt{\pi_i}\sqrt{\pi_i} P_{ij} & = \sqrt{\pi_j}\sqrt{\pi_j} P_{ji} \\
  \sqrt{\pi_i} P_{ij} \frac{1}{\sqrt{\pi_j}} & = \sqrt{\pi_j} P_{ji} \frac{1}{\sqrt{\pi_i}} \\
  S_{ij} & = S_{ji} \ ,
\end{aligned}$$

with $\mathbf{S} = \mathbf{D} \mathbf{P} \mathbf{D}^{-1}$, with $\mathbf{D} = \text{diag}\{ \sqrt{\pi_i} \}$. As the matrices $\mathbf{P}$ and $\mathbf{S}$ are related via a similarity transformation, they have the same eigenvalues



**todo**
- *Discuss the meaning of "reveresible"*


**Ergodicity.** ...**todo** *start from https://en.wikipedia.org/wiki/Markov_chain#Ergodicity*


