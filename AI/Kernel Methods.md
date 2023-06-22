# Definition
A kernal function $k:\mathcal{X}\times\mathcal{X}\rightarrow\mathbb{R}$ is defined as

$$
k(\mathbf {x} ,\mathbf {x'} )=\langle \varphi (\mathbf {x} ),\varphi (\mathbf {x'} )\rangle _{\mathcal {V}}.
$$

where $\langle\cdot,\cdot\rangle\mathcal{v}$ must be a proper inner product in feature space $\mathcal{V}$.

# Explanation
Kernel functions basically map the input space of the data to a higher dimensional feature space, without ever computing the coordinates of the data in raw input space. (This is called the _kernel trick_.)

