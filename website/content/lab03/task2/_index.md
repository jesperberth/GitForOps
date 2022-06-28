---
title: Git config first settings
weight: 20
---

## Task 2 Git config first settings

Lets configure the first most common settings

user.name and user.email is your name and email, this will be put into every commit that you create

__In your terminal type:__

```bash

git config --global user.name "Your Name"

git config --global user.email "youremail@domain.com"

git config --list --show-origin

```

![Alt text](images/003_gitconfig_user.png?raw=true "Git config user")

Lets set two global settings

The first will enable coloring in the git commands

The second will set the default branchname to main, historicaly default branchname was master, to be more inclusive git and others are changing the default to main, however default installation of git is at this time still using master

__In your terminal type:__

```bash

git config --global color.ui auto

git config --global init.defaultbranch main

git config --list --show-origin

```

![Alt text](images/004_gitconfig_color.png?raw=true "Git config color branch")

Lets take a look at the our global config file

__In your terminal type:__

```bash

cd

cat .gitconfig

```

![Alt text](images/005_global_config.png?raw=true "Git global config file")
