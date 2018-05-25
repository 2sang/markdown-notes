#### What does the backward() function do? - [pytorch.org](https://discuss.pytorch.org/t/what-does-the-backward-function-do/9944)
loss.backward() computes dloss/dx for every parameter x which has requires_grad=True.  
These are accumulated into x.grad for every parameter x.  

Optimizer.step updates the value of x using the gradient x.


#### How to extract intermediate feature from pytorch network? - [discuss.pytorch.com](https://discuss.pytorch.org/t/how-to-extract-features-of-an-image-from-a-trained-model/119/5)
fmassa's answer: 
Yes, it’s possible and very easy in PyTorch. All you need to do  
is to return the multiple outputs that you want to retrieve. Here is an example
```python
class Net(nn.Module):
    def __init__(self):
        self.conv1 = nn.Conv2d(1, 1, 3)
        self.conv2 = nn.Conv2d(1, 1, 3)
        self.conv3 = nn.Conv2d(1, 1, 3)

    def forward(self, x):
        out1 = F.relu(self.conv1(x))
        out2 = F.relu(self.conv2(out1))
        out3 = F.relu(self.conv3(out2))
        return out1, out2, out3
```

