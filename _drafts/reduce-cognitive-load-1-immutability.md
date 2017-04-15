---
layout: post
title: Reduce cognitive load - Immutability
tags: out of the tar pit
---

This post is the first in a series of posts on how to reduce the cognitive load on the Code Reader.
If we can reduce the mental resources the Code Reader must use to read and understand the current code,
we free up resources that can be applied to thinking about solving the business problem at hand.
The purpose of this series is two-fold: to bring to your attention some important deficiencies that 
your code may suffer from without you even realising it, and to give you some tips on how to do this.

This series of posts assumes that you write code in a general purpose object oriented programming language. 
Many of the issues highlighted in this series arise because of the way most current object oriented languages are
designed. Some points will be less relevant in, say, a functional programming language.  

##Immutability

The first thing I want to suggest that you start thinking about is mutability and the impact that mutability
has on the Code Readers ability to understand your code. 

```
public class Appraisal {
    public int Score { get; set }
    public string Category { get; set; }
}
```

Value equality

Immutability

No nulls