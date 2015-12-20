title: My web browser is leaking data.
date: 2014-06-11
tags: [Privacy]
---
Everywhere we go we spew forth a veritable deluge of personal information, giving a detailed account of our daily lives to anyone with the tenacity to bother listening. The microscopic minutiae of our most mundane activities is the apparent life-blood of business in the era of 'Big Data'. Yet, somewhat surprisingly, and perhaps worryingly, it all seems entirely normal and not creepy in the slightest.

Before I started writing today I read a news website, watched a YouTube video of a TED talk, and started a Spotify playlist that my girlfriend created for our second anniversary. Three innocuous actions that thousands of people might have done in similar weekend rituals all over the world.
<!-- more -->
Now though, somewhere in an anonymous low-slung concrete building on a mid-Western US industrial estate, the analytical power of a data warehouse is connecting the dots between what news I read, people who like to hear speakers talking about ecology, and people who listen to Elbow. I've inadvertantly added myself to a network graph - a mathematical model that plots our likes and interests, and now the corporate world has a slightly better way of targeting me with their purnicious adverting. There's an amazing amount of information in just a few clicks, and by aggregatting the data and using a few statistical tricks practically any aspect of who you are can be inferred.

Firstly, and most commonly understood, is the issue of 'tracking cookies'. A tracking cookie is a tiny snippet of text that a computer remembers between visits. Typically they record when you arrive and give you a unique ID. The level of security that browsers give these cookies are relatively good - cookies are never shared with other services unless the author of the website specifically sets them to be shared, and they're only shared with a whitelist of services when they are. No one can spy on your cookies.

That doesn't mean they're only useful to the website that sets them though, because websites rarely set their own. When you visit a website you browser is instructed to load things from all over the internet. For example, visiting sainsburys.co.uk loads a Google Analytics asset from doubleclick.net (a domain within Google's advertising network). A subsequent visit to sunderlandecho.co.uk also loads a Google Analytics asset from doubleclick.net. The fact that my browser has visited both websites has been logged by Google. If I was logged in to my Google Mail account from the same computer then both Sainsburys and Sunderland Echo would be connected to *me* rather than just my computer.

There's a lot more than two sites connected by that one service. Google Analytics is used on approximately 2/3rds of the top 1 million websites (by traffic) (https://www.datanyze.com/market-share/Analytics/). That's a lot of information about what we all do online. There is a caveat. Google only do analytics on 1/4 of the top 100 websites, which account for a massively disproportionate amount of internet traffic. While that means a lot of browsing data isn't tracked by Google, which is good, it means that Google get mostly specific interest website information - the small websites and blogs that usally deal with one topic. That means Google's model of who each of us is could be more accuracte.

Browsers leak much more than cookies. The fact that I browse the internet with Apple's Safari browser, on a Macbook with a slightly out of date operating system, and with a particular collection of settings is reported to every website I visit. Every click I make has my browser's UserAgent string attached to send to the server I made a request from;

~~~js
Mozilla/5.0 (Macintosh; Intel Mac OS X 10_7_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/34.0.1847.116 Safari/537.36
~~~

You can see a lot more of what your computer is telling everyone here: https://aboutmybrowser.com/

It gets even worse if you browse the internet on a mobile device. If you've not changed your default settings, you'll be broadcasting what device you use, where you're using it from (located by your internet connection), and possibly your location found by GPS too. If you take and upload a photograph you'll be attaching even more data to what you send. Mobile devices are very open.

(more coming soon)