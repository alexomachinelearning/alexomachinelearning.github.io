---
layout: post
title: "Bayes' Theorem: P(A|B)=P(B|A)P(A)/P(B)"
date:   2019-01-27 12:00:00 -0800

---
I'm trying to make sense of Bayes' Theorem here. So starts the Wikipedia article on [Bayes' theorem](https://en.wikipedia.org/wiki/Bayes%27_theorem):

> In probability theory and statistics, Bayes' theorem (alternatively Bayes' law or Bayes' rule) describes the probability of an event, based on prior knowledge of conditions that might be related to the event.

A month ago, I learned that the mathematical equivalent of the concept in that sentence is **P(A\|B) = P(B\|A)P(A)/P(B)**. It can be read, per Dan Morris's [_Bayes Thereom: A Visual Introduction for Beginners_](https://www.bayestheorem.net/bayes-theorem-formula/), as _the probability of A being true given that B is true is equal to the probability that B is true given that A is true, multiplied by the probability that A is true, divided by the probability that B is true_.

On the right-hand side of the equation, what we have in the numerator is "the probability that B is true given that A is true, multiplied by the probability that A is true".

Consider the xkcd cartoon, [Seashell](https://xkcd.com/1236/). In the numerator on the right, we have:


> The probability that I picked up a seashell, given that I'm near the ocean, multiplied by the probability that I'm near the ocean.

In the denominator, we have "the probability that B is true":

> The probability that I picked up a seashell.

## Rearranging
If you rearrange the equation for Bayes' thereom such that the denominator is moved the left side, we get "the probability of A being true given that B is true, multiplied by the probability that B is true", and, on the right side, what remains is "the probability that B is true given that A is true, multiplied by the probability that A is true":

**P(A\|B)P(B) = P(B\|A)P(A)**

We could also rearrange Bayes' equation such that the _conditional probabilities_ P(A|B) and P(B|A) are both on the left and the _independent probabilities_ P(A) and P(B) are both on the right:

**P(A\|B)/P(B\|A) = P(A)/P(B)**

If we did that, we could read this as "the probability that A is true given that B is true, divided by the probability that B is true given that A is true, is equal to the probability that A is true divided by the probability that B is true".

Returning to the xkcd cartoon, this rearranged form of Bayes' theorem would read as:

> The probability that I'm near the ocean given that I picked up a seashell, divided by the probability that I picked up a seashell given that I'm near the ocean, is equal to the probability that I'm near the ocean divided by the probability that I picked up a seashell.

If I'm thinking of this correctly, then, if I live near the ocean and I don't travel all that often, my P(A) at any given point in time is very high, and if, on top of that, I'm not someone who likes seashells all that much, then my P(B) is very low. Therefore, the right-hand side will have a high value in the numerator divided by a low value in the denominator. Because both sides are equal to one another, this would make the left-hand side of the equation also have a high value in the numerator and a low value in the denominator, which makes sense. You would expect the probability of me being near the ocean given that I'm holding a seashell (which would be very, very rare for me, since I don't like them very much and they are hard to find outside of oceanic beaches, unless you buy them) to be very high, whereas you _would_ expect, from knowing that I do not like seashells very much, and that, therefore, even if I'm on the beach, I'll _probably not_ pick a seashell up, for there to be a low probability that I picked up a seashell given that I'm near (or even on) the ocean.

In _Machine Learning_, Bayes' theorem first appears in the chapter on pattern recognition, in a section on [generative models](https://en.wikipedia.org/wiki/Generative_model). As a downright fun and fascinating coincidence, it turns out that the famous cryptographer and creator of information theory [Claude Shannon](https://en.wikipedia.org/wiki/Claude_Shannon) described an example of generative models in his book, _A Mathematical Theory of Communication_, a book that's also home to the concepts of cryptographic confusion (via S-Boxes in block ciphers) and diffusion (via P-Boxes in block ciphers) that made the Data Encryption Standard (DES) and its successor Advanced Encryption Standard (AES) possible.

These subtle overlaps among cryptography, statistics, and machine learning are cool.

What would be the probability that cryptography exists in a parallel Earth given that statistics has already been discovered there? Would it be the probability that statistics exists given that cryptography already exists, multiplied by the probability that cryptography already exists, divided by the probability that statistics already exists? :)
