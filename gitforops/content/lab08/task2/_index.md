---
title: Merge Conflict abort
weight: 20
---

## Task 2 Merge Conflict abort

In this task we will do a merge of blue and green branch, a conflict will happend and we will use abort to get out of our conflict

__In your terminal type:__

```bash

git checkout blue

git merge green

```

![Alt text](images/003_merge_conflict_abort.png?raw=true "Merge conflict abort")

Now we can either fix the conflict with git or do an abort and solve the issue by our self

__In your terminal type:__

```bash

git merge --abort

```

![Alt text](images/004_merge_conflict_abort.png?raw=true "Merge conflict abort")
