# Lab 3 Git config

In this lab we will configure our local git settings

## Table of Contents

- [Pre](#pre)
- [Task 1 Git config files](#task-1-git-config-files)
- [Task 2 Git config first settings](#task-2-git-config-first-settings)
- [Task 3 Git config local settings](#task-3-git-config-local-settings)

## Pre

Git and windows Terminal must be installed

## Task 1 Git config files

Git has multiple cascading scopes of configuration files the most specific config file takes precedence over the most general

System holds the common settings for all users, like sslbackend, settings are configured under installation, can be changed or overruled in another config

Global is used for user settings an apply to all repositories unless a local config in a repository has another value

On Windows

| Scope | Path |
| ----- | ---- |
| System | install path\etc\gitconfig |
| Global | C:\Users\username\.gitconfig |
| Local | git-repo\.git\config |
| Worktree | git-repo\.git\config.worktree |
| Portable | C:\ProgramData\Git\config |

On Linux

| Scope | Path |
| ----- | ---- |
| System | /etc/gitconfig |
| Global | ~/.gitconfig |
| Local | git-repo\.git\config |
| Worktree | git-repo\.git\config.worktree |

To see what configuration options is set use the command git config --list

__In your terminal type:__

```bash

git config --list

```

![Alt text](pics/001_gitconfig.png?raw=true "Git config")

In my example init.defaultbranch is sat twice so to see which on is going to win we can add an option to the command

__In your terminal type:__

```bash

git config --list --show-origin

```

![Alt text](pics/002_gitconfig_origin.png?raw=true "Git config show origin")

Now we can see where an option is configured and which one will take precedence

## Task 2 Git config first settings

Lets configure the first most common settings

user.name and user.email is your name and email, this will be put into every commit that you create

__In your terminal type:__

```bash

git config --global user.name "Your Name"

git config --global user.email "youremail@domain.com"

git config --list --show-origin

```

![Alt text](pics/003_gitconfig_user.png?raw=true "Git config user")

Lets set two global settings

The first will enable coloring in the git commands

The second will set the default branchname to main, historicaly default branchname was master, to be more inclusive git and others are changing the default to main, however default installation of git is at this time still using master

__In your terminal type:__

```bash

git config --global color.ui auto

git config --global init.defaultbranch main

git config --list --show-origin

```

![Alt text](pics/004_gitconfig_color.png?raw=true "Git config color branch")

Lets take a look at the our global config file

__In your terminal type:__

```bash

cd

cat .gitconfig

```

![Alt text](pics/005_global_config.png?raw=true "Git global config file")

## Task 3 Git config local settings

For out newproject we would like to use another email, we can do this by using the local config which will take precedence from our global config

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

git config user.email "AnotherEmail@domain.com"

git config --list --show-origin

```

![Alt text](pics/006_local_config.png?raw=true "Git local config file")

Next Lab

[Git add status rm](../lab04/lab4.md)
