# Definition & Intuitions
- The number of independent pieces of information that go into the estimate of a parameter
-  In general, the degrees of freedom of an estimate of a parameter are equal to the number of independent scores that go into the estimate minus the number of parameters used as intermediate steps in the estimation of the parameter itself
- Where certain random vectors are constrained to lie in linear subspaces, the number of degrees of freedom is the dimension of the subspace.
- Is essentially the number of "free" components

# In probability distributions
- In applications where these distributions occur, the parameter corresponds to the degrees of freedom of an underlying random vector
- In more sophisticated uses, degrees of freedom can have fractional values and there is no interpretation

# Examples
## Sample variance
Sample variance has $n-1$ degrees of freedom, because in the residuals vector
$$
(x_1 - \bar{x}, ..., x_n - \bar{x})
$$
while there are $n$ independent observations $x_1, ..., x_n$, there are only $n-1$ independent residuals.