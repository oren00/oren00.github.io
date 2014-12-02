---
layout: post
title: Hacking into JSTOR using TOR
author: Geoffrey Byers
date: 2014-08-14
quote: "Exploiting JSTOR is as easy as using TOR."
image: /media/hacking-into-jstor-using-tor/cover.png
excerpt: JSTOR is a digital library of academic journals, books, and primary sources.  They provide access those privy to elite access to universities as well as a free account which provides limited access.  This information is guarded and extremely price prohibitive, sometimes costing an inflated price of up to hundreds of dollars per article.
description: Exploiting JSTOR is as easy as using TOR.
keywords: JSTOR,open source,free,hacking
video: false
comments: true
---

***
##Introduction
JSTOR is a digital library of academic journals, books, and primary sources.  They provide access those privy to elite access to universities as well as a free account which provides limited access.[^1]  This information is guarded and extremely price prohibitive, sometimes costing an inflated price of up to hundreds of dollars per article.[^2]  JSTOR provides access based on the IP address of the computer accessing the website.  If that computer is on a college campus, any login will provide access to JSTOR with full university priority.[^3]  TOR, an anonymity network, obfuscates a user's identity by connecting a user through multiple users and finally an exit node.[^4]  TOR exit nodes are operated in many countries, including the US, as well as universities.  Connecting to a TOR exit node in one of these university allows for JSTOR access.

##Downloading and Installing TOR
![TOR 1](/media/hacking-into-jstor-using-tor/jsTOR_2.png "jsTOR")
Download and Install TOR.[^5]  Restarting your computer is a good idea at this point. 

##Generating a JSTOR account
![TOR 2](/media/hacking-into-jstor-using-tor/jsTOR_3.png "jsTOR")
Now that TOR is installed, go ahead and launch TOR.  Once it opens and you get the initial splash page, visit Guerrilla Mail[^6] to generate a temporary, untraceable email address.  Copy this email address to your clipboard, leave this tab open and open a new tab.  In this new tab visit JSTOR's registration page[^7] and sign up using the email from Guerrilla Mail.  JSTOR should send you a link to this email address.  Confirm your sign up via email and then close TOR.

##Picking an exit node
![TOR IMAGE](/media/hacking-into-jstor-using-tor/jsTOR_4.png "jsTOR")
We need to edit a specific configuration file in order to tell TOR to connect through a university exit node.  All exit nodes are viewable via Tor Network Status.[^8]  Search the page for '.edu' and numerous university exit nodes should pop up.  We need to then navigate to the torrc file in order to edit it.  

* On GNU/Linux - Tor folder > Data > Tor > torrc
* On OSX - Applications > TorBrowser > Data > Tor > torrc

Open the torrc file with a text editor like TextEdit and add the lines to the bottom of the file:

		StrictNodes 1
		ExitNodes routername

Change 'routername' to any of the other university exit nodes router names you found and save the file.

##Ignition
Start TOR, visit JSTOR, and log in using your previously created credentials.  Enjoy gratis access.

##Notes
* This method works for JSTOR and Artstor.
* Abusing JSTOR violates their TOS and Computer Fraud and Abuse Act.  Legal action has been perused in certain cases. [^9]
* Be aware of where you are when you do this (people at the IP address may be liable)
* Running a TOR exit node is legal.[^10]
* Using TOR does not guarantee safety, security, or privacy.[^11]
* Using Tails on a dedicated machine is better than TOR on your day to day OS.[^12]
* Using or even searching for TOR and/or Tails will place you on a watch list, and you will be labeled an extremist.[^13]

##Citations

[^1]: http://about.jstor.org/individuals
[^2]: http://anterotesis.com/wordpress/2011/07/economics-of-jstor/
[^3]: http://about.jstor.org/jstor-help-support/admin-support#396009 
[^4]: https://www.torproject.org/about/overview
[^5]: https://torproject.org
[^6]: https://www.guerrillamail.com/
[^7]: https://www.jstor.org/action/registration?
[^8]: http://torstatus.blutmagie.de/
[^9]: http://en.wikipedia.org/wiki/United_States_v._Aaron_Swartz
[^10]: http://tor-exit.eecs.umich.edu/
[^11]: https://www.torproject.org/about/overview.html.en
[^12]: http://www.wired.com/2014/04/tails/
[^13]: http://arstechnica.com/security/2014/07/the-nsa-thinks-linux-journal-is-an-extremist-forum/