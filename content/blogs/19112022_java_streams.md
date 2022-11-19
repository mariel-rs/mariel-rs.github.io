---
title: "Flowing like a stream"
date: 2022-11-19
draft: false
author: "Mariel"
tags:
  - java
  - streams
  - rambling
  - en
image: 
description: "Discovering streams in Java"
toc: true
---

This has been a hectic period and as a consequence, I have neglected this blog.
I had to push a temporary pause to my Java course, but I'm back. In this post, 
I'll talk about the famous streams that I have never heard about, yet I have
worked similar operations in other programming languages.
<!--more-->

## What is a stream?

My programming background is mostly C# and Python, and further complemented with 
JavaScript. In all these languages, the typical way of handling collections - 
i.e. arrays, dictionaries, lists... - was with loops. Depending on the nature of 
the data being stored in the collections, it could either be a `while-loop` or a 
`for-loop`.

During my early days of programming in 2019, I remember watching a JSConf
presentation where Anjana Vakil was describing how awesome it was to use 3
simple operations for handling almost everything. When I saw the concepts she 
referred to were only available in JavaScript, or so I thought, I left that 
video in a hidden part of my brain and didn't get back to it. However, it made
so much sense to stop mutating objects on every control sequence. The way I used
to program in C# had a lot of imperative style at that time. When I took the 
JavaScript course this summer, I was finally introduced to the famous `map`, 
`reduce` and `filter` operations she talked about with the sandwich example. I 
understood why Anjana was so excited to talk about them! :grin: Link to the 
video [here](https://www.youtube.com/watch?v=e-5obm1G_FY)

The past couple of weeks I have worked on part 10 of the Java course, which 
introduced me to the streams API. Streams are a more natural way of handling 
collections in Java, where things are done in one go - instead of iterating over 
each item and add the required logic to transform them. Streams allow to have
intermediate operations such as the `map`, `reduce` and `filter` operations that 
would process the items in the collection and final operations for closing the 
stream, such as `count`, `max`, `sum`, or even create a new collection. Code 
looks much cleaner as well. 

Let's consider a case where we want to sum the items contained in an `arraylist`

```java
ArrayList<Integer> aListWithNumbers = new ArrayList<>();
listWithNumbers.add(10);
listWithNumbers.add(40);
listWithNumbers.add(50);
```

This is how this sum is done with a `for-loop`:

```java
int sumWithLoop = 0;
for (Integer number : listWithNumbers) {
    sumWithLoop += number;
}
```

Compare against how a stream does this:

```java
int sumWithStreams = listWithNumbers.stream()
                                  .mapToInt(num -> num).sum();
```

This opens a whole new universe for me. Streams allow the programmer to write
more readable code showing the exact sequence of steps that are needed. The
way I see it, it's a bundle of operations done in one go, retaining the original
data collection values the same. **N.b.** I know I shouldn't, but I can't help 
of being reminded of functional programming concepts and another programming
language with similar name :boom: _ :boom:

One of the things I found slightly annoying about programming in Java is the
amount of code I have to write to achieve one simple task. It feels a lot more
verbose, as opposed to C#. I am not even comparing it against Python, where... 
well, they aren't comparable :zany_face: Yet, Streams do offer a quicker way of
making lots of operations without having to write an encyclopedia of code.

Regarding performance, streams do not offer any advantage to the well-known 
loops in a short scale. However, code maintainability does improve as streams
use declarative programming paradigm. For a small list, like the one in the 
example above, there is no performance benefit if using a stream. Now, if the 
list was huge, e.g. a list of files to be processed by a web service, then 
streams are definitely a game-changer as they support parallel processing!

## Side notes to stream on

1. I find streams to be a great enhancer to Java's rigorous object-oriented 
programming paradigm. The language is supplemented with expressions that allow
to write declarative code. It is much easier to read, understand and even
maintain code. I do see functional programming hints that I hope to explore
further. 

2. Two weeks ago I had the chance to take a peek at an in-house developed tool
for comparing output files from two different programs. The tool was developed 
entirely in Java 8 and guess what they were using for processing files? Yes,
streams! The number of files to process ranged from 1000 to 5000, so definitely
not a small collection. To make the processing faster, `parallelStream` was in 
use.

1. After playing with streams and getting my hands on practical stuff that used
streams, I couldn't help but remember my dissertation project - a heuristic
method for allocating slots for landing or taking-off in congested airports. 
The heuristic method was written in Python, given the short timeframe for 
producing a working method and writing the dissertation. The method suffered 
from two main "villains":
     - Curse of dimensionality as the problem to solve was combinatorial. The
      time to find a solution increased as the number of items increased. It 
      also hit quadratic times when doing neighbourhood searches :no_mouth:
     - Python - Sadly, Python is good for prototyping but for production code, 
      it is slow and inefficient.
  
    I made a note on the dissertation conclusions mentioning that it would be 
    worth re-writing the code in a compiled language for speeding up the elapsed 
    times. I could only think on languages such as C++ or even Go at that time. 
    However, Java is now a feasible candidate thanks to its streams.