---
layout: post
title: The importance of the little things
tags: out of the tar pit
---

_Low level code quality matters way more than your architectural style. When your code base is turning into an unmaintainable pulp, and you are itching to rewrite the whole thing, stop. Salvation may be much closer and less risky than you think_. 

Have you ever had the feeling, after toiling with a code base for 6-12 months, that the code base has not turned into the beautiful thing you set out to build? You had the best intentions and swore that _this time_, it was going to be different. Still, as you look at the code base now, it has scars and warts. You are no longer confident when making changes - heck, maybe you don't even really trust the code base. And every time you touch a piece of it, you think "this thing really needs to be refactored".

So, you take the plunge. You start rewriting the whole thing. You put in long hours. You are spewing code, and you are one with the code. You change the architecture to the latest fad. You upgrade all your tools, frameworks, and libraries. For a while, you love the code again, and it loves you. 

You know what is coming, don't you? 

After a while, you start to have doubts. The code starts to feel dated. It is becoming harder to understand than you had anticipated. Your gut feeling is that a new developer would have a hard time understanding the code. Changes are taking longer and longer because the code is becoming an entangled, brittle mess. Again. You are back where you started.

So, what happened? How could it have come to this?

You changed the tools, you changed the frameworks, and you changed the libraries. You changed the architecture. You probably introduced more automated tests. Maybe you even changed the programming language.

What you probably did not change is the way you write code. You did not change the level of attention you pay to detail. You did not become more critical of your own code. Unfortunately, this means that you are likely to keep introducing a number of trivial code smells:

- Objects are mutable for no good reason.
- Use of primitive integers and strings are prevalent ([primitive obsession](http://c2.com/cgi/wiki?PrimitiveObsession)).
- Objects that represent a value (a point, an address, a score) have reference equality semantics.
- Some methods consider `null` a valid argument while others do not.
- Code is not properly isolated, making it hard to determine the presence or absence of dependencies.
- Naming is sloppy and inconsistent.
- Formatting is sloppy and inconsistent.

I claim that _the compounding effect of all these little things will be enormous_ and that this is what brings down your code base over and over.

The effect of each of the code smells mentioned above may seem benign. Heck, what does it matter if that `Address` type is just a bunch of public getters and setters? What does it matter if we use `string` to represent an order reference number? That code block is not properly indented - so what?

Well, every time you introduce (or neglect to remove) one of these code smells, you are putting more [cognitive load](https://en.wikipedia.org/wiki/Cognitive_load) on the Code Reader. Even if _you_ know that the code is working perfectly, the _Code Reader_ (who might, after all, be you in a couple of weeks) does not. He will be spending precious mental resources wondering about things like

- whether `street` and `streetAddress` are inherently different or are just incosistently named, and
- whether some distant part of the program could possibly change a property of a given `Address`, and
- whether that order reference number could possibly be `null` and if that is a valid value, and
- whether a comparison of two objects is to be trusted.

These are things that have nothing to do with the problem domain, so time spent pondering them is time wasted. 

Reading and understanding the existing code is a prerequisite for making any development. Thus, by paying attention to minute detail and fixing these code smells, we can speed up all development activities. Essentially, we can free up the Code Reader's mental resources, making it easier to implement changes and solve problems.

> "We have to keep it crisp, disentangled, and simple if we refuse to be crushed by the complexities of our own making" - Dijkstra

### Conclusion
Before you decide that your code base needs fundamental rewriting and that your tools and architecture need to be killed off, take a long, hard look at the low level quality of your code. You may very well be able to get back to a crisp, disentangled, and simple code base just by rectifying the quality of your code at the very low level. There is no demand to pause development. Rectifying the code from the ground up can be done in small, incremental steps while still fixing bugs and delivering new features. In fact, _improving your code base from the ground up should be part of your daily routine_.
