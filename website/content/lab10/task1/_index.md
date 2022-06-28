---
title: Git Diff
weight: 10
---

## Task 1 Git Diff

Git diff without any options will show the uncommited changes

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

git diff

```

![Alt text](images/001_git_diff.png?raw=true "git diff")

Make a change and lets see again

__In your terminal type:__

```bash

echo "Testing Diff" >> CHANGELOG

git diff

```

![Alt text](images/002_git_diff.png?raw=true "git diff")
