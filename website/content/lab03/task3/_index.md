---
title: Git config local settings
weight: 30
---

## Task 3 Git config local settings

For out newproject we would like to use another email, we can do this by using the local config which will take precedence from our global config

__In your terminal type:__

```bash

cd

cd gitops

cd newproject

git config user.email "AnotherEmail@domain.com"

git config --list --show-origin

```

![Alt text](images/006_local_config.png?raw=true "Git local config file")
