---
title: Take a look in the git folder
weight: 20
---

## Task 2 Take a look in the git folder

Lets take a quick look in the .git folder in newproject

```bash

cd

cd gitops

cd newproject

cd .git

ls

```

![Alt text](images/005_gitfolder.png?raw=true "Git folder ls")

From the top down

- directory "hooks" contain scripts to run at different steps in the git process
- directory "info" contain an exclude file to exclude filetype etc. .gitignore is a better way for excluding files
- directory "objects" gits internal database with blobs, indexed by SHA
- directory "refs" master copy of all refs that exists in your repository, local branches, remote branches, tags and stashes
- file "config" settings for this repository, most used to define where remote lives
- file "description" is for naming the repository but only for git-web
- file "HEAD" current ref you are working at now, this is just a pointer to refs/heads/main

As we start to work with git additional files and folders will appear, we will look back later
