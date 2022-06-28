---
title: Git add
weight: 10
---

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

![Alt text](images/001_add_file.png?raw=true "Git add")

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

![Alt text](images/002_add_dir.png?raw=true "Git add dir")

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

![Alt text](images/003_add_index.png?raw=true "Git add index")
