---
title: Git revert previous commit
weight: 20
---

## Task 2 Git revert previous commit

__In your terminal type:__

```bash

git revert HEAD

```

![Alt text](images/002_git_revert.png?raw=true "git revert")

This will open the default editor (vi) so you can type the Commit massage, you can add a reason to the end of the line

Save the file

```bash

Hit Esc-key

:wq (: for a command w for write and q for quit vi)

```

![Alt text](images/003_git_revert_commit_message.png?raw=true "git revert commit message")

Now lets see what happend

The author.txt file is gone and in git log we can see the new Commit (reverting) our previously commit

__In your terminal type:__

```bash

ls

git log

```

![Alt text](images/004_git_revert_log.png?raw=true "git revert")
