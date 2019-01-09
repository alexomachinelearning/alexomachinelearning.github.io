---
layout: post
title: "Buckets of Concepts About Learning Machines"
date:   2019-01-04 12:00:00 -0800
redirect_from:
  - /2019-01-04-buckets-of-concepts-about-learning-machines.html
---

Figuring out how to sort new knowledge is part of the process of discovery and learning. When you encounter new things, your brain needs a place to sort them into. By analogy, knowing the separation between a person, place, or thing allows you to make sense of new information you encounter regarding people, locations, and objects as you move through the world. It's a process of encountering and sorting, sorting and encountering, in a cycle. But when you're starting out in an entirely new field of knowledge, you won't have either the buckets or the knowledge. But we need structure in order to learn.

From what I've read, the basic ingredients of a learning machine appear to include a set of data, a learning model, a learning algorithm, a learning type, and a neural network:

- data
- learning model
- learning algorithm
- learning type
- neural network

## First, What Do We Mean By a Machine?

Before I attempt to summarize the definitions of these buckets, let's first think about the concept of __a machine__. What is it? What isn't it? I've read a little bit about Turing machines in my other learning journeys with blockchain and cryptography, but I don't have a solid understanding of Turing machines in my long-term working memory yet. Outside of computing, the concept of machines is much broader, but I don't fancy a glance at the history of machines right now either. Typically, when I think of a machine, I think of a physical, robotic object doing things for people, such as manufacturing vehicles inside a factory or vacuuming an apartment with your assistance (or, increasingly, on its own). But what of the machines in our pockets?

I don't normally think of my iPhone as a machine, but it is. Or, rather, it's a machine of machines, because even though an iPhone isn't useful without its physical hardware, what an iPhone is, in the ways we functionally interact with it, is a bunch of software. We enjoy and value and use the device because of the software that it runs. The software *is* the machine.

From what I've gathered, "machine learning" is a phrase that refers primarily to software: software trained in particular ways to do particular things and make predictions of particular sorts. Later, that software is used by hulks of metal (like Teslas), small hunks of plastic (like Alexas), and a growing number of physical interfaces to applications. Thus, from now on, when you read "machine" in this article, think of software.

## Basic Buckets

Now for summaries.

__Data__ refers to the information used to train a learning model, i.e., to teach its neural networks to make predictions. I'll write about the training process and neural networks once I learn more about them.

The __learning model__ has to do with what type of prediction the machine will be making. Amazon has a good primer on different [learning models][1]. For example, _binary classification_ learning models predict if something belongs in one of two classes (categories) and can also be used for making predictions on a yes-or-no question, hence the word "binary", meaning "two". If the response the machine will give includes more than two possibilities, then you select a _multiclass classification_ learning model. For a prediction involving a numerical value, you select a (linear?) _regression_ learning model.

According to [Alpaydin][2] (p.36), "one of the most critical points in learning is the _model_ that defines the template of relationship between the inputs and the outputs". From this, I'm not sure if inputs refer to input cells in neural networks only, or also to input in the form of the training data used for the model. Similarly, I'm not sure if the outputs here refer to the output cells in a neural network or also to the answer provided by the learning machine based on the probabilistic prediction it has made. I'll have to re-watch [3Blue1Brown's video][3] on neural networks to become clearer on the relationship between learning models and the neural networks used to train them. But these resources do clearly suggest that once you know what problem you wish to solve, it becomes very important to select a learning model suited to that sort of problem.

On the __learning algorithm__, I've hit a wall. It refers to the type of mathematical transformation used to train a learning model as you expose it to the training data, *I thought initially*. But this doesn't seem to be the right way to think about them. For example, the _multinomial logistic regression_ used as the learning algorithm in [AWS Machine Learning's multiclass classification learning models][1] is described [in Wikipedia](https://en.wikipedia.org/wiki/Multinomial_logistic_regression) as a statistical classification method, not as a mathematical transformation, function, protocol, or decision-making process. So perhaps the word _algorithm_ in the context of machine learning is used differently than in applied cryptography or in non-statistical math; perhaps it doesn't refer to a step-wise transformation of stuff. Yet [Alpaydin][2] (p.16) does have this to say:

> "To solve a problem on a computer, we need an algorithm. An _algorithm_ is a sequence of instructions that are carried out to transform the input to the output."

Confusion is an important part of the learning process, and I am definitely confused—this is useful, as it suggests a major gap for me to fill. This is one of the buckets in which I should concentrate more of my time relative to others.

The __learning type__ is an approach to how the learning models and neural networks are trained, i.e., how the accuracy of the learning models come to improve over time so that the learning machine outputs better predictions. The three major learning types I've encountered are _supervised learning_, _unsupervised learning_, and _reinforcement learning_. Different learning models, learning algorithms, and neural networks appear to be able to be used with one or more of these learning types, depending on a variety of factors. However, I'm still fuzzy on how to conceptualize learning type: is it an approach to...machine learning? An area of...machine learning? A type of...machine learning? I've encountered all of them and don't yet know if these nouns can be used interchangeably or if a better descriptive concept exists. For now, I know that machine learning can be done in a variety of ways, using one or more learning types.

A __neural network__ is a specific computing architecture through which to pass training data (or real data, after the learning model has been trained to make predictions). Like there are many algorithms, there are also many neural networks. The first and simplest is the _perceptron_, with the more advanced _multi-layer perceptron_ being the neural network of focus in the above-referenced [3Blue1Brown video][3]. There is also a humorously-titled, visual, and informative [article by Sagar Sharma at _Towards Data Science_](https://towardsdatascience.com/what-the-hell-is-perceptron-626217814f53) on perceptrons and how they work. And as I've listed in [Resources for the Newcomer to Machine Learning](https://ahumanlearningmachinelearning.com/2019/01/02/resources-for-the-newcomer-to-machine-learning.html), the Asimov Institute has an excellent set of articles visualizing and describing various neural network architectures. Do note that diagrams of neural networks are simplified versions of actual neural network architectures, which can include hundreds of neurons ("cells").

Even though I have less confusion here, neural networks may become one of my main areas of fascination due to my background in neuroscience and my interest in distributed and decentralized computing. The subject of which neural networks are optimal for different types of data, different problems to solve, different computers of varying computational strength, different libraries built with different programming languages or working with different operating systems, and different learning models, algorithms, and types could keep one busy for a long time. As I eventually wish to use this space is a playground to build neural networks of my own, I look forward to learning a great deal about neural networks.


[1]: https://docs.aws.amazon.com/machine-learning/latest/dg/types-of-ml-models.html "Link to Types of ML Models"

[2]: https://mitpress.mit.edu/contributors/ethem-alpaydin "Machine Learning"

[3]: https://www.youtube.com/watch?v=aircAruvnKk "But what is a Neural Network?"
