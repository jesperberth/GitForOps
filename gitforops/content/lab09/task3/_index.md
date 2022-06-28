---
title: Git revert other commit
weight: 30
---

## Task 3 Git revert other commit

To revert older commits we can either use the SHA-1 value or do a countdown from HEAD

__In your terminal type:__

```bash

git log --oneline

```

![Alt text](images/005_git_log.png?raw=true "git log")

We use ~ to specify how many commits back we want to revert

__In your terminal type:__

```bash

git revert HEAD~2

```

![Alt text](images/006_git_revert_HEAD_2.png?raw=true "git revert HEAD-2")

__In vi type:__

```bash

i (hit i to toggle input)

```

Add your reson for reverting the commit

Save the file

```bash

Hit Esc-key

:wq (: for a command w for write and q for quit vi)

```

![Alt text](images/007_git_revert_HEAD_2_comment.png?raw=true "git revert HEAD-2 Comment")

Lets see what changed

The country.txt file is gone and we have a new commit that reverted the "New Country file" commit

__In your terminal type:__

```bash

ls

git log --oneline

```

![Alt text](images/008_git_revert_log.png?raw=true "git revert result")
