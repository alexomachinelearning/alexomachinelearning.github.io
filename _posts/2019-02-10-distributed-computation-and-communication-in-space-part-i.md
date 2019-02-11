---
layout: post
title: "Distributed Computation and Communication in Space (Part 1)"
date:   2019-02-10 12:00:00 -0800

---
NASA has a cool project called DTN, the Disruption Tolerant Networking for Space Operations program, which has been worked on for a few years and has the following aims:

> The Disruption Tolerant Networking (DTN) program is a step toward building a reliable Interplanetary Internet. The experiment establishes a long-term communications test bed on the International Space Station (ISS), which transmits test messages between the ISS and ground stations. Delay- and disruption-tolerant networks can improve electronic communications by storing data when a connection is interrupted, and forwarding it to its destination using relay stations. ([Disruption Tolerant Networking for Space Operations (DTN) - 06.28.17](https://www.nasa.gov/mission_pages/station/research/experiments/730.html))

Per the description, the goal is to establish an early backbone for interplanetary communication. Servers of ours on Earth, the Space Station, the Moon, Mars once Elon Musk has his way, and wherever else we send our computers to will be able to transmit data. This is a pretty important system to put in place, and I like the emphasis on a solution design that enables both storing data (database) and forwarding that data throughout relay servers until it reaches the intended recipient.

In the [Youtube video](https://www.youtube.com/watch?v=HV8CHoWP9-o) "A Simplified Introduction to Disruption-Tolerant Networking" by NASA's Scientific and Technical Information Program, a visual depiction of how this works is shown. Packets of data go through a sequential series of relay stations ("DTN nodes") between the originating and destination computers. When signal between two DTN nodes is interrupted, the nodes store the packets of data until the signal is re-established. The video compares this against how TCP/IP and UDP/IP protocols transmit packets.

It will be super interesting to learn more about the protocol and to think through some thought experiments of distributed computation for machine learning between Earth and Mars, or how results from, e.g., a TensorFlow training on computers in one part of the solar system can be transmitted using DTN to computers elsewhere.

You can read more about delay-tolerant networking [here](https://en.wikipedia.org/wiki/Delay-tolerant_networking).
