---
layout: post
title: The Guise of AI
author: Geoffrey Byers
date: 2014-12-02
quote: "or how to make automated human computer interactions seem less mechanical and more human"
image: https://farm3.staticflickr.com/2164/2627550713_73a20ed697_o.jpg
attribute_author: Andy Wilson
attribute_url: https://flic.kr/p/51bThv
excerpt: When interactions between humans and software in the digital space seems more closely likened to interactions with other humans in that same digital space, we enter the perceived state of AI.
keywords: automation,robot,bot,ai
video: false
comments: true
---

***
##Overview
Artificial intelligence is a largely a grey area.  In many cases, software can seem human and to think for itself when in reality it is just less robotic.  This is blurred when the digital lens enters into the equation.  When interactions between humans and software in the digital space seems more closely likened to interactions with other humans in that same digital space, we enter the perceived state of AI.  Two main areas I have begun including in my projects include sleeping ie. paused states and randomization of variables.  These rather simple details give the perception of anthropomorphism.  This could be important for a number of reasons ranging from customers interacting with your software to deception for running bots on social media platforms.

##Sleep
Despite our best efforts we cannot achieve perfection.  People have a natural cadence which is not mechanical or bot-like.  If actions repeatedly take place at exactly the same time things tend to look artificial.  This can be ideal in certain situations such as an alarm clock, however less than ideal when creating experiences and interactions that seem human.

###Sleep on start
We rarely start tasks at exactly the same time over and over again.  Slight fluctuations such as the delay in time when actions begin, such as tweeting, show enough of a nuance and inconsistency as to depict human like behavior.

###Hold 'normal' hours
Humans can only work for so long.  Research [suggests](http://www.inc.com/jessica-stillman/why-working-more-than-40-hours-a-week-is-useless.html) there is a steep drop off after 40 hours a week.  Software can run nonstop around the clock, working without taking a break.  Doing so instantly reads as "not a human".  Scheduling actions during 'normal' hours with cron gives software the appearance of not working endlessly and perpetuating the idea that a human could indeed be behind the scenes.

###Sleep between actions such as likes, comments, follows etc.
Certain interactions such as tweeting or liking a photo on Instagram take some incremental time to accomplish.  This is true despite any aesthetically pickiness, as a person can only like so fast.  Using Instagram's API, software can like at a much faster rate than a human.  Even if you are under the technical limits for something such as Instagram automation, it may still be less than ideal to operate in such a fashion.

##Randomization
Humans have a natural order to accomplishing tasks.  Part of that order is not repeating actions in the same exact order.  Another part of that order is not repeating the task in the same exact number.  

###Randomize order
Hashtags allow us to quickly filter content which most likely applies to a topic which is interesting.  Keeping track of hashtags is not out of the ordinary.  Neither is cycling through a handful of relevant hashtags on a recurring schedule.  However, software interacting via a set of hashtags in the same order repeatedly is an excellent way to pick out software from a human.

###Randomize frequency
Follows, likes, posts, retweets all happen on Twitter at seemingly random counts.  The counts for these naturally changes.  A random number of actions within a set min and max range for a given time more closely replicates human behavior.

###Randomize all sleep
Pauses between tweets, favorites, comments and likes should be randomized.  All sleep can benefit from min and max ranges, allowing the software to have sleep patterns with some fluctuation.

###Know your limits
In order to stop abuse and mostly to cut down in spam, most social networks have API limits.  [Instagram](http://instagram.com/developer/limits/#), [Twitter](https://dev.twitter.com/rest/public/rate-limiting), [Facebook]() all have public API limits.  Go easy on these API limits, keep the range of actions 'normal' and random.  The Instagram limit for number of likes in an hour is 100, however 60 likes in an hour is 40% less than the limit and is a much more reasonable cadence.  Just because there is a technical limit, doesn't mean you should brush against it.  Doing so may get your account shut down.