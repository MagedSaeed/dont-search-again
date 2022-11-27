# uncompress

## .7z files

```bash
# https://superuser.com/a/540010/1046355
7za x myarchive.7z
# to extract to a destination folder:
7z x myarchive.7z -o/dest # there should be no space between -o and the dest folder
```

## .zip files
```bash
# https://askubuntu.com/a/86852/786094
unzip -d output archive.zip #-qq for silent unzip, https://apple.stackexchange.com/a/277733
# to zip:
zip -r output.zip folder
```


## .tar.bz2
```bash
tar -xvjf archive.tar.bz2 # https://www.howtogeek.com/409742/how-to-extract-files-from-a-.tar.gz-or-.tar.bz2-file-on-linux/
```

## .tar.gz
```bash
tar -xvzf archive.tar.gz # https://www.howtogeek.com/409742/how-to-extract-files-from-a-.tar.gz-or-.tar.bz2-file-on-linux/
```
