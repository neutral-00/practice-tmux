# vim-tmux-navigator

To seamlessly navigate install and configure this plugin.

## Refernce
https://github.com/christoomey/vim-tmux-navigator

## Update neovim config

Add the below file `vim-tmux-navigator.lua` in plugins folder:

```
{
  "christoomey/vim-tmux-navigator",
  cmd = {
    "TmuxNavigateLeft",
    "TmuxNavigateDown",
    "TmuxNavigateUp",
    "TmuxNavigateRight",
    "TmuxNavigatePrevious",
    "TmuxNavigatorProcessList",
  },
  keys = {
    { "<c-h>", "<cmd><C-U>TmuxNavigateLeft<cr>" },
    { "<c-j>", "<cmd><C-U>TmuxNavigateDown<cr>" },
    { "<c-k>", "<cmd><C-U>TmuxNavigateUp<cr>" },
    { "<c-l>", "<cmd><C-U>TmuxNavigateRight<cr>" },
    { "<c-\\>", "<cmd><C-U>TmuxNavigatePrevious<cr>" },
  },
}
```
## Update your `.vimrc`

```
Plug 'christoomey/vim-tmux-navigator'
```
