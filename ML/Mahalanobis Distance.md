# Mahalanobis distance

$$
    (\mathbf{x}-\boldsymbol{\mu})
        ^\text{T}
    \mathbf{\Sigma}^{-1}
    (\mathbf{x}-\boldsymbol{\mu})
$$

Consider orthonormal eigenvectors $\mathbf{u}_1, ..., \mathbf{u}_D$ of covariance matrix $\mathbf{\Sigma}$.
$$
\begin{align*}
    \mathbf{\Sigma} &=
    \sum_{i=1}^D
    \lambda_i
    \mathbf{u}_i
    \mathbf{u}_i^\text{T} \\

    \mathbf{\Sigma}^{-1} &=
    \sum_{i=1}^D
    \frac{1}{\lambda_i}
    \mathbf{u}_i
    \mathbf{u}_i^\text{T}
\end{align*}
$$
**NOTE** $\textbf{u}_i\textbf{u}_i^{\text{T}}$ means projection onto eigenbasis $\textbf{u}_i$

Then
$$
\begin{align*}
    \Delta^2&=(\mathbf{x}-\boldsymbol{\mu})^\text{T}\mathbf{\Sigma}^{-1}(\mathbf{x}-\boldsymbol{\mu}) \\
    &=\sum_{i=1}^D\frac{y_i^2}{\lambda_i}
\end{align*}
$$

where
$$
y_i=\mathbf{u}_i^{\text{T}}(\mathbf{x}-\boldsymbol{\mu})
$$

and so we have
$$
\mathbf{y}=\mathbf{U}(\mathbf{x}-\boldsymbol{\mu})
$$

With this new coordinate system, the Gaussian distribution takes the form
$$
p(\mathbf{y})=\prod_{j=1}^D\frac{1}{(2\pi\lambda_j)^{1/2}}\exp\{-\frac{y_j^2}{2\lambda_j}\}
$$
**NOTE** The determinant of $\boldsymbol{\Sigma}$ equals the product of its eigenvalues. $|\boldsymbol{\Sigma}|=\prod_{j=1}^D\lambda_j$
