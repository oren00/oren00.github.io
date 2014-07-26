---
layout: post
title: Getting Started: Secure Instant Messaging for OSX and Mobile
date: 2014-07-25
description: You should start using secure messaging now.  Here's how.
excerpt: If you want to have private conversations, you are accountable for making sure those conversations are secure.
keywords: security,privacy,message,messaging,TOR,OTR,encryption
---


##TL;DR
Start using encrypted messaging to keep your communications private.  Use Jitsi on OSX and ChatSecure on iOS an Android.

##Protect Your Privacy
A [plethora](http://www.theguardian.com/commentisfree/series/glenn-greenwald-security-liberty) of [journal](http://www.salon.com/writer/glenn_greenwald/) articles expose the war against security, privacy and anonymity on the internet.  If you want to have private conversations, you are accountable for making sure those conversations are secure.

##Downloading Jitsi for OSX
Adium is one of the best instant messaging applications for OSX which supports encryption.  Head over to Jitsi's [website](https://jitsi.org/Main/Download) and download the latest version.

##Registering a Username
![jitsi](/public/images/blog/2014-07-25-jitsi_1.png "Jitsi")
You'll need to register a XMPP(jabber) user name.  I prefer to have my name hosted with a company outside the US which will provide protection.  Switzerland based [SwissJabber](http://www.swissjabber.ch) has you covered.  With Jitsi open, go to Jitsi > Preferences > Accounts > Add or alternatively go to File > Add New Account.  Select XMPP and select Create New XMPP Account.  Fill the fields changing the server to 'swissjabber.ch' and click add.

##A Note on Privacy and Common Sense
I allow anyone to contact me.  That doesn't mean I talk to anyone, It just means anyone who needs to can find me.  I also share my fingerprint with everyone and you should too.  I also verify with whom I am talking.  I recommend verifying the fingerprint of new contacts with that person.  I also don't try to hide who I am, just keep private what it is I am doing.

##Messaging a Contact
![jitsi](/public/images/blog/2014-07-25-jitsi_2.png "Jitsi")
Go to File > Add Contact to add a contact.  Double clicking a contact opens a window allowing you to chat.  When you start a chat, clicking the lock icon in the top right encrypts the chat.  OTR is the magic sauce.  It stands for Off The Record and is a cryptographic protocol for instant messaging.  By default it keeps logs of conversations.  I would recommend changing this (the hourglass icon) and turning off history for all chats and contacts.  
![jitsi](/public/images/blog/2014-07-25-jitsi_3.png "Jitsi")
To require encryption all the time, go to Preferences > Security and check all three options at the bottom.  Nothing is worse then talking and realizing encryption is off.

##Voice, Video and Screen Sharing
![jitsi](/public/images/blog/2014-07-25-jitsi_4.png "Jitsi")
Jitsi is pretty awesome because it provides [encryption](https://jitsi.org/Documentation/ZrtpFAQ#faqFeat) for voice and video sharing.  I don't use these nearly as much but they are nice to haves.  What it doesn't do is protect metadata, so the contents of the conversation are private but not informaton regarding with whom you are speaking.  Clicking a contact's name once brings up the items for messaging, voice, video and screen sharing.  Alternatively you can access all of these from within a message.

##Mobile App
For mobile messaging [ChatSecure](https://chatsecure.org) for iOS and Android allows OTR encryption over XMPP.  This means you can chat with people, while being protected on your mobile device.  Download ChatSecure and input your account details from the steps above.  This will generate a different fingerprint, however it will let you chat with people on the go.  This will work nicely with other people on ChatSecure, as well as users using Pidgin and Adium.
