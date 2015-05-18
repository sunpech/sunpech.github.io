---
layout: post
title: SOPA Blackout set for January 18 2012
date: '2012-01-17T18:54:00.000-06:00'
author: Steven Suwatanapongched
tags:
- Technology
modified_time: '2012-01-17T20:15:26.398-06:00'
blogger_id: tag:blogger.com,1999:blog-6841384.post-6486066378930805561
blogger_orig_url: http://www.sunpech.com/2012/01/sopa-blackout-set-for-january-18-2012.html
---

Tomorrow, Wednesday January 18, 2012, I plan to block this website out in support of <a href="http://sopablackout.org/">SOPA Blackout</a>. Technically it won't be completed blocked out, as the javascript is only a black message overlay on top of the website. Users will still be able to click through once the popup comes up.

Here is the javascript that will be used in the header:

<blockquote class="tr_bq"><span style="color: #404040; font-family: 'Courier New', Courier, monospace;"><span style="line-height: 18px;">&lt;script type="text/javascript" src="//js.sopablackout.org/sopablackout.js"&gt;&lt;/script&gt;</span></span></blockquote>On one of my other sites, <a href="http://spong.org/">spong.org</a>, will be blocked out completely using:

<blockquote class="tr_bq"><span style="font-family: 'Courier New', Courier, monospace;">&lt;script&gt;</span><span style="font-family: 'Courier New', Courier, monospace;">var today = new Date();</span><span style="font-family: 'Courier New', Courier, monospace;">if((today.getDate() == 18) &amp;&amp; (today.getMonth() == 0) &amp;&amp; (today.getFullYear() == 2012))</span><span style="font-family: 'Courier New', Courier, monospace;">&nbsp;{</span><span style="font-family: 'Courier New', Courier, monospace;">&nbsp; &nbsp; &nbsp; window.location = "http://protestsopa.org";</span><span style="font-family: 'Courier New', Courier, monospace;">&nbsp;}</span><span style="font-family: 'Courier New', Courier, monospace;">&lt;/script&gt;</span></blockquote>

There is a github project for the above:&nbsp;<a href="https://github.com/SaraJo/SOPA-PIPA-Protest-Page">SOPA-PIPA-Protest-Page</a>.