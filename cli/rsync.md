rsync is a pretty handy utility for syncing files and directories remotely or locally. It stands for Remote Sync.

It uses the ssh protocol by default. Has more features than [[SCP]] like compression

Basic Syntax:
```bash
rsync [source-path] [destination-path]
```

#### IMPORTANT - Always use the `--dry-run` flag to test the command once before executing it.

This is a nice way to use the command:

```bash
rsync -Pav [source-path] [destination-path]
```

What do these flags do?

`-P` -> adds a progress bar for the transfer process 
`-a` -> uses archive mode which preservers file metadata during transfer.
`-v` -> verbose output

`-z` is also a handy flag, it turns on compression, useful when you have shitty internet.

Reference:
[# Linux File Transfers Made Easy with rsync](https://www.youtube.com/watch?v=KG78O53u8rY)