---
layout: post
title: "Setting Up a Free Google Cloud Platform Account for Future Machine Learning Work"
date:   2019-01-13 12:00:00 -0800

---
As one of my goals is to build neural networks sometime this year, I started to learn Python this past week. I'm having a lot of fun (see [my GitHub learning repo here](https://github.com/alexomachinelearning/ahumanlearningmachinelearning)). Related to that, a platform I've been wanting to learn about is Google Cloud Platform (GCP). As a newcomer to machine learning, to programming, to computer science, and to cloud applications, high-quality learning materials are a must, and this is an area in which GCP shines. It has the following:

- Strong interactive tutorials within GCP itself
- Strong self-paced modules and tracks via Google Cloud Training
- Specifically, integration with Qwiklabs for interactive "quests", such as the 5-hour [_GCP Essentials_](https://google.qwiklabs.com/quests/23) and the 8-hour [_Baseline: Data, ML, AI_](https://google.qwiklabs.com/quests/34). These are precursors to the following more advanced quests:
  - [_Data Science on the Google Cloud Platform_](https://google.qwiklabs.com/quests/43) (10 hours)
  - [_Data Science on Google Cloud Platform: Machine Learning_](https://www.qwiklabs.com/quests/50) (8 hours)
    - Both of these advanced quests will make it easier to subsequently take two on-demand courses:
      - [Big Data and Machine Learning Fundamentals (v1.1)](https://www.qwiklabs.com/courses/211)
      - [Introduction to Machine Learning with TensorFlow and Cloud ML Engine](https://www.qwiklabs.com/courses/331)

By the time I take all of the above, I will have learned a lot more Python, a lot more about machine learning, and enough about deploying distributed apps in GCP to begin building my own cloud-based neural networks with TensorFlow and other GCP-supported libraries.

In summary, those who wish to become familiar with GCP in general, or GCP for machine learning specifically, should set up a free GCP account and start poking around.

## My GCP Setup Process

Here were the steps that applied to me, written in the imperative voice:

1. Set up a Gmail account if you don't have one already
2. Visit [Google Cloud Platform](console.cloud.google.com)
3. Read and agree to GCP's terms
4. Sign up for a free 12-month trial of GCP, which comes with $300 in credits and lets you build and deploy applications (including machine learning ones) on Google's cloud infrastructure
5. Get your bearings and take the Console Tour, a tutorial that walks you through creating your first project as well as getting to know your Dashboard, Activity Stream, Search Bar, and more  
6. Poke around and get to know the left-hand navigation menu. In my case, a few resources, also called _products_, grabbed my attention:
  - **IAM**, where identity and access management settings can be found, permissions for each project can be set, and the cryptographic materials needed for authentication, authorization, & other operations are managed
  - **Compute > Compute Engine > TPUs**, as I've come across a few discussions about running machine learning models on GPUs vs CPUs vs TPUs (on the TPUs intro page, GCP describes Google Cloud TPUs as "the latest generation of the machine learning hardware that powers Google Search, Street View, Google Photos and Google Translate")
  - **Tools > Endpoints**, which brought to mind that in the world of self-sovereign identity, service endpoints are defined within a document called a _DID Document_, which stores metadata that describes a _decentralized identifier (DID)_. In machine learning, I believe it's all but inevitable that machines and devices will someday utilize self-sovereign identity infrastructure rather than, or in addition to, traditional public-key infrastructure based on X.509 certificates for identity and access management purposes (see ["Decentralized Identifiers (DIDs) v0.11"](https://w3c-ccg.github.io/did-spec/) at _W3C_). I wonder how GCP machine learning API endpoints might be integrated with self-sovereign identity protocols, platforms, or applications in the future
  - **Big Data > Dataprep**, as I suspect that I'll be using this to prep training data once I begin to build and train neural networks
6. Note the main machine learning products that come bundled in GCP, mainly as APIs you can access and try out for free:
  - **ML Engine**, to create and train learning models
  - **Natural Language**, to analyze and classify documents using AutoML (see [AutoML Cloud Natural Language](https://cloud.google.com/natural-language/))
  - **Talent Solution**, a productized Google offering for "enterprise AI-enhanced talent acquisition" (see [Cloud Talent Solution](https://cloud.google.com/solutions/talent-solution/))
  - **Translation**, to translate text (see [AutoML Cloud Translation](https://cloud.google.com/translate/))
  - **Vision**, to analyze and classify images (see [AutoML Cloud Vision](https://cloud.google.com/vision/))
7. Download Google's [Cloud SDK](https://cloud.google.com/sdk) if you wish to interface with GCP from your command line, or use the _Cloud Shell_ tool within GCP to run a Google CLI in-browser

I like this sense of momentum, and the balance between learning about theory and starting to prepare for application too.
