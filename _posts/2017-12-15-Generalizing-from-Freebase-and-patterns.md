---
status: draft
published: false
title: Generalizing from Freebase and Patterns using Cluster-Based Distant Supervision for KBP Slotfilling
citation: Roth, B., Chrupala, G., Wiegand, M., Singh, M., & Klakow, D. (2012). Generalizing from Freebase and Patterns using Cluster-Based Distant Supervision for KBP Slotfilling. In TAC.
categories:
- Applications
- Big data
tags:
- slot filling
- knowledge base population
- wikipedia
- support vector machines
- distant supervision
comments: []
---
This paper describes a system for knowledge base population (KBP) that uses distant supervision to train machine learning models that are then used to perform slot filling tasks within the TAC KBP 2012 task.

## Method

 1. the authors expand query expansion based on Wikipedia link anchor texts: For a query $q$ the wikipedia page that $q$ most likely refers to is determed. Afterwards the top-10 link anchor texts for links that point to that particular Wikipedia page are obtained and used to expand the query.

 2. 
