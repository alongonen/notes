

- We would like to work with the most updated versions of `torch`, `lightning`, etc.
- However, `scgen` works with outdated versions.
- What about using [optional environments in poetry](https://python-poetry.org/docs/managing-dependencies/)? Well, poetry insists that all dependency groups should be consist with each other.
- Instead, 
	- clone `scgen` and associate with it another poetry environment while using `scgen` dependencies
	- add `perturbx` basic dependencies that, i.e. that doesn't contain all model dependences (e.g. `torch`)
- 