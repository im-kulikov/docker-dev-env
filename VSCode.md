# [DEPRECATED] Setup VSCode (use GoLand instead):

Contents of `${workspaceRoot}/.vscode/settings.json`:

```json
{
    "go.inferGopath": true,
    "go.vetOnSave": "workspace",
    "go.vetFlags": ["-all"]
}
```

Contents of `${workspaceRoot}/.vscode/launch.json`:

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Launch",
            "type": "go",
            "request": "launch",
            "mode": "debug",
            "remotePath": "",
            "port": 2345,
            "host": "127.0.0.1",
            "program": "${fileDirname}",
            "env": {},
            "args": [],
            "showLog": true
        }
    ]
}
```

Contents of `${workspaceRoot}/.vscode/tasks.json`:

```json
    // See https://go.microsoft.com/fwlink/?LinkId=733558
    // for the documentation about the tasks.json format
    "version": "2.0.0",
    "tasks": [
        {
            "taskName": "Run",
            "command": "go run ${file}",
            "type": "shell",
            "group": {
                "kind": "build",
                "isDefault": true
            }
        }
    ]
}
```

Use [Dep](https://github.com/golang/dep):

```bash
$ brew install dep
```
