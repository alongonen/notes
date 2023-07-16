## Linear Regression

$$
X = \begin{pmatrix} | ~~~~~~ ~~~~~~ | \\ x_1 ~\cdots ~ x_n \\ | ~~~~~~~~~~~~ | \end{pmatrix} \in \mathbb{R}^{d \times n}~~~~,~~~~Y = \begin{pmatrix} y_1 \\ \vdots \\ y_n \end{pmatrix} \in \mathbb{R}^n
$$
$$
\begin{align*}
&\min f(w) = \frac{1}{2}\|w^\top X - Y\|^2 \Leftrightarrow \\
&\min \frac{1}{2}w^\top Aw-b^\top w
\end{align*}
$$
where $b = Xy,~A=XX^\top$.

### Opt
$$
w^\star = A^{\dagger} b = X^\dagger y
$$

## Interpolation conditions

$$
X = \sum_{i=1}^r \sigma_i u_i v_i^\top \,\,\,\,\,,\,\,\,\,\,\, y=\sum_{i=1}^n \beta_i v_i
$$
$I = \{i \in [N]:\,\beta_i >0 \}$
$$
w^\star = A ^\dagger b= \sum_{i \in I \cap [r]} \sigma_i^{-1} \beta_i u_i \Rightarrow X^\top w^\star = \sum_{i=1}^r \beta_i v_i = \Pi_{X^\top}(y)
$$
$$
W_r = \left \{\sum_{J} \sigma_i^{-1} \beta_i u_i \right: ~~ i \in I \cap [r]\}
$$



| Regime            | Condition                | $I$ vs. $[r]$ |
| ----------------- | ------------------------ | ----------- |
| Underparam.       | $\Pi_{X^\top}(Y) \neq Y$ | $I \not \subseteq [r]$       |
| Critically param. | $\Pi_{X^\top}(Y)$      | $I=[r]$       |
| Overparam.        |                          |    $I \subsetneq [r]$         |




### Recovery conditions
$X = \sum_{i=1}^r \sigma_i u_i v_i^\top\,\,\,,\,A=\sum_{i=1}^r \underbrace{\lambda_i}_{\sigma_i^2} u_i u_i^\top, \, y=\sum_{i=1}^k \beta_i v_i$     
$b = Xy = \sum_{i=1}^{\min \{k,r\}} \sum \beta_i \sigma_i u_i$.

$$
A ^\dagger b=\sum_{i=1}^{\min \{k,r\}} \sigma_i^{-1} \beta_i u_i = X^\dagger y
$$
$$
X^\top w^\star = \sum_{i=1}^{\min \{k,r\}} \beta_i v_i 
$$
That is, $X^\top w^\star$ is the projection of $y$ onto the span of $X^\top$. It is equal to $y$ if and only if $r \ge k$.