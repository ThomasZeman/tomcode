---
title: "Scale Cube"
date: 2020-01-01
draft: false
author: Tom
lightgallery: true
---
The *Scale Cube* refers to a model describing the scalability of three different aspects of a system. Each scalability aspect is denoted on one axis of a cube. In a [first version](https://akfpartners.com/growth-blog/scale-cube) of the Scale Cube these were:

- X: Cloning / Replication
- Y: Split by Dissimilar Things
- Z: Split by Similar Things

For scaling a software application, the axes get the following meaning:

- X: 1 to n artifacts providing the same service behind, e.g., a load balancer
- Y: Functional decomposition from monolith to serverless functions
- Z: One artifact is only responsible for a subset of data, e.g., by horizontal database partitioning 

Chris Richardson has a more detailed explanation of the Scale Cube for software applications on [microservices.io](https://microservices.io/articles/scalecube.html)