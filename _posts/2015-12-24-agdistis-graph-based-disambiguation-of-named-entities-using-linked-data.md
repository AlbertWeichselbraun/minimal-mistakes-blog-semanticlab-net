---
status: publish
published: true
title: AGDISTIS - Graph-Based Disambiguation of Named Entities Using Linked Data
citation: Usbeck, R., Ngonga Ngomo, A.-C., Röder, M., Gerber, D., Coelho, S., Auer, S., and Both, A. (2014). AGDISTIS - Graph-Based Disambiguation of Named Entities Using Linked Data. The Semantic Web &mdash; ISWC 2014 (Vol. 8796, pp. 457-471). Springer International Publishing.
wordpress_id: 879
wordpress_url: https://blog.semanticlab.net/?p=879
date: '2015-12-24 11:38:17 +0100'
date_gmt: '2015-12-24 10:38:17 +0100'
categories:
- Named Entity Linking
tags:
- linked open data
- named entity linking
- graph-based disambiguation
- HITS algorithm
comments: []
math: true
---
## Summary
This paper introduces a graph-based disambiguation approach for named entity linking that achieves higher F-measures than the state of the art and a quadratic time complexity.
The authors consider named entity linking an optimization problem which optimizes the assignment $$\mu^*$$ with

  $$\mu^* = \underset{\mu}{\text{arg max}} (\psi(\mu(C,N), N) + \phi(\mu(C,N),K))$$.

## Method

* The approach use named entity recognition to extract named entities from the text.
* A coherence function $$\psi$$ determines candidate entities *C* in the knowledge base *K* (e.g. based on a string similarity function such as trigram similarity and known surface forms).
* An **expansion policy ensures the mapping of mentions that are substrings of other mentions to the same resource (e.g. Obama and Barack are mapped to Barack Obama, if the later has been mentioned earlier).
* Computation of the optimal assignment of candidate nodes to named entities using a disambiguation graph $$G_d$$ and the HITS algorithm.

## Evaluation
The evaluation has been performed with the (i) English and German DBpedia, and (ii) English YAGO 2 knowledge bases on a total of six different evaluation corpora yielding the following insights:</p>

1. the search depth *d* (i.e. number of links considered in the disambiguation graph) has only a limited influence on the algorithm's performance (unless d=0 is chosen).
2. using string similarity only (rather than surface forms) considerably reduces performance
3. expanding surface forms (e.g. `Obama` to `Barack Obama` if the later form has occured earlier in the text) boosts the F-measure of AGDISTIS by 4%
