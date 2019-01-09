---
layout: post
title: "Should Machines Learn to Process Speech before They Learn to Process Text?"
date:   2019-01-03 12:00:00 -0800
redirect_from:
  - /2019/01/03/should-machines-learn-to-process-speech-before-they-learn-to-process-text.html
---

Today I asked a question in a comment on LinkedIn. My question was, essentially, if there is an advantage to teaching machine learning models to process speech before we teach them to process text. Let me walk you through my reasoning.

### On Tools that Process Natural Language
Dr. Matt Wood of Amazon recently wrote a blog post announcing that AWS Machine Learning can be used by developers to [build natural language processing models into their applications](https://aws.amazon.com/blogs/machine-learning/build-your-own-natural-language-models-on-aws-no-ml-experience-required/). This relies on a service called Amazon Comprehend, which, as the name implies, can analyze text and perform reading comprehension-related tasks. The service is trained with _deep learning_ models and is able to detect certain words, perform sentiment analysis on the language of the text, or even categorize the text by certain topics. Dr. Wood's announcement was about a new capability for Comprehend: 1) the ability to further tailor the service's searches to a particular organization's lexicon, and 2) the ability to sort documents into custom classifications (i.e., categories). Apparently, this type of search-and-analyze is not easy to do, which is why using a machine learning service like Comprehend is useful. This all falls within a category of applied machine learning called _natural language processing_.

Wood's blog post reminded me of something I've seen in Alpaydin's text, _Machine Learning_: __bag of words__. Bag of words is a technique used to figure out whether or not text shows up inside a given document and then sort that document into a category based on its contents. This is one of the techniques used for spam filtering, for example.

The day before Wood's post, Nino Bice of AWS Artificial Intelligence wrote a post titled ["Getting Started with Amazon Comprehend custom entities"](https://aws.amazon.com/blogs/machine-learning/getting-started-with-amazon-comprehend-custom-entities/). In it, Bice describes how the Entities data type now supports "private, custom entity types", specific to an organization, that map to individual words of importance to that organization. Think of this as making the machine learning model more attuned to the language used within a company (or an industry such as healthcare) that is using an app powered by Comprehend's APIs. The organization's custom text data trains Comprehend's natural language processing model in order to better predict how to classify documents or text when the customer's models are exposed to those documents or texts in the future, after the learning models have been trained with the customer's data set. Presumably, the bag of words technique is used somewhere in the process.

### On Primitives of Sight and Sound

At this point, it's helpful to point to a page in Alpaydin's book (p. 103, Fig 4.2) describing how something called _hierarchical processing_ works. Basically, if you feed an image of text to a computer, and you want that computer to be able to recognize what word is contained in the image, it does that by using models trained to perform hierarchical processing, which begins by detecting the visual _primitives_ of letters, "such as arcs and line segments". Alpaydin's Figure 4.2 shows how two curves make an *o*, one vertical line makes an *l*, and so on. In hierarchical processing, the machine would process the pixels that make up those primitives, then combine those primitives into single letters to process, then determine if a given word has a combination of letters that it has learned to recognize, and, finally, identity "more abstract relationships such as the relationship between "book" and [the French equivalent] "livre"". Fascinating.

I recall learning as a young boy how to write the letters *o*, *l*, and all the rest on [big, manuscript ruled D'Nealian paper](https://en.wikipedia.org/wiki/D%27Nealian). The goal of those scholastic routines must be to teach us to learn, identify, and _write_ all the visual primitives of all the letters in the alphabet, which perhaps improves our ability to subsequently learn, identify, and _read_ all the letters of the alphabet (I can't recall if we learn to read or write first).

However, most of us learn to do something else before we learn to read or write: we learn to speak. Speech, like letters, has its own primitives, except that they're oral (when transmitted) and aural (when received) rather than visual:

> Alpaydin (p. 67): "Just as we consider each character image to be composed of basic primitives like strokes of different orientations, a word is considered to be a sequence of _phonemes_, which are the basic speech sounds. In the case of speech, the input is _temporal_; words are uttered in time as a sequence of these phonemes, and some words are longer than others."

We as humans begin to master the phonemes of speech before we master the visual primitives of letters and how they come together to form written words. This brings me to my question.

### Should Our Learning Machines Learn to Listen Before Reading (or Speaking)?

Since humans learn to listen and speak before we learn to read or write, I wonder if there would be some computational or other advantage to training speech learning models on speech data before training natural language processing models on text data, especially of the same words spoken as written, in order to improve efficiency or accuracy. I just don't yet know enough about how either of these work to have an answer.

Further, is there is a speech recognition equivalent to the bag-of-words technique used for text classification of documents? Could such a "bag-of-spoken-words" technique be used in combination with techniques for written text improve the models' predictions?

From the question I posed:

>...would there be a way to take a list of written words that would normally be used to train models for text classification, speak the words aloud and record them, put the speech data through a speech recognition algorithm to train a speech recognition NLP model, and then use the results to train Amazon Comprehend for text classification? Reason I ask is that in human learning, when we learn to read words, we likely associate the visual primitives of the letters with the speech primitives of the spoken versions of those letters, which I suppose accelerates the ability to read and process words because we can speak their spoken counterparts. Thus, I wonder if in machine learning we are yet approaching things in a similar way, coupling NLP for text with NLP for speech during the training process.


There is much to explore.

---

#### Further Learning


[1] [_Machine Learning_](https://mitpress.mit.edu/contributors/ethem-alpaydin) by Ethem Alpaydin (2016)

[2] ["Deep learning"](https://en.wikipedia.org/wiki/Deep_learning) - _Wikipedia_

[3] [_Amazon Comprehend FAQs_](https://aws.amazon.com/comprehend/faqs/) and [_Entity_](https://docs.aws.amazon.com/comprehend/latest/dg/API_Entity.html) - _AWS_

[4] ["Sentiment analysis"](https://en.wikipedia.org/wiki/Sentiment_analysis) - _Wikipedia_

[5] ["Natural language processing"](https://en.wikipedia.org/wiki/Natural_language_processing) - _Wikipedia_

[6] ["Bag-of-words model"](https://en.wikipedia.org/wiki/Bag-of-words_model) and ["Naive Bayes spam filtering"](https://en.wikipedia.org/wiki/Naive_Bayes_spam_filtering) - _Wikipedia_

[7] [_Amazon Comprehend Medical_](https://aws.amazon.com/comprehend/medical/) - _AWS_

[8] ["Phonemes"](https://en.wikipedia.org/wiki/Phoneme) - _Wikipedia_
