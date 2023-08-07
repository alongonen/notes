
 

> [!question] Prior in VAE #someday 
> VAE: In which cases should we enforce normal distribution?



- Our line of thought: ([[Meeting Gal Dec 12, 2022.pdf]])
	- We enforce normal in order to capture variability within conditions.
	- When latent space also captures variability between different conditions
- However, [[@scGen predicts single-cell perturbation responses]] also captures variability between cells and still enforces normal distribution (rather than mixtures)
- [[@Compositional perturbation autoencoder for single-cell response modeling]] use an adversarial approach for disentangling.
- 

