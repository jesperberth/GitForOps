---
title: "Lab 12 Git Tag"
---

In this lab we will learn how Git Tag works

## Table of Contents

- [Pre](#pre)
- [Task 1 Git tag annotated](#task-1-git-tag-annotated)
- [Task 2 Git tag lightweight](#task-2-git-tag-lightweight)

## Pre

Git and windows Terminal must be installed

## Task 1 Git tag annotated

Git tag will show existing tags in project

git tag -a version -m "Comment" will create a annotated tag usually for versioning and releases

__In your terminal type:__

```bash

git tag

git tag -a v1.0 -m "First version tagged"

git tag

```

![Alt text](images/001_git_tag.png?raw=true "git tag -a")

We should have a tag "v1.0" on our HEAD

__In your terminal type:__

```bash

git log

```

![Alt text](images/002_git_log.png?raw=true "git log")

Check with git status that you have an uncommitted change

__In your terminal type:__

```bash

git status

git add .

git commit -m "CHANGELOG modified"

git status

```

![Alt text](images/003_git_status.png?raw=true "git status")

Our v1.0 tag stays the commit it was added to

## Task 2 Git tag lightweight

Lets create a lightweight tag

__In your terminal type:__

```bash

git tag update -m "Update Tag"

git tag

git log

```

![Alt text](images/004_git_tag_light.png?raw=true "git tag lightweight")

Lets delete the update tag

__In your terminal type:__

```bash

git tag

git tag -d update

git tag

git log

```

![Alt text](images/005_git_tag_delete.png?raw=true "git tag delete")
