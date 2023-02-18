# rclone

rclone is an app to mount extrenal storage on linux machine. This file will contain commands to mount google drive on linux machine using __rclone__.

## Install

```bash
sudo apt install rclone
```

## Configure

run `rclone config`. A long list with supported apps will show. Choose google drive (do not be confused with google cloud storage).

This will give a list of instructions and guidlines. One of them is to create google drive app client id and secret.
To do so, follow this [link](https://rclone.org/drive/#making-your-own-client-id) from `rclone` docs.

## List Remotes

```bash
rclone listremotes
```


## Mount/Unmount

To mount a folder from remote:

``bash
rclone mount [--daemon] remote:path/to/files path/to/local/mount
``
use `--daemon` option to allow rclone to mount in the background

To unmount, it similar to the linux command:
```bash
fusermount -u /path/to/local/mount
```


## More
- https://www.youtube.com/watch?v=f8K-V3HHDA0&ab_channel=CBTNuggets
