---
title: "Scale Cube"
date: 2020-06-20T19:42:11+10:00
draft: false
author: Tom
lightgallery: true
---
The *Scale Cube* refers to a model describing the scalability of three different aspects of a system. Each scalability aspect is then denoted on one axis of a cube. In the [first version](https://akfpartners.com/growth-blog/scale-cube) of the Scale Cube these were:

- X: Cloning / Replication
- Y: Split by Dissimilar Things
- Z: Split by Similar Things

applied to Software Architecture:

- X: 1 to n instances providing the same service behind e.g., a load balancer
- Y: Functional decomposition from Monolith to Serverless Functions
- Z: One example is only responsible for a subset of the data (Sharding)

Chris Richardson has a more detailed explanation of the Scale Cube for Software Architecture on [microservices.io](https://microservices.io/articles/scalecube.html)