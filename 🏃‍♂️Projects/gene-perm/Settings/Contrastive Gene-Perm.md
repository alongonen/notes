---
tags: setting
---



## Setting Overview
- Our data consists of gene expression of **single cells**. 
- Therefore, the entire data can be described by a matrix whose rows correspond to single cells, and its columns correspond to **genes**.
- Show both 
- We aggregate several single cells (rows) into *blocks* of size $b$.
- We often restrict the dimensionality restrict the input of the model to $d\ll n$ (fixed) columns (genes).


## Data Generation
- A single input example is a triplet $(x,y,g)$ which is generated as follows:
	- select a *block* consisting of $b$ random rows.
	- choose a random binary label $y \in \{0,1\}$. 
	- if $y=1$, choose a random column $g \in [d]$ and replace the block's $g$-th with another column (possibly from the entire set of $n>d$ genes)
	- if $y=0$, we leave the block intact








## Notation

- $d$: (observable) dimension 
- $m$: number of samples (might be train/val/entire data depending on the context)
- $b$: block size
- $x$: a block, i.e. a matrix of size $b \times d$
- $y$: each $x$




## Some

how permutations are used in machine learning

Permutations are used in machine learning in various ways:

1. Feature Engineering: Permutations can be used to generate new features or transform existing ones to improve the predictive power of a model. For example, feature permutation importance is a technique that computes the importance of each feature in a model by permuting its values and measuring the decrease in performance.

2. Ensemble Methods: Permutations can be used to create ensembles of models that have different permutations of the training data or features. This helps to reduce overfitting and improve generalization.

3. Hyperparameter Tuning: Permutations can be used to search for optimal hyperparameters for a model. This involves creating multiple permutations of hyperparameters and evaluating their performance on a validation set.

4. Data Augmentation: Permutations can be used to augment the training data by generating new instances through random permutations or shuffling.

5. Reinforcement Learning: Permutations can be used as actions in reinforcement learning algorithms where the goal is to learn a policy that maximizes rewards over time. The agent selects actions based on permutations of the state space and learns from the resulting rewards.