---
title: "Git Log"
weight: 110
pre: "<b>Lab 11. </b>"
chapter: false
---

In this lab we will learn how Git Log works

## Table of Contents

- [Pre](#pre)
- [Task 1 Git Log](#task-1-git-log)

## Pre

Git and windows Terminal must be installed

## Task 1 Git Log

Git Log will show the project history in reversed cronologic order

__In your terminal type:__

```bash

git log

```

![Alt text](images/001_git_log.png?raw=true "git log")

Adding --graph to our git log command will give a better view on how branches have been merged to our project

__In your terminal type:__

```bash

git log --graph

```

use the spacebar to scroll down, until you see the merged branches

![Alt text](images/002_git_log_graph.png?raw=true "git log --graph")

git log --oneline will show a oneline summery for all commits, this is usefull when you are looking for the sha1 value

__In your terminal type:__

```bash

git log --oneline

```

![Alt text](images/003_git_log_oneline.png?raw=true "git log --oneline")

Lets try some other ways of using the log

--since is for a date or you can specify xx time ago

-S String will search in the files modified

git log --since="1 days ago"

git log --since="23 hour ago"

git log -S blue

git log -S pictures

__In your terminal type:__

```bash

git log --since="23 hour ago"

git log -S blue

git log -S pictures

```

![Alt text](images/004_git_since_23hourago.png?raw=true "git log --since=23 hour ago")

![Alt text](images/005_git_log_S.png?raw=true "git log -S")
