


> [!question] Upper Triangular Sampling
> How to sample a pair $(i,j) \in A_n := \{(k,\ell): 1\le k \le \ell \le n \}$ uniformly at random?

Instead of sampling from $A_n$ we sample from $B_n := \{1,\ldots,n(n+1)/2\}$ and utilize a bijection between these sets. 

Here's a straightforward bijection from $A_n$ to $B_n$. 
$$
f((i,j)) \mapsto S_{i-1}+j-i+1
$$
where $S_0 = 0$ and for any $1 \le i \le n$, 
$$
S_i = n + (n-1) + \ldots + (n-i+1) = \frac{(n+n-i+1)(i-1)}{2}
$$
How can we compute $f^{-1}$? Given $m \in B_n$, we first need to find the first index $i$ such that $S_{i-1}\le m \le S_i$. Using the definition of $S_i$, this amounts to finding the roots of a quadratic function (with the variable $i$). We then let $j = m - S_{i-1} + i - 1$. 