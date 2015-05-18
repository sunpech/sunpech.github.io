---
layout: post
title: Installing Windows 8 Pro on Parallels Desktop 8
date: '2012-11-05T17:34:00.001-06:00'
author: Steven Suwatanapongched
tags:
- Technology
- Guide
modified_time: '2014-08-08T16:45:30.420-05:00'
thumbnail: http://4.bp.blogspot.com/-l3pToD2O5l0/UJhCTG6KgvI/AAAAAAABVlQ/jYSsgAd8pow/s72-c/IMG_20121105_144324.jpeg
blogger_id: tag:blogger.com,1999:blog-6841384.post-4473399837525284424
blogger_orig_url: http://www.sunpech.com/2012/11/installing-windows-8-pro-on-parallels-8.html
---

Last week I went to a Microsoft launch event, <a href="http://www.microsoft.com/enterprise/events/theneweraofwork/default.aspx">New Era of Work</a>, and got a <i>free</i> copy of Windows 8 Pro. I had already tried Windows 8 Preview as well as have Windows 7 Ultimate running as a virtual machines (VMs) through <a href="http://www.parallels.com/products/desktop/">Parallels Desktop</a> on my Macbook Pro (MBP). I didn't like the preview edition that much, so I uninstalled it after a few days. But after attending the event, I thought I'd give it another look.

<i>Please note that the latest PC I own is a Lenovo Thinkpad T60 from 2006, which the wireless card just broke the other day. </i>So my MBP from 2010 is the latest hardware I own.

<img border="0" height="240" src="http://4.bp.blogspot.com/-l3pToD2O5l0/UJhCTG6KgvI/AAAAAAABVlQ/jYSsgAd8pow/s320/IMG_20121105_144324.jpeg" width="320" />

The problems is that the current Parallels (version 8) does not support <i>upgrading</i> from any Windows OS to Windows 8. Here is the screenshot of what Parallels sent to me via email:

<img border="0" height="222" src="http://4.bp.blogspot.com/-ZVlD_LN1QLY/UJhLBsHm18I/AAAAAAABVl4/k9TsqIUU0-4/s320/Screen+Shot+2012-11-05+at+3.04.49+PM.png" width="320" />

I learned this the hard way when I installed a preview edition of Win8 and upgraded to Win8 Pro, and things were just wacky. The following was screwed up:
<ol>
  <li>Screen resolution was not fully supported. I have a 2560x1440 native res that wasn't supported-- instead I had to run it at 1920x1400, which was pretty sub-optimal.</li>
  <li>The path to the shared home folders was not supported. I couldn't access my Mac's home folder of \\psf\Home, which is an inconvenience.</li>
</ol>

The preview edition of Win8 ran better than the upgraded Win8 on Parallels Desktop through the upgrade! There's no way I was going to try upgrading my Win7 Ultimate that already runs just fine!
But there's a workaround. If you do a full install, it should run just fine. Here's how:
Through Parallels 8, I'm not sure about previous versions, you have an option to install other virtual machines to whatever you already have. From the virtual machines list, click on new.

<img border="0" height="210" src="http://3.bp.blogspot.com/-6-bQJU6nUqI/UJhEf6IJWsI/AAAAAAABVlk/WXdmsmKu6yY/s320/Screen+Shot+2012-11-05+at+2.57.07+PM.png" width="320" />

The window that opens up should allow you to download and install a preview edition of Windows 8 for free. Do that and pick whatever architecture you want (32 or 64 bit). I chose 64 bit and highly recommend that.

<img border="0" height="260" src="http://2.bp.blogspot.com/-LyTYu4sNnLg/UJhEg56336I/AAAAAAABVls/0aUPFR_nHcU/s320/Screen+Shot+2012-11-05+at+2.57.29+PM.png" width="320" />

Let it download and install fully. From here, as per the instruction given to me from my copy of Windows 8 Pro, go to: <a href="http://www.windows.com/nfrdownload">http://www.windows.com/nfrdownload</a>. Follow the instructions there to begin the download process of Win8 Pro. Once that finishes the download, there should be a screen that comes up that asks where to proceed with some options.

<b>Choose to save the Win8 Pro as an ISO on your local computer to install later.</b> Do not choose to install immediately!

Once you have the ISO saved, you can do a full install of Win8 Pro from that. At this point you can go ahead and delete the Win8  preview VM you just installed on your Mac.

Now you can install Win8 Pro from the newly downloaded ISO. The product key I had worked. If the product key you were given was for an upgrade only, there are workarounds for that even-- via some registry edit. See: <a href="http://www.guidingtech.com/16405/probable-fix-activating-windows-8-clean-install/">Probable Fix: Problem in Activating Windows 8 After Clean Install</a>

Note, this is all because Parallels 8 currently doesn't have a clean upgrade path for current Windows OSes. Once that fix is made, then this is probably the only way to get Windows 8 Pro to run on Parallels on your Mac OS X.