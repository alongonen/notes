

---

#### Excalidraw support
![[bias-variance]]

---



## Traditional Bias Variance Tradeoff

![[bias-variance#^frame=_kmM0rxJWw2LI-vGCRbsq|bias variance|500]]


---

## Modern ML

![[🎨Excalidraw/double descent/bias-variance.md#^frame=kN2aDJNOKtWIG_hcZauKY|modern bias variance]]




---

## Random Matrix Theory

- Draw a tall matrix $A \in \mathbb{R}^{N \times n}$ with i.i.d. $\mathcal{N}(0,1)$ entries.

![](https://i.imgur.com/Z4ydNtP.png)

![](https://i.imgur.com/EK7EZe9.png)

---
## Minimum Singular Value of Random Matrix

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

---

