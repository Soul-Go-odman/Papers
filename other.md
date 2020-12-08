[[Do We Need Zero Training Loss After Achieving Zero Training Error?](https://arxiv.org/pdf/2002.08709.pdf)]  
```
output = model(inputs)
loss = criterion(outputs, lables)
flood = (loss - b).abs() + b  # This is it!
optimizer.zerograd()
flood.backward()
optimizer.step()
```  
  