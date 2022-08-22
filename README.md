# Tmux pane cheatsheet
## Interacting with Panes
**Ctrl + b ;**<br/>
Toggle last active pane

**Ctrl + b o** <br/>
Switch to next pane

**Ctrl + b q** <br/>
Show pane numbers

**Ctrl + b q 0 ... 9** <br/>
Switch/select pane by number

**Ctrl + b %**<br/>
Split pane with horizontal layout

**Ctrl + b "**<br/>
Split pane with vertical layout

**Ctrl + b Spacebar** <br/>
Toggle between pane layouts

**Ctrl + b x** <br/>
Close current pane

**Ctrl + b z** <br/>
Toggle pane zoom

**Ctrl + b !** <br/>
Convert pane into a window

### Resizing Panes
**Ctrl + b + [Up Arrow]** <br/>
**Ctrl + b Ctrl + [Up Arrow]** <br/>
**Ctrl + b + [Down Arrow]** <br/>
**Ctrl + b Ctrl + [Down Arrow]** <br/>
Resize current pane height(holding second key is optional)

**Ctrl + b + [Right Arrow]** <br/>
**Ctrl + b Ctrl + [Right Arrow]** <br/>
**Ctrl + b + [Left Arrow]** <br/>
**Ctrl + b Ctrl + [Left Arrow]** <br/>
Resize current pane width(holding second key is optional)

### Moving Panes 
**Ctrl + b {**<br/>
Move the current pane left

**Ctrl + b }**<br/>
Move the current pane right

**Ctrl + b + [Up Arrow]** <br/>
**Ctrl + b [Down Arrow]** <br/>
**Ctrl + b [Right Arrow]** <br/>
**Ctrl + b [Left Arrow]** <br/>
Switch to pane to the direction

### Command mode
**Ctrl + b :** <br/>
Enter command mode

**:set mouse on** <br/>
Enable mouse mode

**:setw synchronize-panes** <br/>
Toggle synchronize-panes(send command to all panes)

**:list-keys** <br/>
**Ctrl + b ?** <br/>
**$ tmux list-keys** <br/>
List key bindings(shortcuts)


## Session management
**$ tmux info**  <br/>
Show every session, window, pane, etc...

**$ tmux ls** <br/>
**$ tmux list-sessions** <br/>
**Ctrl + b s** <br/>
Show all sessions

**$ tmux a** <br/>
**$ tmux at** <br/>
**$ tmux attach** <br/>
**$ tmux attach-session** <br/>
Attach to last session

**$ tmux a -t *mysession*** <br/>
**$ tmux at -t *mysession*** <br/>
**$ tmux attach -t *mysession*** <br/>
**$ tmux attach-session -t *mysession*** <br/>
Attach to a session with the name *mysession*

**$ tmux new -s *mysession*** <br/>
**:new -s *mysession*** <br/>
Start a new session with the name *mysession*

**$ tmux kill-ses -t *mysession*** <br/>
**$ tmux kill-session -t *mysession*** <br/>
kill/delete session *mysession*

**$ tmux kill-session -a** <br/>
kill/delete all sessions but the current

**$ tmux kill-session -a -t *mysession*** <br/>
kill/delete all sessions but *mysession*

**Ctrl + b $** <br/>
Rename session

**Ctrl + b d** <br/>
Detach from session

**Ctrl + b w** <br/>
Session and Window Preview

**Ctrl + b (** <br/>
Move to previous session

**Ctrl + b )** <br/>
Move to next session

## Windows
**$ tmux new -s *mysession* -n *mywindow*** <br/>
start a new session with the name *mysession* and window *mywindow*

**Ctrl + b c** <br/>
Create window

**Ctrl + b ,** <br/>
Rename current window

**Ctrl + b &** <br/>
Close current window

**Ctrl + b p** <br/>
Previous window

**Ctrl + b n** <br/>
Next window

**Ctrl + b 0 ... 9** <br/>
Switch/select window by number

**Ctrl + b l** <br/>
Toggle last active window

**:swap-window -s 2 -t 1** <br/>
Reorder window, swap window number 2(src) and 1(dst)

**:swap-window -t -1** <br/>
Move current window to the left by one position