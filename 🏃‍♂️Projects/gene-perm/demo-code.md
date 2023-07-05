
```js
function hello(name) {
	console.log(`Hello ${name}!`);
}

hello("Bob")
```




```python
import seaborn as sns
import torch
import matplotlib.pyplot as plt
sns.set_style("darkgrid")
iris = sns.load_dataset('iris')
sns.FacetGrid(iris, hue ="species", height = 5).map(plt.scatter, 'sepal_length', 'petal_length').add_legend()

plt.show()
```


