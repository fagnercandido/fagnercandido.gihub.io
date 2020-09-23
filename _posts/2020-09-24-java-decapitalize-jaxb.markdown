---
layout: post
title:  "JAXB and DeCapitalize"
description: java jaxb capitalize
date:   2020-09-24 00:10:00 +0530
categories: java jaxb
---

Recently, i need call another services with XML. And, using JAXB, i had the following problem:

The class name it's decapitalize. I will explain

```
public class MyClass
```

And, in XML:


```
    <myClass></myClass>
```

For me, it's a problem. And the detail it's, when your class it's not a root element, the JAXB decapitalize the name of element.
To solve this, just:

```
    @XmlElementRoot
    public class MyClass
```

Now, in the XML:


```
    <MyClass></MyClass>
```

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
