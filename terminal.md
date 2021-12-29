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

### More
- https://askubuntu.com/a/300417/786094
