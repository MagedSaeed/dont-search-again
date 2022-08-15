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

Make sure you have enough memory on RAM for this opration to finish successfully.

## More
- https://www.redhat.com/sysadmin/clear-swap-linux
- https://askubuntu.com/a/1359/786094


# List listening ports:
```bash
sudo netstat -tunlp
```

## More:
- https://linuxize.com/post/check-listening-ports-linux/


# dpkg error

When faced with the error: `E: dpkg was interrupted, you must manually run 'c' to correct the problem.`
you may try to run the command `sudo dpkg --configure -a` as instructed. If that did not work, you may delete the dpkg tmp updates files in `/var/lib/dpkg/updates`

## More:
- https://askubuntu.com/questions/163200/e-dpkg-was-interrupted-run-sudo-dpkg-configure-a
