---
title: "Protocol Or ABC In Python - When to use which one?"
date: 2023-04-08T15:15:16+07:00
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

This is my summary from this vid 
https://www.youtube.com/watch?v=xvb5hGLoK0A

New terms:
Nominal typing -> suggest relationship (inheritance) -> abc
Structural typing -> look at the structure of the object to determine type -> protocol -> duck typing as we already know


![](/back-end/protocol_abc/1.png)

So basically, with ABC, you are forced to implement all the method you inherent from the base class

![](/back-end/protocol_abc/2.png)

With protocol, there will be error in the call function step, not initizlied step

Pros of ABC: Inheritance propertise, subclass may benefit from init of super class 

Pros of Protocol: Just like an interface of OOP language, just follow the rule
