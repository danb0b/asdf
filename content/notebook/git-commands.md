---
title: Common Git Commands
tags:
  - bash
  - git
---

to clone a repository:

```bash
git clone my_git_address
```

## Branches

list local branches:

```bash
git branch
```

list remote branches:

```
git branch --remote
```

Checkout and track a remote branch:

```bash
git checkout –track origin/xyz
```

## Status

Sometimes you want to see what has changed.  ```git status``` can be used to see which files have changed since the last commit.  Otherwise, you can use ```git diff``` to more closely inspect file changes line by line


## Pushing

Push a quick commit:

If you created a local branch and need to link it to a remote:

```bash
git push --set-upstream origin <localbranchname>
```


```bash
git add *
git commit -m "commit message"
git push
```

or combined:

```bash
git add * && git commit -m "update" && git push
```

## Submodules

from [here](https://stackoverflow.com/questions/1030169/easy-way-to-pull-latest-of-all-git-submodules)

to pull submodules

```
git submodule update --init --recursive
```

```
git submodule update --recursive --remote
```

cd into the proper subdirectory
ensure you are attached to a branch:

```
git branch
```

if not check one out

```
git checkout [branchname]
```
