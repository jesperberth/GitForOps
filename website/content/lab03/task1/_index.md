---
title: Git config files
weight: 10
---

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

![Alt text](images/001_gitconfig.png?raw=true "Git config")

In my example init.defaultbranch is sat twice so to see which on is going to win we can add an option to the command

__In your terminal type:__

```bash

git config --list --show-origin

```

![Alt text](images/002_gitconfig_origin.png?raw=true "Git config show origin")

Now we can see where an option is configured and which one will take precedence
