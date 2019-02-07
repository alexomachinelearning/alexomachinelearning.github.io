---
layout: post
title: "Memory State and Time in Neural and Non-Neural Networks"
date:   2019-02-06 12:00:00 -0800

---

In distributed systems, a participant (one individual computer) in a system of participants is called a _node_. As I learned from three lectures today...

- Seif Haridi - [*Lecture 1. Unit 1. Introduction to Distributed Systems (Compact)*](https://www.youtube.com/watch?v=F_4BCNl0iVk) (2012)
- Ankur Srivastava - [*A Quick Introduction to Distributed Systems*](https://www.youtube.com/watch?v=jhqk8m6kb4U) (2018)
- Natarajan Meghanathan - [*Module 6.0 Introduction to Distributed Systems)*](https://www.youtube.com/watch?v=Yss4MUj5lA8) (2013)

...one of the advantages of distributed systems is the ability to assign computational work to all or a subset of participants, each performing the same work in parallel. A second advantage is the ability to delegate subcomponents of one computational task to different nodes.

However, one disadvantage of this computing model is that the participants in the network do not (cannot) access a single store of shared memory. Each must either keep a copy of the memory or be satisfied with having just one portion of it, if you will.

If we zoom into the computational structures of neural networks, a concept of computational memory called "state" appears in some neural networks, such as recurrent neural networks (RNNs).

State can be thought of as a snapshot—a representation of all the values in a system during a particular moment. Imagine a simple database with just three records, storing one value each. There are three values in the system. The state of the system at a point in time would be the keys and values of those three records. "Memory" in that system would simply represent the state at that moment. Or perhaps it's the state at the moment plus all the state recorded at every previous discrete point in time, creating a continuously timestamped track record. Or it might be more akin to Git or a Google Document, for which when (to my present knowledge) there's a change in a directory or a file, the change triggers the recordation of an event along with its time stamp, such that (and I have to look into this more closely to check its accuracy) "memory" exists at the checkpoints of alteration rather than as a database continuously monitored by a moving clock.

When it comes to neural network state, I'm a little fuzzy on whether or not it's similar or identical to other computing structures. But it seems to be so (Alpaydin, p. 94):

> If we define the state of a network as the collection of the values of all the neurons at a certain time, recurrent connections allow the current state to depend not only on the current input but also on the network state in the previous time steps calculated from the previous inputs.

This makes me recall something Haridi said in his lecture, on the deterministic (and therefore reproducible) nature of _(atomic) message broadcasting_ in a distributed system:

> "We can use the broadcast abstraction...to implement a replicated service: the service consisting of [a] set of machines [that] when they receive an operation, they all perform the operation, and if they receive multiple operations, then they will perform these operations in the same order using an atomic broadcast. Therefore the state [of these machines], given that [each] machine['s] operation is deterministic, will be the same after performing these operations."

This principle of reproducibility, albeit in a way less tightly coupled to time, also appears in the creation and management of hierarchical deterministic (HD) wallet software for payments within the Bitcoin blockchain, with reproducibility made possible by knowledge of a particular security parameter called a root seed ([Antonopoulos, p. 106](https://www.amazon.com/Mastering-Bitcoin-Programming-Open-Blockchain-ebook/dp/B071K7FCD4)):

> "Every key in the HD wallet is deterministically derived from this root seed, which makes it possible to re-create the entire HD wallet from that seed in any compatible HD wallet. This makes it easy to back up, restore, export, and import HD wallets containing thousands or even millions of keys by simply transferring only the mnemonic that the root seed is derived from." (Antonopoulos, p. 106)

Returning to Alpaydin's quote while considering Haridi's, one of the questions I'll have as I study recurrent neural networks in the future is whether the network state of the neurons is recorded in some sequential fashion. If it is, then my follow-up question will be whether time step calculations can be performed by multiple neural networks, i.e., if those computations can be performed in parallel across a distributed neural network.

If all the steps in a particular process could be reproduced by any node in such a system, then what would be the difference between "memory" as stored state and "memory" as the ability to reliably reproduce (re-compute) state on an as-needed basis, and what would building such a system have to teach us about time?
