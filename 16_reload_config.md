# Reload Config


## Reload Config - Keymap
Update your ~/.tmux.conf` to have the below lines:

```
unbind r
bind r source-file ~/.tmux.conf \; display-message "tmux.conf reloaded"
```

This way you can reload with <prefix> r
or in the terminal you can type: `tmux source-file ~/.tmux.conf`
