- create a session:
```bash
tmux 
```
---

- create session with a name:

```bash
tmux new -s [session-name]
```

- attach to session
```bash
tmux a -t [session-name]
```

- detach session from within that session:
```
ctrl+b d
```
---

- list sessions
```bash
tmux ls
```
---

- rename session
```bash
tmux rename-session [-t current-name] [new-name]
```

- rename session from within that session

  short way:
```
ctrl+b $
```
  long way:

`ctrl+b`, `:` then, `rename-session [-t current-name] [new-name]`

---

- kill session
```bash
tmux kill-session [-t session-name]
```

- kill session from within that session

`ctrl+b`, `:` then, `kill-session [-t session-name]`

---

- jumb to another session from within a session
```bash
ctrl+b s
``` 
---