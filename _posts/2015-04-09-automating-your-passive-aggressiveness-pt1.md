---
layout: post
title: Automating Your Passive Aggressiveness PT.1
author: Geoffrey Byers
date: 2015-04-09
quote: "With the different platforms of communication and pure volume of communication touch-points today, messages can be ignored and lost in the ether that is the digital age."
image: https://farm6.staticflickr.com/5348/8971108666_0469ef2729_o.jpg
attribute_author: Fosim
attribute_url: https://flic.kr/p/eEKh4m
excerpt: With the different platforms of communication and pure volume of communication touch-points today, messages can be ignored and lost in the ether that is the digital age.
keywords: automation,communication,telecom,sms
video: false
comments: true
---

***
##Overview
Do you need to get in touch with someone, or automate your messages to them?  Fear not.  You can automate everything, sending SMS messages as frequently as needed.  Most, if not all, cellular providers allow emails to be sent to mobile numbers.  This is accomplished by emailing the number with an extension such as @txt.att.net after the 10 digit number.  These messages are sent via numbers which change after each message sent, meaning mobile users can not block one number and stop further incoming messages.  If you need to send messages once a day or less, [IFTTT](https://ifttt.com/) is the most simple solution.  If you need to send more than one message a day, keep reading.

##The Psychological Impact of repetitive mass communication
With the different platforms of communication and pure volume of communication touch-points today, messages can be ignored and lost in the ether that is the digital age.  My intent was to set a reminder which would build over the course of time, growing in intensity.  This way the 'temperature' would slowly rise as opposed to a flood of messages arriving unexpectedly.  As part of a social experiment I increased the message volume over the course of a few weeks, starting off with one message a day.  I arrived at my intended response well before hitting the one message per second interval.  The timing I implemented utilized the following format:

* (1) 6am
* (2) 6am 6pm
* (3) 8am 12pm 6 pm
* (4) 12am 6am 12pm 6pm
* (5) 12am 6am 9am 12pm 6pm
* (6) 12am 6am 9am 12pm 6pm 9pm
* (8) 12am 3am 6am 9am 12pm 3pm 6pm 9pm
* (24) 1 hour intervals for 24 hours
* (96) 15 minute intervals for 24 hours
* (288) 5 minute intervals for 24 hours
* (1440) 1 minute intervals for 24 hours
* (2,880) 30 second intervals for 24 hours
* (5,760) 15 second intervals for 24 hours
* (86,400) 1 second intervals for 24 hours

## Scheduling with Cron
A dead simple way to automate processes by time frequency, Cron allows for variables for the minute, hour, day of the month, month, day of the week.  An asterisk is used to select all.  

To initiate the script to run four times a day at 12am, 6am, 12pm and 6pm:

	0 0,6,12,18 * * * python /full/path/to/script.py
	
To initiate the script to run once an hour:

	0 0-24 * * * python /full/path/to/script.py
	
To initiate the script to run once a minute:

	* * * * * python /full/path/to/script.py

In this case I had multiple cron jobs ready to go, which I switched out every few days once I was ready to switch the messaging to the next level of frequency.

##Implementation
The following python code uses gmail to email the number of the intended recipient, sending an SMS through the carrier associated with the cellular number provided.  The variables which must change include a gmail account which you own, the password for said gmail account, the phone number of the person you are contacting, the carrier extension, and the message included.  This is the complete code used.  It utilizes python 2.7 and smtplib.

	import smtplib as s
	contact_number = "xxxxxxxxxx"
	username = "xxxxxx@gmail.com"
	
	obj = s.SMTP("smtp.gmail.com", 587)
	obj.ehlo()
	obj.starttls()
	obj.login(username, password)
	print"\n\r"
	
	carrier_extension = "@txt.att.net"
	
	v_phone = str(contact_number) + str(carrier_extension)
	message = ("this is a test message")
	phone_message = ("From: %s\r\nTo: %s \r\n\r\n %s"
		% (username, "" .join(v_phone), "" .join(message)))
	
	obj.sendmail(username, v_phone, phone_message)
	print "Sending messages... Press Ctrl + C to Stop"
	
##Playing Nice with Gmail
Running the following code may produce a 534 error.  Check your [settings](https://www.google.com/settings/security/lesssecureapps) for gmail and make sure that you have enabled access for less secure apps before running the script.

##Cellular Providers Email Extension
Do you only have your contact's number but don't know the carrier?  Enter the number on [Carrier Lookup](https://www.carrierlookup.com/) and then apply the correct extension from the following list.

	#3 River Wireless
	10digitphonenumber@sms.3rivers.net
	#ACS Wireless
	10digitphonenumber@paging.acswireless.com
	#Alltel
	10digitphonenumber@message.alltel.com
	#AT&T
	10digitphonenumber@txt.att.net
	#Bell Canada
	10digitphonenumber@txt.bellmobility.ca
	#Bell Canada
	10digitphonenumber@bellmobility.ca
	#Bell Mobility (Canada)
	10digitphonenumber@txt.bell.ca
	#Bell Mobility
	10digitphonenumber@txt.bellmobility.ca
	#Blue Sky Frog
	10digitphonenumber@blueskyfrog.com
	#Bluegrass Cellular
	10digitphonenumber@sms.bluecell.com
	#Boost Mobile
	10digitphonenumber@myboostmobile.com
	#BPL Mobile
	10digitphonenumber@bplmobile.com
	#Carolina West Wireless
	10digit10digitnumber@cwwsms.com
	#Cellular One
	10digitphonenumber@mobile.celloneusa.com
	#Cellular South
	10digitphonenumber@csouth1.com
	#Centennial Wireless
	10digitphonenumber@cwemail.com
	#CenturyTel
	10digitphonenumber@messaging.centurytel.net
	#Cingular (Now AT&T)
	10digitphonenumber@txt.att.net
	#Clearnet
	10digitphonenumber@msg.clearnet.com
	#Comcast
	10digitphonenumber@comcastpcs.textmsg.com
	#Corr Wireless Communications
	10digitphonenumber@corrwireless.net
	#Dobson
	10digitphonenumber@mobile.dobson.net
	#Edge Wireless
	10digitphonenumber@sms.edgewireless.com
	#Fido
	10digitphonenumber@fido.ca
	#Golden Telecom
	10digitphonenumber@sms.goldentele.com
	#Helio
	10digitphonenumber@messaging.sprintpcs.com
	#Houston Cellular
	10digitphonenumber@text.houstoncellular.net
	#Idea Cellular
	10digitphonenumber@ideacellular.net
	#Illinois Valley Cellular
	10digitphonenumber@ivctext.com
	#Inland Cellular Telephone
	10digitphonenumber@inlandlink.com
	#MCI
	10digitphonenumber@pagemci.com
	#Metrocall
	10digitpagernumber@page.metrocall.com
	#Metrocall 2-way
	10digitpagernumber@my2way.com
	#Metro PCS
	10digitphonenumber@mymetropcs.com
	#Microcell
	10digitphonenumber@fido.ca
	#Midwest Wireless
	10digitphonenumber@clearlydigital.com
	#Mobilcomm
	10digitphonenumber@mobilecomm.net
	#MTS
	10digitphonenumber@text.mtsmobility.com
	#Nextel
	10digitphonenumber@messaging.nextel.com
	#OnlineBeep
	10digitphonenumber@onlinebeep.net
	#PCS One
	10digitphonenumber@pcsone.net
	#President's Choice
	10digitphonenumber@txt.bell.ca
	#Public Service Cellular
	10digitphonenumber@sms.pscel.com
	#Qwest
	10digitphonenumber@qwestmp.com
	#Rogers AT&T Wireless
	10digitphonenumber@pcs.rogers.com
	#Rogers Canada
	10digitphonenumber@pcs.rogers.com
	#Satellink
	10digitpagernumber.pageme@satellink.net
	#Southwestern Bell
	10digitphonenumber@email.swbw.com
	#Sprint
	10digitphonenumber@messaging.sprintpcs.com
	#Sumcom
	10digitphonenumber@tms.suncom.com
	#Surewest Communicaitons
	10digitphonenumber@mobile.surewest.com
	#T-Mobile
	10digitphonenumber@tmomail.net
	#Telus
	10digitphonenumber@msg.telus.com
	#Tracfone
	10digitphonenumber@txt.att.net
	#Triton
	10digitphonenumber@tms.suncom.com
	#Unicel
	10digitphonenumber@utext.com
	#US Cellular
	10digitphonenumber@email.uscc.net
	#Solo Mobile
	10digitphonenumber@txt.bell.ca
	#Sprint
	10digitphonenumber@messaging.sprintpcs.com
	#Sumcom
	10digitphonenumber@tms.suncom.com
	#Surewest Communicaitons
	10digitphonenumber@mobile.surewest.com
	#T-Mobile
	10digitphonenumber@tmomail.net
	#Telus
	10digitphonenumber@msg.telus.com
	#Triton
	10digitphonenumber@tms.suncom.com
	#Unicel
	10digitphonenumber@utext.com
	#US Cellular
	10digitphonenumber@email.uscc.net
	#US West
	10digitphonenumber@uswestdatamail.com
	#Verizon
	10digitphonenumber@vtext.com
	#Virgin Mobile
	10digitphonenumber@vmobl.com
	#Virgin Mobile Canada
	10digitphonenumber@vmobile.ca
	#West Central Wireless
	10digitphonenumber@sms.wcc.net
	#Western Wireless
	10digitphonenumber@cellularonewest.com
	
##Wrap Up
Communication is a powerful tool and this especially has the potential to be abused.  Have fun experimenting, but don't be an asshole.