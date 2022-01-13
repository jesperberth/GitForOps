# Lab 9 Git Revert

In this lab we will learn how to revert a previous commit

## Table of Contents

- [Pre](#pre)
- [Task 1 Create files](#task-1-create-files)
- [Task 2 Git revert previous commit](#task-2-git-revert-previous-commit)
- [Task 3 Git revert other commit](#task-3-revert-other-commit)

## Pre

Git and windows Terminal must be installed

## Task 1 Create files

Lets create some new files we can commit and revert, make sure you are in __main__ branch

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

git status

echo "Denmark" >> country.txt

git add country.txt

git commit -m "New Country file"

echo "Ned Flanders" >> author.txt

git add author.txt

git commit -m "New Author file"

```

![Alt text](pics/001_create_files.png?raw=true "Create files")

## Task 2 Git revert previous commit

__In your terminal type:__

```bash

git revert HEAD

```

![Alt text](pics/002_git_revert.png?raw=true "git revert")

This will open the default editor (vi) so you can type the Commit massage, you can add a reason to the end of the line

Save the file

```bash

Hit Esc-key

:wq (: for a command w for write and q for quit vi)

```

![Alt text](pics/003_git_revert_commit_message.png?raw=true "git revert commit message")

Now lets see what happend

The author.txt file is gone and in git log we can see the new Commit (reverting) our previously commit

__In your terminal type:__

```bash

ls

git log

```

![Alt text](pics/004_git_revert_log.png?raw=true "git revert")

## Task 3 Git revert other commit

To revert older commits we can either use the SHA-1 value or do a countdown from HEAD

__In your terminal type:__

```bash

git log --oneline

```

![Alt text](pics/005_git_log.png?raw=true "git log")

We use ~ to specify how many commits back we want to revert

__In your terminal type:__

```bash

git revert HEAD~2

```

![Alt text](pics/006_git_revert_HEAD_2.png?raw=true "git revert HEAD-2")

__In vi type:__

```bash

i (hit i to toggle input)

```

Add your reson for reverting the commit

Save the file

```bash

Hit Esc-key

:wq (: for a command w for write and q for quit vi)

```

![Alt text](pics/007_git_revert_HEAD_2_comment.png?raw=true "git revert HEAD-2 Comment")

Lets see what changed

The country.txt file is gone and we have a new commit that reverted the "New Country file" commit

__In your terminal type:__

```bash

ls

git log --oneline

```

![Alt text](pics/008_git_revert_log.png?raw=true "git revert result")

Next Lab

[Git diff and log](../lab10/lab10.md)
