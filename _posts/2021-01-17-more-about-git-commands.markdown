---
layout: post
title:  "More about git commands - Search All"
description: Search string in git
date:   2021-01-17 20:30:00 +0530
categories: git commands
---

One fast trick: to search one string in history o git. Feasible:

```
git rev-list --all | xargs git grep "myString"
```

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
