---
layout: post
title: Rallying the team
---

_How do you make a team produce maintainable code? Let values drive your  principles and practices_.



Consistently producing maintainable code is hard. Many factors work against you:
- time pressure
- eager and bold new developers
- plain laziness

Time pressure and plain laziness will encourage developers to make short cuts. New developers may not fully understand the application architecture and will produce code and dependencies that violate that architecture. It takes just a moment of inattention for code rot to creep in, and once that is in, the Broken Windows Syndrome makes it likely to spread.

So, how do you make the team pay attention to maintainable code, all the time?

You need 
First off, you define _maintainable code_ as a core value, and you articulate this to the team and to management. Next, you derive principles from this value. Eventually, you 








Writing maintainable code is a continuous effort. Time pressure, eager new developers and plain laziness are all forces that tear at the code.


NOTE: find motivating example in literature or history - when has somebody let values define their principles and practices and lead their peers through that?


Articulating maintainability as a value means that you can derive your principles and practices from this.
Values can and should be discussed and defined in cooperation with the business.


I recently drew up the Developer's Creed for the development team at a client. It went something like this:

###Values
- We value an uninterrupted and bug free service.
- We value long term productivity.
- We value maintainability.

###Principles
- We err on the side of caution.
- We strive for backwards compatibility.
- Less code is better, because code is a liability, not an asset.
- We strive for composable, side-effect free units of functionality.

###Practices
- TDD, unit test pretty much everything.
- All changes are peer reviewed.
- Deployed services are heavily monitored.
- We do continuous delivery.