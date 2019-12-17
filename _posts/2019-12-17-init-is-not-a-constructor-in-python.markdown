---
layout: post
title:  "__init__ is not a constructor in Python"
description: __init__ method is not a constructor
date:   2019-12-17 12:00:36 +0530
categories: python init
---
Recently, i learned that the init method in Python is not a constructor.

Yes, seem simple, but, this method it's to initialize fields in your class. The construtor method is called new.

Follow the example to init method:
```python
    def __init__()
```
Follow the example to new method:
```python
    def __new__()
```

An important diffence is the new method return an instance of class, and the init method, not has return and only initialize values.

and that's all folks!

To any doubt, problem or suggestion, just say.
