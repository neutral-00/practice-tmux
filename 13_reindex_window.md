# Reindex Window

By default window index starts from 0, which is counter intuitive from the keyboard perspective.

Update your `.tmux.conf` to start the session and window index from 1.

```
# Start session and windows and panes index at 1 and not 0
set -g base-index 1
set -g pane-base-index 1
```

Manually trigger window re-indexing with `tmux move-window -r`
