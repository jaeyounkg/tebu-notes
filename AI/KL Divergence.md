# Definition

A measure of how distribution $P$ is different from reference distribution $Q$.

$$
D_{KL}(P\mid\mid Q)=-\sum_{x\in\mathcal{X}}{P(x)\log\left(\frac{Q(x)}{P(x)}\right)}
$$
The expectation of the logarithmic difference between the probabilities $P$ and $Q$, where the expectation is taken using the probabilities $P$.

# Intuitions & Interpretations

- $P$ represents the "true" distribution of data, observations, etc
- $Q$ represents a theory, model, approximation of $P$
- The average difference of the number of bits required for encoding samples of $P$ using a code optimized for $Q$, not for $P$.
- Positive if $P$ is _sharper_ than $Q$, negative if $P$ is more _flat_
- The **information gain** achieved if $P$ would be used instead of $Q$ which is currently used.
