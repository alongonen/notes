## Metadata
- #[[Notes📓]]
- Readings::
	- [Tutorial part 1](http://mccormickml.com/2017/10/13/product-quantizer-tutorial-part-1/)
	- [Tutorial part 2](http://mccormickml.com/2017/10/22/product-quantizer-tutorial-part-2/)
	- [Survey](https://www.jstage.jst.go.jp/article/mta/6/1/6_2/_pdf)
	- [Product Quantization paper](https://hal.inria.fr/inria-00514462v2/document)
	- [optimal product quantization](http://kaiminghe.com/cvpr13/cvpr13opq_ppt.pdf)
---
## TLDR
Context: [[Approximate Nearest-Neighbor]]
Goal: reduce representation costs.
Quantization: Mapping points to the index of their nearest centroid.
Using {{alias: [[Clustering]]  clustering}} methods for quantization
To improve accuracy (while preserving efficiency), we split each vector to several sub-vectors (aka products) and cluster each part independently. We associate each point with the product of its nearest centroids.
---

## Illustrative Example
### Original data
50K examples in $\mathbb{R}^{1024}$ 
Memory cost per example: $1024*32/8=4096$ bytes.
![Image Vector Dataset](http://mccormickml.com/assets/ProductQuantizer/image_vectors.png)
### Clustering-based quantization
Run $k$-means to partition data and associate each point with its nearest centroid.
Given a query $x$, return one of training points points associated with its nearest centroid.
Caveat: we need huge value of $k$ to obtain a reasonable accuracy.
    - Huge $k$ would require huge amount of data.
    - More critically, this would require huge amount of computation.
### From centroids to product of centroids
Instead of clustering the entire space vectors, we split each vector into 8 sub-vectors of size 128.
We cluster each of the 8 parts independently using $k=256$.
![Vectors sliced into subvectors](http://mccormickml.com/assets/ProductQuantizer/vector_slice.png)
Each subvector in the training data is associated with its closest centroid.
Each of the original training vectors is thus associated with a product of 8 centroids.
The effective number of clusters is $256^8$!!
However, the runtime is only $8 * (\textrm{runtime of 256-means})$
We need $\log(256)=8$ bits to represent each subvector
$\Rightarrow$ We need 256 bits = 8 bytes to represent each vector!!
### Handling Queries with PQ
Given a query $x$, we approximate its distance from the training point $x_i$ by summing the distances from $x_i$'s centroids.
To save computation we can form a look-up table $A$ of size $8*256$ with all distances between x's subvectors and the relevant centroids.
---
## Theoretical Guarantees


> [!question] k-means -> PG
> Can we translate k-means approximation guarantees into PQ guarantees?


