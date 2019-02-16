---
layout: post
title: "The Difficulties of Comparing Human Neural Architecture to Artificial Neural Architecture in a List of Function and Structure"
date:   2019-02-15 12:00:00 -0800

---
While continuing to prep [a list to organize all the artificial neural networks I can find](https://ahumanlearningmachinelearning.com/2019/02/13/a-still-inexhaustive-totally-incomplete-list-of-neural-network-types-wip/), I started to think about creating a parallel list for human neural networks. But as I started doing so, I realized that something like a convolutional neural network (i.e., an ANN architecture devoted to finding mathematical relationships with which to make repeatable predictions about images) doesn't really have a direct analogy in biology, one reason being that in real brains, many brain regions get recruited to perform visual processing, not just one combination of real neurons dedicated to looking at pictures. So I started to run into problems when attempting to create even a basic like-for-like arrangement in a multilevel list format between ANNs and biological NNs. Perhaps the best current analogy that can be made is to equate [neural circuits](https://en.wikipedia.org/wiki/Neural_circuit) to individual artificial neural networks like CNNs.

The challenges don't end there. When you zoom into the unit (node) level of an artificial neuron vs a real neuron, the categorical parallel is equally hard to make. For one, real neurons can be broken "up" into functional divisions, such as [interneurons](https://en.wikipedia.org/wiki/Interneuron), motor neurons, and sensory neurons, and they can also be broken "down" into sub-types (e.g., a [chandelier neuron](https://en.wikipedia.org/wiki/Chandelier_cell) is a sub-type of interneuron). On the other hand, there are no functional categories that artificial neurons can be broken upwards or downwards into, that I know of; though ANNs borrow the name "neuron", such neurons are nothing but ["a mathematical function conceived as a model of biological neurons"](https://en.wikipedia.org/wiki/Artificial_neuron). They are models without unit-level super-models or sub-models. This makes node-level or node component comparisons difficult and potentially unhelpful.

Finally, there are not yet, to my knowledge, any functional superclasses of artificial neural networks in the same way that biological neural networks have [large scale brain networks](https://en.wikipedia.org/wiki/Large_scale_brain_networks), such as the default mode network. So even if it was correct to equate "cluster of different neural circuits working together" to "cluster of different artificial neural networks working together", there aren't yet supersets of cross-functional artificial neural networks. So in a list for artificial neural networks, there's nothing to place but "TBD" at the list level that corresponds to several of the biological neural levels discussed above. (One possibility is that "types of neural networks" is not the best framework for a list, but I'll need to think further on that point; a second possibility is that it won't be a good idea to mix functional levels with structural levels in the same list, in which case, I may need to create multiple, separate lists).

All of this made me reflect on the purpose of biological neural networks, which may well be, simply, to learn. Specifically, to learn the best way to respond to sensed data depending on the type of data being processed. (Also—either as a corollary or as a main function—to learn how to make increasingly better predictions based on pattern recognition and pattern response).

I may settle for "human learning system" and "machine learning system" as a way to conceptualize the relationships I'm trying to show in my multi-level list:

    Learning Systems
        Human learning system
            Large scale brain network
                Default mode network
                Dorsal attention network
                Salience network
                Ventral attention network                
        Machine learning system
            TBD X
                TBD Y
                    Z1
                    Z2
                    Z3

To be continued...
