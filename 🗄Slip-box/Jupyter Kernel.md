
## Context
- [[Poetry with Jupyter]]
## Viewing and Editing the Kernel

You can use the `kernelspec` command to get information about the installed Kernels for your installation.

The command `jupyter kernelspec list` will provide you a list of the installed Kernels, something like: 

```shell
Available kernels:
  python2          /Library/Python/2.7/sitepackages/ipykernel/resources
  redisworkshop    /Users/tague/Library/Jupyter/kernels/RedisWorkshop
```

The display name for a kernel is found in the **kernel.json** file in the corresponding directory for the kernel.  
Edit the `display_name` property in the **kernel.json** file and it will change the display name next time you start Jupyter.


## Resources

[resource](https://stackoverflow.com/questions/45085233/jupyter-kernel-is-there-a-way-to-rename-them)
