---
layout: post
title: "Learning to Read Code"
date:   2019-02-08 12:00:00 -0800

---
One of the joys of learning is discovering treasures of knowledge that are too difficult for you to consume today, then setting them aside for tomorrow when it becomes possible to understand them.

Recently, I've started trying to read code. My first major attempt involved the source code for the cryptographic algorithm DES, in C. C is not a programming language I have any familiarity with; in fact, as I just recently started learning Python in earnest, I'm mostly unfamiliar with programming languages in general. But by the time I attempted this task of reading DES code, I had already read just enough about block ciphers and symmetric encryption in the primary DES section of [Bruce Schneier's "Applied Cryptography"](https://www.schneier.com/books/applied_cryptography/) that I could try to follow the corresponding DES code in the Source Code section of the book. When I did, it was very difficult, and I had many more questions than answers, with a total comprehension rate of less than 10%.

But if I scan the code again now, I can make out a few new markers on the trail:

- statements within curly braces, maybe code blocks
- keywords, maybe, for declaring, maybe, functions
- numbers inside brackets, maybe indices
- assignments of what might be lists, within what might be arrays
- instructions to, maybe, increment values by 1

These I surmise because earlier today I read through a chapter on "Basic JavaScript Instructions" in [Jon Duckett's "JavaScript & JQuery"](http://javascriptbook.com/). The chapter introduced me to the syntax and function of things like statements, code blocks, keywords, variables, arrays, and more. All very, very basic things, but I noticed that they reminded me of aspects of Python that I'm learning about elsewhere but have not yet been presented in the same way as their counterparts in JavaScript in Duckett's book. In turn, as I scan again the DES source code in C, it's nice to see what appear to be some conceptual and syntactical overlaps. If my conjecture above (which is an in-the-dark attempt at making connections) is accurate, then it's good to see similarities in syntax between the three languages, all of which are still more or less alien to me. And this brings me to the topic of this post, of which not much more remains.

On January 25, I wrote about ["The Most Viewed Machine Learning Video on Youtube"](https://ahumanlearningmachinelearning.com/2019/01/25/the-most-viewed-machine-learning-youtube-video/). In it, I mentioned the source code of SethBling's very cool demonstration of a machine learning program trained to play through a level of Super Mario World on its own. I had tried to read through the source code at the time, and scanning [his code](https://pastebin.com/ZZmSNaHX) now, which is written in the Lua programming language, I can make out what appear as functions; declarations of variables and assignments of values; parameters; and statements. At a glance, Lua appears closer to C in construction, and, upon inspection, it looks as though arrays in both C and Lua are encapsulated by curly brackets rather than square brackets, as they are in JavaScript. It's useful to conjecture at comparisons and contrasts among these languages in order to extract patterns.

My goal is to be able to read machine learning code written in Python for libraries and APIs such as TensorFlow and PyTorch within a few months. Exercises like this make it more fun to look at things I don't yet understand that will later become legible as my knowledge grows.
