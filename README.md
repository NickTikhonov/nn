# nn

The most barebones nn implementation + GPU-enabled 
training harness that can be used to train serious models. 
Using only `numpy` and `pandas`. 

```python
import nn

n = nn.NN([784,1000,1000,10], Tanh, gpu=True)
opt = nn.Adam(n, X_train, Y_train, X_test, Y_test, batch_size=4096 * 4)
opt.train(epochs=100, lr=0.001, momentum=0.90).
```

Supports:

* Feed-forward deep neural nets
* Sigmoid + Tanh activation
* Gradient descent + Adam optimisers
* CPU + GPU training
