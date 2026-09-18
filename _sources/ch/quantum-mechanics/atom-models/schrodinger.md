(quantum-mechanics:atom-models:schrodinger)=
# Schrodinger model


````{dropdown} Position operator

```{dropdown} Definition
:open:

$$\hat{\mathbf{r}} | \mathbf{r} \rangle = \mathbf{r} | \mathbf{r} \rangle$$

```


```{dropdown} Wave function in space basis
:open:

$$\Psi(\mathbf{r}, t) := \langle \mathbf{r} | \Psi_t \rangle \ .$$


```

```{dropdown} Orthonality, and identity operator
:open:

$$\begin{aligned}
  1
  & = \int_{\mathbf{r} \in \Omega} \Psi^*(\mathbf{r},t) \Psi(\mathbf{r},t) d \mathbf{r} = \\
  & = \langle \Psi_t | \, \underbrace{\int_{\mathbf{r} \in \Omega} | \mathbf{r} \rangle \langle \mathbf{r} | d \mathbf{r}}_{= \hat{\mathbf{1}} } \, | \Psi_t \rangle  = \\
  & = \langle \Psi_t | \Psi_t \rangle \ .
\end{aligned}$$

So that the identity operator in space basis reads $\hat{\mathbf{1}} = \int_{\mathbf{r} \in \Omega} | \mathbf{r} \rangle \langle \mathbf{r} | d \mathbf{r}$. A wave function can be thus written as

$$| \Psi \rangle = \int_{\mathbf{r}' \in \Omega} | \mathbf{r}' \rangle \langle \mathbf{r}' | \, d \mathbf{r}' \, | \Psi \rangle \ .$$ (eq:quantum:space-representation)

```

```{dropdown} Expansion in space basis
:open:

$$\begin{aligned}
  \langle \mathbf{r} | \Psi \rangle = \Psi(\mathbf{r},t)
  & = \int_{\mathbf{r}' \in \Omega} \delta(\mathbf{r} - \mathbf{r}') \Psi(\mathbf{r}',t) \, d \mathbf{r}'
\end{aligned}$$

Comparing the last expression, with the projection of the expression {eq}`eq:quantum:space-representation` over $\langle \mathbf{r} |$,

$$\begin{aligned}
  \langle \mathbf{r} | \Psi \rangle = \langle \mathbf{r} |  \ , \int_{\mathbf{r}' \in \Omega} | \mathbf{r}' \rangle \langle \mathbf{r}' | \, d \mathbf{r}' \, | \Psi \rangle = \int_{\mathbf{r}' \in \Omega} \langle \mathbf{r} | \mathbf{r}' \rangle \langle \mathbf{r}' | \Psi \rangle \,  d \mathbf{r}' = \int_{\mathbf{r}' \in \Omega} \langle \mathbf{r} | \mathbf{r}' \rangle \Psi(\mathbf{r'},t ) \,  d \mathbf{r}' \ ,
\end{aligned}$$

if follows the orthogonality condition $\langle \mathbf{r} | \mathbf{r}' \rangle = \delta(\mathbf{r} - \mathbf{r}')$.

```
````

