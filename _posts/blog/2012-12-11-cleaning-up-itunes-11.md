---
title: Cleaning up iTunes 11
layout: post
tags: [technology, apple]
comments: true
share: true
categories: blogpost
---
iTunes, especially on Windows, has never been a joy to use. Of course, there are a lot of alternative iPod/iPhone/iPad sync softwares out there, but only iTunes offer the full-featured functionality for Apple-devices management. Although I regularly used iTunes when I had my MacBook but on Windows I had kept it out like a virus. But upon getting an iPad, I had to install it but I still only fire it up when I have to perform a sync. The the problem is that even if you don&#8217;t use it often, it runs a few system-level processes and services on startup.

*   Bonjour (mDNSResponder.exe)
*   Apple Mobile Device Support
*   iTunes Helper
*   iPod Service

So when I updated my iTunes installation to the latest version, I had to perform a new set to tweaks to keep my system devoid of running any Apple iTunes-related processes and services, but still being able to successfully sync my devices.

#### Bonjour

Go to Computer management > Services and change the startup of &#8216;Bonjour&#8217; service to Manual. Or you can just uninstall Bonjour from &#8216;Uninstall or change programs&#8217; window.

#### Apple Mobile Device Support

Change the startup type of &#8216;Apple Mobile Device Support&#8217; to Manual. Although this will cause iTunes to throw an error box but it&#8217;ll be still able to automatically start this service when you try to connect an Apple device.

#### iTunes Helper

This process does nothing but preload iTunes libraries on startup speeding up the launch of iTunes. You can safely disable it in Startup tab of Task Manager. (on Windows 7 and earlier, you will have to use msconfig, the System Configuration tool)

#### iPod Service

This service is responsible for automatically launching iTunes whenever you connect an Apple device to sync. To disable it, change its startup type to Manual in Computer Management > Services. It will also be automatically launched when you try to sync.

### Update:

It seems that there is another item called &#8216;Apple Push&#8217; on select iTunes installations on Windows which is something related to iCloud. It can also be disabled using Task Manager startup&#8217;s tab or msconfig.