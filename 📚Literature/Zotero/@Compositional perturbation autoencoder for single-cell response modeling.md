---
title: Compositional perturbation autoencoder for single-cell response modeling
authors: Mohammad Lotfollahi, Anna Klimovskaia Susmelj, Carlo De Donno, Yuge Ji
year: 

---

notes: <h1>Annotations
 (12/13/2022, 2:21:14 PM)</h1> 

“What would have the gene expression of this 140 cell looked like, had it been treated differently?” (Lotfollahi et al., p. 4) rather than generating from scratch, we fix the input to the encoder and use different attributes 

“uncertainty” (Lotfollahi et al., p. 4) 

“MDM2” (Lotfollahi et al., p. 5) gene 

“Nutlin” (Lotfollahi et al., p. 5) perturbation 

“To demonstrate OOD properties, we withhold cells 157 exposed to the second to the largest dose among all drugs” (Lotfollahi et al., p. 6) 

“most of the drugs at the highest dosage” (Lotfollahi et al., p. 6)

---

# Notes


## Method

![](https://media.heptabase.com/v1/images/25a8d397-455e-4251-a2e7-8e34a8dffd4d/d401ac47-8900-458a-8d5d-7a2cdf647371/image.png)

* Discriminator’s role is to disentangle the attributes from the expression.

* &nbsp;

### Encoding

![](https://media.heptabase.com/v1/images/25a8d397-455e-4251-a2e7-8e34a8dffd4d/139fce71-267c-41a1-9729-c218edbc5d22/image.png)

* where $d_{i,j}$ is the dosage of perturbation $j$ applied to cell $i$.

* $c_{i,j}$: additional covariates

&nbsp;

### Uncertainty estimation

* Estimate either cosine or Euclidean metric between latent queries example and each example in the train. 

* Pick the minimal distance.

![](https://media.heptabase.com/v1/images/25a8d397-455e-4251-a2e7-8e34a8dffd4d/7b48f5ea-a9ad-4b0b-9e42-34191dae5955/image.png)

![](https://media.heptabase.com/v1/images/25a8d397-455e-4251-a2e7-8e34a8dffd4d/c6b0ecda-e196-4729-b6eb-73952e8145b4/image.png)

### Decoding

**TBA**

## Sciplex2

* Fit unseen dosage (red circles)

* Here we choose the *MDM2* gene which exhibits large differential expression on the *Nutlin* cell line.

* the unseen dosage of Nutlin is predicted well whereas some seen/observed dosages of BMS are predicted poorly

&nbsp;

![](https://media.heptabase.com/v1/images/25a8d397-455e-4251-a2e7-8e34a8dffd4d/17401005-1eb6-4569-8b2f-7a44df01bd61/image.png)