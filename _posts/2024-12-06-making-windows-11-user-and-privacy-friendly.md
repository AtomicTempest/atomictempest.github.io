---
layout: post
title:  "Making Windows 11 user and privacy friendly"
summary: "Modifying Windows 11 to get an older style UI back. Also disabling microsoft telemetry, tracking, and other bullshit"
author: atomictempest
date: '2024-12-06 4:00:00 +1300'
category: ['guides', 'windows']
tags: windows11, privacy
thumbnail: /assets/img/posts/tech_padlock.png
keywords: Windows11, privacy, UI customization, shell customization, telemetry blocking
usemathjax: false
permalink: /blog/making-windows-11-user-and-privacy-friendly/
---

# Making Windows 11 user and privacy friendly

A few months ago I had the interesting whim to try out the hardware-based encryption on my SSD. Now this was a bit of a pain, since to enable it I needed to reset my OS. I'm not going to get into the details of enabling hardware-based encryption here; it's complicated and a pain. Also for those in the know, yes, I do know that hardware encryption on some drives is insecure; mine is an Opal 2.0 drive, and I don't need perfect security. The problem is that BitLocker on the version of Windows 10 I was installing would not detect that my SSD was compatible with hardware-based encryption. I spent far too much time trying to figure out the cause and fix it but came up empty. Now it's not like I really need disc encryption on my desktop; I doubt anyone is going to be trying to physically hack my PC. However, at this point, I had already wiped the drive.

Now I had resisted upgrading to Windows 11 for a while now. Mainly because I dislike the UI, I like the Windows 10 UI much better. Windows 10 is losing support soon, though, so I eventually decided that this was a good chance to try out Windows 11. After researching a few different ways to mod the UI, I took the plunge. The hardware encryption worked on the first try, although that's not the point of this blog post. In this post I'm instead going to share some of the methods I used to customise Windows 11, making it more privacy friendly and, subjectively, more user friendly.

## Part 1 - The Windows 11 Setup

The first part of making Windows 11 better comes when installing Windows 11 and doing the first setup. The TLDR is that bypassing using a Microsoft account and using a local account instead makes Windows 11 much better. Based on what I've seen and heard from other people. By using a local account, I've skipped lots of popups, OneDrive ads, and all sorts of Microsoft bullshit by not using a Microsoft account.

So how do you skip logging into a Microsoft account? Well, it's not hard. Simply follow the Windows 11 install progress until you get to the "Choose a country" screen. Next hit `Shift + F10`. A command prompt should appear. Then type OOBE\BYPASSNRO and hit enter. The computer will reboot and return you to the same screen. Next you need to disable the internet. The simplest way is to unplug any ethernet cable. A potentially faster way is to open the command prompt again and type `ipconfig /release` and hit enter. Then just continue the installation. Once it gets to the point of trying to connect to the internet, it should have a button that says, I don't have Internet. After that you will also have a button, Continue with limited setup. The rest is pretty self-explanatory. If any of this was confusing or doesn't work, there are tonnes of more detailed guides out there on the internet that are easy to find and may be more up to date with any changes Microsoft has made.

## Part 2 - Making Windows 11 more privacy friendly

Now no self-respecting digital privacy enthusiast would call Windows 11 privacy friendly, even when you toggle off all the tracking and telemetry settings they give you. Even Windows 10 isn't very privacy friendly by default. Now I know, of course, that if you want excellent privacy, you should use Linux instead. I actually have Linux as an alternative OS on another drive. But Linux is not perfect for everything. Gaming is a good example of something that Windows definitively does the best. So how do we make Windows reasonably private?

Well, fortunately, others have done most of the hard work for us. There are several good third-party tools that allow us to toggle loads of privacy settings that Windows doesn't show you. My current favourite is a program called the Windows Privacy Dashboard. It should show up near the top of any search, but here is the current link at the time of writing. [WPD](https://wpd.app). Windows Privacy Dashboard allows you to toggle tonnes of telemetry settings and gives recommendations of what to disable and what each option does. One recommendation I have is to make sure you don't disable push notifications if you plan to run some UWP-style apps like the relatively new NVIDIA app or the Realtek Audio Console. These apps will crash on launch if you have push notifications disabled while giving you absolutely no useful error message or crash logs. It drove me crazy for a little while until I eventually found the cause and solution. You should also make sure not to disable Windows Defender unless you plan to replace it with a third-party antivirus. I personally think that modern Windows Defender is perfectly good, especially for a simple home user.

Another part of the Windows Privacy dashboard allows you to enable certain blocklists that will add block rules to the Windows firewall for a bunch of Microsoft IP addresses used for telemetry. Just note that the extra blocklist will block some Microsoft websites like LinkedIn and is probably not needed.

## Part 3 - Changing the Shell/UI to be more user friendly

Now this is the more subjective part. You might like the Windows 11 Shell (User Interface). I personally don't. I especially hate the Windows 11 compacted context menu, as well as the new style Windows 11 start menu. So here is where I'm going to share the tools I used to customise the Windows 11 Shell and User Interfaces. Now I'm not going into extreme detail about all the options available; there are plenty of them, and some people have already made videos showing them off. Those videos can show the different options far better than I could with a blog post. Instead I'm just going to tell you about the software I ended up deciding to use. Some of the software available to customise the Windows shell costs money. All of the software I have used, though, is available for free. Do note, however, that Windows updates can potentially break this software, and although I've had very few problems, reliability is not guaranteed. 

The first piece of software I have used is called ExplorerPatcher. It's currently available at [ExplorerPatcher](https://github.com/valinet/ExplorerPatcher). ExplorerPatcher is a great piece of software that allows you to bring back the Windows 10 style context menu with all the options without an extra click. Another thing it can do is change the Windows File Explorer and/or the taskbar to look more like Windows 10. It also has a Windows 10 start menu option; however, I don't use this personally.

For the start menu, I use a program called Open-Shell. Currently available at [Open-Shell](https://open-shell.github.io/Open-Shell-Menu/). Open-Shell is a great program that allows you to configure a highly customisable start menu that can look however you want. My personal start menu looks like a more modern version of the Windows 7 Start Menu and has buttons for quickly reaching both the control panel and Windows settings app. It also has a button to quickly reach the network connections page of the control panel, which shows all the network adapters, which I like immensely. It also includes a shortcut button to my user folder. This only scratches the surface of what Open-Shell can do. It has its own search functionality and has a lot of themes. Maybe you want nostalgia of a Windows 98 or XP-style start menu. It can do that.

## Part 4 - Conclusions

This concludes my guide on making Windows 11 privacy and user-friendly. Do note this is not a full guide on making your PC private. The privacy part was only about disabling most of Windows 11's telemetry, and more is required to become completely private, especially online. I have not talked about web browsers, VPNs, or other privacy tools and services. In the future I may add another guide on becoming nearly fully private online. There are plenty of great guides online about this already, though. In particular, I like a YouTube channel called Techlore that has plenty of great guides on the subject. For anyone who actually ends up reading this, I hope you found this either interesting or informative.



