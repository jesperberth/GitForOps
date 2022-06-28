---
title: Merge Conflict
weight: 30
---

## Task 3 Merge Conflict

We will do the git merge again but now we will fix the issues

__In your terminal type:__

```bash

git checkout blue

git merge green

```

![Alt text](images/005_merge_conflict.png?raw=true "Merge conflict")

Lets fix the issue in notepad

__In your terminal type:__

```bash

<<<<<<<<< HEAD is our current branch "blue" and the line below is the text we entered

======= seperates the two branches

Next comes the lines we are trying to merge into our current branch "blue"

>>>>>>>>> shows the branch we are merging from "green"

```

```bash

notepad.exe color.txt

```

![Alt text](images/006_merge_conflict_notepad.png?raw=true "Merge conflict in notepad")

```bash

change the lines to

blue and green

```

![Alt text](images/007_merge_conflict_notepad_fixed.png?raw=true "Merge conflict in notepad fixed")

Save the file and exit notepad.exe

Now lets finsh the merge and clean up

__In your terminal type:__

```bash

git status

git add color.txt

git commit -m "Changed color"

git merge green

cat color.txt

git branch -d green

git checkout main

git status

ls

git merge blue

ls

git branch -d blue

```

![Alt text](images/009_merge_conflict_finish2.png?raw=true "Merge conflict finish")
