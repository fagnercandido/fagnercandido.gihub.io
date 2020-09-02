---
layout: post
title:  "First time the code appeared in Git and how to find your branch"
description: git branch commit
date:   2020-09-02 11:00:00 +0530
categories: git commit branch
---

Recently, i had needed of found the first time that one code appeared in project.
So, in git it's very simple, just:

```
git log -S "mySuperCode" --source --all
```

But, i needed know how branch belong this commit, it's more easy yet: 

```
    git branch -a --contains hashOfMyCommit
```

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
