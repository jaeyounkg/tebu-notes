![Image](https://miro.medium.com/max/1204/1*9OsQV0PqM2juaOtGqoRISw.jpeg)

A Bayesian network is a **directed acyclic graph** in which

- each edge corresponds to a conditional dependency
- each node corresponds to a unique random variable

Bayesian networks satisfy the **local Markov property**, which states that

- A node is [[Conditional Independence|conditionally independent]] of its non-descendants given its parents.

Using this property, the join distribution for a Bayesian network can be simplified like following:

$$
\begin{align}
    P(X_1, ..., X_n) &= \prod_{i=1}^n P(X_i | X_1, ..., X_{i-1}) && \text{連鎖性}\\
    &= \prod_{i=1}^n P(X_i | Parents(X_i))
\end{align}
$$

This property greatly reduces the amount of required computation.
