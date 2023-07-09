

Each Layer consists of the following layers:
- `torch.nn.Linear`
- `LayerNorm`
- Non-linear activation layer (e.g. ReLU).


Since we use blocks, the above operations yield a matrix. Therefore, we proceed as follows:
```pyhon
x = torch.mean(x, dim=1)  
x = self.classifier(x)  
x = torch.ravel(x)  
x = self.sigmoid(x)
```
