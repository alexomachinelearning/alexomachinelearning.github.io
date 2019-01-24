---
layout: post
title: "My In-Depth Introduction to Deep Learning Basics (Part 3)"
date:   2019-01-23 12:00:00 -0800

---
The final 30 [slides](https://www.dropbox.com/s/c0g3sc1shi63x3q/deep_learning_basics.pdf?dl=0) from the first lecture in the Spring 2019 session of MIT's _6.S094: Deep Learning for Self-Driving Cars_ covers topics I know the least about. As a result, I'll have less prior-based commentary to share than I did yesterday in ["My In-Depth Introduction to Deep Learning Basics (Part 2)"](https://ahumanlearningmachinelearning.com/2019/01/22/my-in-depth-introduction-to-deep-learning-part-2/)—and more questions.

## My Slide Down Deep Learning Basics Concludes

- **S38**: when does it make sense to use the Sigmoid vs Tanh vs ReLU activation function?
- **S40**: since the learning rate is described here as the "fraction of the weight's gradient [that] is subtracted from the weight", then what sorts of things lead to bigger fractions being found as quickly as possible? Are there any types of learning for which it's, counterintuitively, advantageous to have a slower learning rate with many small fractions being subtracted, even though the option would otherwise exist to subtract a few very large fractions?
- **S47**: this one's making me wonder how often nodes fail and why they do; what's the minimum level of node redundancy needed to ensure the network reliably outputs its predictions?
- **S49**: all of these seem to relate, but as this stuff is all beyond my current knowledge horizon, I'm not sure exactly how: normalization and its relationship with mini-batch size (S49); the relationship between weight penalty / weight decay and error derivatives + overfitting (S48); early stoppage as a technique to (seemingly) deal with big deviations between validation sets and test sets (S47); and the problem of overfitting with respect to small sets of data (S44). If there's one thing I've learned from studying other aspects of computer science, it's that every solution design involves compromises, and getting technology to work often comes down to picking the combination of complementary approaches that leads to the fewest possible number of downsides. There's something of that theme in the last few slides, if I'm reading them accurately
- **S50**: TensorFlow's ["Neural Network Playground"](https://playground.tensorflow.org) looks great. The major categories of levers you can control include which training dataset to use; the ratio of training to test data (how does one _evaluate_ how to decide this?); the amount of noise (is noise used primarily for the input layer? See the Note in S47); the batch size (which appears to have a hard cap of 30); which properties to feed (from _x<sub>1</sub>_ to _sin(x<sub>2</sub>)_); the number of hidden layers (up to 6); and the number of neurons in each hidden layer (up to 8). The learning rate, type of activation, regularization, rate of regularization, and problem type (e.g. regression vs classification) are also adjustable. All told, there are nearly 100 options among everything I've just listed. I'll have to go experiment with this Playground sometime, while incorporating concepts and comments from the aforementioned lecture slides to see how all of these choices and compromises come together

In the final 19 slides, I felt wowed many times, at once by the range of neural networks, the complexity of their architectural designs, and the realization that, when you zoom out to the level of real-world use cases, there is so much math and statistics and code going on in the back-end in order to manifest the experience of the software working as intended on the front-end, and of making high-quality predictions suited to the task it was trained on. It's pretty mind-blogging.

The last image in the slideshow, which is [Simon Wardley's "Three Stages of Expertise"](https://blog.gardeviance.org/2008/04/three-stages-of-expertise.html), is a perfect way to end (albeit noting that Wardley intended the image to be "a joke" rather than a demonstration of truth). As with blockchains and decentralized systems, machine learning is yet another computer science space for which there appears to be forevermore a much greater amount of knowledge to learn than can possibly be learned by any one individual, thereby reminding us of the power of communities and of the necessity of collaboration.

---


This concludes my three-day summary of what I learned, asked, and remembered as I read through Lex Fridman's 2019 lecture slides for "Deep Learning Basics".
