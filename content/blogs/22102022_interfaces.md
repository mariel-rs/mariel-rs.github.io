---
title: "Interfaces"
date: 2022-10-22
draft: false
author: "Mariel"
tags:
  - java
  - interfaces
  - rambling
  - en
image: 
description: "Relearning interfaces in Java"
toc: true
---

After some weeks of neglecting my self-study Java time, I finally got the time 
to get back on track this week and I reached the **Interfaces** topic. I learned 
this topic when I studied C# some years ago, but it's not quite like that time.
<!--more-->

## What is an interface anyway?

When I was taught interfaces in C# I was confused about the difference between
a class and an interface. They seem to be exactly the *same*, they have methods,
they have instance variables and can be instantiated as well. I still remember
asking the instructor about the differences and sadly getting an unclear answer 
:zany_face:

Leaving C# aside and at a first glance, a Java interface seems to be more 
related to an abstract class than a class itself. However, there's a catch. An 
interface is more of a contractual obligation, if we wish to call it that way, 
than an *extension* of an abstract class or a parent class. An interface defines 
a general description of a how a class should behave with abstract methods but
nothing much more aside from that.

Java has several built-in interfaces - `List`, `Map`, `Set`, to name a few. 
These interfaces are the "precursors" to ArrayList, HashMap and HashSet data 
structures. Having these interfaces in mind, an interface appear to be a general 
data structure definition. Each one of these interfaces are also implementations 
of the `Collection` interface. After that penny-drop, I understand why we also 
call ArrayLists and HashMaps collections.

Coming back to abstract classes, it's not possible to instantiate from an
abstract class, yet it is possible to use interfaces as a method parameter or 
to use it as a return value. Thanks to polymorphism, it is possible to compare
objects from different classes that are implementations of the same interface,
because of this "contractual" obligation that forces the classes to honour.

## Takeaways

In my yet limited experience in Java, I see interfaces as a minimalistic
definition that a class can implement with as many details as necessary for the
functionality in question. Revisiting the collections example, an interface
can be an interface of an interface, and with this, we either get more 
flexibility when handling different data structures or we open up Pandora's box 
:wink:

I remember that in C#, it was preferred to use classes instead of interfaces as
interfaces tended to have lower performance. Plus, at my previous work, class
inheritance and interfaces were discouraged for better code maintenance. I
would have to look up the performance and best practices for Java.

The proprietary language used at work is Java-like and it also uses collections
as a generic way to refer to arrays (static and dynamic). I feel it's all coming
together. Keep it coming Java :coffee: