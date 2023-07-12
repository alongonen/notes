
## FSD
- $X = [a,b] \subseteq \mathbb{R}$ 
- $f: X \rightarrow Y$ is a low degree polynomial, say $f(x)=4(x-2.5)^2$.
- Training sample: 
  $$x = (0,1, 2,3,4,5), ~~y = (25,9,1,1,9,25)$$.

![](https://i.imgur.com/IAUndgH.png)

- Model: a shallow neural net with one hidden layer.
  
  $$x \mapsto w^\top (\phi_1(x), \ldots, \phi_d(x))$$where