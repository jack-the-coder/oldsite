---
layout: post
title:  "Make Emacs Cool Again"
date:   2019-07-26 15:52:57 -0500
categories: emacs
---

**FIX DATE BEFORE PUBLISHING**

Emacs has something that no other programming environment has on a modern computer: the ability to modify the running editor in real-time. While applications like Visual Studio Code technically support similar techniques, in practice the process of writing a VS Code extension is much more complicated and time-consuming than opening the scratch buffer and evaluating an S-expression. This is where the fundamental divide comes in between Emacs and everything else: the ease of temporary modification. If I want to make a repeated edit across a buffer, I can start a keyboard macro. After realizing that I need to perform it more than once, I can turn it into a piece of Emacs Lisp code and assign it a keybinding. Before long, it might be a part of my init file, so that it over time becomes part of my day-to-day editing experience. 

In practice, however, new users to Emacs feel that the editor is miles behind everything they've used before. If they try vanilla Emacs, the keybindings and terminology provides a hump on the learning curve that might not be worth ascending. If they try a pre-made configuration like Spacemacs, it won't be long until they notice that the entire thing is a great big ball of hacks glued on top of one another. In an attempt to use Vim keybindings wherever possible, Spacemacs pastes another layer of complexity over existing packages, making it so that the official documentation for a package (like Org mode or Magit) uses completely different keybindings than the ones enabled for the Spacemacs layer. 

Therein lies the problem. While a single global namespace for everything means that adding a new feature to the running editor takes a few seconds, other people's packages clash with one another in difficult-to-predict ways, leading to instability and an overall lack of cohesiveness. 

## The age-old question
In reality, this issue has nothing to do with Emacs. It's a war that's been fought many times throughout computing history. 