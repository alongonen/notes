
## Keep or Delete
- [ ] learning curve callback 🔽  
- [ ] hooks such as `training_epoch_end` 🔽 
- [x] `ae_tr_model_sets.predict_sets` 🔽 ✅ 2023-05-03
- [x] `matching_penalty==adv` 🔽 ✅ 2023-05-03
- [x] `config_l1000` 🔽 ✅ 2023-05-03
- [ ] `use_ext_attributes` 🔽 
- [x] `num_celltypes`  🔽 ✅ 2023-04-24
- [x] `num_perturbations` 🔽   ✅ 2023-04-24
- [ ] various experiments in experiments folder 🔽 
- [ ] `holdout_dataloader` is not consistent with `LightningDataModule` 🔽 



## Data
- [ ] why do we duplicate the control data for each perturbation? 🔽 
- [x] `num_perturbations=3` in `experiment3`  ✅ 2023-04-24
- [ ] sciplex3 vs. sciplex: number of examples, num genes 📅 2023-05-02 


## Model
- [ ] predict step
- [ ] save the trained model's prediction on hold-out set (using `on_training_end`)


## Trainer
- [ ] progress bar
- [ ] ensure  DDP support with multiple GPUs
