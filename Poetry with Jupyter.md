
## Create Poetry Environment with JupyterLab


- `poetry add jupyterlab`


## Open Jupyter with Srun 

- Connect to HPC with ssh as usual 
- run `srun` command with suitable arguments to obtain note witresources 
```shell
srun --partition=gpu --cpus-per-task=1 --gres=gpu:1 --time=1-00:00 --mem=32G --pty bash
```

- Copy the node name (e.g. gpu-003
```shell
jupyter lab --no-browser --port 9099
```
- 

## Tuneling

```shell
ssh -t -t ag116384@ushpc-login1.gsk.com -L 7077:localhost:8088 ssh gpu-003 -L 8088:localhost:9099
```