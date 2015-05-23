---
layout: post
title: Android SDK issue on Windows 7 x64
date: '2010-01-26T18:59:00.000-06:00'
author: Steven Suwatanapongched
tags:
- Technology
- Software Development
- Android
- Guide
modified_time: '2014-08-07T20:14:24.526-05:00'
thumbnail: http://3.bp.blogspot.com/_7U5MdumP-no/S1-JuvXb-TI/AAAAAAAAOEc/-7CpDZMLDBA/s600/Android_error_message_64bit.jpg
blogger_id: tag:blogger.com,1999:blog-6841384.post-6014119442015021448
blogger_orig_url: http://www.sunpech.com/2010/01/android-sdk-issue-on-windows-7-x64.html
redirect_from: /2010/01/android-sdk-issue-on-windows-7-x64.html
---

I recently installed the <a href="http://developer.android.com/sdk/">Android SDK</a> and <a href="http://www.eclipse.org/downloads/">Eclipse</a> (32-bit) onto my Windows 7 Ultimate 64-bit machine.  First thing I wanted to do was go through the <a href="http://developer.android.com/guide/tutorials/hello-world.html">Android Hello World Tutorial</a>. 

Well, I ran into the following error message:

<blockquote><span style="font-family: 'Courier New', Courier, monospace;">'java' is not recognized as an internal or external command, operable program, or batch file.  SWT folder '' does not exist.  Please set ANDROID_SWT to point to the folder containing swt.jar for your platform.</span></blockquote><a href="http://3.bp.blogspot.com/_7U5MdumP-no/S1-JuvXb-TI/AAAAAAAAOEc/-7CpDZMLDBA/s600-h/Android_error_message_64bit.jpg"  style="clear: left; display: inline !important; float: left; margin-bottom: 1em; margin-right: 1em;"><img border="0" height="64" src="http://3.bp.blogspot.com/_7U5MdumP-no/S1-JuvXb-TI/AAAAAAAAOEc/-7CpDZMLDBA/s640/Android_error_message_64bit.jpg"  /></a>


I read somewhere that I should install the x64 Java version.  However, when I went to <a href="http://www.java.com/en/download/manual.jsp">Java download page</a>, it didn't even have the x64 version available to download.  Turns out that the problem was that I was using <a href="http://www.google.com/chrome">Google Chrome</a> to browse there.  I had to use Internet Explorer (x64 bit version) to get the x64 Java link to even show up!

This worked for me, but you can check out the following link at StackOverflow:

<a href="http://stackoverflow.com/questions/1919340/android-sdk-setup-under-windows-7-pro-64-bit">http://stackoverflow.com/questions/1919340/android-sdk-setup-under-windows-7-pro-64-bit</a>


