# Generate SSH keys

There is a possiblity that an SSH key is already generated. To list the existing keys:

```bash
ls -l ~/.ssh/id_*.pub
```
If no match found, then there is no key generated.

## Generate a new key
```bash
ssh-keygen -t rsa -b 4096 -C "my_email@adress.me"
```

## To see the generated key:

```bash
ls ~/.ssh/id_*
```
What will be prompted is two files, one for the private key and the other is for the public one.

### Detailed resources
- https://linuxize.com/post/how-to-set-up-ssh-keys-on-ubuntu-20-04/


# Forwarding keys to server

In many cases, it is required to perform ssh-authorized operations on remote using the authorizing key. In order to allow such operations, key should be forwarded to remote. To do so, add:
```
Host host.com
    ForwardAgent yes
```
to ~/.ssh/config file

## More:
- https://stackoverflow.com/a/12409249/4412324


# General SSH tips

## List all keys allowing ssh-authorized operations:
```bash
ssh-add -l
```

