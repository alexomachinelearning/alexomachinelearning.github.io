---
layout: post
title: "My Introduction to TensorFlow (Part I)"
date:   2019-02-25 12:00:00 -0800

---
Google's Martin Gorner gave a lecture at Devoxx 2016 called ["Tensorflow and Deep Learning - Without a PhD"](https://www.youtube.com/watch?v=vq2nnJ4g6N0). I'm about 20% through it. A few favorites so far:

- The video clarifies for me the value of training data and its relationship to test data, and why it's important to keep tabs on the _variables_ (weights and biases) during training iterations to ensure _convergence_ takes place; it's helpful to consider that _supervised learning_ might be about more than just supplying correct values for training data. It also is about keeping an eye on the results of the training sessions to ensure that they proceed in an effective way and produce reasonably accurate results
- Gorner mentions that humans are very good at calculating gradients (i.e., at knowing which way "down" is in physical dimensional space). Useful analogy for understanding _stochastic gradient descent_ and _loss functions_, which I'm still having a hard time with
- TensorFlow's magic comes from its functions (e.g., `tf.library.function()`) generating not a result as such but rather a computation in the form of a "computation graph in memory". Groder explains that this is ideal: since TF is built for distributed computation, you have different computers in a distributed system each performing different computations on different parts of the training data to train the learning model. Thus holding a computation graph in memory is what makes it possible to distribute that workload
- The concept of key-value pairs pops up in a few slides, and some of the Python code in TensorFlow is slowly becoming legible to me :)

To be continued.
