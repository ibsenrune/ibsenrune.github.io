---
layout: post
title: Immutability - Reduce cognitive load  
tags: reducing cognitive load
---

This post is the first in a series of posts on how to reduce the cognitive
load on the Code Reader.  If we can reduce the mental resources the Code
Reader must use to read, understand, and reason about our code, we free up
precious mental resources that can be applied to thinking about solving the
business problem at hand.

This series of posts assumes that you write code in a general purpose object
oriented programming language. Many of the issues highlighted in this series
arise because of the way most current object oriented languages are
designed. Some points will be less relevant in, say, a functional
programming language.  

##Immutability

The first thing I want to suggest is that you start thinking about is
mutability and the impact that mutability has on the Code Reader's ability to
reason about your code. 

Let's assume that you are asked to refactor the following piece of code:

```
public void 
```

```
public class Appraisal {
    public int Score { get; set }
    public string Category { get; set; }
}
```

Value equality

Immutability

No nulls
