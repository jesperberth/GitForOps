---
title: Git status
weight: 30
---

## Task 3 Git status

Lets take a look at git status

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

echo Changelog >> CHANGELOG

git status

```

![Alt text](images/006_status_untracked.png?raw=true "Git status untracked")

CHANGELOG isn't tracked as we haven't added it to the staging area

If you add -s to git status you will get the short description

Add CHANGLOG to staging

Check the status

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

git status -s

git add CHANGELOG

git status -s

git status

```

![Alt text](images/007_status_s.png?raw=true "Git status s")

Lets add some text to the CHANGELOG

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

echo "Version 1" >> CHANGELOG

git status

git status -s

```

If we do a commit now, the text "Version 1" won't be commited as the change hasn't been staged

![Alt text](images/008_status.png?raw=true "Git status")

__In your terminal type:__

```bash

git add CHANGELOG

git status -s

git status

```

![Alt text](images/009_status_add.png?raw=true "Git status after add")
