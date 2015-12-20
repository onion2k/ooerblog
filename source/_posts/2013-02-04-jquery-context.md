title: jQuery Context Selectors
date: 2014-01-05
tags: [Development]
---
jQuery selectors are pretty straightforward things. The way they work under the bonnet isn’t quite so obvious though. For example;
~~~js
$('.foo')
~~~
That’s going to go to the DOM and find everything with that has a class of ‘foo’. Easy. What’s going on behind the scenes though, is that jQuery is looking at every DOM node to see if it has the ‘foo’ class. Even in a small app that can be a very costly operation. It’s very unlikely that you really want to find every node with the ‘foo’ class. You’re usually looking for a subset of them. Instead, you probably want this, right?
<!-- more -->
~~~js
$('#bar .foo')
~~~
Seemingly slightly oddly though, this doesn’t do what you might think. Rather than finding the nodes with an id of ‘bar’ and looking for nodes inside that have a class of ‘foo’, jQuery looks for all the nodes with a class of ‘foo’, and then checks if they’re a child of any elements with an id of ‘bar’. It’s actually slower than simply looking for all the ‘foo’s, although not by very much. Fortunately however, jQuery has a context argument for selectors;
~~~js
$('.foo','#bar')
~~~
This does what you’d expect. It find the nodes with an id of ‘bar’, which is a very fast operation thanks to browsers implementing the getElementByID() call, and then jQuery looks for all the ‘foo’s inside of them rather than the entire DOM tree. Obviously this is a good thing; jQuery is doing much less work.
