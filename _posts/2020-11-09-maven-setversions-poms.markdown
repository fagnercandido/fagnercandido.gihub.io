---
layout: post
title:  "Decorators in Python"
description: Using Decorators in Python
date:   2020-11-07 21:00:00 +0530
categories: python decorators
---

Decorators in Python is basically metaprogramming. To understand decorators in Python, some things will be clear:
- function are high-order objects
- you can pass funcions as arguments
- you can declare inner functions

Now, it's very simple create one decorator:

```
import time


def time_execution(function):
    def wrapper():
        start_time = time.time()
        function()
        end_time = time.time()
        print("[{function}] Time Execution: {total_time}".format(
            function=function.__name__,
            total_time=str(end_time - start_time))
        )

    return wrapper

@time_execution
def main():
    for n in range(0, 10000000):
        pass

main()

```

First thing, we import the module time.
Second, we use the sugar sintax "@". This indicate to the Python that is a decorator.
The core is the function "time_execution". Her receive on function and involves the real function, called of "wrapper".
So, you first decorator works fine.

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
