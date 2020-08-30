---
layout: post
title:  "Using record in Java 14"
description: java record new features
date:   2020-08-30 16:00:00 +0530
categories: java 14 record
---

In more recently times the Java had receive new lauched more frequently. One these features it's the records.
With record now it's possible create "class" more easily and that transport datas.

Let's code:

```
record Test(String name, String age) {}
```

This a definition of record more seems structure of "class". To use is more easy:

```
public class Example {

    public static void main(String[] args) {
        Test test = new Test("myName", "45");
        System.out.println(test);
        System.out.println(test.age());
        System.out.println(test.name());
    }
}

```

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
