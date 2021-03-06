# Bash
## Loop over directory files in terminal

- to run on all files:

```bash
for filename in /Data/*.txt; do
    ./MyProgram.exe "$filename" "Logs/$(basename "$filename" .txt)_Log$i.txt"
done
```
- to run on files with some pattern, like numeric pattern:

```bash
for filename in /Data/*.txt; do
    for ((i=0; i<=3; i++)); do
        ./MyProgram.exe "$filename" "Logs/$(basename "$filename" .txt)_Log$i.txt"
    done
done
```

You can play with the strucutre the way you want.


### More
- https://stackoverflow.com/questions/20796200/how-to-loop-over-files-in-directory-and-change-path-and-add-suffix-to-filename

## Open audio file from terminal

This tool is useful if you are labeling large number of audio files. You can install `mplayer` by `sudo apt-get install mplayer` "I installed it on Ubuntu 20.04, expecting it to work on Debian based distros". Loop over your files, and label.

To open the file: `mplayer -vo caca <filename>`. I took these parameters from [here](https://askubuntu.com/a/300417/786094). You can investiage more.

### More
- https://askubuntu.com/a/300417/786094


## Zip a directory
```bash
zip -r compressed_filename.zip foldername
```
### More
- https://askubuntu.com/questions/27349/how-do-i-compress-a-directory

## Unzip parted files

By parted zip files, we mean those kind of files which are parted to a specific size like 50MB, 100MB etc. 

First, collect the parts via:

```bash
cat folder.zip.* > folder.zip
```
then unzip using
```bash
unzip folder.zip -d folder
```


## Watch a command

If you want to monitor command output every n seconds, you can use `watch` utility. Example of watching `nvidia-smi` memory usage:

```bash
watch -n 1 nvidia-smi
```
`n` here refers to the number of second to poll the command again.

### More
- https://stackoverflow.com/a/35913280/4412324

