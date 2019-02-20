---
layout: post
title: "On Selecting Programming Languages for Machines and their Software"
date:   2019-02-19 12:00:00 -0800

---
_"To make robust and reliable distributed programs on the Internet, object-oriented programming just does not solve the right problems"_. This is a [fascinating quote](https://www.youtube.com/watch?v=XQ32gbtUtRU&index=2&list=PLx3mQFFeHPjlcuFzis6XzjStIfA493MV-) by Professor Peter Van Roy of the online lecture series, [_Paradigms of Computer Programming_](https://www.youtube.com/playlist?list=PLw454N-VXALSIzIe_eL5U8L4S68v2X_ak), based on the University of Louvain course of the same name. When hearing it, I began to wonder which programming languages (based on the _programming paradigms_ they are intended to support) might reign within the world of autonomous vehicles.

For example, some years ago, I read a fascinating article by then-SpaceX employee Robert Rose describing how and why everything made at SpaceX is (or was then) built using Linux (see [the LWN summary](https://lwn.net/Articles/540368/) of Rose's 2013 presentation "Lessons Learned Developing Software for Space Vehicles").

Linux is written in the C programming language. The paradigms C supports are _imperative programming_, _procedural programming_, and _structured programming_. I wonder what, if relevant to this question, makes these paradigms optimal for solving problems such as how to make reliable software for self-landing rockets. (With more regards to machine transportation in space, Linux is also used in the [software for Mars Curiosity Rover](https://linux.softpedia.com/blog/curiosity-rover-controlled-with-a-linux-computer-by-nasa-495914.shtml), and _assembly_, a programming language that inspired C, was used in the Apollo program's [Apollo Guidance Computer](https://en.wikipedia.org/wiki/Apollo_Guidance_Computer). What about Linux—is there something about the problems it solves and the way it does that, or is the choice of Linux just a matter of convention or preference?

Returning to Van Roy's quote, he also says that _multi-agent dataflow programming_ offers a better alternative for building distributed programs for use on the web. A few noteworthy things to point out from the [_dataflow programming_](https://en.wikipedia.org/wiki/Dataflow_programming#Languages) Wikipedia article:

> Data flow has been proposed as an abstraction for specifying the global behavior of distributed system components: in the live distributed objects programming model, distributed data flows are used to store and communicate state, and as such, they play the role analogous to variables, fields, and parameters in Java-like programming languages.

This seems interesting, but I don't yet understand why.

In regards to state (the assembly pun is not intentional), the article also specifies an advantage of using dataflow programming languages:

> Most programming languages require a considerable amount of state information, which is generally hidden from the programmer. Often, the computer itself has no idea which piece of information encodes the enduring state. This is a serious problem, as the state information needs to be shared across multiple processors in parallel processing machines. [...] Where a sequential program can be imagined as a single worker moving between tasks (operations), a dataflow program is more like a series of workers on an assembly line, each doing a specific task whenever materials are available. Since the operations are only concerned with the availability of data inputs, they have no hidden state to track, and are all "ready" at the same time.

Noteworthily, for this blog, the Wiki goes on to say that one of the languages that uses the dataflow programming paradigm is "Orange". But it links to the software called [Orange](https://en.wikipedia.org/wiki/Orange_(software), which comes with ML algorithms for classification, regression, clustering, and more but is not to be confused with the programming language called [Orange](https://github.com/orange-lang/orange), which is unrelated to that software and does not appear to be a dataflow programming language, but rather an imperative and object-oriented language.

That is a beautiful and confusing coincidence. :)
