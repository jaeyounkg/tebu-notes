# Freezing part of a module
Set `require_grad` at the module level with `nn.Module.requires_grad_()`
- Setting `require_grad` should be the main way to locally disable gradient computation
- It doesn't make sense to set `require_grad` for non-leaf tensors (tensors that have `grad_fn`)
	They have a backward graph associated with them and their gradients are needed as an intermediary result to compute the gradient for leaf tensors that require grad
 - Instead apply `.requires_grad_(False)` to individual parameters
 - `nn.Module.requires_grad_()` takes effect on all of the module's parameters
 
 [reference](https://pytorch.org/docs/stable/notes/autograd.html#locally-disable-grad-doc)
 