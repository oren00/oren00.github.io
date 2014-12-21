---
layout: post
title: Using Wget to Download Streaming Videos
author: Geoffrey Byers
date: 2014-12-21
quote: "Videos streaming behind a flash player can be a shitshow to grab for offline viewing."
image: https://farm3.staticflickr.com/2642/3696386615_19c3c56b23_b.jpg
attribute_author: Stian Eikeland
attribute_url: https://flic.kr/p/6CCWXH
excerpt: Videos streaming behind a flash player can be a shitshow to grab for offline viewing.
keywords: wget,downloading,streaming,ripping
video: false
comments: true
---

***
##Finding the files
Videos streaming behind a flash player can be a shitshow to grab for offline viewing.  I recently wanted to watch a PBS documentary about North Korea, but wanted to download the file for later viewing.  In this example, the files exist beneath a flash video player making things a bit cumbersome.  There are a few ways to find the source stream, using firebug being one of the easier ways.  For this example head over to the PBS documentary ['Secret State of North Korea'](http://video.pbs.org/video/2365155890/).  [Firebug](https://addons.mozilla.org/en-US/firefox/addon/firebug/) is an addon for firefox, giving you access to some developer tools.  A few options exist for Chrome, but I'm not going to dig into those.  After installing firebug, start playing the video, right click and choose 'inspect element with firebug'.  Go to the 'Net' tab  and below that make sure the 'All' tab is selected.  Sort files by size and look for something ~1.3MB in size.  Hovering over this item reveals a link which resembles this:

http://ga.video.cdn.pbs.org/videos/frontline/773e4c49-c6a6-47a0-b075-7f298847a106/56135/hd-mezzanine-16x9/00003206-16x9-hls-800k-00001.ts

Copy this link using 'Copy Location'.

##Scraping with Wget
Wget comes installed with most linux and osx distributions.  Opening terminal, we can issue commands with Wget using the url from firebug.  Getting multiple files in Wget is pretty straightforward.  I had some difficulties getting files 1 to 500 in one go, but using the syntax below works to download batches of files at once.

	wget -r http://ga.video.cdn.pbs.org/videos/frontline/773e4c49-c6a6-47a0-b075-7f298847a106/56135/hd-mezzanine-16x9/00003206-16x9-hls-800k-0000{1..9}.ts

	wget -r http://ga.video.cdn.pbs.org/videos/frontline/773e4c49-c6a6-47a0-b075-7f298847a106/56135/hd-mezzanine-16x9/00003206-16x9-hls-800k-000{10..99}.ts

	wget -r http://ga.video.cdn.pbs.org/videos/frontline/773e4c49-c6a6-47a0-b075-7f298847a106/56135/hd-mezzanine-16x9/00003206-16x9-hls-800k-00{100..500}.ts

Using this script downloads the folder and contents into the current directory.  In this case the structure is ga.video.cdn.pbs.org/videos/frontline/773e4c49-c6a6-47a0-b075-7f298847a106/56135/hd-mezzanine-16x9/ followed by the 323 .ts files.  

##Playing with VLC
In addition to the .ts files, wget grabbed a file named 00003206-16x9-hls-800k.m3u8 which plays in [VLC](http://www.videolan.org/vlc/index.html).  Open this with VLC and you'll get seamless playback.