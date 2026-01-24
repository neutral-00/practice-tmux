# Enable Mouse

Great! Now let's enable **mouse support** in tmux.

### **Step 1: Modify your `.tmux.conf`**
Open your config file and add this line:
```bash
set -g mouse on
```

### **Step 2: Apply Changes**
Either restart tmux or reload the config:
```bash
tmux source-file ~/.tmux.conf
```

### **Step 3: What This Enables**
- **Click to select panes** ✅
- **Scroll using the mouse** ✅
- **Resize panes by dragging** ✅
- **Switch windows with mouse clicks** ✅

### **Possible Issues**
1. **Terminal Emulator Settings**
   - If scrolling doesn’t work, check if your terminal overrides mouse behavior.
   - In **Kitty**, set: `mouse_maps yes` in `kitty.conf`.
   - In **Alacritty**, enable mouse bindings in `alacritty.yml`.

2. **Tmux Plugin Interference**
   - Some plugins modify mouse behavior. If issues arise, try disabling plugins temporarily and testing.

