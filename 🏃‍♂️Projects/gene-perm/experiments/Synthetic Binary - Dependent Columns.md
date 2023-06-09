---
tags: experiment
wandb: https://wandb.ai/alongnn/gene-perm-v1/table?workspace=user-alongnn 
config: synthetic-dep-cols
---


settings:: [[Observable Genes vs. Decoy Genes]] 
## Data Generation

- We create a $\{-1,1\}^{m \times d}$ matrix as follows:
- For each row, we put $+1$ in random $d/2$ columns and $-1$ in the rest.
- A single input example is generated as follows:
	- select a *block* consisting of $b$ random rows.
	- choose a random binary label $y \in \{0,1\}$. 
	- if $y=1$, choose a random column $j \in [d]$ and replace the elements in this column with $b$ randomly drawn i.i.d. Bernoulli RV.
	- if $y=0$, we leave the block intact.
	- send the block as $x$ and $y$ as the label.

### Model
To motivate our construction we make the following observations:
- The rows of negative examples ($y=0$) are balanced, i.e., sum to $0$. 
- On the other hand, positive examples's rows are either positive or negative with equal probability. 
- Therefore, by summing over the features, taking absolute value and averaging over the block rows, we should be able to distinguish between positive and negative examples.
- We therefore consider the following model:

```python
# B = batch size, b = block size, d = dim
f1 = nn.Linear(d,1) 
f2 = nn.lLinear(1,1) 


z = f1(x) # x is B x b x d -> f1(x) is B x b x 1
u = torch.abs(z)
v = torch.sign(z) # notaional only
q = torch.mean(u)
s = f2(q)
y_pred = nn.Sigmoid()(x)
```




## Results


#### Single Hidden Layer

- Dim=100
![](https://i.imgur.com/Mc5M3wy.png)


- Dim=300

![](https://i.imgur.com/DJTE5oE.png)


### Questions


> [!question] Does Embedding Help?   #next 
> Does Embedding Help in this case?



> [!question] Why adding more layers seem to hurt?      #next
>  Wrong architecture?

## Appendix

### Differentiation

Let's differentiate (with blocks of size $b=1$).
$$
\begin{align*}
&z = w^\top x := f_1(x) \\
&u = |z| \\
&v = \mathrm{sgn}(z) ~~~~~~~~~\textrm{(notational)}\\ 
&q = b^{-1}\,\sum u_i \\
&s = f_2(q) \\
&y_{\textrm{pred}} = \sigma(s)
\end{align*}
$$

$$
\begin{align*}
\frac{dq}{dw_j} = \frac{dq}{du} \frac{du}{dz}\frac{dz}{dw_i} 
= (b^{-1},\ldots,b^{-1})^\top \mathrm{diag}(v)(x_{1,j},\ldots,x_{b,j} )
\end{align*}
$$

