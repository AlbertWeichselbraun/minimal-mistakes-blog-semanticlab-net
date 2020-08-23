---
status: publish
published: true
title: "Employment relations: a data driven analysis of job markets using online job boards and online professional networks"
citation: "Vukosi Marivate and Nyalleng Moorosi. 2017. Employment relations: a data driven analysis of job markets using online job boards and online professional networks. In Proceedings of the International Conference on Web Intelligence (WI '17). ACM, New York, NY, USA, 1110-1113."
categories:
- Applications
- Big data
tags:
- project
- clustering
- latent dirichlet allocation
comments: []
---
Career websites contain valuable data on employees, their skill sets and, employment history. This article uses *k-means clustering* on keywords describing skill sets that have been transformed using either
 1. term frequency inverse document frequency (TF-IDF) or
 2. t-distributed stochastic neighbor embedding (TSNE).

A third experiment performs the clustering after 20 keywords have been selected using Latent Dirichlet Allocation.

In addition the authors extract the chronological information about positions to visualize potential career paths.

## Insights

 1. clustering jobs per title yields job titles commonly used for different kind of work (e.g. web developer, business intelligence, oracle development, etc.)
 2. the network generated from the chronological information shows (i) typical career paths and (ii) identifies positions with high in- and out-degrees.
