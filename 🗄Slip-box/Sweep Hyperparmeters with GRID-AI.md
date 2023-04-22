
## Sweep Hyperparameters with GRID-AI


---
## GRID-AI: Background
- Provides (both web and cli) infrastructure for running experiments in scale.
- Integrates with AWS or any custom cluster.
- Main modules:
	- datastore
	- run
	- **session**

---
### Additional Features
	- Access via notebooks, cli, 
	- ssh interpreter
	- spot instances

---


![](https://i.imgur.com/IdWAO5C.png)



Under the hood GRID-AI creates a GPU instance and for each of the 16 configurations.

---
## WANDB Sweeps

- [Weights and Biases also support sweeps](https://docs.wandb.ai/guides/sweeps/quickstart) while providing nice visualizations of the importance of each hyperparameter.
- However, the user has to initialize each agent.

