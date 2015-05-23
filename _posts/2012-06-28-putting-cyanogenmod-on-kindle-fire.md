---
layout: post
title: Putting CyanogenMod on the Kindle Fire
date: '2012-06-28T11:00:00.000-05:00'
author: Steven Suwatanapongched
tags:
- Technology
- Android
modified_time: '2014-08-07T19:36:22.312-05:00'
thumbnail: http://1.bp.blogspot.com/-yU7gPhRWdPg/T-wtYgHP_BI/AAAAAAABOks/dvPzH189ZBg/s600/Nexus7_tablets.jpg
blogger_id: tag:blogger.com,1999:blog-6841384.post-7235748124438055884
blogger_orig_url: http://www.sunpech.com/2012/06/putting-cyanogenmod-on-kindle-fire.html
redirect_from: /2012/06/putting-cyanogenmod-on-kindle-fire.html
---

After seeing the <a href="http://www.engadget.com/2012/06/27/nexus-7-tablet-hands-on/">Nexus 7 tablet</a> make its debut at <a href="https://developers.google.com/events/io/">Google I/O</a> yesterday, it made me realize how my Kindle Fire (KF) is kind of lame. I <a href="/2011/11/kindle-fire-review">reviewed the Kindle Fire</a> back in November 2011.

<a href="http://1.bp.blogspot.com/-yU7gPhRWdPg/T-wtYgHP_BI/AAAAAAABOks/dvPzH189ZBg/s600/Nexus7_tablets.jpg" ><img border="0"  src="http://1.bp.blogspot.com/-yU7gPhRWdPg/T-wtYgHP_BI/AAAAAAABOks/dvPzH189ZBg/s400/Nexus7_tablets.jpg"  /></a>

To be fair though, my needs have changed. When I initially purchased the KF, I didn't want an iPad2 or a 10" tablet. I just wanted a simple reading device that could browse the web a bit and play some games. And that's exactly what the KF was, and <i>still</i> is.

My needs have changed in that I want more. I want Gmail. I want YouTube. I want more apps.

The problem is that over the past eight months, I haven't seen any big improvements happen from Amazon. The <a href="http://www.amazon.com/appstore">Amazon App Store</a> has fewer of the apps I like available compared to <a href="https://play.google.com/store">Google Play</a>. On top of that, the Google Apps such as Gmail and YouTube aren't available. To me, the biggest reason to use Android is Google's products and services: Gmail, Google Maps, YouTube, etc. These are all solid apps that should be on any Android device.

Besides the lack of Google Apps, there's no native Facebook app! The one in the Amazon App store simple redirects to a browser of the mobile site! This is incredibly misleading.

On top of all of this, there are other nuances with the KF: The UI sucks. The carousel and bookshelf is just stupid. I'm sure there are folks that like how this UI is rather simple. It's just not for me. I ended up installing Go Launcher EX alongside it. <i>(See <a href="http://www.pcworld.com/article/252821/get_more_out_of_your_kindle_fire_tablet_five_tips.html">instructions</a> on how to install it.) </i>The volume UI also is not readily available-- requires an extra click to get there. The rotating wallpapers cannot be customized either.

Recalling all these frustrations, I got pretty close to <a href="https://play.google.com/store/devices/details?id=nexus_7_8gb&amp;feature=single-wide-banner">pre-ordering the Nexus 7</a>, which is priced exactly at $199, very competitively against the Kindle Fire.

But I didn't. Instead, I decided to just hack my Kindle Fire and see how close to a vanilla Android I could get.

Below are instructions I followed to get a custom ROM (Simple CyanogenMod 9) onto my Kindle Fire by rooting it. <i>Disclaimer: I am not responsible for anything that goes wrong with your device if you attempt anything I have written and linked to below.</i>

The instructions are pretty clear and I highly recommend reading and following them.

<ol>
  <li>Get Kindle Fire Utility (I used v0.9.6). See instructions <a href="http://forum.xda-developers.com/showthread.php?t=1399889">here</a>.</li>
  <li>Unzip the Kindle Fire Utility and install the drivers.</li>
  <li>Root the device.</li>
  <li>Install TWRP Recovery. For instructions, see: <a href="http://www.androidauthority.com/how-to-root-and-install-custom-recovery-on-kindle-fire-using-the-kindle-fire-utility-53451/" style="background-color: white;">How to Root and Install Custom Recovery on Kindle Fire using Kindle Fire Utility</a>.</li>
  <li>Install <a href="http://forum.xda-developers.com/showthread.php?t=1689000">Simple CyanogenMod 9 ROM (6-10-2012)</a>. For instructions, see: <a href="http://www.androidauthority.com/kindle-fire-install-simple-cyanogenmod-9-cm9-custom-rom-94468/">Amazon Kindle Fire: Flashing the Simple CM9 custom ROM</a>.</li>
</ol>

<i>Note, for the developers out there that have the Android SDK installed, the KF Utility has adb packaged in it already.</i>

So, I was able to put Simple CM9 on my Kindle Fire using the instructions in the links listed above. Here's a picture my KF running Google Play that's downloading Google Chrome browser.

<img border="0" src="http://3.bp.blogspot.com/-hr8zlreqFxA/T-wdvcKwkLI/AAAAAAABOkU/AzA_v4aHOpQ/s400/KindleFire_install.jpg" style="color: #0000ee;"  />

Here is a screenshot of my homescreen after some customizations.

<a href="http://4.bp.blogspot.com/-9JkOUEYz448/T-wdudcS1AI/AAAAAAABOkM/9bI-Duke840/s600/KindleFIre_screenshot.jpg" ><img border="0"  src="http://4.bp.blogspot.com/-9JkOUEYz448/T-wdudcS1AI/AAAAAAABOkM/9bI-Duke840/s400/KindleFIre_screenshot.jpg"  /></a>

Another screenshot of the Settings and tablet information.

<a href="http://3.bp.blogspot.com/-4CwSoFCK5UA/T-wocAEdv_I/AAAAAAABOkg/D4rvCf0SAX0/s600/KindleFire_screenshot_02.jpg" ><img border="0"  src="http://3.bp.blogspot.com/-4CwSoFCK5UA/T-wocAEdv_I/AAAAAAABOkg/D4rvCf0SAX0/s400/KindleFire_screenshot_02.jpg"  /></a> 

Overall, it was a pretty simple process. Just follow the instructions. I was able to re-download my Kindle books again using Kindle app in the Google Play store. My Kindle Fire is just awesome now. Maybe I'm speaking too soon, as it hasn't even been a full twenty-four hours of running it just yet. I do notice that it sucks up the battery a lot more, but that should be obvious as I'm running a heavier UI and more apps.

These are exciting times aren't they? Microsoft has entered the tablet space (once again) with their <a href="http://www.microsoft.com/surface/en/us/default.aspx">Surface</a>. Or at least the announcement of it. There's <a href="http://www.theverge.com/2012/6/26/3119096/amazon-kindle-fire-successor-july-31-release-rumor">rumor</a> of a new Kindle Fire from Amazon next month. A lot of competition, which in the end the consumers win.

<b>Update (January 8, 2013)</b>

Just wanted to add that there is a way to root the Kindle Fire from a Mac. Just use <a href="http://northmendo.com/breakdroid/downloads/">BreakDroid</a>. The Kindle Fire Utility doesn't work on my Windows 8 Pro virtual machine like it did on Windows 7 Ultimate.

Also, I switched to use <a href="http://forum.xda-developers.com/showthread.php?t=1766829">Jandycane</a> instead of CM. Still basically the same steps as above, but it gives me Jelly Bean on the tablet. I don't expect any more updates for custom ROMs on KF simply because Google Nexus tablets are superior in every way.

<b>Update (August 7, 2013)</b>

A few weeks ago I switched back to using <a href="http://wiki.cyanogenmod.org/w/Otter_Info">Cyanogenmod on the Kindle Fire</a> (1st Generation). Overall it's been pretty good, but my KF is now my secondary tablet device since I got a <a href="http://www.google.com/nexus/7/">Nexus 7</a> (2nd Gen).

<a href="http://4.bp.blogspot.com/-EhMga98kv8g/UgIfPMwrWSI/AAAAAAABhZs/WBJ6dUCSoOc/s600/cyanogenmod_KF.jpg" ><img border="0"  src="http://4.bp.blogspot.com/-EhMga98kv8g/UgIfPMwrWSI/AAAAAAABhZs/WBJ6dUCSoOc/s400/cyanogenmod_KF.jpg" width="187" /></a>

