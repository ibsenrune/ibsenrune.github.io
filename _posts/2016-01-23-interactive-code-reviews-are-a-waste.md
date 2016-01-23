---
layout: post
title: Interactive code reviews are a waste
---

Code reviews have been around at least since the late '70s. These days, most software development teams worth their salt do code reviews. However, not all code reviews were created equal, and one particularly prevalent type is worthless at best.

The type of code review I have seen the most is what I like to call the "interactive" code review. Here, the author and the reviewer sit down together to go through the code. If they are co-located, the review will often take place at the author's desk. Otherwise, it might be facilitated by video conferencing software. While this is typically a speedy process, the interactive code review process has a number of drawbacks, that I would like to highlight:

#### The author tends to take the driver's seat
When the reviwer and the author sit together, the author tends to take the driver's seat, guiding the reviewer through the code. This often happens because the author is eager to show off his work or because he has been toiling with this task for a while and is aching to close it and move on. 

While the author gives his whirlwind presentation, the reviewer has to

- understand the problem that the author is addressing.
- think critically about the solution.
- wonder if the code would actually be understandable without a guided tour.

Having to juggle all these tasks is a tall order, and the reviewer will typically end up making assumptions and easing off on the critical thinking. This, of course, greatly reduces the quality of the review. In addition, a guided tour of the code is counterproductive when the reviewer is supposed to asses whether the code is easily readable and understandable.

#### Social pressure
[Research carried out by Microsoft Research](http://dl.acm.org/citation.cfm?id=2819015) shows that the reviewer's position in the social hierarchy of the team influences the quality of the code review, causing a reviewer to be less critical of code written by someone higher in the social hierarchy. This effect is likely to be exacerbated when the author and the reviewer sit together.

#### Lack of flexibility
To do a review together, the author and the reviewer have to agree on a free time slot for the review. This leads to interruptions and a preference for short code reviews. It also means that having multiple review iterations and having multiple reviewers becomes a real pain.

#### Introspection
It is not all bad news, however. As the author goes through the code and explains it to the reviewer, he revisits and articulates his own thought process. This may lead him to realise an error in his reasoning or a fault in his assumptions, or it may just highlight that some part of his code is not as easily understandable as he initially thought. Such experiences teaches the author about himself and his habits. As Galileo said: "You cannot teach a man anything; you can only help him to find it within himself."

Despite this, having to interrupt a colleague for a code review seems like a high price to pay to have the author go over his own thought process. After all, he might as well have have been talking to a [rubber duck](https://en.wikipedia.org/wiki/Rubber_duck_debugging) or a [cardboard cutout dog](http://www.sjbaker.org/humor/cardboard_dog.html).

## Code reviews done right

So, how do we do code reviews more efficiently? Well, what would you do if the matter to review was a quote for a client, or a piece of prose, and you were the author? You would let the reviewer read the prose in silence and in his own time. After all, what you are after is his assesment of your work. Is it a pleasant read? Is it easily understandable? Is it correct?

This leads us to the conclusion that efficient code reviews should

- be left solely to the reviewer.
- be done asynchronously.

Allowing the reviewer to do the review in his own time means that he can pick up the work when it suits him, and he can take the time he needs for a thorough review. It also means that having multiple reviewers becomes much more feasible. 

The experience of a reviewer doing a review in isolation is comparable to that of a developer, who later has to pick up the code to make changes. Thus, this is a good test for whether the code is actually maintainable. Moreover, since the reviewer will have to communicate with the author in writing, any questions raised or decisions reached during the review will be documented for future reference.

Most version control services provide some mechanism for reviewing code in this manner. Bitbucket and Github both provide excellent tools for reviewing pull requests in this manner. Even if you are not using one of these services, you still have [lots of options](https://en.wikipedia.org/wiki/List_of_tools_for_code_review).

## Conclusion
Avoid the interactive code reviews. They are, at best, a waste of time. To be effective, code reviews must be carried out on the reviewer's terms.
