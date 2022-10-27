---
layout: post
title: My 1st year with GNU/Linux
date: 2022-10-24
---

As a musician, I've always had an inquisitive perspective on life. I like to know how things work. When I was a kid, I remember fiddling with some version of Ubuntu on one of my dad's laptops, but besides that I hadn't really used GNU/Linux on my own.
That was until the first half of 2021, when I had started to gain interest in Linux, and a growing distaste for Windows 10 and Microsoft's unethical, anti-consumerist practices. 
In the past, I'd heard distro names like Manjaro, Linux Mint, etc. but never *really* knew what GNU/Linux was, so I decided to take it for a spin. 

To start off, I chose Linux Mint, likely due to it being highly recommended to beginners to GNU/Linux, and those migrating from Windows.
Once I had felt I was ready to take the plunge (though I still dual-booted for a bit), I spun up a Linux Mint Live CD and installed it.
The first thing I noticed right off the bat was screen tearing when watching videos, and that dragging windows/programs around on the screen would cause this insufferable stutter/lag to the whole machine (display and audio).
Also, I had a very poor experience getting games to run, if at all. Of course, this all came down to the fact that I had an NVIDIA GPU, and I believe the open-source Nouveau drivers were installed.
I can't clearly remember what had happened, but I had a rough time trying to get the proprietary drivers installed/working properly. Mind you, I was still very new to GNU/Linux at the time (and still am haha) but I feel like if I had that issue, a lot of other new users eager to make the switch may encounter it as well, and that could very easily turn potential users away.

It got to the point where I gave up on Linux Mint, but I didn't want to give up on GNU/Linux altogether. I decided to try Pop!_OS, mainly due to the fact that their live CD comes with the proprietary NVIDIA drivers pre-installed for you. 
I was able to get games running much easier, however I was not a fan of the desktop environment Pop!_OS ships with by default. 
That's when I discovered you can install different desktop environments, even multiple at a time, and that changed the game for me.

The desktop environment I switched to was KDE. Like most people, when switching from Microsoft Windows to GNU/Linux, you want the transition to feel smooth, and you want your environment to feel comfortable/familiar.
Going from Windows to KDE is honestly great. I'd even go as far as to say that KDE is MILES ahead of the Windows DE, although it can be buggy, I will admit.
So now, I'm using Pop!_OS with KDE, playing games, getting acquainted with the command line, and just getting an overall feel for GNU/Linux.
I still had to dual boot for a couple games, but as time went on, I found myself being on Windows less and less. (Fast forward to the present - there are only TWO games in my Steam library that can't run, and they're titles I have little to no interest in playing. Impressive!)

Around mid-November, I decided to fully make the switch to a GNU/Linux OS, and erase my Windows partition. At that point, I had gotten 9/10ths of my Steam Library running, and the games that were borked, I was willing to part ways with. I had all of my programs on Windows either running through Wine or a native Linux version (Over time, I have dropped several Windows programs in exchange for FOSS alternatives that not only do I enjoy more but ultimately have more control over).

A few months passed, and I was enjoying my cozy KDE setup on Pop!_OS, but I was beginning to grow tired of the familiar layout. In some video I saw, they mentioned how desktop environments and window managers are two separate things, and that you technically don't even need a full-fledged desktop environment; it's possible to have a fully functioning environment with just a window manager. I remember at the time, I couldn't wrap my head around that concept, so I looked into standalone window managers a little more. I specifically remember seeing this one [screenshot of an i3 rice](https://i3wm.org/screenshots/i3-9.png) and being like "How the hell do people use their computer like this?"

The whole idea of just running a window manager seemed so foreign to me, so outlandish that nobody could possibly do that. Well, I decided to try a window manager out for myself, so I installed awesomeWM. Not sure why I chose that one specifically. By default, awesomeWM is *usable*, but by no means is it pretty, or jam packed with features. In fact, one of the first things I noticed was just how absolutely minimal everything was (No system tray, bloated menus, etc.)

One thing that really stood out to me was the fact that any modifications you wanted to make to your window manager had to be done through config files. Again, this whole concept of only managing settings through text/CLI was so foreign to me, it was very strange at first. As time went on, I learned about awesome-copycats, how to theme awesome, and add some extensions/widgets to make it a tad more usable. As I was learning about awesome, and how to set up various things within it, I would hop back and forth between it and KDE. Overall though, awesomeWM was pretty much exactly what I had been looking for - something different from the look and feel of Windows (and even macOS), truly something of it's own - something I could make MY own.

Another few months passed, and I had been getting real comfy with my awesomeWM setup, learning the basics of writing bash scripts, tweaking various configs, really just trying to understand the system more and more. However, as the time went on I would frequently run into roadblocks/issues where I would find a piece of software I wanted to install while on Pop!_OS and it would only be available on the AUR, or it wouldn't have a PPA, or the .deb package for it was hella outdated. It made discovering new software a hassle. (Recently I've heard of software called [Distrobox](https://github.com/89luca89/distrobox) that could potentially be a workaround to this issue!) There were also a lot of minor inconsistencies or issues that hindered my experience.  I don't really blame Pop!_OS for this at all.

Once again, I found myself wanting to switch distros. I had been daily driving GNU/Linux "full-time" for about 6 months, and felt I was comfortable enough to switch to something that required a bit more elbow grease. I kept running into weird issues with Pop!_OS when I tried to modify certain things to my liking. Pop!_OS is geared towards beginners of GNU/Linux, or those simply looking to have a "just works" system, and I will say that while it does a good job of giving you a stable, usable system out of the box, it feels like it downplays exploring your system, figuring out the ins and outs of it, tweaking things to your liking. Of course, this is all in an attempt by System76 to avoid people breaking their OS, which is helpful in some ways, but limiting in others.

Mid-May of 2022, an updated version of the "archinstall" script for Arch Linux released. I had heard of Arch, but I'd always avoided it as it seemed quite advanced. As strange as it might sound, I find Arch Linux much simpler to use than Pop!_OS. Mind you, I didn't do a manual install (I have installed Gentoo in a VM though), but everything from the installation script to system management just seems more straightforward. Pretty much any and every issue I had while on Pop!_OS was non-existent on Arch Linux. Not to mention the [wiki](https://wiki.archlinux.org) is a tremendous help. (Although it is not perfect.)

I dual-booted Arch Linux and Pop!_OS for a brief period, as I was still familiarizing myself with things like pacman - the package manager for Arch, and really figuring out what applications/packages I needed to build a fully-functioning system with my window manager, as I wasn't going to rely on any other DE for core system applications. There's no "settings GUI" (unless you install one). There's no "app store" (does pamac work with vanilla Arch?). There's the command line, and the endless possibilities within it.

Once I had everything running smoothly on Arch that I had on Pop!, I decided it was time to say goodbye to Pop!. With Arch Linux, I have more control over my system than ever before. It's so comfy and tailored to me that I wouldn't give it up for anything in the world. As amazing as it is for choosing each and every package you run on your machine, I  would really only recommend it to those who are willing to  "babysit" their system, as it does require more maintenance or upkeep. It's mainly just due to it's release model (it's a rolling release). So for beginners, or even those just looking to have a "set it and forget it" system, I'd recommend sticking with something with a static release model. (Pop!_OS and Linux Mint are two viable options, though with my aformentioned experience with both, I'd say your results may vary.)

It wasn't until I had been using GNU/Linux for a few months that I had begun looking into the history/origins of it all.
I'd always hear "Linux is the kernel", but didn't fully understand it for a while. Okay, Linux is the kernel, but what's everything else then?
So, to break it down very briefly, there's kernel space, and then there's user space; that's where GNU comes in.
Software like the Bash shell, the GNU coreutils, Glibc and the GCC (GNU C Compiler), among many others are what makes the GNU operating system (unless you're an Alpine Linux user, I guess). I looked more into the GNU Project, the FSF and the Free Software Movement.
It's unfathomable just how incredible it is that we have this LIBRE operating system today.
The thought of only having Windows or macOS to choose from is truly dystopian. I'm so grateful I'm not limited to how one company forces my computing experience to be - I have control - I get to choose.

One thing I will say about making any sort of change in your life, especially big changes, is that it'll most likely come at some sort of price, or you'll end up having to sacrifice something. It's also very much okay to take your time with these changes; even small, incremental choices build up into a big change. When it comes to switching from Windows to GNU/Linux, a piece of advice I can give is to look at every piece of software you have installed, every program you use on a daily and ask yourself the following:

1) Is this software Free(Libre) and Open-Source? (check the license)

2) Is this software available on GNU/Linux? (Or if need be, can this run through Wine?)

3) Is there a [FOSS alternative](https://alternativeto.net) I could be using instead?

4) Do I *really* need this software? (e.g. for work, school, etc)

Bit by bit, I swapped out proprietary software like music players, text editors, web browsers, etc. for FOSS ones.
Personally, I ended up enjoying the free and open source software alternatives more than what I was initially using. 
In the end, you as a user have more control over the software. Using freedom/privacy respecting software when and where possible is the best thing you can do, but of course it is ultimately your choice to use proprietary software (that is all part of freedom, however in no way are you free to do what you want with that software - the developer has the control). I still use a handful of proprietary programs/software, even the graphics drivers I use are proprietary. As much as I push for free software, I also tend to have a pragmatic perspective on things, therefore I'm willing to compromise where I see fit (of course, until there are better FOSS alternatives for said software/drivers).

I've only been using GNU/Linux as my daily driver for just under a year, and Arch for about 5 months. By my third month of using Arch, I wrote [a script that replicates my setup](https://whitevhs.xyz/kaarbs), with all my packages+configs included. It's very handy :)

I feel within that year, I've learned a lot about software in general, and the bigger picture of how important it is in our lives, what role it plays and how we as people need to be much more mindful of it. I've also learned about the importance of free software, specifically in sectors like government, schools, healthcare, etc. Even things in the majority of peoples daily lives like communications; these services we depend on tremendously, and for them to be run on proprietary software/services is, in a way, doing a disservice to the very people it's serving. We need free software to be prioritized ESPECIALLY in those high-profile sectors. That's a whole other conversation though.

When you take the time to learn about GNU/Linux, it can truly be eye-opening in many ways. This is just the beginning of my "Linux Journey", and I am excited to see where I will end up next.

-H
