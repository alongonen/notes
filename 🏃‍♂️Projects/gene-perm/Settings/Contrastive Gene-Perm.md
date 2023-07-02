---
tags: setting
---



## Setting Overview
- Our data consists of gene expression of **single cells**. 
- Therefore, the entire data can be described by a matrix whose rows correspond to single cells, and its columns correspond to **genes**.
- Show both 
- We aggregate several single cells (rows) into *blocks* of size $b$.
- We restrict the dimensionality to $d\ll n$ (fixed) columns. This usually corresponds to dominant genes.


## Data Generation
- A single input example is a triplet $(x,y,g)$ which is generated as follows:
	- select a *block* consisting of $b$ random rows.
	- choose a random binary label $y \in \{0,1\}$. 
	- if $y=1$, choose a permutation over a (predefined parameterized) fraction of the genes and permute the columns of $x$ accordingly.  [[Kanban#^48c179|| should we permute only observed or decoy]]










## Notation

- $d$: (observable) dimension 
- $m$: number of samples (might be train/val/entire data depending on the context)
- $b$: block size
- $x$: a block, i.e. a matrix of size $b \times d$
- $y$: each $x$




## Some

