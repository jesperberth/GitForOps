---
title: Create a local repository
weight: 10
---

## Task 1 Create a local repository

Open Windows Terminal, you should be in your home directory

![Alt text](images/001_windows_terminal.png?raw=true "Windows Terminal")

create a new directory __gitops__ we will use this as our root directory for the rest of the course

```bash

mkdir gitops

cd gitops

```

![Alt text](images/002_gitops_dir.png?raw=true "Gitops dir")

We can create a new git repository with __git init project name__ or __git init__

__git init project name__ will create a new git repository in a folder with the name of __project name__

__git init__ will create a new git repository in the current folder

```bash

git init newproject

cd newproject

ls -force

```

![Alt text](images/003_gitinit.png?raw=true "Git init")

Create a new folder and run __git init__ make sure you are back in the gitops folder

```bash

cd ..

pwd

mkdir testproject

cd testproject

git init

```

![Alt text](images/004_gitinit2.png?raw=true "Git init")