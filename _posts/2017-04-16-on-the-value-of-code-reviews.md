---
layout: post
title: On the value of code reviews
tags: code review
---

_Teams evaluating the pros and cons of code reviews often draw wrong conclusions. This is because the main benefit of code reviews is not what the team thinks._

As software developers, we strive every day to write code that is free from bugs. One thing that obviously helps avoid bugs is to do code reviews: whenever someone has authored a piece of code, someone else reviews it before it goes into the code base. Yet, few teams have code reviews as a core part of their development process. Why is that?

## Why would you omit code reviews?
For some teams, it may not be a conscious choice not to have code reviews. Most schools do not include code reviews in the development process they teach, and since few teams do them, you can easily spend quite a few years in the industry without encountering code reviews. Thus, teams may omit code reviews solely because it does not occur to anybody on the team that reviews might be a thing, let alone that they might be worth the effort.

Other teams consciously decide to omit code reviews because they do not consider them worth the effort. 

Code reviews certainly require effort, and for them to be effective, they require substantial effort. A team that tries to adopt code reviews as part of the development process realises this very quickly. So, the benefits that such reviews provide must be equally substantial, or they will be a waste of time.

How do we measure these benefits? In my experience, there are two popular approaches to doing this: if a team is very serious about improving their development process, they will try out code reviews for a fixed time period. At the end, they will _count the bugs found in reviews_ and equate that to the benefit of the reviews. Teams less hell-bent on gathering empirical data may count all the bugs that have been identified in their software in the last year (in production, though testing, or otherwise) and consider the identification of these bugs an upper bound on the benefit of code reviews, since code reviews _might_ have identified these bugs earlier.

Now, if a team is building software for space ships, then finding bugs is very valuable and they are likely to conclude that code reviews are a great tool. However, most teams write applications that are slightly more mundane, where occasional bugs are tolerated. Thus, the latter teams are likely to conclude that code reviews are too costly.

## Code reviews are about more than bugs
Doing code reviews mainly to remove bugs is a fallacy. [Research](http://dl.acm.org/citation.cfm?id=2819015) shows that only 15% of review comments pertain to possible bugs in the code. The rest of the review comments are about pointing out opportunities for improving clarity and readability to ensure long-term maintainability.

The value of improved readability alone is enormous, since reading and understanding the existing code is a prerequisite for making any sort of changes, be they bug fixes or new features. Long-term maintainability is vital as well because it helps avoid costly rewrites.

Finally, code reviews are a great vehicle for spreading institutional knowledge and sharing tips and tricks. I have on multiple occasions been amazed at how quickly I could add junior developers to very experienced teams and make them productive team members. I attribute a great deal of this success to an efficient code review process. 

## Conclusion
Code reviews are not only about bugs. When evaluating whether code reviews should be part of your development process, remember that code reviews have other benefits than just identifying bugs. If your team writes code that needs to be reasonably bug-free and maintainable for years, then code reviews should probably be a part of your development process. This is even more true if you occasionally add new team members.
