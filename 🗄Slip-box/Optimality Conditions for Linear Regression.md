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

## Regimes of Parameterization

$$
X = \sum_{i=1}^r \sigma_i u_i v_i^\top \,\,\,\,\,,\,\,\,\,\,\, y=\sum_{i=1}^n \beta_i v_i
$$
$$I = \{i \in [N]:\,\beta_i >0 \}$$
$$
w^\star = A ^\dagger b= \sum_{i \in I \cap [r]} \sigma_i^{-1} \beta_i u_i \Rightarrow X^\top w^\star = \sum_{i=1}^r \beta_i v_i = \Pi_{X^\top}(y)
$$
Equivalent solutions:
$$
W^\star = \left \{w^\star + \sum_{i \in [r] \setminus [I]} \alpha_i u_i :\,\,(\forall i) ~~ \alpha_i \in \mathbb{R} \right\}
$$




| Regime            | Interpolation | Deg. of Freedom                | $I$ vs. $[r]$ |
| ----------------- | ------------------------ | ----------- | -----|
| Underparam.       | $Y \notin X^\top W^\star$ | - |$I \not \subseteq [r]$       |
| Critically param. | $Y = X^\top W^\star$      | $W^\star = \{w^\star\}$ | $I=[r]$       |
| Overparam.        |  $Y = X^\top W^\star$|  $\{w^\star\} \subsetneq W^\star$      |    $I \subsetneq [r]$         |

