---
layout: post
title:  "__init__ is not a constructor in Python"
description: __init__ method is not a constructor
date:   2019-12-17 12:00:36 +0530
categories: python init
---
Recently, I learned that the ``init`` method in Python is not a constructor.

Yes, seems simple, but, this method is used to initialize fields in your class. The constructor method is called ``new``.

Follow the example to init method:
```python
    def __init__()
```
Follow the example to new method:
```python
    def __new__()
```

An important difference is that the ``new`` method return an instance of class, and the ``init`` method, does not have a return and only initialize values.

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
