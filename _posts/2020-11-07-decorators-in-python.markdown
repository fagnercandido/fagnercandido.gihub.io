---
layout: post
title:  "Decorators in Python"
description: Using Decorators in Python
date:   2020-11-09 14:15:00 +0530
categories: maven pom
---

Recently, we need changes all version in pom file. But, there are a little problem: the are more than 70 modules in project.
Ok, you can do replace for all files using Notepad++ or another tool. But, the maven provides one manner more easy:

```
    mvn versions:set -DnewVersion=myNewVersion
    mvn versions:commit
```
Now, all poms are updated.

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
