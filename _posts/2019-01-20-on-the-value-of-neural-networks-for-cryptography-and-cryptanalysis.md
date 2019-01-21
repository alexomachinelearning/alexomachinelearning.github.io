---
layout: post
title: "On the Value of Neural Networks for Cryptography and Cryptanalysis"
date:   2019-01-20 12:00:00 -0800

---
I read about cryptography on Sundays. Cryptography is a [branch of mathematics and engineering](https://en.wikipedia.org/wiki/Cryptography#Computer_era) dealing with questions of how to secure digital information for data storage and data transmission. Cryptanalysis is the related academic discipline that attempts to find weaknesses in cryptographic algorithms or protocols, necessary to ensure that ever-more secure digital infrastructures can be created and implemented.

Previously, I've wondered about whether or not machine learning might be useful in the worlds of cryptography or cryptanalysis. Today, while reading about the history and implementation of the Data Encryption Standard (DES), I came across this passage in Bruce Schneier's famous 1996 text ["Applied Cryptography (2nd Edition)"](https://www.amazon.com/Applied-Cryptography-Protocols-Algorithms-Source/dp/0471117099) (p. 155):

> Neural Networks
>
> Neural nets aren't terribly useful for cryptanalysis, primarily because of the shape of the solution space. Neural nets work best with problems that have a continuity of solutions, some better than others. This allows a neural net to learn, proposing better and better solutions as it does. Breaking an algorithm provides for very little in the way of learning opportunities: You either recover the key or you don't. (At least this is true if the algorithm is any good.) Neural nets work well in structured environments where there is something to learn, but not in the high-entropy, seemingly random world of cryptography.

This was written in 1996. In 2016, Schneier released a 20th Anniversary edition of the book. I checked to see if the passage had been updated to reflect any change in opinion, but it had not been. Schneier made a fascinating point that's really about the value of predictions: they are valuable because they're reusable. Predictions make it possible to reduce perceived randomness in time or space and increase predictability within a continuum; being able to meaningfully anticipate events is only useful because it transfers. When we learn, what we gain is the possibility to reapply, in the same context or another, some thing to some future instance. But in a context that is truly random, where there are no patterns, learning cannot happen. Here's Alpaydin in ["Machine Learning"](https://mitpress.mit.edu/contributors/ethem-alpaydin): "Machine learning, and prediction, is possible because the world has regularities. Things in the world change smoothly. We are not "beamed" from point A to point B, but we need to pass through a sequence of intermediate locations." (p.40)

In the context of well-designed and well-implemented cryptographic techniques, for example, with respect to high-avalanche one-way hash functions or the highly entropic generation of large symmetric or asymmetric keys, the random or effectively-random "[cryptographically secure pseudo-randomness](https://en.wikipedia.org/wiki/Cryptographically_secure_pseudorandom_number_generator)" of events would seem to make machine learning moot or of too low value. Why bother using neural networks in an environment of impossibly large mathematical ranges and unreproducible sequences (Schneier, pp. 44-46), where reusability is effectively zero? In that "seemingly random world of cryptography", where some events do happen as though "'beamed' from point A to point B", why even attempt to build learning machines for cryptanalysis?

Because humans don't produce errors at random, even if some of the systems we produce are designed to *be* random. And we ought to become better at recognizing the patterns of error our brains produce when we design systems that are intended to be error-free.

## S-Boxes, P-Boxes, Relationships, and Patterns
In section 14.10, on "Theory of Block Cipher Design", Schneier describes two of the concepts that make block ciphers effective in encrypting data (p. 346):

> Confusion serves to hide any relationship between the plaintext, the ciphertext, and the key. Remember how linear and differential cryptanalysis can exploit even a slight relationship between these three things? Good confusion makes the relationship statistics so complicated that even these powerful cryptanalytic tools won't work.

On the next line, he adds the second concept:

> "Diffusion spreads the influence of individual plaintext or key bits over as much of the ciphertext as possible. This also hides statistical relationships and makes cryptanalysis more difficult."

In block cipher design, S-boxes are used to add "confusion" and P-boxes are used to add "diffusion". Some encryption standards of course employ both S-boxes and P-boxes as part of the algorithms used to securely encrypt data. As stated above, S-boxes and P-boxes are intended to reduce, or at least obscure through complexity (hide), relationships among plaintexts, ciphertexts, keys, and keybits.

So if you were to employ machine learning to the task of cryptanalysis in order to detect weaknesses in cryptographic protocols, then one obvious place at which to point the learning models might be at identifying statistically relevant patterns in those relationships and make the "relationship statistics" less complicated. If the learning machine could identify better-than-random patterns in spaces that appear random to us, then perhaps the learning models could be used to train next-generation cryptanalytic software that makes subsequent analysis more efficient.

But where to look or start? In section 12.4, on matters of "Differential Cryptanalysis", the book states that (pp.285-286):

> Differential cryptanalysis looks specifically at ciphertext pairs: pairs of ciphertexts whose plaintexts have particular differences. It analyzes the evolution of these differences as the plaintexts propagate through the rounds of DES when they are encrypted with the same key.[...] As you analyze more and more ciphertext pairs, one key will emerge as the most probable.[...] Certain differences in plaintext pairs have a high probability of causing certain differences in the resulting ciphertext pairs.

Perhaps certain differences in cryptographic algorithms produce certain differences in the probability that they have weaknesses of certain kinds. Humans are good at learning, but we are also good at replicating our mistakes. Reading that reminds me, at this early phase in my understanding of machine learning, of how weights are updated on the connections between artificial neurons in neural networks, especially those in deep reinforcement learning. If there's a pattern to find, even a very difficult pattern to find, then given enough time and attention, the pattern is findable and will be found. If that pattern does turn out to be useful, transferable, and applicable to better cryptographic solution designs, then perhaps neural networks will be useful to cryptography after all, particularly if what we learn about recurrent errors in design can be used to "update the weights" reliably, sort of speak.

It may yet be the case that human brains are uniquely suited to detecting certain patterns that even our best machines won't ever be optimized for but that there are some patterns in the universe and in mathematics that machine-based pattern recognition systems will be much better for, and that those learning machines will come to cover our blind spots.
