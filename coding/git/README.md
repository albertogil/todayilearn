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

Clear stash:

```
$ git stash clear
```

## Create subfolders of branchs

By typing **/** in the branch name will create a subfolder on the git branching. Example:

```
$ git checkout -b feature/login-CODE-123
```

## Rollback from a wrong commit

Will undo the commit and keep the changes.

```
$ git reset HEAD~ 
```

## Adding pre commit hooks

Install package [pre-commit](https://www.npmjs.com/package/precommit) on dev dependencies.

```
$ npm install pre-commit --save-dev
```

Add a new script to run by pre-commit in the package.json, like:

```
...
  "scripts": {
    "lint:diff": "LIST=`git diff-index --name-only HEAD | grep .*\\.js | grep -v json`; if [ \"$LIST\" ]; then eslint $LIST; fi",
    ...
  },
...
```
Add the pre-commit script on the package.json :
```
"pre-commit": [
  "lint:diff"
]
```
More info:
- [Git Hook](https://githooks.com/)
- [ESLINT Script](https://gist.github.com/oroce/11282380) and [another option](https://gist.github.com/dahjelle/8ddedf0aebd488208a9a7c829f19b9e8)
