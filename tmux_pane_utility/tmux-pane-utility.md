# Synchronize Command Panes Using TMUX

## First create a new session

```bash
tmux new -t [session_name]

eg: tmux new -t random
```

## Open and Split windows into multiple axis

> For vertical

```bash
[Ctrl + b] %
```

> For horizontal

```bash
[Ctrl + b] "
```

## Now Synchronize your Panes by following command and same command for disabling Synchronization

```bash
[Ctrl + b] :setw synchronize-panes
```