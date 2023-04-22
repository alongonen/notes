
## Preliminaries


### Strassen Normal Form

- Given $A, B \in \mathbb{R}^{n \times n}$ we approximate $C = AB$ using
  $$
 \begin{align*}
 &\tilde{C} = W_C \left((W_A A) \circ (W_B B) \right) \\
 &W_A, W_B \in \{-1,0,1\}^{r \times {n^2}}~~,W_c \in \{-1,0,1\}^{n^2 \times r}~,~~~~~r \in \mathbb{N} 
 \end{align*}
 $$
 where $\circ$ stands for component-wise multiplication. 

![[Strassen Normal Form | 700]]
-  **Motivation**: the operations of $W_A, W_B$ only involve additions. Therefore, we the number of multiplications is $r$. When $r \ll n^3$ we significantly reduce the number of multiplications. It's worth mentioning that:

**Lemma 1:** For $r = n^3$ we can exactly compute $C$. 

- See proof [[#^e98a1d|below]].
- We can do better using [Strassen algorithm](https://en.wikipedia.org/wiki/Strassen_algorithm) who showed that $r=7$ suffices for exact computation with $n=2$. 
- We can easily generalize the above to non-square matrices $A \in \mathbb{R}^{m \times n}, B \in  \mathbb{R}^{n \times k}$.

### Unfolding convolutions
- Assume images of size $c_{in} \times W \times H$. 
- Consider a 2-dimensional convolution layer with *kernel* of size $k \times k$, $\textrm{stride}=1$ and $c_{out}$ output channels.  
- For each output channel we vectorize the associated filter into a row vector of size $c_{in} k^2$.  Stacking these vectors we obtain a matrix $A$ of size $c_{out} \times c_{in}k^2$.    
- For every  every pixel $(i,j)$ and input channel, we consider the patch associated with the coordinates $(s,t)$ for $s \in \{i,i+1,\ldots, i+k-1\},~t \in \{i,i+1,\ldots, i+k-1\}$. For each pixel $i,j$ we vectorize the corresponding $c_{in}$ patches and concatenate them into a column vector of size $c_{in}k^2$. Let $B$ be the resulted matrix.
- It is seen that $C=AB$ is equal to the outcome of the convolution operation.

![[Unfolding Convolution|700]]


## Application to ResNets
### Inefficient Direct application 
In the context of image classification using ResNet, it is natural to consider the following approach:  
- Unfold each 2D-CONV operation,, resulting in matrices $A,B$ that correspond to the filter and the data images, respectively.
- Approximate the corresponding matrix multiplication using SNF. Hopefully, we won't sacrifice too much accuracy by using small values of $r$. 
However, this approach yields large matrices $W_A, W_B, W_C$ with shapes
$$
r \times {c_{out} c_{in} k^2}~,~~r \times c_{in} k^2WH~,~~ c_{out}WH \times r~,
$$
respectively.

### Broadcasting along image dimensions
Instead of learning a weight matrix $W_B$ with respect to the entire image, we can utilize the structure of $B$ and apply $W_B$ to single columns of $B$ (which correspond to single patches in the image). Importantly, we will learn a single $W_B$ (also single $W_A$ and $W_C$) for all the columns (rather than $WV$ weight matrices).   


> [!NOTE] Broadcasting
> We consider approximation of $WV$ matrix multiplications, $AB^{(1)}, \ldots, AB^{(WV)}$,  where $B^{(1)}, \ldots, B^{(WV)}$ are the columns of $B$ (corresponding to single patches in the image), using fixed weight matrices $W_A, W_B, W_C$. 

### Another simplification
Note that both the matrix $W_A$ and $A$ are learned during the training. Hence, it makes sense to directly learn the $r$-dimensional product $\tilde{a}:=W_A A$.  
The resulted approximation is:
$$
\begin{align*}
\tilde{c} &= W_C  \begin{pmatrix} | & | & | \\
  \tilde{a} \circ (W_B B^{(1)}) & \cdots & \tilde{a} \circ (W_B B^{(WV)}) \\  | & | & | \end{pmatrix} = W_C \left(\tilde{a} \circ \begin{pmatrix} | & | & | \\
  W_B B^{(1)} & \cdots &  \circ W_B B^{(WV)}  \\  | & | & | \end{pmatrix} \right) \\& = W_C \left(\tilde{a} \circ (W_BB) \right)
  \end{align*}
$$
where the second $\circ$ is interpreted as a broadcast component-wise multiplication between $\tilde{a}$ and the columns $W_B B^{(1)}, \ldots, W_B B^{(WV)}$. 
### Back to (ternary) convolutions
- Due to the structure of $B$, the product $W_B B$ is actually a convolution with $c_{in}$ input channels, $r$ output channels and kernel dimensions $(k,k)$.  
- The product $W_C \left(\tilde{a} \circ (W_BB) \right)$ can be seen as convolution with $c_{out}$ output channels, $1$ input channel and  kernel dimensions $(3,3)$.

### Realizing local spatial compression
#TBA

## Omitted Proofs

^e98a1d

### Proof of Lemma 1 
Let's introduce some notation first. For $e,f,g,h,\ell \in [n]$, denote by
$$
\begin{align*}
&(W_{A})_{e,f,g,h,\ell} = (W_A)_{(e-1)n^2 + (f-1)n + g,n(h-1)+\ell} \\
&(W_{B})_{e,f,g,h,\ell} = (W_B)_{(e-1)n^2 + (f-1)n + g, n(h-1)+\ell} \\
&(W_C)_{h,\ell, e,f,g} = (W_{C})_{ n(h-1)+\ell, (e-1)n^2 + (f-1)n + g} \\
& \tilde{c}_{h,\ell} = \tilde{c}_{n(h-1)+\ell}
\end{align*}
 $$
 Then for $h,\ell \in [n]$ we have
   
   
   
   $$
 \tilde{c}_{h,\ell} = \sum_{e,f,g}(W_C)_{h,\ell, e,f,g} \left(\sum_{i,j} (W_A)_{e,f,g,i,j}A_{i,j}\right)\left(\sum_{i,j} (W_B)_{e,f,g,i,j}B_{i,j}\right)
 $$
 Setting
 $$
 \begin{align*}
(W_{C})_{h,\ell,e,f,g} = \mathbb{1}_{e=h,~f=\ell}\\
(W_{A})_{e,f,g,i,j} = \mathbb{1}_{e=i,~f=j,~g=j} \\
(W_{B})_{e,f,g,i,j} = \mathbb{1}_{e=i,~f=j,~g=i}
\end{align*}
$$
yields
$$
\tilde{c}_{h,\ell} = \sum_{g}\underbrace{(W_C)_{h,\ell, h,\ell,g}}_{1} A_{h,g} B_{g,\ell} = \sum_{g} A_{h,g} B_{g,\ell} = C_{h,\ell}.  
$$
Q.E.D.

