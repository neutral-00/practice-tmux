# Custom Status Bar


You're on a roll! Next up: **customizing the tmux status bar for better readability.**  

### **Step 1: Modify Your `.tmux.conf`**
You can enhance the status bar colors, structure, and information display using the following configuration:  

```bash
# Background and foreground colors
set -g status-bg colour234  # Dark background
set -g status-fg colour137  # Bright text

# Left section: Session name
set -g status-left "#[fg=green]Session: #S#[default]"

# Right section: Hostname & Date/Time
set -g status-right "#[fg=blue]#H #[fg=yellow]%Y-%m-%d %H:%M#[default]"

# Center section: Active window & pane
set -g window-status-current-format "#[bg=yellow]#[fg=black] #I:#W #[default]"
set -g window-status-format "#[bg=black]#[fg=white] #I:#W #[default]"
```

### **Step 2: Apply Changes**
Reload tmux:
```bash
tmux source-file ~/.tmux.conf
```

### **Step 3: Breakdown of What’s Changed**
✅ **Better contrast** (dark background, bright text)  
✅ **Left panel shows session name**  
✅ **Right panel shows hostname & date/time**  
✅ **Highlight active window in yellow**  

### **Step 4: Optional Enhancements**
If you'd like power-user functionality:  
1. **Show battery percentage** _(for laptops)_:
   ```bash
   set -g status-right "#[fg=blue]#H #[fg=yellow]%Y-%m-%d %H:%M #[fg=red]#(acpi -b | awk '{print $4}')#[default]"
   ```
2. **Add Git branch (if inside a repo)**:
   ```bash
   set -g status-right "#[fg=green]#(git rev-parse --abbrev-ref HEAD 2>/dev/null)#[default]"
   ```

Let me know how it looks after applying the changes! Want to tweak colors further? 🎨
