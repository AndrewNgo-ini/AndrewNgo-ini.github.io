---
title: "My attempt to build an end-to-end mlops application"
date: 2023-03-27T15:15:16+07:00
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

1. My first attempt
+ Set up:
++ Huggingface inference pipeline
++ fastapi
++ locust
++ 1000 user
++ 1s spawn time
++ 5 token text
Result:
+ rps 43.4, fail 1%
+ responsttime linnear, 15kms at 450user

add feature store


