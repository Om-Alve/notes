If you want to change your ssh passphrase, you can use the following command:

```bash
ssh-keygen -p -f ~/.ssh/key
```

`-p` -> Requests changing the passphrase of a private key file instead of creating a new private key
`-f` -> Specifying the key
