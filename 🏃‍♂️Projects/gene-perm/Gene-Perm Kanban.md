---

kanban-plugin: basic

---

## In Progress

- [ ] ### Verify DataLoader @{2023-06-19}
- [ ] ### to consider <br>- one-hot / fixed embeddings / nothing<br>- [[Ranking Genes for Permutations|highly variable genes]]<br>- Jeremy: maybe fixed small representation with different genes
- [ ] ### synthetic data<br>- questions in [[Synthetic Binary - Dependent Columns]]
- [ ] ### Gaussian Synthetic
- [ ] ### Finish MLP<br>- [no activations in last hidden and classifier?](https://github.com/facebookresearch/multimodal/blob/5dec8a/torchmultimodal/modules/layers/mlp.py)<br>- classifier + sidmoid should be part of the MLP


## Next

- [ ] ### Additional datasets (sciplex?)
- [ ] ### conditions<br>[[How Conditions Are Relevant For Permutations?]]
- [ ] ### No Order<br>permute examples to discard positions?
- [ ] ### Differentiable Pooling


## Someday

- [ ] ### sweep<br>- wandb integration<br>- from config
- [ ] ### embeddings vs finetuning
- [ ] ### ddp with more gpus
- [ ] ### structured config<br>allows boolean conditions (e.g. `use_embed` depend on `baseline_mode`)


## Inbox
- [ ] contrastive




---

## Archive

- [x] Infrastructure<br>- [[Gene-Perm With Wandb|use wandb]]<br>- efficient sweep @{2023-05-22}
- [x] ### recall status and update missing reports @{2023-05-22}
- [x] ### new setup <br>[[gene-perm modeling.canvas]]
- [x] delete code<br>- ~~one of the data creation file~~



%% kanban:settings
```
{"kanban-plugin":"basic"}
```
%%