# Display popup

Did you know we can open a terminal in a popup in tmux?

We can with the command ctrl-b :display-popup

Then you can close by press esc.


This can come in handy in a lot of scenarios.


## Scenario 1 - open lazygit to perform git operations

Add the below settings in `~/.tmux.conf`
```
bind C-y display-popup \
  -w 90% \
  -h 90% \
  -d "#{pane_current_path}"
  -E "lazygit"
```



For this make sure you are in a git repo location then press ctrl-b ctrl-y


## Reference
> Eric McKevit https://youtu.be/7BP9iWiKx8Q
