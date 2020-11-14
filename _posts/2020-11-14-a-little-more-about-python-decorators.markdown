---
layout: post
title:  "A little more about Decorators in Python"
description: Using anothers decorators in Python
date:   2020-11-14 13:45:00 +0530
categories: python decorators
---

In recent post i talk about some decorators in Python. Now, we show how to use another decorators.
The first example is with static method decorator. This decorator is very easy and represent one static method in you class:

```
class Example3:
    
    @staticmethod
    def test() -> None:
        print('Im a static method')



Example3.test()

```

Note that in this example besides that @staticmethod annotation i'm using type hint to help IDE.

And the other example is about abstract method. In this case we define one abstract method in parent class. Let's go:
```
from abc import ABCMeta, abstractmethod


class Example4(metaclass=ABCMeta):
    @abstractmethod
    def one_abstract_method():
        ...

class TestExample4(Example4):

    def test():
        print('only a test')

    def one_abstract_method():
        print('one abstract method')

test_example_4 = TestExample4
test_example_4.test()
test_example_4.one_abstract_method()


```

In parent class Example4 was created the abstract method called one_abstract_method and in the child class TestExample4 is implemented the method.


and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
