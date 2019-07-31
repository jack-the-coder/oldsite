---
layout: post
title:  "The perfect language (and why Go still isn't it)"
date:   2019-07-31 15:52:57 -0500
categories: programming
---

The evolution of many a programming language seems to follow a set trajectory: 

1. The language starts small. It's supposed to be simple, hoping to fix issues in previous similar languages. It probably has poor tooling (such as debuggers) and limited abstraction power (but maybe with plans to improve it in the future). 
2. The creators implement more of the basic features needed for it to compete. Focus is on on the standard library and on getting developers to choose it. The language receives relatively wide adoption, especially since some "cool" projects are written in it.
3. Programmers from other more established languages find that something that would be simple in their language is difficult in the new language. 
4. Implementors of the new language say that that feature is too complex and cannot be integrated cleanly. 
5. The community backs up the implementors, sometimes even saying that the feature is "not good enough" or "not ready" for their language. 
6. Implementors realize that the feature is needed and implement it in a slightly different way, making it sound like it is unique and has always been on the roadmap. 
7. Some community members still think it's a bad idea. "It's no longer a simple language," they cry. 
8. Steps 3 through 7 continue with features of varying degrees of controversy. The language gets more and more like the others that have come before it, no longer simple enough for a brand-new programmer to wrap their head around. 
9. A new programming language comes along, saying that it will be simpler than the last one. 

Now, it's obvious that I'm talking about Go here. It's the most famous example of being stuck in a hamster wheel of slowly bolting on features that other languages have had for years. 

Regardless of what you think of Go (in fact, I quite like it for many applications, since it has a great ecosystem and standard library), I think we can agree that this kind of evolutionary path is a dangerous one. While it pretends to selectively allow new features into the language and practice good taste by not bolting on every new idea in computer science, it leads to a language that has intentionally stuck its head in the sand with regards to ideas that have proven themselves useful elsewhere. 

## Searching for perfection
Given that this is not the way to go about creating the ultimate programming language, what is? In my opinion, there's three fundamental tenets of a language that must be held in balance for it to be maximally useful in as wide an array of situations as possible: 

- Size. A small language with as few gotchas and corner cases as possible is preferable. A small language increases the odds that it is consistent throughout. Of course, the language must contain enough substance to be as useful as possible. 
- Power to create abstractions. Being able to write code at the level of your problem domain makes adding new features to your program a breeze. At the same time, the language must avoid making it too easy to "silo" into a custom DSL that other programmers must learn to work on your program. 
- Good tooling. This includes a good debugger (bonus points for what Common Lisp does by not unwinding the stack!), interoperation with editors to allow interactive programming, dependency management, build tools, and everything else outside of the language that makes writing software comfortable. 

So far I simply haven't seen a language that keeps everything in balance. Common Lisp's "silo" problem can make it difficult to write code that interoperates with other code and larger teams, as well as to create a community like there is with less "powerful" languages. CL is also huge and inconsistent, due to its design-by-committee nature and the incompatible Lisps it was intended to unify. At the same time, the tooling is really good, even including ideas that are practically unseen in mainstream languages. 

It could be that it's impossible to find an optimal balance between abstraction-ness and the removal of footguns. Go was specifically intended so that it scales to large teams of Google programmers; the language imposed many decisions upon  them to avoid making too many choices that would lead to incompatibility. Outside of Google, this strategy worked, in that it lead to a plethora of compatible libraries for every need. All Go code looked the same and followed the same general semantics. 

Scheme seems to be an interesting compromise. Within an implementation, there's usually only one "correct" way to do something. The entire community for a Scheme implementation rallies behind a single web framework, for instance, instead of eight half-complete, undocumented libraries (like you might see in CL). At the same time, Scheme is not very popular, and it doesn't help that incompatible implementations fragment the ecosystem. 

## The best we have
We're not going to get a "perfect" programming language anytime soon. However, I'd like to see a language with the following features, which I think ensure a vibrant future:

- Some kind of BDFL, whether that be a corporation or an individual. Without a singular focus, the language would turn right into the next C++ or CL: huge and with many incompatible programming styles. We don't want to have a *Your Language: The Good Parts* book published, if it can be avoided. 
- A small core and powerful abstractions. 
- A rich standard library, full of well-maintained, "blessed" options for writing a variety of kinds of programs. This has proved to be important to Go's success (especially `net/http`). While Python does come with a large standard library, its "batteries have been leaking" recently as parts of the stdlib have been unmaintained. The inclusion of some kind of Web framework (similar to `net/http` in scale and simplicity) and image processing in the standard library would help with initial adoption. 
- Really good tooling from the start. Go didn't have much in the way of debugging until Delve matured, and this certainly made for a tough sell compared to Java for other large companies. IDE support has also been relatively recent. 

---

Whether or not it's possible to keep everything above in equilibrium, I think a language built on those principles would be better than pretty much all that we have today. If you have any suggestions for more criteria to add to the list, please let me know!

Are you aware of any language that has sidestepped the issues I highlighted above? I'd be happy to hear about it.
