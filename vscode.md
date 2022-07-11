# Change Directory when running debugger

add this setting to your launch.json debug configuration file.

```json
"cwd": "whatever"
```
some useful variables to use:
- ${workspaceFolder} to specify the workspace folder
- ${fileDirname} for the file name directory

## More
- https://stackoverflow.com/questions/38623138/vscode-how-to-set-working-directory-for-debugging-a-python-program
