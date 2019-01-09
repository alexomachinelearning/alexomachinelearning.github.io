---
layout: post
title: "Small Fleet Networks (SFNs) and the Need for Distributed Black Boxes in Future Self-Driving Systems"
date:   2019-01-08 12:00:00 -0800
redirect_from:
  - /2019/01/08/small-fleet-networks-sfns-and-the-need-for-distributed-black-boxes-in-future-self-driving-systems.html

---

Here are some preliminary thoughts on general design requirements of self-driving networks. In the future, small fleets of networked vehicles will likely communicate, in a decentralized way, with one another as the fleets move. In addition to this fleet-to-fleet communication, there will likely be a need for fleet-to-system communication, with each small fleet communicating at regular intervals with a systemwide architectural layer. Finally, each "small fleet network" (SFN) will need a means of ensuring trusted communication among the vehicles that make up the group at a given point in time, as well as a mechanism to rapidly record vital information contributed to a **distributed black box**.

This distributed black box is to be a secure distributed database of data that is vital to safety and can be collected and analyzed for the purpose of preventing failures. These distributed black boxes could also be used as data stores for subsequent machine learning training sessions as well as repositories from which to coordinate _transfer learning_ for other self-driving and other systems.

Recently, machine learning research scientist Lex Fridman shared news that MIT is opening its competition for [the DeepTraffic project](https://selfdrivingcars.mit.edu/deeptraffic/) to all. Fridman teaches a course, [MIT 6.S094: Deep Learning for Self-Driving Cars](https://selfdrivingcars.mit.edu/), in which students explore machine learning technologies for autonomous vehicles, particularly the use of reinforcement learning-based deep neural networks. The related DeepTraffic project has as its goal "to create a neural network to drive a vehicle (or multiple vehicles) as fast as possible through dense traffic" (["DeepTraffic"](https://selfdrivingcars.mit.edu/deeptraffic/)).

But for such a neural network, once built, to become usable and deployable in future self-driving vehicle software, larger architecture design questions will need to be answered. The [visual simulation Fridman posted](https://www.linkedin.com/feed/update/urn:li:activity:6487379223915872256/) along with his announcement made me think about the need for such vehicles to share a distributed black box.

# Requirements of Small Fleet Networks (SFNs)

Imagine ten cars moving autonomously on a highway in close proximity to one another in a cluster and at high speeds. Let's call this a small fleet network (SFN). For this fleet to operate safely, what might be necessary?

* A database in each vehicle that records all speed, position, and other driving data for that vehicle (a black box)
* A very reliable communication method for each of the ten vehicles to transmit information about itself to the other nine so that the SFN can autonomously coordinate real-time adjustments, dynamically, of every vehicle's speed, position, and velocity (perhaps via fleet-level software that spins up to coordinate such activity when 2 or more vehicles self-assemble into an SFN; such "fleet master software" could run on a temporary virtual machine)
* A distributed database in which to record this shared information, as well as a log of when the vehicle-to-vehicle and vehicle-to-fleet information was shared (a distributed black box)
* An autonomous and fault-tolerant consensus mechanism to ensure all vehicle-to-vehicle messages reach one another and also propagate reliably to the SFN's distributed black box
* A means of SFN-to-SFN communication within a large localized space, so that multiple fleets can communicate SFN-specific data with one another (a distributed black box of distributed black boxes, for the localized system)
* Byzantine-fault tolerance at the vehicle level, at the SFN network level, and at the localized multi-SFN system level, to ensure individual vehicles and individual fleets continue to operate effectively in the presence of software malfunction, intentional data corruption, or intentional disruption of communication, and to ensure proper transmission of data to a systemwide architectural layer (if necessary)
* An identity and access management system that guarantees fast, strong authentication of each vehicle into the SFN communication network; cybersecure authorization policies for all SFN participants; and reliable self-identification of each vehicle (machine-to-machine identity)
* Privacy policies and data anonymization techniques to ensure personally identifying data about the vehicles' owners and/or passengers is not recorded or accessible by any unauthorized parties

In future posts, I'll return to these ideas, invoking in more detail concepts from decentralized blockchains, consensus mechanisms, fault-tolerance, Byzantine fault-tolerance, distributed systems, self-sovereign identity, traditional identity authentication and authorization, message broadcasting, store-and-forward systems (like NASA's Delay/Disruption Tolerant Networking (DTN)), timestamping, Git fast-forward merges, hybrid-cloud architectures, and, of course, machine learning and neural networks.
