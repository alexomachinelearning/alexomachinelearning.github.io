---
layout: post
title: "The Most Viewed Machine Learning Video on Youtube"
date:   2019-01-25 12:00:00 -0800
redirect_from:
  - /%0A.md/2019/01/25/the-most-viewed-machine-learning-youtube-video/

---
Super Mario Brothers was a great game. It's also (pleasantly) featured in the most popular machine learning video on Youtube, by view count: [_MarI/O - Machine Learning for Video Games_](https://www.youtube.com/watch?v=qv6UVOQ0F44). The creator is Seth Bling, a software developer who wrote the demo software called "MarI/O" in the Lua programming language. He trained neural networks to learn how to play the game level, "Donut Plains 1".

As Bling explains in the video, the software learns to play completely from scratch. It appears that a random neural network is created to mathematically model how Mario's movements advance him through the level (using the BizHawk emulator) and predict the best buttons to press to get Mario to move towards the end of the level. The level's "playing field" is represented by white blocks and objects such as enemies and power-ups are represented by black blocks, which is how the software "sees" the Donut Plains 1 course.

The neural networks have eight output units, corresponding to the four directions of the SNES controller (up, down, left, and right) and the four buttons "A", "B", "X", and "Y". As can be seen in the video, as the software simulates the pushing of those buttons, Mario's character moves on-screen. The goal of the software's neural networks is to learn which combination of button "presses" moves Mario forward in the level as quickly as possible.

With each run, a different neural network is generated, based on parameters hardcoded in the software. As you can see [in the source code](https://pastebin.com/ZZmSNaHX), there's a chance for "mutations" that change several aspects of the neural networks, such as the weights and biases. Through randomness and many training sessions, the model optimizes over time. What makes this all possible are ideas from a research paper by UT Austin researchers K. O. Stanley and R. Miikkulainen called ["Evolving Neural Networks through Augmenting Topologies"](http://nn.cs.utexas.edu/downloads/papers/stanley.ec02.pdf) (2002). The paper, which I look forward to reading in depth, outlines how principles of genetics and biological natural selection can be used in computer science to create reinforcement learning neural networks that learn more quickly by passing on, or effectively "transferring", their learning to subsequent generations of neural nets, in a process called [_neuroevolution_](https://en.wikipedia.org/wiki/Neuroevolution). Bling does a good job of explaining the basics in the video, though I'm rusty on my genetics from college and need to return to some concepts to see if they map directly or should be considered loose analogies. I have some old memories from a BIO 160 course on Evolution and Biodiversity and a NEURO 400 course on Senescence that are now percolating as potentially relevant, but I can't quite place their context.

A few of the terms in the source code jumped out at me as familiar given some of the MIT slides I studied in the last few days: _sigmoid function_, *dx*, *dy*, *step sizes*, and of course _links_, _weights_, _biases_, _inputs_, and _outputs_.

Very cool video, and it's not hard to see why it's the most popular machine learning video on Youtube.
