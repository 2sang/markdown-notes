#### What does the backward() function do? - [pytorch.org](https://discuss.pytorch.org/t/what-does-the-backward-function-do/9944)
loss.backward() computes dloss/dx for every parameter x which has requires_grad=True.  
These are accumulated into x.grad for every parameter x.  

Optimizer.step updates the value of x using the gradient x.
