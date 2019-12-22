---
layout: post
title:  "Java and ModelMapper Converter - Destination is null"
description: Java and ModelMapper Converter
date:   2019-12-05 12:00:36 +0530
categories: java model mapper converter null
---
Recently, I needed to create mappers in Java using ModelMapper.

But, I needed to create converters in those mappers too. So, when I needed a destination, I always received a NPE.

To resolve that, follow the solution:
```java
    context.getMappingEngine().createDestination(context);
```
In this solution I created manually a destination. Now, I can make get/set in fields.

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
