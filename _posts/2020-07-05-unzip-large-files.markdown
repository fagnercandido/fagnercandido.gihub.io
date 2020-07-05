---
layout: post
title:  "Unzip Large Files"
description: Unzip files large than 4GB
date:   2020-07-05 21:00:00 +0530
categories: python brazil public transparency
---

Recently, i had that unzip files very huge. The file had 17GB. So, i was tried unzip and i was not success.

Searching... i found two tools very useful. One of these it's very curious and the another more formal.

So, the first it's traditional tool:

```
7z x myBigFile.zip 
```

Yes, i used 7z to do this.

But, it's possible too with Java/Jar! Yes, just do:

```
jar xf myBigFile.zip 
```

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
