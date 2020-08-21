---
layout: post
title:  "@CSVBindByName using format"
description: opencsv csvbindbyname format
date:   2020-08-21 11:00:00 +0530
categories: java csv
---

Do you use the library called OpenCSV? With this library generate any csv file is more easy. 

So, because the excel and scientific notation i needed put one equals(=) before the some values.

Using the annotation @CSVBindByName it's possible with attribute called format.

```
@CSVBindByName(format = "=%s")
```

I had to read the case test of documentation to find any example of use this attribute, but, nice!

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
