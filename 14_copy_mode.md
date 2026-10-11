# Copy Mode

Yes, **tmux** has a feature called **copy mode**.

**Copy mode** in tmux lets you scroll through the terminal buffer, select and copy text (even text far above what's currently visible), and optionally paste it later within tmux panes. It's extremely useful for reviewing output, grabbing commands, or saving information from a session.

### Key Features of Copy Mode
- **Scrollback:** Move through lines previously displayed in a pane’s history.
- **Navigation:** Use vi- or emacs-style bindings to move around quickly (arrow keys, page up/down, search, etc.).
- **Selection:** Mark text for copying.
- **Copy/Paste:** Copy selected text to the tmux buffer and paste it with a key press.

### Common Key Bindings (Default tmux)
- **Enter copy mode:**  
  - Press `Ctrl+b` then `[`
- **Move cursor:**  
  - Arrow keys, PageUp/PageDown, or vi-style (h/j/k/l)
- **Start selection:**  
  - Press `Space` (in default, starts marking text)
- **Copy selection:**  
  - Press `Enter` (copies selection to buffer)
- **Exit copy mode:**  
  - Press `q`
- **Paste copied text:**  
  - Press `Ctrl+b` then `]`

### Customizations
You can set tmux to use emacs or vi key bindings (most distros default to vi). This affects navigation in copy mode.

***

**Summary:**  
**Copy mode** is a built-in, highly valuable tmux feature for interacting with text history, making it possible to scroll, search, select, copy, and paste content efficiently in your terminal multiplexed sessions.
