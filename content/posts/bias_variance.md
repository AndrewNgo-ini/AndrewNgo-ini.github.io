---
title: "Bias variance"
date: 2022-11-14T14:51:28+07:00
draft: false
---
Bias ?
Variance ?

By looking at training error and valid error, we can diagnose what is the problem with our model

<img href= "Bias-Variance/Bias-Variance-classify-example.png">

+ At first column, Train-error perform well, but Dev set not generalize well => High Variance (Overfit)
+ At second column, train-error did not well nor Dev set => High bias (Underfit)
+ At third column, High bias because not doing well on training set and High variance because even not doing well on trainset but dev set is even worse 
+ Final column, low bias low variance => we want this

Ilustration of all those things
<img href = "Bias-Variance/ilu1.png">
<img href = "Bias-Variance/ilu2.png">