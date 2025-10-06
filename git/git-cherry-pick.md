#git
### To cherry-pick a specific commit:

```bash
git cherry-pick <commit-hash>
```

### You can also cherry-pick a range of commits:

```bash
git cherry-pick <start-commit-hash>^..<end-commit-hash>
```

`^` ensures that the start commit is included while cherry-picking, by default it is not included.

### You can also edit the commit message while cherry-picking by using the `-e` flag:

```bash
git cherry-pick -e <commit>
```
