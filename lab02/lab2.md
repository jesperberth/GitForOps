# Lab 2 Create a local repository

In this lab we will create a local git ripository and take a look inside

## Table of Contents

- [Pre](#pre)
- [Task 1 Create a local repository](#task-1-create-a-local-repository)
- [Task 2 Install Visual Studio Code](#task-2-install-visual-studio-code)
- [Task 3 Install Windows Terminal](#task-3-windows-terminal)

## Pre

Git and windows Terminal must be installed

## Task 1 Create a local repository

Open Windows Terminal, you should be in your home directory

![Alt text](pics/001_windows_terminal.png?raw=true "Windows Terminal")

create a new directory __gitops__ we will use this as our root directory for the rest of the course

```bash

mkdir gitops

cd gitops

```

![Alt text](pics/002_gitops_dir.png?raw=true "Gitops dir")

We can create a new git repository with __git init__ or __git init project name__

```bash

git init newproject

cd newproject

ls -force

```

![Alt text](pics/003_gitinit.png?raw=true "Git init")

