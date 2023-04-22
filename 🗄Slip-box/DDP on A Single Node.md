
Using DDP on a single node is easy as we only need to change the execution command.

```shell
python -m torch.distributed.launch --nproc_per_node=8 script.py
```

With more than one node, we need to invoke the command from each node and specify which of them is the `master`. 



``