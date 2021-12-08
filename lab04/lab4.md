# Lab 4 Git add status rm

In this lab we will learn how to add files monitor our status and remove files

## Table of Contents

- [Pre](#pre)
- [Task 1 Git add](#task-1-git-add)
- [Task 2 Git rm](#task-2-git-rm)
- [Task 3 Git Status](#task-3-git-status)

## Pre

Git and windows Terminal must be installed

## Task 1 Git add

We use git add to register files for sourcecontrol

Files in our working directory is not monitored by git, when adding a file to git, git will register the file making a SHA 1 hash value and put it into the index, any changes to the file is now monitored and is now in the staging area

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

git status

notepad.exe README.md

- Add the text # Newproject

- and save the file

git status

git add README.md

git status

```

![Alt text](pics/001_add_file.png?raw=true "Git add")

Lets add a directory for out html pages

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

mkdir html

git add html

git status

```

![Alt text](pics/002_add_dir.png?raw=true "Git add dir")

Note that git dosn't monitor empty directories

Add a file to the html directory

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

notepad.exe html/index.html

- save the file

git add html/index.html

git status

```

![Alt text](pics/003_add_index.png?raw=true "Git add index")

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

![Alt text](pics/004_git_rm.png?raw=true "Git rm")

So the file cannot be removed as it hasn't been commited to the repository, and there for there is no way to undo it

__In your terminal type:__

```bash

git rm html/todo -f

git status

```

![Alt text](pics/005_git_rm_f.png?raw=true "Git rm f")

## Task 3 Git status

Lets take a look at git status

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

echo Changelog >> CHANGELOG

git status

```

![Alt text](pics/006_status_untracked.png?raw=true "Git status untracked")

CHANGELOG isn't tracked as we haven't added it to the staging area

If you add -s to git status you will get the short description

Add CHANGLOG to staging

Check the status

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

git status -s

git add CHANGELOG

git status -s

git status

```

![Alt text](pics/007_status_s.png?raw=true "Git status s")

Lets add some text to the CHANGELOG

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

echo "Version 1" >> CHANGELOG

git status

git status -s

```

If we do a commit now, the text "Version 1" won't be commited as the change hasn't been staged

![Alt text](pics/008_status.png?raw=true "Git status")

__In your terminal type:__

```bash

git add CHANGELOG

git status -s

git status

```

![Alt text](pics/009_status_add.png?raw=true "Git status after add")

Next Lab

[Git commit](../lab05/lab5.md)
