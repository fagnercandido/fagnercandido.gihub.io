---
layout: post
title:  "SimpleDateFormat is not ThreadSafe"
description: Problems with SimpleDateFormat
date:   2020-10-14 20:00:00 +0530
categories: java8 simpledateformat threads
---

Recently, i needed generated one csv with until 50k rows. One theses fields was an date.
Optmizing the iteration in collection:

```
    myBigList.parallelStream(...)
```

In the middle of setters was one SimpleDateFormat and NumberFormatException and errors of multiple lines was showed.
So, i remember: SimpleDateFormat is not thread safe. In this case, to solve this, just use DateTimeFormatter, that is thread safe.
The difference is that DateTimeFormatter work with LocalDateTime.

```
DateTimeFormatter formatter = DateTimeFormatter.ofPattern("myPattern");
LocalDateTime dateTime = LocalDateTime.parse(str, formatter);
```

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
