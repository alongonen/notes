
```python
import anndata as ad
import scanpy as sc
path = '/Users/alongonen/sciplex.h5ad'
adata = sc.read(path)
```


## Indexing

We can index AnnData both using row numbers and row indices. The following lines yield the first line of the observations dataframe associated with the AnnData.

```python
adata[0].obs
```

```python
adata['AAACCTGAGAGCAATT-1-0'].obs
```

```python
print(adata.obs.iloc[0])
```