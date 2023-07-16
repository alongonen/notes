
```python
import numpy as np  
import seaborn as sns  
import matplotlib.pyplot as plt

min_sv = []
max_sv = []
d = 1000
steps = 500
for i in range(0, 2*d+1, steps):  
	x = np.random.randn(d, max(1, i))  
	_, s, _ = np.linalg.svd(x)  
	max_sv.append(s[0])  
	min_sv.append(s[-1])  
plt.plot(list(range(0, 2*d+1, steps)), min_sv, label='min singular value')  
plt.plot(list(range(0, 2*d+1, steps)), max_sv, label='max singular value')  
plt.legend()  
plt.show()
plt.close()
```
