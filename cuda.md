# To reset a GPU

```bash
sudo nvidia-smi --gpu-reset -i 0 # -i is the target gpu index
```

# To list/kill processes using GPUs

list:

```bash
sudo fuser -v /dev/nvidia*
```
kill:

```bash
sudo fuser -v /dev/nvidia* -k
```

