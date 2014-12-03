---
layout: post
title: The Guise of AI
author: Geoffrey Byers
date: 2014-12-02
quote: "or how to make automated human computer interactions seem less mechanical and more human"
image: /media/the-guise-of-ai/cover.jpg
excerpt: When interactions between humans and software in the digital space seems more closely likened to interactions with other humans in that same digital space, we enter the perceived state of AI.
keywords: automation,robot,bot,ai
video: false
comments: true
---

***
##Overview
Artificial intelligence is a largely a grey area.  In many cases, software can seem human and to think for itself when in reality it is just less robotic.  This is blurred when the digital lens enters into the equation.  When interactions between humans and software in the digital space seems more closely likened to interactions with other humans in that same digital space, we enter the perceived state of AI.  Two main areas I have begun including in my projects include sleeping, or resting states and randomization of variables.  These, while not complex, give the perception of anthropomorphism.  This could be important for a number of reasons ranging from customers interacting with your software to deception for running bots on social media platforms.

##Sleep
Despite our best efforts we cannot achieve perfection.  People have a natural cadence which is not mechanical or bot-like.  If actions repeatedly take place at exactly the same time things tend to look artificial.  This can be ideal in certain situations such as an alarm clock, however less than ideal when creating experiences and interactions that seems human.

###Sleep on start
We rarely start tasks at exactly the same time over and over again.  Slight fluctuations such as the time when tweets are sent out show enough of a nuance and inconsistency as to depict human like behavior.

###Hold 'normal' hours
Humans can only work so long.  Some studies suggest there is a steep drop off after 40 hours a week.  Software can run nonstop around the clock, working without taking a rest.  This instantly reads as "not a human".  Scheduling during 'normal' hours with cron gives software the appearance of not working endlessly.

###Sleep between actions such as likes, comments, follows etc.
Certain interactions such as following people on Instagram or liking a photo take some incremental time to accomplish.  This is true despite any aesthetically pickiness, as a person can only like so fast.  Using Instagram's API, software can like at a much faster rate than a human.  Instagram has [API limits](http://instagram.com/developer/limits/#) because of this.  Even if you are under the technical limits for something such as Instagram automation, it may still be less than ideal to operate in such a fashion.

##Randomness
Humans have a natural order.  Part of that order is not repeating actions in the same exact order.  Another part of that order is not repeating the same exact number of actions.

###Randomize order
Liking photos belonging to a set of hashtags in the same order repeatedly is an excellent way to pick out software from a human.

###Randomize frequency
Setting min and max ranges for number of actions.  One example would be number of followers in an hour. 

###Randomize all sleep
Sleep should have min and max ranges as well, allowing the software to have sleep patterns with some fluctuation.

###Know your limits
Go easy on the API limits, keep the range of actions 'normal' and random.  Just because there is a technical limit, doesn't mean you should brush against it every time.  