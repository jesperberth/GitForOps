---
title: Git commit
weight: 10
---

## Task 1 Git commit

We use git commit to record the changes in our repository, we will write a comment to every commit

By default git uses vi to edit commit messages

Commands to use in vi

i = enable input

Type you commit message here

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

- Type your commit message here

- press esc key

- press : key

- type wq

- hit enter

git status

```

![Alt text](images/001_git_commit.png?raw=true "Git commit")

![Alt text](images/002_vi.png?raw=true "vi comment")

![Alt text](images/003_git_commit_done.png?raw=true "Git commit done")

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

![Alt text](images/004_git_editmsg.png?raw=true "Git commit message")

Take a look with git log

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

git log

```

![Alt text](images/005_git_log.png?raw=true "Git log")

Git log will give us the date and time for the commit aswell as who did it and it will show us the SHA-1 value of the commit

We can take a look in the .git folder to find the objects, the first to two digits will tell us which directory our commit is stored - in this case __"fe"__

__In your terminal type:__

```bash

ls .\.git\objects\fe\

```

![Alt text](images/006_git_object.png?raw=true "Git object")

The file "1d835b3e9020d29717468ff3b3a0970b15655c" is a hashed compressed binary file of all our commited files
