---

kanban-plugin: basic

---

## Code: Infrastructure

- [ ] `test_step` with optional save predictions to dataframe @{2023-05-04}
- [ ] DDP with multiple GPUs @{2023-05-18}
- [ ] `learning_curve` callback
- [ ] instantiating datamodule and model with hydra
- [ ] logging_utils: delete log_hyperparams?
- [ ] wandb: integrate and [update config with hydra](https://docs.wandb.ai/guides/integrations/hydra)
- [ ] [[Solving Conflicts between perturb-x and scgen with Poetry]]


## Code: Preprocessing

- [ ] duplicating control for every perturbation is redundant @{2023-05-04}


## Model

- [ ] Discrepancy in Latent Space <br>- MMD vs other penalties <br>- s
- [ ] gene weights
- [ ] adding noise needed
- [ ] selection layer
- [ ] l1, l2 reg needed


***

## Archive

- [x] ## Sciplex chemCPA<br>- [x] splits
- [x] `config_l1000`

%% kanban:settings
```
{"kanban-plugin":"basic","append-archive-date":false,"archive-with-date":false,"link-date-to-daily-note":false}
```
%%