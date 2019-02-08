---
layout: post
title: "Uses of Machine Learning for Online Shopping"
date:   2019-02-07 12:00:00 -0800

---
I've turned off Autocorrect on my phone after noticing a troublesome dip in my ability to self-correct grammar mistakes, something I've historically been very good at catching. One reason I consider likely for this dip in performance is my recent over-reliance on tools that automatically check for mistakes and correct them, specifically on my phone keyboard, from which I type hundreds of words a day. It might be an unfair correlation to make, but if it's the case that mistake detection is a "use it or lose it" function, then perhaps my previous capabilities have indeed been dulled.

My decision to turn off this feature prompted me to look into whether or not and how machine learning is used in the now-commonplace software that performs autocompletions, autocorrections, and suggestions on our phones. The exercise led me to learn about a mostly unrelated set of problems and solutions.

## Search and Online Shopping

In [_Lessons from Integrating Machine Learning into Data Products_](https://www.slideshare.net/cloudera/lessons-from-integrating-machine-learning-into-data-products) (2017), machine learning engineer Sharath Rao of _Instacart_ describes the technology required to deliver groceries to customers when they place an order in the app. Some of this technology revolves around search queries and the presentation of results within the application. For example, see the following list of required capabilities shown in Slides 16-19 of Rao's presentation:

- S.16: Optimizing the order of items in an online storefront
- S:17: Ranking the results of a search for a specific purchase item
- S.18: Complementary recommendations for a product the customer just selected (this is a good time to read pp. 118-123 of [Alpaydin](https://mitpress.mit.edu/contributors/ethem-alpaydin), on the modern use of _generative models_ and _matrix decomposition_ for recommendation and anticipation systems)
- S.19: Anticipating a product that can suitably replace another (plus see note above)

All of these relate to search. Interestingly, "studies show [that] slower response times [are] causally linked to lower customer engagement" (S.21), so it becomes important to use pre-computation and data caching (S.22) techniques alongside machine learning software in order to deliver search results fast enough to convert and retain users. It's always insightful to remember the primacy of customer experiences and the interlocking nature of computer science solutions aimed at solving not just technical problems but practical, human nature problems, too.  

Amidst all this background information on shopping, autocompletion emerges on S.24 as an example of a low-latency task (right there alongside the Okapi Best Matching 25 (BM25) search ranking function, which is ["used by search engines to rank matching documents according to their relevance to a given search query"](https://en.wikipedia.org/wiki/Okapi_BM25)). From the quadrant provided by Rao in that slide, I couldn't make out if the idea is that users expect autocomplete to be very fast (low latency), although that would make sense: when you're typing quickly on a phone screen, even small delays between your input and the response of the autocorrection or autocompletion software are highly noticeable and highly undesirable. Anything above a certain time duration renders the software functionally unusable.

On the 28th and final slide, I noted that "query autocorrection" and "query spell correction" are just two products on a long list of productized machine learning technologies used for problems of search and discovery. Upon reflection, it makes a lot of sense to bundle autocorrection software into apps utilizing other query technologies where search results depend, of course, on accurately spelled words to begin with.

This was a fun way to learn about search.

Thanks, Autocorrect.
