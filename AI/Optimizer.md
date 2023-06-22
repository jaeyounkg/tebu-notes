# Gradient descent optimizers
- Batch gradient descent
	- Use tho whole dataset at once
- Stochastic gradient descent
	- Use one instance at a time
- Mini-batch gradient descent

$$\theta = \theta - \eta\cdot\nabla_{\theta} J(\theta; x^{(i:i+n)}; y^{(i:i+n)})$$

## Takeaways
- Learning rate has to be manually tuned
- Bad for sparse data
- Likely to get stuck into a suboptimal local minima

# Adaptive optimizers
- Adagrad
- Adadelta
- RMSprop
- Adam