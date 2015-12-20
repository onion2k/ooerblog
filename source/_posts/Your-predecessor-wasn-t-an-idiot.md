title: "Your predecessor wasn't an idiot"
date: 2015-12-05 10:52:39
tags: [Testing,Development]
---
Every time a developer picks up a project that was started and maintained by someone else there's always a moment of "What the hell were they thinking?" It seems like a rational reaction to a common problem - the code base has problems, it wasn't built "properly", and it looks for all the world like the previous developer, at times at least, was a colossal moron.

But we all ought to realise that that almost always isn't true.
<!-- more -->
Psychologists have a term for it. It's called "The Fundamental Attribution Error", and it goes something like this; what someone does is a function of their personality and their environment. When we assess what someone else has done we overemphasise the person's personality in our reasoning, while when we look at what we've done we overemphasise the environment. In reality they're the same - it's a combination of the environment and personality that causes someone else to act the way they do whether it's someone 

<aside>![Our perception of other developers can be a bit ... off.](/images/turkey.jpg)</aside>

While it's relatively easy to remember not to castigate a former developer for what you think are gross errors, it's also relatively easy to make sure the person who'll end up looking at your code isn't going to recoil in horror when they look at what you've written. There's only one thing you need to remember:

### Document the hell out of everything.

To some extent your code is your documentation. Well written code with good naming, logical modularity and comments that explain how things work (rather than what they are) is exceptionally useful to the maintainer of your code, but it's not nearly enough on it's own. There's more needed.

1. Actual documentation.

   Less experienced developers tend to think of documentation as a job they're made to do due to the sadistic whims of development managers. Horrible as writing documentation might seem, if you're going to work as part of a team it's a fundamental skill. People need to understand the system when you're not there.

   More than that though, it's vital to keep documentation up to date. Old docs that don't detail what's actually the case for an application can be worse than no documentation at all.

2. Well thought out commit messages.

   A commit message needs to detail what was changed in the diff, and why it was changed. If possible it should link to an issue tracker. Someone should be able to read the commitlog for an application and understand when a particular feature was introduced. Each commit should be as atomic as possible - code in a commit shouldn't include extra things that aren't be a part of the feature it was merged in to.

3. Tests. All of the tests.

   The number one problem for any developer taking on maintaining a large system is the problem of regressions - adding code without completely understanding the previous code, and breaking what was there before. This is one of the key reasons why tests are important. If a new developer can write code against an existing system and know that they're going to be told if they're broken something then they can be a great deal more confident in their approach.

In the end there's always going to be horrible code out there that we inherit as developers. Code that was written with old versions of bad languages, clunky frameworks, and non-existent specifications. We need to remember that when we're laughing, or crying, at the code we find ourselves taking over. As much as we like to think we're better, if we were in the situation that previous developer was in we might well write some pretty awful code too.