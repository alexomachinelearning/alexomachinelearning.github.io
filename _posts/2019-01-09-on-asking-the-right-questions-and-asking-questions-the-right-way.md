---
layout: post
title: "On Asking the Right Questions and Asking Questions the Right Way"
date:   2019-01-09 12:00:00 -0800

---

Einstein can be said to have been one of humanity's smartest humans. By some approximations, the Earth has carried 100 billion humans (["World population estimates"](https://en.wikipedia.org/wiki/World_population_estimates)). One of my favorite Einstein quotes is [this](https://www.goodreads.com/quotes/60780-if-i-had-an-hour-to-solve-a-problem-i-d):

> “If I had an hour to solve a problem I'd spend 55 minutes thinking about the problem and 5 minutes thinking about solutions.”

Outside of having years of professional training in his trade, something that made Einstein such an effective scientist is that he asked very good questions. The more curiosity a person has, and the more they learn about the world and its mysteries, the better they likely get at asking the right questions and asking questions the right way. This is a skill that, for many reasons, leads to accumulated efficiencies in problem-solving and knowledge acquisition, not the least of which is that the learner becomes deeply engaged with the work in those last figurative five minutes if they spend the first 55 as the architect of their query.

Yesterday, an article on Axios, ["Amazon's new ad strategy: Free samples based on what it knows about you"](https://www.axios.com/amazon-ad-strategy-free-samples-based-on-consumer-data-5ce0fe5b-6112-4d59-8d28-39278f457b6d.html), made the rounds on LinkedIn. The article only mentions _machine learning_ once: "Samples of new products are sent to customers selected using machine learning based on Amazon's data about consumer habits, according to recent job postings and details listed on its site".

Despite it not mentioning which learning models are used for this, we know from Amazon's Machine Learning Developer Guide that **multiclass classification** machine learning models can be trained to make predictions with multiple (> 2) possible choices. One example question given is, "Which category of products is most interesting to this customer?" (["Types of ML Models"](https://docs.aws.amazon.com/machine-learning/latest/dg/types-of-ml-models.html)). And this brings me to the topic of today's post.

## A Really Good Question

There's a consequential difference between the following questions:

1. Is Alex likely to enjoy Starbucks coffee: yes or no?
2. Which three of the following four items is Alex likeliest to enjoy: Salt and Straw ice cream, Starbucks coffee, _The Hitchhiker's Guide to the Galaxy_, and _Of Mice and Men_?
3. What is the numerical probability that Alex would enjoy a free sample of Starbucks coffee?

The combination of learning models, learning algorithms, neural networks, and training types used to arrive at such predictions will change depending on how you ask the question, as may what training data you provide. And that's really very interesting. Because asking a good question, and asking a good question in a manner optimized for the kind of learning that needs to happen in order to make a prediction on the response, is important in human decision-making as well as in machine learning inferencing.

If Amazon is using multiclass classification (and possibly other) learning models to predict which free items to send consumers, then I wonder what sorts of questions they're asking and what sorts of answers they hope to get about consumer purchasing behaviors—and to what they'll apply those answers once they get them.
