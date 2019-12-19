---
layout: post
title:  "Python and Logging"
description: Python and Logging
date:   2019-11-23 20:00:36 +0530
categories: python logging
---
Do you know how to log in Python? Maybe you used a logger in another languages. But how about in Python?

It's very simple, so follow me and let's go. The first step is to import logging:

```python
import logging
```

Now, log a message:

```python
logging.warning('this a message of warning level')
logging.info('this a message of info level') #but this message will not show up, because default level is warning
```

By default, only warning messages are showed.

Additionally, to put messages inside a file, just add the following:

```python
logging.basicConfig(filename='test.log', filemode='w', level=logging.DEBUG)#put message inside a file
```

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.

Sources: [Sources](https://github.com/fagnercandido/loggingpython)
