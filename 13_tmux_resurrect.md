# tmux-resurrect

How to resurrect a tmux session?


You can resurrect a **tmux** session using **tmux-resurrect** and **tmux-continuum**. Here's how:

### 🔹 **Saving a tmux Session**
Manually save your session with:
```sh
prefix + Ctrl-s
```
(`prefix` is usually `Ctrl-b` unless you've changed it.)

### 🔹 **Restoring a tmux Session**
To restore the last saved session, use:
```sh
prefix + Ctrl-r
```

### 🔹 **Enable Automatic Saving & Restoring**
If you want **tmux-continuum** to automatically save and restore sessions, add these lines to your `.tmux.conf`:
```sh
set -g @continuum-restore 'on'
set -g @resurrect-strategy-vim 'session'
set -g @resurrect-strategy-nvim 'session'
set -g @resurrect-capture-pane-contents 'on'
```
This ensures that Vim/Neovim sessions and pane contents are restored.

### 🔹 **Installation (If Not Installed)**
If you haven't installed the plugins yet, add these lines to your `.tmux.conf` (assuming you're using TPM):
```sh
set -g @plugin 'tmux-plugins/tmux-resurrect'
set -g @plugin 'tmux-plugins/tmux-continuum'
```
Then reload tmux and install the plugins:
```sh
tmux source-file ~/.tmux.conf
prefix + I
```

For more details, check out [tmux-resurrect on GitHub](https://github.com/tmux-plugins/tmux-resurrect)or [this guide on automatic restoration](https://www.rockyourcode.com/how-to-start-and-restore-tmux-sessions-automatically-with-tmux-continuum/).

Let me know if you need help configuring it further! 🚀
