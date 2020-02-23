---
layout: page
title: Projects
permalink: /projects/
---
Most of these aren't nearly as fleshed-out as I would like them to be, but I figured someone might find something interesting. Right now I'm starting work on something more serious that I hope can be published here in the coming months.

## [Prime](https://github.com/jack-the-coder/prime)
![cool pattern](https://raw.githubusercontent.com/jack-the-coder/prime/master/4321.png)
This mini-project arose from my interest in finding out if there was any pattern to the modulus of prime numbers. The program makes a simple square image where large rectangles (bigger than a single pixel) are centered over a pixel whose number (starting at the top-left corner) is prime. Since the process wraps around each row of the image, you can see some interesting patterns occur. In that repository, I have a few images that highlight the effect and a shell script to run the program many times, making images from 1x1 to a specified size.

**Technologies**: C, Cairo

## [Cryptux](https://github.com/jack-the-coder/cryptux)
Writing a real encrypted messaging application is a lot of work, both from a cryptography standpoint and a software engineering standpoint. Cryptux implements a simple messaging application in under 200 lines of code, meaning that I had to take a few shortcuts and break a few best practices (client polls server every 1/10 seconds, server only stores last message). While that means it won't scale, Cryptux was a satisfyingly quick project that highlights how simple crypto is to work with in Go. 

**Technologies**: Go

## [GoCraft](https://github.com/jack-the-coder/gocraft)
![Screenshot](https://camo.githubusercontent.com/99ba6331786b8ff415f904861ed72b1237f6555d/68747470733a2f2f692e696d6775722e636f6d2f767247524467312e706e67)
I wanted to play with terrain generation algorithms, so I forked a nice little Minecraft clone written in Go and messed with the terrain generator. If I had more time to spend on this project, I would have added a couple more realistic terrain options. I ran into limitations pretty quickly with the fact that the project I forked uses 2D chunks (meaning that each chunk of blocks must be loaded from the lowest to the highest point all at once); this meant that I couldn't use any algorithm that generated particularly tall or deep underground terrain features. 

**Technologies**: Go, OpenGL

## [Feeder](https://github.com/jack-the-coder/feeder)
This project makes and formats a nice PDF with the day's headlines, ready to be printed. I briefly had a setup where it would print the news every morning, but that wastes a lot of paper. 

**Technologies**: Python, LaTeX

## [soundSynth](https://github.com/jack-the-coder/soundSynth)
I built a capacitive-touch-based piano keyboard with strips of conductive tape on cardboard back in the summer of 2017. Unfortunately I don't have any photos of the working device, but I do have the code for it. You can probably find better code to do the same thing from one of those "banana keyboard" projects if you're interested in building one. 

**Technologies**: C++, Arduino, an entire rat's nest of wires

## [mango-melon](https://github.com/jack-the-coder/mango-melon)
This was a half-finished attempt at a social network. My [friend's version](https://github.com/thunderdynamics/tdic) was much better. I would not suggest doing anything with either of these except as a historical artifact, but they were satisfying to make. 

**Technologies**: Python, Flask

## [pmm-old](https://github.com/jack-the-coder/pmm-old)
Before the new version of Project Mango Melon (see above), this was the original image-sharing social network. It never really worked, but I was pretty proud of it at the time. 

**Technologies**: Python, Flask

---

That's the beginning of time, at least from the perspective of all the programming projects I've worked on. I've grown and improved a lot since those first couple of lines of code back in 2014 or 2015, so it's fun to occasionally go back through the archives and see how much better my current code looks. 