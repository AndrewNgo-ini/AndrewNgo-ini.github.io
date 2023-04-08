---
title: "Bias and Variance in Machine Learning"
date: 2022-11-14T15:15:16+07:00
tags:
  - "tech"
  - "learn"
draft: false
cover:
    #image: "https://i.ibb.co/K0HVPBd/paper-mod-profilemode.png"
    # can also paste direct link from external site
    # ex. https://i.ibb.co/K0HVPBd/paper-mod-profilemode.png
    alt: "<alt text>"
    caption: "<text>"
    relative: false # To use relative path for cover image, used in hugo Page-bundles
---

By looking at training error and valid error, we can diagnose what is the problem with our model

![alt text](/bias-variance/biasvariance-1.png)


+ At first column, Train-error perform well, but Dev set not generalize well => High Variance (Overfit)
+ At second column, train-error did not well nor Dev set => High bias (Underfit)
+ At third column, High bias because not doing well on training set and High variance because even not doing well on trainset but dev set is even worse 
+ Final column, low bias low variance => we want this

Ilustrations
![alt text](/bias-variance/biasvariance-2.png)
![alt text](/bias-variance/biasvariance-3.png)