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


# Cloning a repo in a cluster

Sometime, when cloning a private repo or interacting with `git`, the password dialog is not shown for some reason with a warning message like:
![image](https://user-images.githubusercontent.com/18549783/187428968-4efdb65b-cb7d-4594-8503-3a270fd737f0.png)

Try:

```bash
unset SSH_ASKPASS
```
Then clone the repo as: `https://<account>@github.com/<account>/<repo>.git`. You will be prompted with a password or tokne, just put it and hopefully the problem will be resolved.

## More:
- https://stackoverflow.com/questions/16077971/git-produces-gtk-warning-cannot-open-display
