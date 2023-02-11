# Tmux pane cheatsheet

## Interacting with Panes

**Ctrl + b ;**
Toggle last active pane

**Ctrl + b o**
Switch to next pane

**Ctrl + b q**
Show pane numbers

**Ctrl + b q 0 ... 9**
Switch/select pane by number

**Ctrl + b %**
**:splitw -h**
Split pane with horizontal layout (two panes side by side)

**:selectp -t *right***
**:selectp -t *left***
Select top pane (assuming there are two side by side panes)

**Ctrl + b "**
**:splitw -v**
Split pane with vertical layout (two stacked panes)

**:selectp -t *top***
**:selectp -t *bottom***
Select top pane (assuming there are two stacked panes)

**Ctrl + b Spacebar**
Toggle between pane layouts

**Ctrl + b x**
Close current pane

**Ctrl + b z**
Toggle pane zoom

**Ctrl + b !**
Convert pane into a window

**:set -g pane-active-border-style bg=*red***
Set active pane border to red (tmux > ver. 2.9 otherwise remove *bg=*)

### Resizing Panes

**Ctrl + b + [Up Arrow]**
**Ctrl + b Ctrl + [Up Arrow]**
**Ctrl + b + [Down Arrow]**
**Ctrl + b Ctrl + [Down Arrow]**
Resize current pane height(holding second key is optional)

**Ctrl + b + [Right Arrow]**
**Ctrl + b Ctrl + [Right Arrow]**
**Ctrl + b + [Left Arrow]**
**Ctrl + b Ctrl + [Left Arrow]**
Resize current pane width(holding second key is optional)

### Moving Panes

**Ctrl + b {**
Move the current pane left

**Ctrl + b }**
Move the current pane right

**Ctrl + b + [Up Arrow]**
**Ctrl + b [Down Arrow]**
**Ctrl + b [Right Arrow]**
**Ctrl + b [Left Arrow]**
Switch to pane in the direction of *arrow*

### Command mode

**Ctrl + b :**
Enter command mode

**:set mouse on**
Enable mouse mode

**:setw synchronize-panes**
Toggle synchronize-panes(send command to all panes)

**:list-keys**
**Ctrl + b ?**
**$ tmux list-keys**
List key bindings(shortcuts)

## Session management

**$ tmux info**
Show every session, window, pane, etc...

**$ tmux ls**
**$ tmux list-sessions**
**Ctrl + b s**
Show all sessions

**$ tmux a**
**$ tmux at**
**$ tmux attach**
**$ tmux attach-session**
Attach to last session

**$ tmux a -t *mysession***
**$ tmux at -t *mysession***
**$ tmux attach -t *mysession***
**$ tmux attach-session -t *mysession***
Attach to a session with the name *mysession*

**$ tmux new -s *mysession***
**:new -s *mysession***
Start a new session with the name *mysession*

**$ tmux kill-ses -t *mysession***
**$ tmux kill-session -t *mysession***
kill/delete session *mysession*

**$ tmux kill-session -a**
kill/delete all sessions but the current

**$ tmux kill-session -a -t *mysession***
kill/delete all sessions but *mysession*

**Ctrl + b $**
Rename session

**Ctrl + b d**
Detach from session

**Ctrl + b w**
Session and Window Preview

**Ctrl + b (**
Move to previous session

**Ctrl + b )**
Move to next session

## Windows

**$ tmux new -s *mysession* -n *mywindow***
start a new session with the name *mysession* and window *mywindow*

**Ctrl + b c**
Create window

**Ctrl + b ,**
Rename current window

**Ctrl + b &**
Close current window

**Ctrl + b p**
Previous window

**Ctrl + b n**
Next window

**Ctrl + b 0 ... 9**
Switch/select window by number

**Ctrl + b l**
Toggle last active window

**:swap-window -s 2 -t 1**
Reorder window, swap window number 2(src) and 1(dst)

**:swap-window -t -1**
Move current window to the left by one position
