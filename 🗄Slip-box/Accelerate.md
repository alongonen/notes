---
Tags: [[code]]
---

# Accelerate by Hugging Face

---

## Overview
- **DDP** support by [Huggingface]([[../STS/Huggingface]])


---

## Motivation
- Running training/evaluation code on multiple GPUs requires writing and maintaining **boilerplate code**
- Accelerate reduces this effort in a relatively transparent way

---

## Background on DDP

---

![[DP vs. DDP.excalidraw.png]]


---
 
 ## DDP Implementation using Torch.distributed

- Specifying and initializing involved processes 
- Broadcasting the model to all processes
- Partitioning and broadcasting the data
- Broadcasting gradients

---
## Torch Code: Initialization
```python
import os
import torch
import torch.nn.functional as F
from datasets import load_dataset
from torch.utils.data import DistributedSampler
from torch.nn.parallel import DistributedDataParallel

local_rank = int(os.environ.get("LOCAL_RANK", -1))
device = torch.device("cuda", local_rank)
```
---
## Torch Code: Initialization cont’d

```python
model = torch.nn.Transformer().to(device)
model = DistributedDataParallel(model)  
optim = torch.optim.Adam(model.parameters())

dataset = load_dataset('my_dataset')
sampler = DistributedSampler(dataset)
data = torch.utils.data.DataLoader(dataset, sampler=sampler)

```

---
## Torch Code: Train

```python
model.train()
for epoch in range(10):
  sampler.set_epoch(epoch)  
  for source, targets in data:
	  source = source.to(device)
	  targets = targets.to(device)
	  optimizer.zero_grad()
	  output = model(source)
	  loss = F.cross_entropy(output, targets)
	  loss.backward()
	  optimizer.step()
```
## Torch Implementation: More Complications
> “...These changes will make your training script work for multiple GPUs, but your script will then stop working on CPU or one GPU (unless you start adding if statements everywhere)...”

Source: [Introducing accelerate](https://huggingface.co/blog/accelerate-library)

---
## Accelerate: High-level Interface above Torch
- Abstraction for the ab
- Additional complications: fp16, TPU

---

## The Accelerator: Init.
**In**
```python
from accelerate import Accelerator
accelerator = Accelerator()
# define model, dataloader and optimizer)
model, optim, data = accelerator.prepare(model, optim, data)
```
**Out**  
```python
model = model.to(device)
```

---
## The Accelerator: Forward and Backward

```python
+ accelerator.backward(loss)
- loss.backward() 
```

## Additional Pros And Features
- Works with any sampler (does not rely on a *DistributedSampler*)
- Allows running some code on single process using
```python
if accelerator.is_main_process():
	...
else: [[optional]]
	accelerator.wait_for_everyone() 
```
(tip: pass accelerator to other participating modules if necessary)

---
## The Accelerator: Gather Predictions
```python
for inputs, targets in validation_dataloader:
    predictions = model(inputs)
    # Gather all predictions and targets
    all_predictions = accelerator.gather(predictions)
```

---

## Accelerate Config 
- Before running the code, use the config CLI tool:
```shell
accelerate config
```
to determine number of GPUs, fp16, ....

---
## Accelerate Launch
- Run the code using
```shell
accelerate launch /../script.py
```

## Internal Usage
```shell
/homes/alongo/python3/hugging_faiss/hugging_faiss/sentence_embedding.py
```




```ad-idea
idea:: here is another idea
```
