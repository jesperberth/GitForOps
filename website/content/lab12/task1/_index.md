---
title: Git tag annotated
weight: 10
---

## Task 1 Git tag annotated

Git tag will show existing tags in project

git tag -a version -m "Comment" will create a annotated tag usually for versioning and releases

__In your terminal type:__

```bash

git tag

git tag -a v1.0 -m "First version tagged"

git tag

```

![Alt text](images/001_git_tag.png?raw=true "git tag -a")

We should have a tag "v1.0" on our HEAD

__In your terminal type:__

```bash

git log

```

![Alt text](images/002_git_log.png?raw=true "git log")

Check with git status that you have an uncommitted change

__In your terminal type:__

```bash

git status

git add .

git commit -m "CHANGELOG modified"

git status

```

![Alt text](images/003_git_status.png?raw=true "git status")

Our v1.0 tag stays the commit it was added to
