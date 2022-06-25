---
title: "Lab 10 Git Diff"
---

In this lab we will learn how Git Diff

## Table of Contents

- [Pre](#pre)
- [Task 1 Git Diff](#task-1-git-diff)
- [Task 2 Git Diff commit commit](#task-2-git-diff-commit-commit)

## Pre

Git and windows Terminal must be installed

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

## Task 2 Git Diff commit commit

We can get changes in a range between two commits

git diff from commmit sha1 to commit sha1

Select the two commits __add blue__ and __change color__

__In your terminal type:__

```bash

git log --oneline

git diff 9edb95f 69a4908

```

![Alt text](images/003_git_log.png?raw=true "git log")

![Alt text](images/004_git_diff_commit_commit.png?raw=true "git diff commit commit")
