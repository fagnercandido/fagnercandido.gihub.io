---
layout: post
title:  "Using virtualenv in Python"
description: python virtualenv
date:   2020-08-25 00:10:00 +0530
categories: python virtualenv
---

Sometimes it's interesting using virtual environments to develop. One different version of version installed in SO is enough.
In Python exists the virtualenv. In these virtual environment it's possible use the version by project independent of SO.

Let's code:

```
python3.8 -m venv myvenv
```

By default venv would be installed in your SO. If not just, in Ubuntu:

```
sudo apt-get install python3-venv
```

Now, the new folder was created. Just activate the virtualenv:

```
source bin/activate
```

Done. Now just use python in virtualenv.

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
