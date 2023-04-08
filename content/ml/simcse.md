---
title: "What is SimCSE?"
date: 2023-03-22T15:15:16+07:00
tags:
  - "tech"
  - "learn"
draft: false
cover:
    image: "/simcse.png"
    # can also paste direct link from external site
    # ex. https://i.ibb.co/K0HVPBd/paper-mod-profilemode.png
    alt: "<alt text>"
    caption: "<text>"
    relative: false # To use relative path for cover image, used in hugo Page-bundles
---

![abc](https://github.com/princeton-nlp/SimCSE/blob/main/figure/model.png?raw=true)


`Q:` how does they know which one is posstiive or negative in unspervised task SimCSE

`A:` Suppose we have two sentences, "The cat sat on the mat" and "The dog chased the ball." The SimCSE algorithm first encodes these sentences into vectors using a pre-trained transformer-based language model like BERT. These sentence embeddings are then used to compute the similarity score between them. In SimCSE, the similarity score is calculated using the cosine similarity metric.

In this example, the similarity score between the two sentences is likely to be low since they are about different topics. SimCSE then adjusts the sentence embeddings to maximize the similarity score between similar sentences and minimize the similarity score between dissimilar sentences.

Therefore, the algorithm does not require any explicit labeling of sentences as positive or negative. Instead, it learns to distinguish between similar and dissimilar sentences based on the context and meaning of the text. By doing so, it can identify semantic similarities and differences between sentences, which can be useful for various natural language processing tasks.

`Q:` Ok, just give me the loss function

`A: `
![abc](/simcse.png)


