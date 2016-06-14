---
layout: post
title: Installing Thai fonts onto an Android device
date: '2010-08-30T09:00:00.110-05:00'
author: Steven Suwatanapongched
tags:
- Technology
- Android
- Guide
modified_time: '2014-08-07T20:13:45.291-05:00'
thumbnail: http://1.bp.blogspot.com/_7U5MdumP-no/THt8iBDVVQI/AAAAAAAAWWA/ppE6gy3cFIw/s600/Screen+shot+2010-08-30+at+4.40.01+AM.png
blogger_id: tag:blogger.com,1999:blog-6841384.post-6665102534805821074
blogger_orig_url: http://www.sunpech.com/2010/08/installing-thai-fonts-onto-android.html
redirect_from: /2010/08/installing-thai-fonts-onto-android.html
header-img: /public/images/headers/android.jpg
---

I've received numerous requests asking for help on how to install Thai fonts onto an Android device after my initial post on <a href="/2010/01/rooting-my-nexus-one-and-installing">Rooting my Nexus One and installing Thai fonts</a>.  Since I do update my Android phone with the <a href="http://www.cyanogenmod.com/">CyanogenMod ROM</a> quite often (which wipes the Thai fonts on each install), I thought I'd share a simple shell script to help get Thai fonts onto Android.

This post <b>does not cover how to root an Android device</b>.  I will leave that to you to figure out.  But if you happen to have a Nexus One like me, check out the following link: <a href="http://androidandme.com/2010/01/hacks/video-how-to-unlock-and-root-a-nexus-one/">Video: How to unlock and root a Nexus One</a>.

Also, you will need to have the <a href="http://developer.android.com/sdk/index.html">Android SDK</a> on your system (hopefully Mac or Linux-- which is what the script is written for, although for Windows it won't be hard to figure out what commands need to be run-- hint: use .\adb.exe instead of ./adb  in DOS or whatever command prompt and skip the shell script).

Those are the <u>two prerequisites</u> to installing Thai fonts: <b>a rooted device </b>and<b> the Android SDK </b>on your system.  Oh, and I guess how to run some basic knowledge of the command line in a shell (Terminal).

#### Instructions

<ol>
  <li>Attach your Android device to your computer via USB and mount it.</li>
  <li>Download: <a href="http://www.mediafire.com/?464j2791iccuan9"><b>InstallThaiFontsOntoAndroid.zip</b></a>. </li>
  <li>
      Unzip it and you will see a folder.

    <a href="http://1.bp.blogspot.com/_7U5MdumP-no/THt8iBDVVQI/AAAAAAAAWWA/ppE6gy3cFIw/s600/Screen+shot+2010-08-30+at+4.40.01+AM.png" alt="" ><img   border="0" height="158" src="http://1.bp.blogspot.com/_7U5MdumP-no/THt8iBDVVQI/AAAAAAAAWWA/ppE6gy3cFIw/s400/Screen+shot+2010-08-30+at+4.40.01+AM.png" alt=""  /></a>

    The contents of the folder should be placed in the <i>tools folder</i> of the Android SDK where adb is.

    <a href="http://4.bp.blogspot.com/_7U5MdumP-no/THt3wnkUvrI/AAAAAAAAWV0/kbDhyy2OiBA/s600/Screen+shot+2010-08-30+at+4.19.06+AM.png" alt=""><img   border="0" height="145" src="http://4.bp.blogspot.com/_7U5MdumP-no/THt3wnkUvrI/AAAAAAAAWV0/kbDhyy2OiBA/s400/Screen+shot+2010-08-30+at+4.19.06+AM.png" alt=""  /></a>

    <a href="http://4.bp.blogspot.com/_7U5MdumP-no/THt4gn4_XCI/AAAAAAAAWV4/hw9ChuVl1d0/s600/Screen+shot+2010-08-30+at+4.22.30+AM.png" alt=""><img   border="0" height="285" src="http://4.bp.blogspot.com/_7U5MdumP-no/THt4gn4_XCI/AAAAAAAAWV4/hw9ChuVl1d0/s400/Screen+shot+2010-08-30+at+4.22.30+AM.png" alt=""  /></a>
  </li>
  <li>
    Open up a Terminal (Applications-&gt;Utilities-&gt;Terminal.app) and go into the directory where your android SDK and go into the folder: <i>tools</i>.

    <a href="http://3.bp.blogspot.com/_7U5MdumP-no/THt6S0SffzI/AAAAAAAAWV8/oRgkGqYEnCs/s600/Screen+shot+2010-08-30+at+4.30.23+AM.png" alt=""><img   border="0" height="210" src="http://3.bp.blogspot.com/_7U5MdumP-no/THt6S0SffzI/AAAAAAAAWV8/oRgkGqYEnCs/s400/Screen+shot+2010-08-30+at+4.30.23+AM.png" alt=""  /></a>
  </li>
  <li>
    You can test to make sure that your device is connected by the following command in the terminal:

    <blockquote>
      <pre>
./adb devices
      </pre>
    </blockquote>
  </li>
  <li>
    And to mount it:

    <blockquote>
      <pre>
./adb remount
      </pre>
    </blockquote>
  </li>
  <li>
    Make sure that the script, install_thai_fonts.sh, is executeable by running:

    <blockquote>
      <pre>
chmod +x install_thai_fonts.sh
      </pre>
    </blockquote>
  </li>
  <li>
    <ul>
    <li>
    <b>[Recommended]</b> Now you are ready to run the shell script to install the six fonts onto the device.

    <blockquote>
      <pre>
./install_thai_fonts.sh
      </pre>
    </blockquote>

    <i>Or, if you don't wish to run the shell script...</i>
    </li>
    <li>
    <b>[Alternate]</b> Run the following line by line (you can copy &amp; paste them line by line into Terminal):

    <blockquote>
      <pre>
./adb push ./fonts/DroidSans.ttf /system/fonts/DroidSans.

./adb push ./fonts/DroidSans-Bold.ttf /system/fonts/DroidSans-Bold.ttf

./adb push ./fonts/DroidSerif-Bold.ttf /system/fonts/DroidSerif-Bold.ttf

./adb push ./fonts/DroidSerif-BoldItalic.ttf /system/fonts/DroidSerif-BoldItalic.ttf

./adb push ./fonts/DroidSerif-Italic.ttf /system/fonts/DroidSerif-Italic.ttf

./adb push ./fonts/DroidSerif-Regular.ttf /system/fonts/DroidSerif-Regular.ttf
      </pre>
    </blockquote>
    </li>
    </ul>
    If there were no error messages, then you should now have the Thai fonts on the Android device.
  </li>
  <li>
    <b>Reboot</b> and you will see Thai on webpages, SMS, and files names that are in Thai.
  </li>
</ol>

<a href="http://2.bp.blogspot.com/_7U5MdumP-no/THsv9JiqFhI/AAAAAAAAWVQ/IgkgPKQu6Ag/s600/IMG_2253.jpg" alt=""><img   border="0"  src="http://2.bp.blogspot.com/_7U5MdumP-no/THsv9JiqFhI/AAAAAAAAWVQ/IgkgPKQu6Ag/s640/IMG_2253.jpg" alt="" /></a>
