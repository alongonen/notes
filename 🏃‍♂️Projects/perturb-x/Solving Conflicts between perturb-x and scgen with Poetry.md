

- We would like to work with the most updated versions of `torch`, `lightning`, etc.
- However, `scgen` works with outdated versions.
- What about using [optional environments in poetry](https://python-poetry.org/docs/managing-dependencies/)? Well, poetry insists that all dependency groups should be consist with each other.
- Instead, we can clone `scgen` and associate with it another poetry environment while using `scgen` dependencies together with `pertur`