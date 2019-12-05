---
layout: post
title:  "Java and ModelMapper Converter - Destination is null"
description: Java and ModelMapper Converter
date:   2019-12-05 12:00:36 +0530
categories: java model mapper converter null
---
Recently, i had needed create mappers in Java using ModelMapper.

But, i too had needed create converters in these mappers. So, when i was use destination, i always received a NPE.

To resolve this, follow the solution:
```java
    context.getMappingEngine().createDestination(context);
```
In this solution i create manually a destination. Now, i can make get/set in fields.

and that's all folks!

To any doubt, problem or suggestion, just say.
