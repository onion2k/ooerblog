title: Compiling LESS on save.
date: 2014-01-05
tags: [Development,DevOps]
---
One of the technologies that I use daily is Less, the CSS compiler. It’s awesome. It let’s you compile your CSS using variables and mixins. But one problem with Less is using in the browser is a pain. And when things are painful, it’s a sign you should automate.
<!-- more -->
The Less compiler, lessc, is a lovely Node.js app that runs from the commandline. Nodemon is a lovely Node.js that restarts Node.js apps. The problem is that, by default, Nodemon only monitors things that end in .js and only runs them using the node.js runtime. By default. Fortunately there’s an option to execute other commands, and a parameter to watch different files.
~~~sh
nodemon --exec ./compilecss.sh --ext '.less.css|.less'
~~~
What’s going on here is that Nodemon is executing the ./compilecss.sh shell script whenever a file with the .less or .less.css file extension is changed. With Nodemon running in the background, whenever I update a less file it’s automatically recompiled to the necessary CSS that I can load in a browser without needing to put Less in to the front-end code. Nice and tidy.