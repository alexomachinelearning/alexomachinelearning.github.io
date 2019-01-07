---
layout: post
title: "Advice on Selecting Programming Languages for Working with Neural Networks"
date:   2019-01-06 12:00:00 -0800
---

One of my long-term goals for this blog is to build neural networks of my own and to share them with the world. I'll start by learning about machine learning, then proceed to deeply inspect how we train learning machines, and then apply that knowledge to build architectures for such learning.

 In anticipation of my "applied machine learning days", one early question I have is about programming languages. (See _Miscellaneous Topics_ in [Resources for the Newcomer to Machine Learning](https://ahumanlearningmachinelearning.com/2019/01/02/resources-for-the-newcomer-to-machine-learning.html) for other early questions).

This morning, I signed up for the MIT machine learning Slack group  [Deep MIT](https://deep-mit-slack.herokuapp.com/), which has been set up in advance of Lex Fridman's upcoming MIT course on deep neural networks for self-driving vehicles. In the Slack group, I asked a new connection of mine, artificial intelligence researcher Mo K., the following questions:

1.  _Would you recommend to someone with no CS [computer science] background or programming experience to focus on learning Python?_
2. _In general, does the choice of programming language constrain one to certain neural network libraries?_
3. _Should language selection instead be done by evaluating which types of neural networks you wish to build (e.g., DNN [deep neural networks] vs non-DNN), and then selecting a language known to have strong libraries for that type of network?_

Mo generously supplied helpful responses that I'll summarize and extend below.

## Awesome Advice from Awesome Human Mo K.

The following advice was provided and includes additional content I found when exploring his suggestions.

> 1.  _Would you recommend to someone with no CS [computer science] background or programming experience to focus on learning Python?_

Certain machine learning tools, such as [Orange](https://orange.biolab.si/) and [AutoML](https://www.automl.org/automl/), do have graphical user interfaces to perform [visual programming](https://en.wikipedia.org/wiki/Visual_programming_language), or feature tools that automate the process of creating or working with neural networks. However, to work with certain learning models or participate in certain areas of machine learning research, one should be comfortable coding. That said, languages such as Python are relatively easy to learn, and coding for machine learning won't require the same depth of familiarity with the language and its uses as might be required when using Python for general computer science programming.

> 2. _In general, does the choice of programming language constrain one to certain neural network libraries?_

This could be said to be the case, i.e., it's possible that for some libraries, one might need to learn a library-specific language. A language like Python, however, works with many frameworks, including the popular Google library [TensorFlow](https://www.tensorflow.org/), Berkeley Vision's deep learning framework [Caffe](http://caffe.berkeleyvision.org/), Francois Chollet's multi-platform library [Keras](https://keras.io/), the deep learning platform [PyTorch](https://pytorch.org/), and many others. Thus learning Python won't be all that constraining, advice echoed previously by others I've spoken to.

> 3. _Should language selection instead be done by evaluating which types of neural networks you wish to build (e.g., DNN [deep neural networks] vs non-DNN), and then selecting a language known to have strong libraries for that type of network?_

Whichever language has the most support for the neural networks you wish to build or type of work you wish to conduct should get consideration. For example, R is a strong choice for solving statistical problems. The deep learning programming library Deeplearning4j (DL4J), which is also a ["computing framework with wide support for deep learning algorithms"](https://en.wikipedia.org/wiki/Deeplearning4j), is written in Java and "works with any JVM language", per the project's website—though it will also work with Python if you're using Keras as an API.

(Side note: for clarification of ideas relating to my article ["Buckets of Concepts About Learning Machines"](https://ahumanlearningmachinelearning.com/2019/01/04/buckets-of-concepts-about-learning-machines.html), see ["Core Concepts in Deeplearning4j"](https://deeplearning4j.org/docs/latest/deeplearning4j-concepts) for a useful description of how to prep data for a learning model, build a neural network, and train the learning model.)

In addition to providing the very wonderful suggestions above, Mo also recommended the following two mega-resources for newcomers:

* ["What are the best ways to pick up Deep Learning skills as an engineer?"](https://www.quora.com/What-are-the-best-ways-to-pick-up-Deep-Learning-skills-as-an-engineer) at _Quora_
* ["Machine Learning Curriculum"](https://github.com/off99555/machine-learning-curriculum) by Chanchana Sornsoontorn (off99555) at _GitHub_

A very special thank you to Mo for the insightful perspective and welcoming spirit. Here's to a great year learning about machine learning.
