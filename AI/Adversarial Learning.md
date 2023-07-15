[Adversarial ML Tutorial](https://adversarial-ml-tutorial.org/introduction/)

Think of _maximizing_ the loss function $\ell$ _w.r.t. input_ $x$ instead of parameters $\theta$

$$
\max_{\delta\in\Delta} \ell(h_{\theta}(x+\delta), y)
$$
$\Delta$ represents an allowable set of perturbations to $x$ that _shouldn't_ change the output.

# Implementations
- [[Gradient Reversal Layer]]