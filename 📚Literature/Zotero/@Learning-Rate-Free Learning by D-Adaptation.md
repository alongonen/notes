---
title: Learning-Rate-Free Learning by D-Adaptation
authors: Aaron Defazio, Konstantin Mishchenko
year: 2023
tags: []
status:
---
## Annotations  
(8/7/2023, 3:16:29 PM)

> “automatically setting the learning rate which asymptotically achieves the optimal rate of convergence for minimizing convex Lipschitz functions” 

> “first hyper-parameter free method for this class without additional multiplicative log factors” 

## Main Result

- Extensive experiments validate the the theory.
- In practice, when optimizing non-convex losses, LR scheduling is necessary. The adaptive step size in this paper doesn’t replace scheduling .   

## Implementation

[Github](https://github.com/facebookresearch/dadaptation)

## Context
- Standard upper bound of (Online) Gradient Descent:  
$$
\frac{\|w_0 - w^\star\|^2}{\eta} + \frac{\eta}{2} \sum \limits _{t=1}^T \|g_t\|^2 
$$
   where $\eta$ is a fixed step size, $w_0$ is the initial iterate, $w^\star$ is an optimal solution, and $g_t$ is the gradient at time $t$. 
- Optimal tuning of the step size:
    $$
    \eta^\star = \frac{\|w_0-w^\star\|}{\sqrt{\sum \limits _{t=1}^T \|g_t\|^2}}
	$$
- This optimal tuning requires knowledge of the initial distance to the minimizer and also knowledge of (the magnitude) of future gradients.
- However, both are not known in general.
- The first requirement can be replaced by an upper bound on Lipschitzness of the loss function, when applicable.    
- Adaptive methods such as _AdaGrad_ resolves the the first requirement without assuming Lipschitzness.
- The second requirement can be replaced by an upper bound on the diameter (i.e. global bound on the model’s weights), when applicable.
- This work completely resolves the second requirement without making such assumption.
    
## Description
- The step size has two components, namely, $\gamma_t$ and $d_t$. The first component normalizes  the gradient magnitudes. It is defined as
$$
\gamma_{k+1} = \frac{1}{\sqrt{\sum\limits _{i=0}^{k}\|g_i\|^2}}
$$
- In Dual Averaging we maintain a weighted sum of the gradients. The iterate at time t is
$$
\hat{d}_{k+1} = \frac{\gamma_{k+1} \|s_{n+1}\|^2 - \sum \limits _{i=0}^k \|g_i\|^2}{2 \|s_{k+1}\|}
$$
$$d_k = \max \{d_{k-1}, \hat{d_k}\}$$
$$s_{k+1} = s_k + d_k g_k$$
## Additional Relevant Papers

- **DoG is SGD’s Best Friend: A Parameter-Free Dynamic Step Size Schedule:** worse by some logarithmic factors.
    

- **Prodigy: An Expeditiously Adaptive Parameter-Free Learner:** follow-up paper that attempts to close the gap discussed above between GD and Dual Averaging.

