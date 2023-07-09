

```python
import anndata as ad
import scanpy as sc
path = '/Users/alongonen/sciplex.h5ad'
adata = sc.read(path)
```

```python
adata[0].obs
```