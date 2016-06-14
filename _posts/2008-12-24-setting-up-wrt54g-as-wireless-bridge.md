---
layout: post
title: Setting up WRT54G as a wireless bridge with DD-WRT
date: '2008-12-24T23:39:00.000-06:00'
author: Steven Suwatanapongched
tags:
- Technology
- Guide
modified_time: '2014-08-08T17:01:27.441-05:00'
thumbnail: http://4.bp.blogspot.com/_7U5MdumP-no/SVMeq-RLbEI/AAAAAAAAIZk/b33sMkW_w9o/s600/linksys_wrt54g.jpg
blogger_id: tag:blogger.com,1999:blog-6841384.post-7628154985244238079
blogger_orig_url: http://www.sunpech.com/2008/12/setting-up-wrt54g-as-wireless-bridge.html
redirect_from: /2008/12/setting-up-wrt54g-as-wireless-bridge.html
header-img: /public/images/headers/technology.jpg
---

My parents have a <a href="http://www.thaitv.tv/">Thai TV</a> ethernet box of some kind so they can tune in to their Thai stations, shows, and even radio on their HDTV.  However, I had to run a 50 foot CAT5 cable from the upstairs to the first floor great room, which is quite messy.  So for Christmas this year, I bought them a <a href="http://www.amazon.com/gp/product/B000BTL0OA?ie=UTF8&amp;tag=sunpech-20&amp;linkCode=as2&amp;camp=1789&amp;creative=9325&amp;creativeASIN=B000BTL0OA">Linksys-Cisco WRT54GL Wireless-G Broadband Router</a>.

<img  border="0" id="BLOGGER_PHOTO_ID_5283600511454112834" src="http://4.bp.blogspot.com/_7U5MdumP-no/SVMeq-RLbEI/AAAAAAAAIZk/b33sMkW_w9o/s400/linksys_wrt54g.jpg" />

The setup I wanted was to have the Thai TV box, which uses an ethernet port for all data, connect to the wireless router, and have the wireless router connect to the wireless router upstairs.  This setup required a wireless bridge, which the router did not come configured with.  So after some googling, I found the proper links to set it all up with:

<img  border="0" id="BLOGGER_PHOTO_ID_5283760857843106034" src="http://1.bp.blogspot.com/_7U5MdumP-no/SVOwgXHaAPI/AAAAAAAAIZs/CVLq9lAx7To/s400/WIFIBRDG.GIF" />

First thing to do, is to figure out what to do with your particular router: <a href="http://www.dd-wrt.com/wiki/index.php/Linksys_WRT54G/GL/GS/GX">Linksys WRT54G/GL/GS/GX</a>.  For me, I had to <a href="http://www.dd-wrt.com/wiki/index.php/How_To_Flash_the_WRT54Gv8">Flash the WRT54Gv8</a>.

Unfortunately for me, I messed up the installation, and "bricked" my router.  But after more googling, I found out how to "unbrick" it: <a href="http://blog.rim3y.net/zero/?p=942">UnBrick your Linksys router - WRT54GS v7</a>.  Apparently my problem was that the tftp program was just incredibly slow in uploading the firmware, and I closed the DOS window too quickly due to what appeared to be inactivity.

The last thing I had to do was set up the <a href="http://www.dd-wrt.com/wiki/index.php/Wireless_Bridge">wireless bridge</a>, which was the easy part.  So there you have it, how to set up a wireless bridge using DD-WRT.<span style="font-weight: bold;"></span>
