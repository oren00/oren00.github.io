---
layout: post
title: Switching to Markdowns
date: 2014-05-14
description: I switched from writing in Wordpress and HTML to markdown.
excerpt: Here I write about using markdown and include some code from a template.
keywords: markdown,wordpress,html,blog,blogging
---

Here I write about using markdown and include some code from a template.

	---
	layout: post
	title: Template for markdown
	date: 2014-05-14
	description: This is a super simple template for markdown which I use with Jekyll.
	keywords: template,diy,how-to
	---


	#Headers#
	# This is an H1 #
	## This is an H2 ##
	### This is an H3 ###
	#### This is an H4 ####
	##### This is an H5 #####
	###### This is an H6 ######

	#Block Quotes#
	> This is a blockquote with two paragraphs. Lorem ipsum dolor sit. amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.


	> Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

	#Lists#
	Asterisks, hypehs and plus signs can all be used to designate list items.  The words must be spaced with 4 spaces or a tab.

	*   Red
	*   Green
	*   Blue

	Or 

	+   This is a list item with two paragraphs.

	    This is the second paragraph in the list item. You're only required to indent the first line. Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

	+   Another item in the same list.

	Ordered lists utilize numbers followed by periods.

	1. Red
	2. Green
	3. Blue

	#Codeblocks#
	A code block continues until it reaches a line that is not indented (or the end of the article).

	Within a code block, ampersands (&) and angle brackets (< and >) are automatically converted into HTML entities. 

	This is a normal paragraph:

	    This is a code block.

	#horizontal rules#
	You can produce a horizontal rule by placing three or more hyphens, asterisks, or underscores on a line by themselves. If you wish, you may use spaces between the hyphens or asterisks. Each of the following lines will produce a horizontal rule:

	***
	OR
	- - -
	OR
	---------------------------------------

	#Links#
	##Inline links##
	[This link](http://example.net/) has no title attribute.

	##Reference links##
	I get 10 times more traffic from [Google] [1] than from
	[Yahoo] [2] or [MSN] [3].

	  [1]: http://google.com/        "Google"
	  [2]: http://search.yahoo.com/  "Yahoo Search"
	  [3]: http://search.msn.com/    "MSN Search"

	##Automatic links##
	<http://example.com/>

	#Emphasis#
	*em*
	_em_
	**strong**
	__strong__

	#Code#
	Use the `printf()` function.

	#Images#
	![Alt text](/path/to/img.jpg)
	![Alt text](/path/to/img.jpg "Optional title")

	#Esacpes

	\\   backslash
	\`   backtick
	\*   asterisk
	\_   underscore
	\{\}  curly braces
	\[\]  square brackets
	\(\)  parentheses
	\#   hash mark
	\+   plus sign
	\-   minus sign (hyphen)
	\.   dot
	\!   exclamation mark

	#Thanks#
	http://daringfireball.net/projects/markdown/
