SCP (Secure Copy Protocol) is a command that let's your copy files from a remote system to your local system and vice versa securely. 

It's based on the SSH Protocol and hence requires keys for authentication. 

This is the basic syntax for the SCP command.

Transferring files from local directory to a remote server.

```bash
scp [OPTION] [local-file-path] [destination-ip:destination-path]
```

Transferring files from remote server to a local directory:
```bash
scp [OPTION] [destination-ip:destination-path] [local-file-path]
```

e.g. `scp -P 1800 -i ~/.ssh/key text.txt om@test.com:~/test.txt`

Some useful OPTIONS are:

`-P` -> specify the ssh port to connect to the remote host.

`-i` -> specify the private key file for the ssh connection.

`-r` -> copy files from a folder recursively.

A better alternative of SCP is [[rsync]]


References:
[Guide to SCP](https://snapshooter.com/learn/linux/copy-files-scp)