---
layout: post
title:  "Using Callbacks with Java"
description: Using callbacks in Java
date:   2020-10-05 16:00:00 +0530
categories: java8 lambda callbacks
---

Certainly you know use callbacks in JavaScripts, right. Or maybe pass one pointer to function in C, for example.
Ok, but, since Java 8 and method references and lambdas we can callbacks in Java. For example:

```
public class MyClass {

    String callback(String name, Function<String, String> myFunction) {
        return myFunction.apply(name);
    }

    public static void main(String[] args) {
        MyClass myClass = new MyClass();
        String result = myClass.callback("Your Name", item -> "Your name is : "+item);
        System.out.println(result);
    }

}
```

First thing to note is i'm using Function. The make part of ```java.util.function``` package.
The method callback(very creative name) receive two arguments: one string to apply and one Function.

And finally i invoke this in method main passing with argument one lambda, function.

So, you can use callbacks in Java.

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
