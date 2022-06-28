---
title: Create branches
weight: 10
---

## Task 1 Create branches

Lets create two branches __green__ and __blue__

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

git status

git branch blue

git branch green

git checkout blue

echo "blue" >> color.txt

git add color.txt

git commit -m "Add blue"

```

![Alt text](images/001_create_branches.png?raw=true "Create branches")

Lets do some changes in our green branch

__In your terminal type:__

```bash

git checkout green

echo "green" >> color.txt

git add color.txt

git commit -m "Add green"

```

![Alt text](images/002_change_green_branch.png?raw=true "Create branches")
