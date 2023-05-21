```toc
```

## Introduction 

### Why?

Use correlations between genes in RNA-seq data to find meaningful gene representations.

### How?

- Train a model to identify permutations in the gene expression.

### Considerations

- **Conditions**: Different conditions contribute to variability. Maybe we need to “inform” the model regarding the conditions.

- **Single cells vs. k cells vs. bulk**: Single cells give more variability but also harder to distinguish between genes (e.g. due to dropouts).

- **Anchor Genes**: Curse of dimensionality - number of genes taken into account (also named *anchor genes*). Greater dimensionality -> more information but more complexity.

- **Which genes** should be permuted?

  - Permute two fixed genes from the anchor genes? -> Train one model per pair?
    - Permuting two dominant genes yields a harder task. On the other hand, permuting a dominant gene with non-dominant gene yields a easier task. 
    - Harder might be better for learning non-trivial patterns/correlations.

- **Order of genes** seems to be important. We should take that into account when considering more datasets.

  

### Current Effort

- Data and input: 
  - Mixseq
  - single cells 
  - permuting fixed pair of genes
  - Conditions are not presented to the model
  - We compute the most dominant genes based on the differential expression 
- model:
  - MLP with varying number of hidden layers and hidden dimensions. (Each layer consists of a linear layer, ReLU and dropout)

---

## Results

### Complex model allows higher dimensionality

 <!--tb subproject: hidden_dims-->

- When using a single hidden layer, presenting more genes (`input_dim`$\ge 30$) deteriorates the accuracy of the model. Note that with `input_dim`$=2$ we already reach a reasonable accuracy (approx. 0.76). But presenting two genes severely limits the amount of information we can extract.

![image-20230227112126085](https://p.ipic.vip/gfzpmd.png)

%%
![image-20230227112103176](https://p.ipic.vip/64dbao.png)
%%



- Adding more layers enables us to increase the input dimension.

![image-20230227112552553](https://p.ipic.vip/2hq3rd.png)

![image-20230227105332439](https://p.ipic.vip/lkawfg.png)

### Relative Rank

 <!--tb subproject: relative_rank-->

Here we investigate the choice of the permuted pair. Each pair is associated with two indices representing their variability rank. The general trend we see is that the more distant are the genes (in terms of their rank), the easier is the task. However, there are few exceptions (e.g. [5,6] is easier than [0,20]). 



![image-20230301130630443](https://p.ipic.vip/g0zqb8.png)



### From single cells to k cells

- Instead of  single cells, we now divide the data into chunks of size $k$, such that each example now consists of $k$ single cells, i.e., a matrix of size $k \times d$, where $d$ is the number of genes presented to the algorithm. For fach of these matrices, we decide whether to permute the fixed pair of genes we chose in advance.
- This clearly reduces the noise associated with dropouts, etc.
- We start by considering a single 128-dimensional hidden layer. 
- The results below show that for relatively small values of k (k>4), the problem becomes rediculously easy. For example, with a single hidden layers and $k=5$ we get an accuracy of 0.98 (whereas with $k=1$ we got an accuracy of 0.79).



![image-20230301140444388](https://p.ipic.vip/mdb31t.png)



### Adversarial Blocks

<!--adv_blocks-->

- Instead of permuting fixed two genes from the anchor genes, we fix only a single gene from the anchor genes and select the second one in adversarial manner from the list of non-anchor genes. Specifically, for each block we choose the gene whose expression is closest to the fixed anchor gene (according to Euclidean distance).
- As we see below, the best accuracy is close to 1.00

- With $k=1$ the best performance is 0.73. Recall that with non-adversarial choice (of the second gene), the accuracy was 0.87.

![image-20230312140951480](https://p.ipic.vip/7qwkmx.png)

- With number of anchor genes $\le 6$, the best accuracy is around 0.87.

![image-20230312141139283](https://p.ipic.vip/smcq6l.png)











---

## TODOS



### Next steps

- [ ] 

### Main TODOS

- [x] k cells

### Code Infrastructure








​	
