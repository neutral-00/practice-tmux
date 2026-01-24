# Customize Tmux

create the config file

```sh
nvim ~/.tmux.conf
```

add the following

```
## change the prefix from C-b to Alt-a
set -g prefix M-a
unbind C-b
bind M-a send-prefix

## reload the config
In the terminal type:

tmux source-file ~/.tmux.conf
