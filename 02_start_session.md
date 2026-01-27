# Start Tmux Session

To start a new **tmux** session with a specific name, use:

```bash
tmux new -s session_name
```

Example:

```bash
tmux new -s work
```

That creates the session **and** attaches you to it right away.

A couple handy extras while we’re here:

* Start it **detached**:

  ```bash
  tmux new -s work -d
  ```

* List sessions:

  ```bash
  tmux ls
  ```

* Attach to a named session later:

  ```bash
  tmux attach -t work
  ```

If you want shortcuts or a `.tmux.conf` trick for this, I’ve got you.

