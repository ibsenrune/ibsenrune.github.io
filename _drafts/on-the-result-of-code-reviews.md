---
layout: post
title: On the result of code reviews
---

_Teams evaluating the pros and cons of code reviews often draw wrong conclusions. This is because the main benefit of code reviews is not what they think._

Code reviews have a long history in our industry. I think this stems from the old mantra "the cheapest way to remove bugs is to not put them in in the first place." One way of removing bugs before they are put into  them into our software is to do code reviews. 

So, you would think that code reviews were an established part of our craft and that everybody did them. You would think that code reviews were taught at universities. Yet, they are not. Code reviews are not taught at universities, and many teams do not do code reviews.

This is because the number of bugs found by code reviews does not retfærdiggøre the substantial effort that goes into doing proper code reviews. Teams may try out code reviews for a while, but when they pause to evaluate and think about the number of bugs found in, they are likely conclude that code reviews are too costly. And they are probably right.

Doing code reviews to remove bugs is a fallacy! Research by Microsoft shows, that only 15% of review comments pertain to possible bugs in the code.

 However, my experience shows that this is not the case at all. 
They used to be called formal inspections and consist of a large number of people sitting in a meeting reviewing code. These days, code reviews are typically more light weight. 


Outline:
The purpose of the code review is not what you think. Most programmers think that code reviews are performed to catch bugs (Back this up with Microsoft Research Article.). Instead, the real benefit of code reviews is maintainable code. This view of things is supported by the fact (find reference) that 
the cheapest way to remove bugs is not to put them in  in the first place.
Now, this means that when teams evaluate the benefits of code reviews versus the drawbacks (a proper code review takes time), they are inclined to count the number of bugs found in code reviews, compare that to the time spent in code reviews and on that basis conclude that code reviews are not worth the effort.

Code reviews do not find bugs. Thus, they are not worth teaching in universities, where students do not maintain code over extended periods of time.

Sell code reviews!