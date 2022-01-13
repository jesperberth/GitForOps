# Lab 9 Git Revert

In this lab we will learn how a merge conlict happens and how to fix it

## Table of Contents

- [Pre](#pre)
- [Task 1 Create branches](#task-1-create-branches)
- [Task 2 Merge Conflict abort](#task-2-merge-conflict-abort)
- [Task 3 Merge Conflict](#task-3-merge-conflict)

## Pre

Git and windows Terminal must be installed

## Task 1 Create branches

Lets create two branches __green__ and __blue__

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

git status

git branch blue

git branch green

git checkout blue

echo "blue" >> color.txt

git add color.txt

git commit -m "Add blue"

```

![Alt text](pics/001_create_branches.png?raw=true "Create branches")

Next Lab

[Git revert](../lab09/lab9.md)
