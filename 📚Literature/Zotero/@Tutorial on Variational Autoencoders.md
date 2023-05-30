---
title: Tutorial on Variational Autoencoders
authors: Carl Doersch
year: 2021
status: toread
---

notes: <h1>Annotations
 (12/11/2022, 8:37:10 PM)</h1> 

“get examples X distributed according to some unknown distribution Pgt(X), and our goal is to learn a model P which we can sample from, such that P is as similar as possible to Pgt.” (Doersch, 2021, p. 2) 

“variatonal Bayesian methods and “minimum description length”” (Doersch, 2021, p. 2) 

“latent variable.” (Doersch, 2021, p. 3) 

“f(z; θ” (Doersch, 2021, p. 3) 

“P(X|z; θ) = N (X| f(z; θ), σ2 ∗ I)” (Doersch, 2021, p. 3) 

“some z” (Doersch, 2021, p. 3) 

“needs to result in samples that are merely like X” (Doersch, 2021, p. 4) 

“the output distribution is not required to be Gaussian:” (Doersch, 2021, p. 4) 

“avoid deciding by hand what information each dimension of z encodes” (Doersch, 2021, p. 5) 

“P(X) ≈ 1 n ∑i P(X|zi)” (Doersch, 2021, p. 7) wrong.. 

“Since P(X|z) is an isotropic Gaussian, the negative log probability of X is proportional squared Euclidean distance between f (z) and X.” (Doersch, 2021, p. 7) 

“[Q(z|X)kP(z)]” (Doersch, 2021, p. 8) 

“P(z|X) is not something we can compute analytically” (Doersch, 2021, p. 9) 

“X” (Doersch, 2021, p. 10) only P(z)

---
