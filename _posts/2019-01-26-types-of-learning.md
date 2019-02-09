---
layout: post
title: "Types of Learning"
date:   2019-01-26 12:00:00 -0800
redirect_from:
  - /%0A.md/2019/01/26/types-of-learning/
---
Tonight, I decided to spend some time learning a little more about various learning types: supervised learning, augmented supervised learning, semi-supervised learning, reinforcement learning, and supervised learning.

My resources were:

1) Slide 23 in Lex Fridman's Spring 2019 MIT Deep Learning Course, [Lecture 1](https://www.dropbox.com/s/c0g3sc1shi63x3q/deep_learning_basics.pdf?dl=0#)

2) Part 1 of Adam Geitgey's article, ["Machine Learning Is Fun"](https://medium.com/@ageitgey/machine-learning-is-fun-80ea3ec3c471)

3) The _Approaches_ section of ["Machine Learning"](https://en.wikipedia.org/wiki/Machine_learning#Algorithm_types) on Wikipedia

I picked up a few more shelves:

* _Supervised learning_ is the only learning type in which 100% of the learning model's learning is guided by a person. By "learning", it's meant how the computer comes to figure out which mathematical model and what mathematical relationship describes the data (if there is a valid relationship that can be described). I like Geitgey's intuitive example of arithmetic equations that are missing the operators: say, "2 4 = 6". You give the computer the input numbers ("2" and "4"), you give it the output answer ("6"), and the work of the computer is to deduce that the correct operation is addition ("+"). The math, statistics, and programming required to get it to do so is complicated, but the general concept of what the computer is trying to do is straightforward. I also learned that a Support Vector Machine (SVM) is a (or _the_) sub-type of supervised learning used to classify material into one of two categories

* I need to learn much more about _Augmented Supervised Learning_ and _Semi-Supervised Learning_, as currently all I see, from Fridman's slide, is a difference in how much or little human involvement is required to train the model (that is, how many of the 'correct answers' are provided to the computer with the training data)

* _Reinforcement learning_, per the Wikipedia article, is suited to situations in which an exact mathematical model is not already known (in which case it would make sense to have _some_ involvement by a person during training, per Fridman's slide, because presumably _something_ of the mathematical model is known, albeit it being inexact). Here, the process by which the software improves its predictive accuracy is reinforced by a feedback loop in which "software agents...take actions in an environment so as to maximize some notion of cumulative reward." The language there seems very specific, so I'll need to learn more about agents and rewards in this context

* _Unsupervised learning_ is the only learning type in which the learning model appears to be completely 'on its own'. That is, it isn't provided any results, ["only inputs"](https://en.wikipedia.org/wiki/Machine_learning#Unsupervised_learning). The data appears to be unstructured as well, and the computer learns to identity patterns in the structure, to make sense of the data. Something here gives me an itch regarding my question of how data stored in future blockchains and other directed acyclic graph databases be analyzed.

So much to learn.
