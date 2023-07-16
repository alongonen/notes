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
- Interpolation occurs when $X^\top w^\star = y$, i.e., when 
$$
y \in \mathrm{span}(X^\top)
$$
- The rank of $X^\top$ (typically) increases with the rank.
- Underparameterization: $\mathrm{span}(X^\top)$ is not rich enough.
- Interpolation point occurs when $y$ "enters" the span.
- Overparameterization: $X^\top w =y$ has many solutions. 


| Regime            | Existence | Uniqueness               |
| ----------------- | ------------------------ | ----------- |
| Underparam.       | No | - |$I \not \subseteq [r]$       |
| Critically param. | Yes    | Yes|
| Overparam.        |  Yes| No      |

## GD Converges to Min-Norm Solution
- GD always converges to $w^\star$, which has minimal norm among existi


## Regimes of Parameterization - Detailed

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
Solution exists iff $X^\top w^\star = y$.
If the solution exists, it's unique iff $W \star = \{w^\star\}$.


