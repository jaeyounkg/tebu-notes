# Multivariate Gaussian Distribution

$$
\begin{align*}
    \mathcal{N}(x|\mu,\sigma^2)&=\frac{1}{(2\pi\sigma^2)^{1/2}}\exp\{-\frac{1}{2\sigma^2}(x-\mu)^2\} \\
    \mathcal{N}(\mathbf{x}|\boldsymbol{\mu},\mathbf{\Sigma}) &=
    \frac
        {1}
        {(2\pi)^{D/2}}
    \frac
        {1}
        {|\mathbf{\Sigma}|^{1/2}}
    \exp\{
        -\frac{1}{2}
        (\mathbf{x}-\boldsymbol{\mu})
            ^\text{T}
        \mathbf{\Sigma}^{-1}
        (\mathbf{x}-\boldsymbol{\mu})
    \}
\end{align*}
$$

平方完成

[[Mahalanobis Distance]]
