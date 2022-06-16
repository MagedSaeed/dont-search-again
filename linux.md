# Clear swap memory

sometime, it feels annoying to see the swap memory almost full while the memory has space available. To check the status of memory devices on the system:
```bash
free -m
```
to clear and switch off the swap memory:

```bashs
swapoff -a
```

to enable the swap memory again:

```bash
swapon -a
```
## More
- https://www.redhat.com/sysadmin/clear-swap-linux
