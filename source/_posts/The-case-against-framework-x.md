title: The Case Against Framework X
date: 2015-12-06 17:25:05
tags: [Development]
---
It's not hard to find opinionated articles and blog posts that argue in favour of or against a particular choice of framework. Sometimes they detail why a framework goes against the 'proper' way to code something, sometimes they're 'benchmarks' that helpfully tell you why a library is too slow for production use, and sometimes they're just an angry diatribe against something that a developer hasn't been able to use.

Mostly it's that last one.

Developers sometimes mistake an argument a particular framework as an argument against frameworks in general - the number of front end web developer articles that state jQuery is unnecessary in the face of vanilla JS, or that ES2015 will replace the need for underscore.js shows at least some belief that frameworkless code can be a good thing. Further to that, there are myriad blog posts that say angularJS is too slow, or that ember.js is too heavy for production, or backboneJS is unmanagable in a large application. It's easy to think the weight of all that content should push you towards starting from scratch and building something of your own. After all, you've been coding for years and you're good at this stuff, right? Can't you do something that, while maybe not as flexible, is actually good enough for the jobs you have?
<!-- more -->
So why not write your own framework?

The first thing to note is that there's a damn good reason to write your own code every single time, and no discussion of libraries and frameworks will ever change that reason: __writing something in order to learn how to write better code.__

<aside>![It's important to consider which drum you beat.](/images/night-parade-1200.jpg)</aside>

If your aim is to write better code then building something that abstracts the actual code in to a pure, generic, applicable-to-anything library is a fantastic approach to figuring out what's really important. I wouldn't even begin to argue against doing that.

But most articles about why you shouldn't use Framework X aren't about learning. They're about production code.

### The majority of framework code is boring.


### Your code is much worse than you think.


### Writing your own code is a career limiting manuveur.

Lastly, and perhaps something that doesn't occur to many developers who start building a framework, any code that you write and deploy is effectively useless as soon as you change job. If you've been in a company long enough for your team to trust you to build an in-house library that's a great thing, but that trust doesn't go with you if you change job. It's highly unlikely that your next employer is going to accept your framework in place of anything that they already use - Framework X is unproven and unknown, it'd take resources for other developers to learn it, and those developers will have their own opinions about what they should be using.

Using a well known open source framework puts everyone on a level playing field, with new developers able to come in to the team with existing knowledge of the code before they've even joined. That reduces the time it takes for a developer to be productive, which from the point of view of the business is absolutely critical.

### Your time could be better spent on other things.

