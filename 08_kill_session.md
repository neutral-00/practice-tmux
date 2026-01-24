# Kill Session


You can end a specific **Tmux session** using the following methods:

### **1. Kill a Session by Name**
First, list all running sessions:
```sh
tmux ls
```
This will output something like:
```
0: bash (attached)
1: vim (detached)
```
To kill a session (e.g., `vim`), run:
```sh
tmux kill-session -t 1
```
This will **terminate** session `1`.

### **2. Kill the Current Session**
If you're inside a session and want to **close only the active one**, simply type:
```sh
tmux kill-session
```
This closes **only the session you're in** without affecting others.

### **3. Kill All Tmux Sessions**
To **end ALL running sessions**, use:
```sh
tmux kill-server
```
This completely shuts down Tmux.

Would you like to set up an alias for easier session management? 🚀
