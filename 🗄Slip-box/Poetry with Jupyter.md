
## Create Poetry Environment with JupyterLab

- `poetry add jupyterlab`

## Open Jupyter with SRUN 

- Connect to HPC with ssh as usual 
- run `srun` command with suitable arguments to obtain note with GPU.
```shell
srun --partition=gpu --cpus-per-task=1 --gres=gpu:1 --time=1-00:00 --mem=32G --pty bash
```

- This creates a connection to a node on HPC. In our case, it is named `gpu-003`.
- run `jupyter lab` with port forwarding
```shell
jupyter lab --no-browser --port 9099
```
- Copy the url.

## Tuneling
- Finally, from a different terminal instance, connect to the created node.
```shell
ssh -t -t ag116384@ushpc-login1.gsk.com -L 7077:localhost:8088 ssh gpu-003 -L 8088:localhost:9099
```
- paste the above url into your browser.


