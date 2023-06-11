---
tags: experiments
wandb: 
config: synthetic2
---

### Gene-Perm Synthetic Data
Data Generation
- We create a $\{\pm 1\}^{m \times d}$ matrix as follows:
- For each row, we put $+1$ in random $d/2$ columns (chosen uniformly without replacement). In the rest of the columns we put $-1$. 
- A single input example is generated as follows:
	- select a block of $b$ random rows from the table.
	- choose a random binary label $y \in \{0,1\}$. 
	- if $y=1$, choose a random column $j \in [d]$ and replace the elements in this column with $b$ randomly drawn i.i.d. Rademacher variables ($\pm 1$ with equal probability).
	- if $y=0$, we leave the block intact
	- send the block as $x$ and $y$ as the label.

Model
- Note that for any $0$-labeled input, every row is balanced, i.e. sums to $0$.
- On the other hand, for positive example we expect half of its rows to be balanced and the rest unbalanced. 
- Therefore, by summing over the features, taking absolute value and averaging over the block rows, we can distinguish between positive and negative examples.
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

Let's differentiate with $B=1$.
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


