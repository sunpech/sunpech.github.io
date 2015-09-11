---
layout: post
title: Setting up Windows Phone 8 Emulator on a Virtual Machine
date: '2012-11-14T11:00:00.000-06:00'
author: Steven Suwatanapongched
tags:
- Software Development
- Guide
modified_time: '2014-08-08T16:44:52.111-05:00'
thumbnail: http://1.bp.blogspot.com/-zmyacljuX2g/UKN_RJcTrtI/AAAAAAABVvU/68s9SzlJNw0/s600/VMF5_WinPhone8.jpg
blogger_id: tag:blogger.com,1999:blog-6841384.post-7557647617734760650
blogger_orig_url: http://www.sunpech.com/2012/11/running-windows-phone-8-emulator-on.html
redirect_from: /2012/11/running-windows-phone-8-emulator-on.html
header-img: /public/images/header_software_development.jpg
---

Not long ago I blogged about <a href="/2012/11/installing-windows-8-pro-on-parallels-8">Installing Windows 8 Pro on Parallels Desktop 8</a>. That of course worked for me, but when it came time to having Visual Studio 2012 (VS2012) and running an emulator for Windows Phone 8, it simply doesn't work. I searched the Internet as to why, and came up with the following links:

<ul>
  <li><a href="http://stackoverflow.com/questions/13148828/unable-to-create-the-virtual-machine">StackOverflow: Unable to create the virtual machine</a></li>
  <li><a href="http://social.msdn.microsoft.com/Forums/en-US/wpdevelop/thread/860f4203-e3f7-410e-8bf5-2999224df312">MSDN: Having problems running the Windows Phone 8 Emulator?</a></li>
  <li><a href="http://blog.catenalogic.com/post/2012/10/31/Running-the-Windows-Phone-8-emulator-in-a-virtual-machine.aspx">Running the Windows Phone 8 emulator in a virtual machine</a> (I followed this guide)</li>
</ul>

As a lot of people <a href="http://forum.parallels.com/showthread.php?p=646448#post646448">pointed out</a>, it's not really possible in <a href="http://www.parallels.com/products/desktop/">Parallels Desktop 8</a> (PD8), but is possible through <a href="http://www.vmware.com/products/fusion/overview.html">VMware Fusion 5</a> (VMF5) with a small workaround.

<img border="0" src="http://1.bp.blogspot.com/-zmyacljuX2g/UKN_RJcTrtI/AAAAAAABVvU/68s9SzlJNw0/s320/VMF5_WinPhone8.jpg" />

I recommend following <a href="http://blog.catenalogic.com/post/2012/10/31/Running-the-Windows-Phone-8-emulator-in-a-virtual-machine.aspx">this guide</a>, but will supplement some more information as it pertains to VMF5, as it's not exactly the same as <a href="http://www.vmware.com/products/workstation/overview.html">VMware Workstation 9</a>.

First off, I recommend installing from scratch. I tried to import my existing virtual machine created through PD8, and failed many, many, many times. I ended up with a blue screen screen and countless reboots that try to fix something that didn't get fixed. Save yourself time and just do a clean install of Windows 8 on VMF5.

Even if you have or haven't installed VS2012 with <a href="http://dev.windowsphone.com/en-us/downloadsdk">Windows Phone 8 SDK</a>, you should uninstall Hyper-V.

You can get to this in Windows 8 through Control Panel and search for "windows features". Then click on "Turn Windows features on or off".
<img border="0" src="http://1.bp.blogspot.com/-C7zU-pHW7Jw/UKN37F-5vDI/AAAAAAABVuw/nzMZOJBcOdo/s600/WindowsFeaturesOnOff.jpg" />

Make sure these boxes are unchecked, as in off. <i>You'll check these back on later.</i>
<img border="0" src="http://3.bp.blogspot.com/-XR-8QkUXTbc/UKN36ddCFpI/AAAAAAABVuo/9tFQJ48tGHI/s600/WindowsFeatureHyperV.jpg" />

Next in the virtual machine's settings, in Processors &amp; Memory, uncheck "Enable hypervisor applications in this virtual machine". <i>You'll check this back on later.</i>
<img border="0" src="http://1.bp.blogspot.com/-sCtRF5kTCfY/UKN5_Jt_bbI/AAAAAAABVvI/i90-4JqzU30/s600/VMF5_Settings_ProcMemory.jpg" />

<img border="0" src="http://1.bp.blogspot.com/-cyYSt7ZXA5U/UKN35aaDeNI/AAAAAAABVuY/o4hbXsnSDvc/s600/Enable_HypervisorApps.jpeg" />

Next you have the Virtual Machine Library window open, and then right click + hold alt (option) key to get the option to "Open Config File in Editor".
<img border="0" src="http://3.bp.blogspot.com/-pQzTbbDdYys/UKN3592LDpI/AAAAAAABVug/YITcCVyxs_w/s600/VirtualMachineLibrary_screenshot.jpg" />

Here add the following settings, as they shouldn't exist.

<span style="font-family: Courier New, Courier, monospace;">hypervisor.cpuid.v0 = "FALSE" </span>
<span style="font-family: Courier New, Courier, monospace;">mce.enable = "TRUE"</span>

<img border="0" src="http://4.bp.blogspot.com/-AHePf3IN7os/UKN45Tx3lZI/AAAAAAABVvA/ywwBSwzJpYk/s600/EditVMXFile.jpg" />

Finally, check back on everything you unchecked from before. A restart is probably needed for the Windows Hyper-V install again.

Now you'll be able to run a Windows Phone Emulator within VMware Fusion 5, on a Mac!
<img border="0" src="http://1.bp.blogspot.com/-gieJA_9CfPE/UKN38Cjws5I/AAAAAAABVu4/TIrgwj5uh3c/s600/WindowsPhoneEmulator.jpg" />

Happy coding!

<i>Note: I haven't purchased my copy of VMware Fusion 5 yet. I'll likely buy it before the 30-day trial is up.</i>
