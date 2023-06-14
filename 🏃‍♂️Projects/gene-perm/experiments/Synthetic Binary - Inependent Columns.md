---
tags: experiment
wandb: 
config: synthetic-ind-cols
---


settings:: [[Observable Genes vs. Decoy Genes]] 
## Data Generation

- We create a $\{-1,1\}^{m \times d}$ matrix whose cells are drawn i.i.d. from $\mathrm{Ber}_{\pm 1} (1/2+\epsilon)$, where $\epsilon$ is a
- A single input example is generated as follows:
	- select a *block* consisting of $b$ random rows.
	- choose a random binary label $y \in \{0,1\}$. 
	- if $y=1$, choose a random column $j \in [d]$ and replace the elements in this column with $b$ i.i.d. RV drawn from $\mathrm{Ber}_{\pm 1} (1/2)$
	- if $y=0$, we leave the block intact.
	- send the block as $x$ and $y$ as the label.

### Model
#TBA 
