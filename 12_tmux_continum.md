# tmux-continuum

Features:

- continuous saving of tmux environment
- automatic tmux start when computer/server is turned on
- automatic restore when tmux is started

Together, these features enable uninterrupted tmux usage. No matter the computer
or server restarts, if the machine is on, tmux will be there how you left it off
the last time it was used.

Tested and working on Linux, OSX and Cygwin.

#### Continuous saving

Tmux environment will be saved at an interval of 15 minutes. All the saving
happens in the background without impact to your workflow.

This action starts automatically when the plugin is installed. Note it requires
the status line to be `on` to run (since it uses a hook in status-right to run).

#### Automatic restore

Last saved environment is automatically restored when tmux is started.

Put `set -g @continuum-restore 'on'` in `.tmux.conf` to enable this.

#### Dependencies

`tmux 1.9` or higher, `bash`,
[tmux-resurrect](https://github.com/tmux-plugins/tmux-resurrect) plugin.

### Installation with [Tmux Plugin Manager](https://github.com/tmux-plugins/tpm) (recommended)

Please make sure you have
[tmux-resurrect](https://github.com/tmux-plugins/tmux-resurrect) installed.

Add plugin to the list of TPM plugins in `.tmux.conf`:

    set -g @plugin 'tmux-plugins/tmux-resurrect'
    set -g @plugin 'tmux-plugins/tmux-continuum'

Hit `prefix + I` to fetch the plugin and source it. The plugin will
automatically start "working" in the background, no action required.


#### Resurrect
None of the previous saves are deleted (unless you explicitly do that). All save
files are kept in `~/.tmux/resurrect/` directory, or `~/.local/share/tmux/resurrect`
(unless `${XDG_DATA_HOME}` says otherwise).<br/>
Here are the steps to restore to a previous point in time:

- make sure you start this with a "fresh" tmux instance
- `$ cd ~/.tmux/resurrect/`
- locate the save file you'd like to use for restore (file names have a timestamp)
- symlink the `last` file to the desired save file: `$ ln -sf <file_name> last`
- do a restore with `tmux-resurrect` key: `prefix + Ctrl-r`

You should now be restored to the time when `<file_name>` save happened.
