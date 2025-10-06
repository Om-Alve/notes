#tools
[mprocs](https://github.com/pvolok/mprocs) runs multiple commands in parallel and shows output of each command separately.

## Installation:
```bash
npm install -g mprocs
```

## How to use:
```bash
mprocs "command1" "command2" ..... "command n"
```

You can also specify the name of the process by using the `--names` flag

```bash
mprocs --names "server,nvim" "npm run dev" "nvim" 
```

This results in the following:
![[Pasted image 20251006235825.png]]

Pretty nice utility! Let's you view different services without managing multiple windows/panes with something like [[tmux]] .Even better if you use it with [[just]].

> You can also create an `mprocs.yaml` file and run the `mprocs` command in the same directory.


Reference:
[mprocs github repo](https://github.com/pvolok/mprocs)