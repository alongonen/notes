
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


```python
import pandas as pd
df = pd.DataFrame({'Animal': ['Falcon', 'Falcon','Parrot', 'Parrot'],
				   'Max Speed': [380., 370., 24., 26.]})
# print(df)
x = df.groupby(['Animal', 'Max Speed'])
for a,b in x:
	print(a)
	print("**")
	print(b)
	print("\n\n\n")

```



