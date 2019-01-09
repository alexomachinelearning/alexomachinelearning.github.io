---
layout: post
title: "A Little on Early History in Machine Learning"
date:   2019-01-05 12:00:00 -0800
redirect_from:
  - /2019-01-05-a-little-on-early-history-in-machine-learning.html
---

I read this quote in ["Marvin Minsky's Vision of the Future"](https://www.newyorker.com/magazine/1981/12/14/a-i) by Jeremy Bernstein (1981) in _The New Yorker_:

> Rosenblatt, who was a pioneer in artificial intelligence, became a researcher at the Cornell Aeronautical Laboratory, where he invented what was called the Perceptron. In the early nineteen-sixties, the Perceptron became the prototypical artificial-intelligence machine for a generation of young computer scientists.

I like the quote because it catches light at multiple angles regarding some of the people, places, and things that were important to that machine learning era.

## People
**First**, the enduring legacy of early researchers like Frank Rosenblatt, whose work Bernstein goes on to describe as he interviews Minsky in the article. (Minsky was another important figure in early machine learning and artificial intelligence throughout the 1960s and 1970s, hence the interview in 1981).

## Places
**Second**, where and how much history was made in those key early years. Bernstein's article tells us that 1959 saw the invention of Rosenblatt's perceptron prototype, and [Wikipedia tells us](https://en.wikipedia.org/wiki/Machine_learning#History_and_relationships_to_other_fields) that the phrase _machine learning_ was created that same year by then-IBMer and computer science giant Arthur Samuel.

Why _then_, why 1959?

The same wiki has this to say:

> Machine learning grew out of the quest for artificial intelligence...in the early days of AI as an academic discipline, some researchers were interested in having machines learn from data.

So computing companies like IBM and research universities like Cornell were incentivized by the market and academic forces of the time to contribute important work to that quest, and they contributed greatly to applied research and development whose output we now enjoy in our email applications, voice assistants, and self-driving vehicles.

You might note a small discrepancy between the fact that the perceptron prototype was _created_ in 1959 and the description in the quote above that "the Perceptron _became_ the prototypical artificial intelligence machine [in the 1960s]". That's just because of timing and probably the fact that it takes a few years for a new academic advancement to make it into academic circles, journals, and so on. Here's [Alpaydin](https://mitpress.mit.edu/contributors/ethem-alpaydin) (p. 86) on when Rosenblatt's perceptron started to make its presence known:

> "In the 1960s, the perceptron model was proposed as a model for pattern recognition (Rosenblatt 1962)...[as] a network composed of artificial neurons and synaptic connections, where each neuron has an activation value, and a connection from neuron A to neuron B has a weight that defines the effect of A on B."

## And Things
**Third**, how consequential the creation of the perceptron, and the perceptron as a thing itself (as a neural network proper) was for the machine learning field. I mentioned in ["Buckets of Concepts About Learning Machines"](https://ahumanlearningmachinelearning.com/2019/01/04/buckets-of-concepts-about-learning-machines.html) that the perceptron was the first and simplest neural network. Ironically, being first and being simple doesn't always turn out to be simple. A variety of resources I've come across describing the perceptron allude to what is a tragic mix of complexity and confusion: the complexity and confusion that sometimes comes with being the first thing of its class. To appreciate what I mean, you can view and read [Professor Geoffrey Hinton's perceptron lecture](https://www.youtube.com/watch?v=YRMvQuutgS8&list=PLoRl3Ht4JOcdU872GhiYWf6jwrk_SNhz9&index=8&t=0s), [Bernstein's Minsky interview](https://www.newyorker.com/magazine/1981/12/14/a-i), and [Chapter 4 of Ethem Alpaydin's book](https://mitpress.mit.edu/contributors/ethem-alpaydin). (Essentially, a widespread misunderstanding and attendant academic overcorrection in the 1970s appears to have pressed a 10-year pause button on R&D in machine learning neural networks. See _backpropagation_ on p. 92 of Alpaydin's book to see what unpaused it).

That notwithstanding, the rich world of machine learning received quite the jumpstart with this invention, because if you're using data to teach a learning machine, then you need a physical architecture for that data to pass through, and the perceptron provided such an architecture.

On that note, as I learn more about the important connection between computing database architectures and data structures, I'm going to find it helpful, even necessary, to explore outside of immediate coloring lines. For example, machine learning concepts intersect with concepts in adjacent fields such as _knowledge discovery_. For additional context on these overlaps, see the definitions in Ron Kohavi and Foster Provost's 1998 ["Glossary of Terms: Special Issue on Applications of Machine Learning and the Knowledge Discovery Process"](http://robotics.stanford.edu/~ronnyk/glossary.pdf). The glossary may help me clarify some of my existing confusion around terms like _learning algorithm_ and _learning type_ (per yesterday's article).
