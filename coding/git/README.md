# Git

## Use stash to store temporal information

By typing:

```
$ git stash
```

You store the actual changes on a queue, so that you can do un related changes to a different branch or commit. Without the need of mixing the changes or the need to commit unfinished work.

And to recover the changes, you type:

```
$ git stash pop
```

## Create subfolders of branchs

By typing **/** in the branch name will create a subfolder on the git branching. Example:

```
$ git checkout -b feature/login-CODE-123
```
