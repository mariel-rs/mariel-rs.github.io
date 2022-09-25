---
title: "Java Programming I MOOC"
date: 2022-09-12
draft: false
author: "Mariel"
tags:
  - java
  - en
image: false
description: "Finished my first Java course"
toc: true
---

This weekend I finished the Java Programming I course offered as a MOOC by the
University of Helsinki. Here are my thoughts after _circa_ 6 weeks of Java. This
is going to be a lengthy post, so if you feel like reading, let's crack on.
<!--more-->

## Learning Java with the University of Helsinki MOOC

The way I have learned programming languages had always been, fortunately, in 
instructor-lead courses, and then I moved onto studying on my own after
gathering a good foundation.

Considering this is my third (or forth...?) programming language, I felt that I 
could go through a self-paced course on my own without relying on an instructor. 
Books are a great resource, yet at the level I was (and I still am), I don't 
feel confident enough to follow a book and perhaps get lost on the amount of 
information. Books will be for a later stage.

Before jumping and enrolling into any random Coursera / edX / udemy / 
_insert name of online course provider here_, I had to do a thorough research
because this time, I didn't know a thing about Java. There are way too many 
options available of online courses and without having prior exposure, it was 
hard to discern which was good and which was crap. Fortunately, I came across a 
post on Reddit that curated a list of free online courses for Java and this 
course was highly recommended.

The material is carefully prepared and the exercises were quite helpful for 
ramping up on Java. I should admit that, at some point, I found the exercises to 
be a bit of a game that I had to ace. It never got boring or tiresome that I
would consider dropping out.

I finished the whole course on circa 6 weeks, dedicating an average of 6 hours 
per part. The course material advises to allocate at least 10 hours per part, 
with each part being covered in one week. Considering this is not my first 
programming language, I got curious on how much time I would take to cover the 
topics, so I kept a log of the amount of hours dedicated per part with Clockify
and WakaTime. 

I am aware that the answers are only a _google-search_ away, yet I decided to 
challenge myself to write code myself. I did consult the documentation and some 
reference material for revising some topics though! So here I declare the answer 
to the programming exercises are solely my own work! :zany_face:

There are some typos on the material here and there, which to be fair, they are 
quite minor and harmless. I came across a few Finnish words popping up suddenly 
in the exercise's carcasses. For example, *luku* instead of *number*, but it was 
easy to figure out what they meant from the context.

## Highlights and fun times

As you may know, the course is split in 7 parts, and builds up to more 
challenging exercises and topics. Here are a few comments and the most highlights
(personal opinion) of each part.

### Introduction (Part 1 and Part 2)

These parts have the usual introductory material when learning a programming
language - variables, data types, conditionals and loops. The exercise list was
quite long, but I understand why the course organizers decided to do that. This
course does not assume the student has prior programming experience.

I found useful the "Recurring problems and patterns" section as it offered clear
explanations on why the patterns are used that way and why we should make our
programs smart. I have used these patterns before at work, without realizing 
there was a reason the programs were designed in such way.

### First data structures (Part 3)

Part 3 focused on lists and arrays data structures and their main methods. After 
programming for almost two years in Python non-stop, and not writing much in C#
for a while, I got a bit "lazy" with several data structures. In particular,
lists (_ArrayList_) and arrays. C# also has these data structures and so this
part was a good refresher. 

### Object-oriented programming (Part 4)

This part introduces object-oriented programming (OOP) concepts. However, on an 
interesting turning point, it focused a lot on opening and handling files. I 
struggled a bit here because I run into a silly situation - my code was correct
but it simply would not open any file! :zany_face: 

I figured out it was because the program was being compiled from a different 
folder (wtf), rather than the project folder and so the file search did not work 
out. But that reminded me of an important lesson: read the documentation! 

### More OOP (Part 5)

This part went back to object-oriented programming topics and extended on what was
introduced on part 4. I found to be extremely helpful the "Primitive and 
reference variables" and the "Objects and references" sections. The explanations 
were clear and the exercises were great for reinforcing the material.

### Object handling, spliting functions and unit testing (Part 6)

This was my most favourite part of the course. The course took a major step up
and introduced me to unit testing using Maven and JUnit. I enjoyed exploring 
Maven and finding out why my development environment kept complaining about a 
_missing_ Maven... I didn't install it! :rofl: I must have missed it. 

I couldn't help myself from comparing Jest (for JavaScript) and JUnit. Both 
share a similar syntax but I liked that JUnit allows annotations, especially
useful for data that can be brought *@Before* running the test suite.

### Programming paradigms, algorithms and large programming exercises (Part 7)

This was mainly a recap part where the content shows the advantages and 
disadvantages of procedural and object-oriented programming paradigms. The last
three exercises were fun to do, as they were only given as functionalities to
be implemented, rather than explicit instructions on which files, classes,
methods, variables, ..., to create. I particularly enjoyed the Algorithms 
section, though to my taste it was too short! :wink:

## Final thoughts (aka tl;dr)

I see why this course has such popularity amongst programmers. It's engaging, 
fun, no-nonsense exercises and straight to business. I saw how the course builds 
up on complexity and introducing to useful stuff, for instance, unit testing, 
test-driven development, program logic, reference vs primitive variables and in 
general, useful topics.

I have also taken a look at other courses that the University has on offer. 
In particular, the Full Stack Open course looks great. But for now, I'll stick 
to Java. I am definitely enrolling in the second part of the course. 
Hard to believe that I am enjoying programming in Java, but hey, :coffee:
**never say never**.