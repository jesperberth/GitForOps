# Lab 8 Git Branches merge conflict

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

Lets do some changes in our green branch

__In your terminal type:__

```bash

git checkout green

echo "green" >> color.txt

git add color.txt

git commit -m "Add green"

```

![Alt text](pics/002_change_green_branch.png?raw=true "Create branches")

## Task 2 Merge Conflict abort

In this task we will do a merge of blue and green branch, a conflict will happend and we will use abort to get out of our conflict

__In your terminal type:__

```bash

git checkout blue

git merge green

```

![Alt text](pics/003_merge_conflict_abort.png?raw=true "Merge conflict abort")

Now we can either fix the conflict with git or do an abort and solve the issue by our self

__In your terminal type:__

```bash

git merge abort

```

![Alt text](pics/004_merge_conflict_abort.png?raw=true "Merge conflict abort")

## Task 3 Merge Conflict

We will do the git merge again but now we will fix the issues

__In your terminal type:__

```bash

git checkout blue

git merge green

```

![Alt text](pics/005_merge_conflict.png?raw=true "Merge conflict")

Lets fix the issue in notepad

__In your terminal type:__

```bash

<<<<<<<<< HEAD is our current branch "blue" and the line below is the text we entered

======= seperates the two branches

Next comes the lines we are trying to merge into our current branch "blue"

>>>>>>>>> shows the branch we are merging from "green"

```

```bash

notepad.exe color.txt

```

![Alt text](pics/006_merge_conflict_notepad.png?raw=true "Merge conflict in notepad")

```bash

change the lines to

blue and green

```

![Alt text](pics/007_merge_conflict_notepad_fixed.png?raw=true "Merge conflict in notepad fixed")

Save the file and exit notepad.exe

Now lets finsh the merge and clean up

__In your terminal type:__

```bash

git status

git add color.txt

git commit -m "Changed color"

git merge green

cat color.txt

git branch -d green

git checkout main

git status

ls

git merge blue

ls

git branch -d blue

```

![Alt text](pics/009_merge_conflict_finish2.png?raw=true "Merge conflict finish")

Next Lab

[Git revert](../lab09/lab9.md)
