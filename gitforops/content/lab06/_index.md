---
title: "Git ignore"
weight: 60
pre: "<b>Lab 6. </b>"
chapter: false
---

In this lab we will learn how to exclude files and folders using .gitignore

## Table of Contents

- [Pre](#pre)
- [Task 1 gitignore](#task-1-gitignore)

## Pre

Git and windows Terminal must be installed

## Task 1 gitignore

[git docs - gitignore](https://git-scm.com/docs/gitignore)

In some projects we have data to use for testing or we build part of the software local but arent interested in managing this with git or pushing it to remote repositories

Lets create a data directory and the .gitignore file, .gitignore needs to be added to the git project

__In your terminal type:__

```bash
cd

cd gitops

cd newproject

mkdir data

echo "" > .gitignore

git add .gitignore

git commit -m "add .gitignore"

git status

```

![Alt text](images/001_git_ignore.png?raw=true "Git ignore")

Next lets exclude the folder "data" we add the line data/* to the .gitignore file

__In your terminal type:__

```bash

echo data/* > .gitignore

git commit -a -m "update .gitignore"

cat .gitignore

```

![Alt text](images/002_git_ignore.png?raw=true "Git ignore")

Lets test that git ignores changes in our data directory

First add some data and run git status, it should state nothing to commit as the only changes we made are in the data directory

__In your terminal type:__

```bash

echo "Donald Duck" >> data/users.txt

echo "Mickey Mouse" >> data/users.txt

git status

```

![Alt text](images/003_git_ignore.png?raw=true "Git ignore")

We can ask if a file or directory is ignored by git, if there is an output the file is ignored, -v will tell us where the ignore comes from

__In your terminal type:__

```bash

git check-ignore data/*

git check-ignore data/* -v

```

![Alt text](images/004_git_ignore.png?raw=true "Git ignore")
