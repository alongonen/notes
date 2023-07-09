---
tags: setting
---


## Setting Overview
- Our data consists of gene expression of **single cells**. 
- Therefore, the entire data can be described by a matrix $n \times d$ whose rows correspond to single cells, and its columns correspond to **genes**.
- We aggregate several single cells (rows) into *blocks* of size $b$.
- We often restrict the dimensionality restrict the input of the model to $k\ll d$ (fixed) columns (genes).


## Data Generation
A single input example is a triplet $(x,y,g)$ which is generated as follows:
- select a *block* consisting of $b$ random rows.
- choose a random binary label $y \in \{0,1\}$. 
- if $y=1$, choose a random column $g \in [d]$ and replace the block's $g$-th column with a random column $j$.
- if $y=0$, we leave the block intact.