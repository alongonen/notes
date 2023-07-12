
## FSD
- $X = [a,b] \subseteq \mathbb{R}$ 
- $f: X \rightarrow Y$ is a low degree polynomial, say $f(x)=4(x-2.5)^2$.
- Training sample: 
  $$x = (0,1, 2,3,4,5), ~~y = (25,9,1,1,9,25)$$.

![](https://i.imgur.com/IAUndgH.png)

- Model: we will fit a linear regressor to random features of the data. 
- Formally, consider linear model applied to random features inject non-linearity in a random fashion and a shallow neural net with one hidden layer.
  
  $$x \mapsto w^\top (\phi_1(x), \ldots, \phi_d(x))$$where $\phi_i$ has the form $\phi(x)=|x-t_i|$ for randomly chosen threshold $t_i$. 
- ![[un]]