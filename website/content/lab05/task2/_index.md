---
title: Git commit and remove files
weight: 20
---

## Task 2 Git commit and remove files

Lets add and commit some files

git commit -m "Some comment" will add a one line comment to the commit, without using vi

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

echo Issues >> ISSUES.md

git status

git add ISSUES.md

git commit -m "Adding ISSUES file"

git status

git log

```

![Alt text](images/007_git_commit.png?raw=true "Git commit")

We can untrack the file with git rm --cached ISSUES.md, the file will stay on the disk but will no longer be monitored by git

__In your terminal type:__

```bash

git rm --cached ISSUES.md

git status

git commit -m "Removed ISSUES.md"

```

![Alt text](images/008_git_rm.png?raw=true "Git rm")

Lets add back the ISSUES.md file and add some text

If we do a commit after editing the file the changes will not be commited, if we add -a to the commit it will add changed files

git commit -a will commit all changed files

__In your terminal type:__

```bash

git add ISSUES.md

echo "Missing pictures" >> .\ISSUES.md

git status

git commit -a -m "Adding ISSUES.md back"

git status

```

![Alt text](images/009_git_commit_a.png?raw=true "Git commit a")

Do a final git log to see all our commits

__In your terminal type:__

```bash

git log

```

![Alt text](images/010_git_log.png?raw=true "Git log")
