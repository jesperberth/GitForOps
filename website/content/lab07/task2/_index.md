---
title: Git merge
weight: 20
---

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
