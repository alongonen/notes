

![[sweep-pipe.excalidraw|30000]]


## Workflow

-   Create a `yaml` configuration file as above.
	- **program**: path to python script
	- **method**: search method (Grid/Random/Bayes)
	- **Parameters**: 
		- configurable parameters (from the primary config) and their associated ranges.
		- when using either Random or Bayes search strategy, ranges may correspond to distributions. See usage in [W&B docs](https://docs.wandb.ai/guides/sweeps/configuration#method).
-   The `parameters` section in this config should contain parameters from the primary config of the script. This primary config should be integrated into the `wandb` initialization.
-   Run the sweep command: 
```shell
wandb sweep —project <project name> <path to sweep config file>
```
-   Receive the command to run from any agent (starting with `wandb agent)`

## Advanced features
### Bayes search strategy
- Bayes is the most advanced search strategy. 
- As opposed to "Random", the choice of parameters is based on previous runs, where the underlying idea is to create a surrogate that simulates the dependence between the desired metric and the searched Hyperparameters. Over time, the confidence intervals around the surrogate tighten, and the search focuses on promising regimes.


### Early termination
[Wandb Docs](https://docs.wandb.ai/guides/sweeps/configuration#early_terminate)
- Hyperband early termination strategy:
	- divide the run into brackets of lengths 
$$
	\eta \cdot \textrm{min\_iter}~,~ \eta^2 \cdot\textrm{min\_iter}~, ~\ldots
$$
- Example configuration: 
	- default val of $\eta$: 3
```yaml
early_terminate:
  type: hyperband
  min_iter: 3
```

which yields the following brackets.
```python
[3, 3*eta, 3*eta*eta, 3*eta*eta*eta] = [3, 9, 27, 81]
```


#### Example

![](https://i.imgur.com/S06B9qy.png)
