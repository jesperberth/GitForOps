# Lab 5 Git commit

In this lab we will learn how to add files monitor our status and remove files

## Table of Contents

- [Pre](#pre)
- [Task 1 Git commit](#task-1-git-commit)
- [Task 2 Git commit and remove files](#task-2-git-commit-and-remove-files)

## Pre

Git and windows Terminal must be installed

## Task 1 Git commit

We use git commit to record the changes in our repository, we will write a comment to every commit

By default git uses vi to edit commit messages

Commands to use in vi

i = enable input

esc + : to enter commands

wq to write and quit

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

git status

git commit

- press i to input comment

- press esc key

- press : key

- type wq

- hit enter

git status

```

![Alt text](pics/001_git_commit.png?raw=true "Git commit")

![Alt text](pics/002_vi.png?raw=true "vi comment")

![Alt text](pics/003_git_commit_done.png?raw=true "Git commit done")

Now lets see what has changed

In our .git directory a new file has apperead

COMMIT_EDITMSG

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

git status

cat .git/COMMIT_EDITMSG

```

![Alt text](pics/004_git_editmsg.png?raw=true "Git commit message")

Take a look with git log

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

git log

```

![Alt text](pics/005_git_log.png?raw=true "Git log")

Git log will give us the date and time for the commit aswell as who did it and it will show us the SHA-1 value of the commit

We can take a look in the .git folder to find the objects, the first to two digits will tell us which directory our commit is stored - in this case __"fe"__

__In your terminal type:__

```bash

ls .\.git\objects\fe\

```

![Alt text](pics/006_git_object.png?raw=true "Git object")

The file "1d835b3e9020d29717468ff3b3a0970b15655c" is a hashed compressed binary file of all our commited files

## Task 2 Git commit and remove files

Lets add and commit some files

git commit -m "Some comment" will add a one line comment to the commit, without using vi

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

echo Issues >> ISSUES.md

git status

git add ISSUES.md

git commit -m "Adding ISSUES file"

git status

git log

```

![Alt text](pics/007_git_commit.png?raw=true "Git commit")

We can untrack the file with git rm --cached ISSUES.md, the file will stay on the disk but will no longer be monitored by git

__In your terminal type:__

```bash

git rm --cached ISSUES.md

git status

git commit -m "Removed ISSUES.md"

```

![Alt text](pics/008_git_rm.png?raw=true "Git rm")

Lets add back the ISSUES.md file and add some text

If we do a commit after editing the file the changes will not be commited, if we add -a to the commit it will add changed files

git commit -a will commit all changed files

__In your terminal type:__

```bash

git add ISSUES.md

echo "Missing pictures" >> .\ISSUES.md

git status

git commit -a -m "Adding ISSUES.md back"

git status

```

![Alt text](pics/009_git_commit_a.png?raw=true "Git commit a")

Do a final git log to see all our commits

__In your terminal type:__

```bash

git log

```

![Alt text](pics/010_git_log.png?raw=true "Git log")

Next Lab

[Git ignore](../lab06/lab6.md)
