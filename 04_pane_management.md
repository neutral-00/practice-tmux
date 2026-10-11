# Pane / Split Management

**Panes** allow you to split a single window into multiple independent terminal tiles (vertically or horizontally).

Here is the complete guide to creating, navigating, resizing, and organizing tmux panes.

---

## 1. Key Shortcuts Inside tmux (Prefix-based)

> **Default Prefix:** `Ctrl + b`
> Press `Ctrl + b`, release, then press the shortcut key.

| Action | Shortcut | Description |
| --- | --- | --- |
| **Split horizontally (top / bottom)** | `Prefix` + `"` | Divides the current pane into top and bottom halves |
| **Split vertically (left / right)** | `Prefix` + `%` | Divides the current pane into left and right halves |
| **Navigate panes** | `Prefix` + `Arrow Key` | Move focus to the pane in that direction (`↑`, `↓`, `←`, `→`) |
| **Cycle panes in order** | `Prefix` + `o` | Rotates focus to the next pane in the current window |
| **Toggle pane zoom (full screen)** | `Prefix` + `z` | **Very useful** — maximizes current pane; press again to unzoom |
| **Show pane numbers & switch** | `Prefix` + `q` | Displays overlay numbers on panes; press the number to switch |
| **Convert pane into a window** | `Prefix` + `!` | Breaks the active pane out into its own separate tab/window |
| **Cycle preset layout styles** | `Prefix` + `Spacebar` | Cycles through built-in layouts (even-horizontal, main-vertical, etc.) |
| **Close active pane** | `Prefix` + `x` | Prompts for confirmation (`y/n`) to kill the pane |

---

## 2. Resizing Panes

Hold `Prefix` (`Ctrl + b`), then press **and hold** `Alt` or repeat the arrow key:

| Action | Shortcut | Description |
| --- | --- | --- |
| **Resize 5 cells in direction** | `Prefix` + `Alt + Arrow Key` | Nudges pane boundary up, down, left, or right |
| **Resize 1 cell in direction** | `Prefix` + `Ctrl + Arrow Key` | Fine-grain adjustment |

---

## 3. Command Mode (`Prefix` + `:`)

Press `Ctrl + b` then `:` to enter command mode:

| Action | Command |
| --- | --- |
| **Split horizonally** | `:split-window` *(or `:splitv`)* |
| **Split vertically** | `:split-window -h` *(or `:splith`)* |
| **Kill current pane** | `:kill-pane` |
| **Swap pane position** | `:swap-pane -D` *(down/next)* or `:swap-pane -U` *(up/prev)* |
| **Set specific layout** | `:select-layout even-horizontal` *(or `even-vertical`, `main-horizontal`, `tiled`)* |

---

## 4. Useful Shell Commands for Panes

You can also send pane-level split instructions directly from your shell script or command line:

```bash
# Split active window horizontally and run htop immediately
tmux split-window -h "htop"

# Split vertically and open a specific directory
tmux split-window -v -c "~/projects/my-app"

```

---
