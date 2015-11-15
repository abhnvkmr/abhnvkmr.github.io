---
title: 'Remove Windows Defender from context menu'
layout: post
tags: [technology]
share: true
comments: true
summary: 'How to download Windows 10 ISO without Media Creation Tool'
---
Microsoft released Windows 10 Fall update this week with. It is running very good on my system. But one pet-peeve I have with the update is that it adds a "Scan with Windows Defender" command in context menus of files and folders. Even if you use a third-party antvirus installed and have Defender disabled. Although one can ignore it and move on with their life, my OCD gets...you know...

I have even removed "Play with Windows Media Player" and "Shop online for music" items. (I use foobar2000.)

To remove the Defender menu item.

Either delete the following registry key:
`HKEY_CLASSES_ROOT\CLSID\ {09A47860-11B0-4DA5-AFA5-26D86198A780}`

or run the following in elevated Command Prompt:
`regsvr32 /u "C:\Program Files\Windows Defender\shellext.dll`

...and it will be gone. Poof!