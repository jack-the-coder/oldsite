---
layout: post
title:  "PSA: GNOME Boxes works much better than VirtualBox for Windows VMs on Linux"
date:   2020-02-09 15:52:57 -0500
categories: programming
---
Windows software is so prevalent that it's practically impossible to avoid running it in some way. Luckily, virtual machines let you run the occasional .EXE on an isolated system without dual-booting. The go-to free virtual machine program for years has been VirtualBox, but after having it screw up my Arch Linux system and trying out GNOME Boxes on Fedora, I can wholeheartedly recommend that everyone who's currently using VirtualBox to run Windows switch to Boxes. 

## VirtualBox requires you to manually go through the install process
I wasn't even aware that it was possible to completely skip entering all of the information into the installer ISO or the user account setup screens until I saw that Boxes lets you type a username, password, and product key in the initial setup wizard. Since I'm not going to pay for a Windows license to use a virtual machine for three hours a month, I just used the default Windows 10 Pro product key (`VK7JG-NPHTM-C97JM-9MPGT-3V66T`), which sets the system up without activating Windows. It's nice to be able to hit the start button and grab a drink of water and come back to a completed installation. 

## GNOME Boxes is far more integrated
Having to install a kernel module for VirtualBox is a somewhat annoying consequence of it being cross-platform. Boxes can get away with using libvirt and so it works immediately without loading anything into the kernel. Once you install the SPICE guest tools on the Windows side, the size of the virtual machine's screen is set to perfectly fill the window (no need to scroll, zoom, or have huge black borders). VirtualBox also uses Qt instead of GTK; that doesn't matter a ton but it means that Boxes looks a lot nicer and fits in better with the rest of the system. 

All in all, I quite like the way that GNOME Boxes looks and feels on a system using the GNOME desktop environment, but it even looks and feels much nicer than VirtualBox on tiling window managers like Sway. If you want some more power-user functionality, virt-manager is similar to GNOME Boxes (also developed by Red Hat) and uses the same technologies under the hood. 

## Boxes doesn't freeze up all the time and require a reboot of the host system
I'm not sure if this issue had to do with my specific Arch setup (I used the Sway window manager), but as soon as I started using the graphics driver included with the VirtualBox Guest Additions image, the Windows guest would freeze up every few minutes after I started using it. At first, I could quickly switch to a virtual terminal and issue a quick `pkill vbox && pkill virtual` or even `pkill -u jack` to completely log myself out. If the freeze occurred when I wasn't paying attention, however, I would soon find that a hard reboot was the only way to get back to a functioning system. When my web browser would stop receiving input from my keyboard every few minutes and require me to restart it, even when I wasn't using VirtualBox, I knew that it was time to either restore from a backup from before installing it or do a full reinstall. Since my important user data is transferable between distributions, I decided this would be a good opportunity to try Fedora again. 

Even if you've never had issues with VirtualBox freezing on you, maybe the smooth UI and convenient time-saving features of Boxes might entice you to give it a try? 