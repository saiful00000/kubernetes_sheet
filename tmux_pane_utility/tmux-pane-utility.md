# Synchronize Command Panes Using TMUX

First of all open up your terminal. Then follow along.

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

# Or here is the all posible commands

```bash
Ctrl+b c Create a new window (with shell)
Ctrl+b w Choose window from a list
Ctrl+b 0 Switch to window 0 (by number )
Ctrl+b , Rename the current window
Ctrl+b % Split current pane horizontally into two panes
Ctrl+b " Split current pane vertically into two panes
Ctrl+b o Go to the next pane
Ctrl+b ; Toggle between the current and previous pane
Ctrl+b x Close the current pane
```
