---
layout: post
title:  "Facts and Fallacies of Software Engineering &mdash; Book Discussion"
date:   2018-04-01
categories: books, programming
---

I consider myself a late-bloomer in programming. There is the notion of a stereotypical programmer, tinkering with computers at a young age (although this may not be the dominant stereotype anymore), but I didn't learn to code until I took an elective computer science course in university and decided to become a (half) computer science major. During my first co-op job, I spent hours reading Stack Overflow questions and eventually found Jeff Atwood's and Joel Spolsky's blogs, and I was hooked. They are both proponents of reading books (see [Joel Spolsky's book recommendations](https://www.joelonsoftware.com/2005/11/22/reading-list-fog-creek-software-management-training-program/) and [Jeff Atwood's book recommendations](https://blog.codinghorror.com/programmers-dont-read-books-but-you-should/)), and I hope to work my way through many of the "classic" programmer books over the next few years.

Something I've noticed is that whenever I'm reading older books, I find myself trying to visualize scenarios in my head to match what the author is describing. This book in particular was published 15 years ago (2003), and feels dated in some places (there is a section discussing the merits of COBOL, and I diligently tried to imagine myself working with a business application written in COBOL). I wonder if these "classic" books hold as much weight as they did when they were published; some of his Facts read like common sense, and others describe scenarios I can only abstractly imagine. What follows isn't so much of a book review as a discussion on some of Glass' Facts and Fallacies, from the perspective of a relatively junior developer building web applications.

## Capital-M methodologies and continual improvement

A large part of this book discusses software methodologies and metrics. I have no experience with capital-M methodologies or [pointy-haired bosses](https://en.wikipedia.org/wiki/Pointy-haired_Boss) or productivity metrics. I also have never been on a failed or runaway software project (whether due to luck or inexperience remains to be seen). I'm imagining that Glass' perspective of software projects centers around traditional "shrink-wrapped software". Software estimates are perhaps less relevant these days now that software is more convenient to deploy. Instead of having big releases, we update our web application regularly, and new features are incorporated into production whenever they're done.

> Quality is _not_ user satisfaction, meeting requirements, meeting cost and schedule targets, or reliability. (Fact 47, p. 132)

I didn't understand how Glass' decided what is and isn't considered "quality"; that "human engineering (usability)" is considered quality but "user satisfaction" isn't feels like pointless arguing of semantics. In fact, earlier he lists "reliability" among his list of attributes of quality (Fact 46, p. 129), which seems to contract the current Fact. In any case, I can't imagine a work scenario that would lead someone to say "we should do X instead of Y because doing X prioritizes 'reliability' while Y is merely 'meeting requirements'". Maybe I'm missing the point?

## On testing

> [T]here is a lot of the testing activity that cannot be automated. (Fact 35, p. 101)
> 
> Rigorous inspections can remove up to 90 percent of errors from a software product before the first test case is run. (Fact 37, p. 104)

I don't have much experience with testing so I'm more willing to take Glass' opinions on testing at face value. Testing is hard work, and I don't trust myself to do it rigorously, or to make sure that I haven't accidentally broken some old code with new changes. I haven't had a lot of luck with either manual testing or code reviews (I'm assuming that's what he means by "rigorous inspections") and finding bugs in production always causes me distress.

## Relentless optimism

> Design is a complex, iterative process. The initial design solution will likely be wrong and certainly not optimal. (Fact 28, p. 81)
> 
> Maintenance consumes 40 to 80 percent of software costs. (Fact 41, p. 115)

It's comforting to hear that not only do we not need to get it right the first time, it's impractical to try to do so. Building software is a process of [continuous improvement](https://en.wikipedia.org/wiki/Kaizen) and nothing is ever done, especially in the age of cloud software. I had a conversation with a more senior coworker where I jokingly implored why everything couldn't be perfect and he replied, "because perfect is the enemy of good".

> The answer to a feasibility study is almost always "yes". (Fact 13, p. 42)

I've never participated in a feasibility study (even the name sounds formal and academic), but I'm inclined to disagree with the concept of feasibility studies on principle. As software engineers, we should strive to build the best solution we can for the problem. I haven't encountered a problem at work (so far, at least) that we haven't been able to find a satisfactory solution for, although we are rate-limited by the size of our team.

> The best programmers are up to 28 times better than the worst programmers. (Fact 2, p. 14)

I don't understand the methodology behind this assertion&mdash;the references include studies measuring differences in "productivity" and "capability" of individual programmers, without defining those terms (I couldn't be bothered to look up the original papers). However, the general sentiment initially disheartened me; if software quality depends this much on specific people, aren't we all doomed? At work I'm constantly thinking of ways to script or automate things to reduce dependencies on specific people, because humans are forgetful and inconsistent, while a script runs exactly the same every time. In keeping with the theme of relentless optimism, I propose a positive spin on this statement: we can greatly improve the quality of the software we build by continually striving to learn and improve.