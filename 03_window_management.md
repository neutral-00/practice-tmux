# Window / Tab Management

Managing **windows** in `tmux` allows you to run multiple terminal screens within a single session, similar to browser tabs.

Here is a complete breakdown of all window management commands and keyboard shortcuts.

---

## 1. Key Shortcuts Inside tmux (Prefix-based)

> **Default Prefix:** `Ctrl + b`
> Press `Ctrl + b`, release, then press the shortcut key.

| Action | Shortcut | Notes / Description |
| --- | --- | --- |
| **Create new window** | `Prefix` + `c` | Opens a fresh tab/window in the current session |
| **Rename current window** | `Prefix` + `,` | Prompts to change the active window's label |
| **Close current window** | `Prefix` + `&` | Asks for confirmation (`y/n`) to kill the window |
| **Next window** | `Prefix` + `n` | Moves to the next window in order |
| **Previous window** | `Prefix` + `p` | Moves to the previous window in order |
| **Switch by index** | `Prefix` + `0`–`9` | Jump directly to window number `0` through `9` |
| **Last active window** | `Prefix` + `l` | Toggles back to the previously active window |
| **Interactive window list** | `Prefix` + `w` | Menu to browse/switch between windows and panes |
| **Find window by name** | `Prefix` + `f` | Search open windows by name/content |

---

## 2. Command Mode (`Prefix` + `:`)

Press `Ctrl + b` then `:` to open the command prompt at the bottom:

| Action | Command |
| --- | --- |
| **Create named window** | `:new-window -n <name>` |
| **Rename window** | `:rename-window <new-name>` |
| **Kill specific window** | `:kill-window -t <target>` |
| **Swap window positions** | `:swap-window -s <src> -t <dst>` |
| **Move window index** | `:move-window -t <target-index>` |

---

## 3. Creating Windows from Terminal (Shell)

You can also manipulate windows directly from your command line inside or outside tmux:

```bash
# Create a new named window in the current session
tmux new-window -n editor

# Create a new window executing a specific command immediately
tmux new-window -n logs "tail -f /var/log/syslog"

# Kill a specific window by name/number
tmux kill-window -t editor

```

---
