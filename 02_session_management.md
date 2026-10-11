# Session Management
Here is a complete, quick-reference guide to all **`tmux` session management** commands and shortcuts.

---

## 1. Commands from Outside tmux (Terminal / Shell)

These commands are run directly in your terminal to create, list, attach, or manage sessions:

| Action | Command | Notes / Options |
| --- | --- | --- |
| **Start a new session** | `tmux` | Creates an unnamed session (0, 1, 2...) |
| **Start named session** | `tmux new -s <name>` | **Recommended** — easily identify sessions |
| **List running sessions** | `tmux ls` | *(or `tmux list-sessions`)* |
| **Attach to last session** | `tmux a` | *(or `tmux attach`)* |
| **Attach to specific session** | `tmux a -t <name>` | `-t` stands for "target" |
| **Kill specific session** | `tmux kill-session -t <name>` | Closes the session and all its windows |
| **Kill all tmux sessions** | `tmux kill-server` | Terminates the tmux daemon and all sessions |

---

## 2. Key Shortcuts Inside tmux (Prefix-based)

> **Default Prefix:** `Ctrl + b`
> Press `Ctrl + b`, release, and then press the key below.

| Action | Shortcut | Description |
| --- | --- | --- |
| **Detach from session** | `Prefix` + `d` | Leaves the session running in background |
| **List & Switch sessions** | `Prefix` + `s` | Opens an interactive session picker |
| **Rename current session** | `Prefix` + `$` | Opens a prompt at bottom to rename |
| **Command mode** | `Prefix` + `:` | Opens command prompt (e.g., type `detach`) |

---

## 3. Session Commands Inside tmux Command Mode

If you press `Ctrl + b` then `:`, you enter command mode. Here are the session commands you can type:

* `:detach` — Detach from the current session.
* `:rename-session <new-name>` — Rename the active session.
* `:new-session -s <name>` — Create and switch to a new session immediately without leaving tmux.
* `:kill-session` — Terminate the active session and switch to another open session (if available).

---

## Quick Workflow Example

```bash
# 1. Start a session named "dev"
tmux new -s dev

# 2. Do your work... then detach with:
#    Press Ctrl + b, then release and press d

# 3. Check if your session is active
tmux ls

# 4. Re-attach to your session later
tmux a -t dev

```
