---
layout: post
title:  "Lambda and Python"
description: Using Lambda in Python
date:   2020-06-23 23:59:36 +0530
categories: python lambda functional programming
---

Lambda calculus it's not a new. Alonzo Church formalized this calculus in 1930's.

Lambda can be undertand with a anonymous function. Yes, in Python, Lambda is a function.

To use in Python it's very simple. Follow the example:

```python
xpto = lambda x : x * 120
```

In the example before, our lambda function receive one argument and return the multiply by 120.

We can make lambda functions better. For example, give a list, we want take the value more near of zero, but for example, there are -1 and 1, the positive value is printed.

With Lambda:

```python
result = [-2,-3,-1, 1,3,2]
print(min(result, key=lambda v: (abs(v), v < 0)))
```

In this case, we're using the function min that receive a lambda function that use abs to calculate the value.

For more references: [Doc](https://docs.python.org/3/tutorial/controlflow.html)

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
