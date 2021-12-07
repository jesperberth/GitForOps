# Lab 2 Create a local repository

In this lab we will create a local git ripository and take a look inside

## Table of Contents

- [Pre](#pre)
- [Task 1 Create a local repository](#task-1-create-a-local-repository)
- [Task 2 Take a look in the git folder](#task-2-take-a-look-in-the-git-folder)

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

We can create a new git repository with __git init project name__ or __git init__

__git init project name__ will create a new git repository in a folder with the name of __project name__

__git init__ will create a new git repository in the current folder

```bash

git init newproject

cd newproject

ls -force

```

![Alt text](pics/003_gitinit.png?raw=true "Git init")

Create a new folder and run __git init__ make sure you are back in the gitops folder

```bash

cd ..

pwd

mkdir testproject

cd testproject

git init

```

![Alt text](pics/004_gitinit2.png?raw=true "Git init")

## Task 2 Take a look in the git folder

Lets take a quick look in the .git folder in newproject

```bash

cd

cd gitops

cd newproject

cd .git

ls

```

![Alt text](pics/005_gitfolder.png?raw=true "Git folder ls")

From the top down

- directory "hooks" contain scripts to run at different steps in the git process
- directory "info" contain an exclude file to exclude filetype etc. .gitignore is a better way for excluding files
- directory "objects" gits internal database with blobs, indexed by SHA
- directory "refs" master copy of all refs that exists in your repository, local branches, remote branches, tags and stashes
- file "config" settings for this repository, most used to define where remote lives
- file "description" is for naming the repository but only for git-web
- file "HEAD" current ref you are working at now, this is just a pointer to refs/heads/main

As we start to work with git additional files and folders will appear, we will look back later

Next Lab

[Git config](../lab03/lab3.md)
