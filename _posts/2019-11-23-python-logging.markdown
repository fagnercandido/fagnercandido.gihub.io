---
layout: post
title:  "Python and Logging"
description: Python and Logging
date:   2019-11-23 20:00:36 +0530
categories: python logging
---
Do you know logging in Python? Maybe you put logger in another languages. But in Python?

It's very simple, and let's go. The first step is import logging:

```python
import logging
```

Now, put message logging:

```python
logging.warning('this a message of warning')
logging.info('this a message of info') #but this message not show, because, default level is warning
```

By default, only warning messages is showed.

But, to put messages inside a file, just:

```python
logging.basicConfig(filename='test.log', filemode='w', level=logging.DEBUG)#put message inside a file
```

and that's all folks!

To any doubt, problem or suggestion, just say.

Sources: [Sources](https://github.com/fagnercandido/loggingpython)
