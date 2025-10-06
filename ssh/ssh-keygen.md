#ssh
### Recommended way to generate an ssh key.

```bash
ssh-keygen -t ed25519 -a 100
```

Where:
`-t` -> type of key, `ed25519` in this case.
`-a` -> Specifies the number of KDF (key derivation function, currently bcrypt_pbkdf(3)) rounds used. Higher numbers result in slower passphrase verification and increased resistance to brute-force password cracking (should the keys be stolen).
