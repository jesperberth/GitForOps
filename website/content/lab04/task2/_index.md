---
title: Git rm
weight: 20
---

## Task 2 Git rm

We can remove files from our repository with git rm

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

echo test >> html/todo

git add html/todo

git status

git rm html/todo

```

![Alt text](images/004_git_rm.png?raw=true "Git rm")

So the file cannot be removed as it hasn't been commited to the repository, and there for there is no way to undo it

__In your terminal type:__

```bash

git rm html/todo -f

git status

```

![Alt text](images/005_git_rm_f.png?raw=true "Git rm f")
