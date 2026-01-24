# Setup Tmux


**Tmux** will supercharge your terminal workflow. Let's get it installed on **Ubuntu 25.04**.

## Reference
https://github.com/tmux/tmux/wiki/Installing

### **Step 1: Install Tmux**
Run the following command to install Tmux from the official Ubuntu repository:
```sh
sudo apt update && sudo apt install tmux
```
Alternatively, you can download the `.deb` package manually from [Ubuntu's package repository](https://ubuntu.pkgs.org/25.04/ubuntu-main-amd64/tmux_3.5a-3_amd64.deb.html).

### **Step 2: Verify Installation**
Once installed, check the version to confirm:
```sh
tmux -V
```
You should see something like `tmux 3.5a`.

### **Step 3: Start a Tmux Session**
To begin using Tmux, simply run:
```sh
tmux
```
This will start a new session.

### **Step 4: Basic Commands**
Here are some essential Tmux commands to get started:
- **Detach from session:** `Ctrl + B`, then `D`
- **List sessions:** `tmux ls`
- **Reattach to a session:** `tmux attach -t <session_name>`
- **Create a new window:** `Ctrl + B`, then `C`
- **Split panes horizontally:** `Ctrl + B`, then `%`
- **Split panes vertically:** `Ctrl + B`, then `"`

Would you like to configure a custom `.tmux.conf` for better usability? 🚀
