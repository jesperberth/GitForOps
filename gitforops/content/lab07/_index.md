---
title: "Git Branches"
weight: 70
pre: "<b>Lab 7. </b>"
chapter: false
---

In this lab we will learn how to create branches and merge two branches together

## Table of Contents

- [Pre](#pre)
- [Task 1 Git Branch](#task-1-git-branch)
- [Task 2 Git Merge](#task-2-git-merge)

## Pre

Git and windows Terminal must be installed

## Task 1 Git branch

Lets take a look on how a branch works

git status will tell which branch we are working in

git branch branchname will create a new branch

git checkout branchname will change our working branch

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

git status

```

![Alt text](images/001_git_branch.png?raw=true "Git status show branch")

We are on main branch

Lets create a new branch called __development__

__In your terminal type:__

```bash

git branch development

git status

git log --oneline --decorate

```

![Alt text](images/002_git_branch_dev.png?raw=true "Git branch development")

We are still working in main branch, git log tells us that branch developemnt exists

Lets change working branch

git checkout development

__In your terminal type:__

```bash

git checkout development

git status

git log --oneline --decorate

```

![Alt text](images/003_git_checkout_dev.png?raw=true "Git checkout development")

Lets add something to our project

__In your terminal type:__

```bash

echo "Adding pictures to project" >> CHANGELOG

git commit -a -m "updating CHANGLOG"

mkdir images

```

![Alt text](images/004_git_commit_dev.png?raw=true "Git commit development")

Download the picture "In case of fire..."

![Alt text](images/in-case-of-fire-1-git-commit-2-git-push-3-leave-building.png?raw=true "In Case of fire")

Save it in the images directory

__In your terminal type:__

```bash

git add images

git commit -a -m "added picture"

git status

```

![Alt text](images/005_git_commit_dev.png?raw=true "Git commit development")

Lets change branch to main and see whats happend

__In your terminal type:__

```bash

git checkout main

git status

cat CHANGELOG

ls images

```

![Alt text](images/006_git_checkout_main.png?raw=true "Git checkout main")

We are on the main branch but are missing the last line in our CHANGELOG and the picture isn't in the images directory

Try to change back to branch development

__In your terminal type:__

```bash

git checkout development

git status

cat CHANGELOG

ls images

```

![Alt text](images/007_git_checkout_development.png?raw=true "Git checkout development")

Now the changes are visible again

## Task 2 Git merge

In this task we will merge our changes in branch development to main branch

We need to be en the branch we are merging into "main"

__In your terminal type:__

```bash

git checkout main

git status

git merge development

```

![Alt text](images/008_git_merge_development.png?raw=true "Git merge development")

Lets check the result

__In your terminal type:__

```bash

git status

cat CHANGELOG

ls images

```

![Alt text](images/009_git_checkout_main.png?raw=true "Git checkout main")

Now that we have merged our development branch to main we can cleanup and delete the development branch

__In your terminal type:__

```bash

git branch -d development

```

![Alt text](images/010_git_branch_delete.png?raw=true "Git branch delete development")
