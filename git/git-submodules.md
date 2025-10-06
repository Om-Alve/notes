#git 

git-submodules are basically git repositories inside another git repository.

You can add a git repository in an existing git repo as a submodule via the following command:
```bash
git submodule add <repo-link>
```

Git tracks changes to the submodule separately from your original repo.

A new `.gitmodules` file is added when you add a new submodule. It contains information about the submodules in the current repo.

When you clone a project with submodules, you only get the directories of the submodule and don't get the actual files inside it,  to do so, you can use the following command:

```bash
git submodule update --init --recursive
```

To fetch changes from upstream in a submodule, `cd` into the submodule and run `git fetch` and `git merge`.

Reference:
[Git Submodules Docs](https://git-scm.com/book/en/v2/Git-Tools-Submodules)