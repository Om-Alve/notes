#tools 

[watchexec](https://github.com/watchexec/watchexec) is a pretty handy tool for running commands for a particular event.

It watches a path and automatically runs a command when it detects any modifications.

This can be pretty useful if you're making changes in a server and want to restart it on save.

## Installation:

You can install it with [any package manager](https://github.com/watchexec/watchexec/blob/main/doc/packages.md)
```bash
sudo apt install watchexec-cli # this doesn't work for some reason

# Try homebrew (works)
brew install watchexec
```

## How to use:

```bash
watchexec -e tsx,jsx npm run build
```

This runs the `npm run build` command whenever any file with the `jsx` or `tsx` extension is modified.

```bash
watchexec -r --stop-signal SIGKILL -e py python main.py
```

Restarts `main.py` whenever any python file is changed within the project. Sends a `SIGKILL` signal to the old python process. 

Pretty handy! 

References:
[watchexec  repo](https://github.com/watchexec/watchexec)