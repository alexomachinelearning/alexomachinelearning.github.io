---
layout: post
title: "A Few JavaScript Libraries for Machine Learning, Discovered through NPM"
date:   2019-01-24 12:00:00 -0800

---
Tomorrow, I have a conversation with a company, not related to the machine learning space, that has a javascript library for web3 developers to interact with user data. The idea is that users can establish a social profile using this company's application. The social profile is based on an Ethereum address. The user can make some of their profile data public and some of it private, managing their data within the application.

In addition to this application for the user to create and manage their social profiles, and in addition to the database used to store information, there's an API for developers of decentralized applications to integrate with this system. The API is JavaScript-based, so to see if I could try it out, I went to install Node.js, a popular [JavaScript runtime environment](https://en.wikipedia.org/wiki/Node.js). Node.js also installs [npm](https://www.npmjs.com/), a package manager for Node.js which is necessary to install the js API in question.

I decided to set up an npm account, and after I did, I noted that there are currently a whopping 893,000+ available packages within the npm community. This made me wonder what javascript packages are available for machine learning. I found quite a few.

You can read about what these and many other packages do by searching for ["machine learning"](https://www.npmjs.com/search?q=machine%20learning) or ["artificial intelligence"](https://www.npmjs.com/search?q=keywords:neural%20network) on the npm website, but here were three I found interesting:

- [brain.js](https://www.npmjs.com/package/brain.js) - a library of recurrent, long short-term memory NNs, and gated recurrent neural networks written in js
- [apparatus](https://www.npmjs.com/package/apparatus) - simple algorithms to perform anything from sentiment analysis to classification of text
- [opencv4nodejs.js](https://www.npmjs.com/package/opencv4nodejs) - per the documentation, apparently computer vision tasks are computationally demanding and js doesn't do well with them, so this library integrates with the well-known C/C++ vision library [OpenCV](https://en.wikipedia.org/wiki/OpenCV), and, as the name suggests, opencv4node brings some of OpenCV's powerful functionality to js environments

It was cool to see a tiny slice of the machine learning space through a few javascript-based packages that are available for developers.
