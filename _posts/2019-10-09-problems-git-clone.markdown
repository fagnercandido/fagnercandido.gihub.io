---
layout: post
title:  "Problems with git clone and Windows"
description: Problems with git clone and Windows
date:   2019-10-09 17:00:36 +0530
categories: git clone windows
---
Git is a powerful version manager control. However, it does have many details. Recently, I've had problems with git clone:

#####Git fatal: protocol 'https' is not supported

To resolve this, just:

```sh
git clone "https://myRepo/a.git"
```

Yes, just write the URL between quotation marks.


and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
