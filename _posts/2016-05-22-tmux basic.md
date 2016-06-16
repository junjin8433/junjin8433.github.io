---
layout: post
section-type: post
title: tmux basics
category: tech
tags: [ 'tutorial' ]
---

tmux is a terminal multiplexer: it enables a number of terminals to be created, accessed, and controlled from a single screen. tmux may be detached from a screen and continue running in the background, then later reattached.
When tmux is started it creates a new session with a single window and displays it on screen. A status line at the bottom of the screen shows information on the current session and is used to enter interactive commands.

## Basic operations

### split screen
By default, we use prefix keys "C-b" as an example.

```
"    split current pane into two, up and down
%    split current pane into two, left and right
[    enter copy mode to copy text or view the history
]    paste the most resently copied buffer to text
up/down/left/right    change to the corresponding pane
C-up/down/left/right    resize the current pane
```

## Some user configurations

### use vim mode
```
set-window-option -g mode-keys vi
```

### Change prefix keys as C-a

```zsh
unbind C-b
set -g prefix C-a
```

### Bind up-down-left-right as k-j-h-l

```
bind-key k select-pane -U
bind-key j select-pane -D
bind-key h select-pane -L
bind-key l select-pane -R
```

### Bind change-size as C-h/j/k/l

```
bind -r ^k resizep -U 5 # upward (prefix Ctrl+k)
bind -r ^j resizep -D 5 # downward (prefix Ctrl+j)
bind -r ^h resizep -L 5 # to the left (prefix Ctrl+h)
bind -r ^l resizep -R 5 # to the right (prefix Ctrl+l)
```
