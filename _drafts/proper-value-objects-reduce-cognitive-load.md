---
layout: post
title: Code quality will save your architecture
tags: out of the tar pit
---

_Low level code quality matters way more than your architectural style. When your code base is turning into an alienated stranger, an unmaintainable pulp, and you are itching to rewrite the whole thing, stop. Salvation may be much closer and less risky than you think_. 

Have you ever had the feeling that, after toiling with a code base for 6-12 months, the code base has not turned into the beautiful thing you set out to build? You had the best intentions and swore that _this time_, it was going to be different. Still, as you look at the code base now, it has scars and warts. You are no longer confident when making changes - heck, maybe you don't even really trust the code base. And every time you touch a piece of it, you think "this thing really needs to be refactored".

So, you take the plunge. You start rewriting the whole thing. You put in long hours. You are spewing code, and you are one with the code. You change the architecture to the latest fad. You upgrade all your tools, frameworks, and libraries. For a while, you love the code again, and it loves you. 

You know what is coming, don't you? 

After a while, you start to have doubts. You have had to make a few compromises. The code is becoming harder to understand than you had anticipated. Maybe the architectural style you chose doesn't fit your application as well as you had been lead to believe? Changes are taking longer and longer because the code is becoming an entangled, brittle mess. Again. You are back where you started.

So, what happened? How could it have come to this?

You changed the tools, you changed the frameworks, and you changed the libraries. You changed the architecture. You probably introduced more automated tests. Maybe you even changed the programming language. What is left? You.

What you probably did not change is the way you write code. You did not change the level of attention you pay to detail. You did not become more critical of your own code.

Yet, this is exactly what is needed. 

Unless your initial choice of programming language was [brainfuck](https://en.wikipedia.org/wiki/Brainfuck), chances are that others have had great success with this language. Your pick of tools, frameworks and libraries were probably fine. Your architectural style is overrated. You can do a [Multilayered Architecture](https://en.wikipedia.org/wiki/Multilayered_architecture), a [Sliced Architecture](https://vimeo.com/131633177), a [Hexagonal Architecture](http://alistair.cockburn.us/Hexagonal+architecture), or an [Onion Architecture](http://jeffreypalermo.com/blog/the-onion-architecture-part-1/).

It all doesn't matter one iota if you do not pay attention to the individual characters on your screen that make up your code. You must care for your code blocks, just like an author cares for and nurtures the sentences he produces.

> "We have to keep it crisp, disentangled, and simple if we refuse to be crushed by the complexities of our own making" - Dijkstra

Does your code suffer from any of these code smells:

- objects are mutable for no good reason.
- the most prevalent data types in use are integers and strings ([primitive obsession](http://c2.com/cgi/wiki?PrimitiveObsession)).
- objects that represent a value (a point, an address, a score) have reference equality semantics.
- some methods consider `null` a valid argument while others do not.
- naming is sloppy and inconsistent.
- formatting is sloppy and inconsistent.

The effect of each of these code smells may seem benign. Heck, what does it matter if that `Address` type is just a bunch of public getters and setters? What does it matter if we use `string` to represent an order reference number? That code block is not properly indented. So what?

Well, every time you introduce (or neglect to remove) one of these code smells, you are putting more [cognitive load](https://en.wikipedia.org/wiki/Cognitive_load) on the Code Reader. The compounding effect of all these little things can be enormous. Even if _you_ know that the code is working perfectly, the _Code Reader_ (who might, after all, be you in a couple of weeks) will be spending precious mental resources wondering whether some distant part of the program could possibly change the value of that `Address`, or whether that order reference number could, in some obscure scenario, be `null` and if that is a valid value.

By fixing these code smells, you free up mental resources. You will be able to keep larger portions of the code in your mind at one time. As a consequence, you will start having more confidence in the code and implementing changes and solving problems will require much less effort.

### Conclusion
Before you decide that your code base needs fundamental rewriting and that your tools and architecture need to be killed off, take a long, hard look at the low level quality of your code. You may very well be able to get back to a crisp, disentangled, and simple code base just by rectifying the quality of your code at the very low level. There is no demand to pause development. Rectifying the code from the ground up can be done in small, incremental steps while stile fixing bugs and delivering new features. In fact, improving your code base from the ground up should be part of your daily routine.
