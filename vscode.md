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


# Change root Directory of Jupyter notebooks

- Got to settings, "ctrl+<".
- Search for notebook file root
- change `${fileDirname}`  to whatever value. For instance `${workspaceFolder}`

## More
- https://stackoverflow.com/questions/55491046/how-to-set-the-running-file-path-of-jupyter-in-vscode
