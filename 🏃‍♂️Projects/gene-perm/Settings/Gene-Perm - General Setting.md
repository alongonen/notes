---
tags: setting
---


## Setting Overview
- Our data consists of gene expression of **single cells**. 
- Therefore, the entire data can be described by a matrix $n \times d$ whose rows correspond to single cells, and its columns correspond to **genes**.
- We aggregate several single cells (rows) into *blocks* of size $b$.
- We often restrict the dimensionality of the input to $k\ll d$ (fixed) columns (genes). We call them *primary genes*, whereas the other column are called *decoy genes*.


## Data Generation
A single input example is a triplet $(x,y,g)$ which is generated as follows:
- select a *block* consisting of $b$ random rows.
- choose a random binary label $y \in \{0,1\}$. 
- if $y=1$, permute the block's columns.
- if $y=0$, we leave the block intact.

Different settings correspond to different permutation mechanisms




## Questions


> [!question] Memorization #next
> Each example appears many times both in positive and negative blocks. This allows memorization. How can we avoid that?

^a031a2




