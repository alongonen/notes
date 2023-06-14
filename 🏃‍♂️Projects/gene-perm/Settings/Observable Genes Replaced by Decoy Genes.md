---
tags: setting
---

- Our data consists of gene expression of **single cells**. 
- Therefore, the entire data can be described by a matrix whose rows correspond to single cells, and its columns correspond to **genes**.
- We aggregate several single cells (rows) into *blocks* of size $b$.
- We often restrict the dimensionality restrict the input of the model to $d\ll n$ (fixed) columns (genes).


- A single input example $(x,y,g)$ is generated as follows:
	- select a *block* consisting of $b$ random rows.
	- choose a random binary label $y \in \{0,1\}$. 
	- if $y=1$, choose a random column $g \in [d]$ and replace the block's $g$-th with another column (possibly from the entire set of $n>d$ genes)
	- if $y=0$, we leave the block intact
	- send the block as $x$ and $y$ as the label.
- Each input to the model is a triplet $(x,y,g)$:
	- $x$: a random block, i.e., a matrix of size $b \times d$
	- $y \in \{0,1\}$: binary label
	- $g \in [d]$
	- if $y=0$, 

## Notation

- $d$: (observable) dimension 
- $m$: number of samples (might be train/val/entire data depending on the context)
- $b$: block size
- $x$: a block, i.e. a matrix of size $b \times d$
- $y$: each $x$