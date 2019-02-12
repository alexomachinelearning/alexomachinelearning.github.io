---
layout: post
title: "Something Brief I Don't Understand about Convolutional Neural Networks"
date:   2019-02-11 12:00:00 -0800

---
Here's something very brief I don't understand about [convolutional neural networks](https://en.wikipedia.org/wiki/Convolutional_neural_network), which are used in deep learning for visual processing. From [Alpaydin](https://mitpress.mit.edu/contributors/ethem-alpaydin), p. 101:

> [...] In such cases, when designing the connections between layers, units are not connected to all of the input units because not all inputs are dependent. Instead, we define units that define a window over the input space and are connected to only a small local subset of the inputs. This decreases the number of connections and therefore the number of parameters to be learned. Such a structure is called a convolutional neural network where the operation of each unit is considered to be a convolution—that is, a matching—of its input with its weight.

Is this design used in order to make CNNs as computationally efficient as possible given our current limits on computing power for model training, or is this approach to network design deliberate, based on observations of how human sight works in nature? A few resources that may help answer this include ["An Intuitive Guide to Convolutional Neural Networks"](https://medium.freecodecamp.org/an-intuitive-guide-to-convolutional-neural-networks-260c2de0a050) by Daphne Cornelisse and the Lex Fridman lectures ["MIT 6.S094: Deep Learning for Human Sensing"](https://www.youtube.com/watch?v=Z2GfE8pLyxc) and ["MIT 6.S094: Computer Vision"](https://www.youtube.com/watch?v=CLOAswsxudo).
