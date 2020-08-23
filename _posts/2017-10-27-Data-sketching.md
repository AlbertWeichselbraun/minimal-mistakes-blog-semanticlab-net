---
status: publish
published: true
title: Data sketching
citation: Cormode, G. (2017). Data Sketching. Communications of the ACM, 60(9), 48–55. https://doi.org/10.1145/3080008
categories:
- Big data
tags:
- data structures
comments: []
---
This article introduces three popular data structures that efficiently handle and summarize large data sets.

 1. **Bloom filters** are basically sets which answer the question of whether an item is part of the set (i.e. has been seen by the filter) with either (i) "the item is definitely not a part of the set", or (ii) "the item *might* be part of the set. 

 2. The **Count-Min Sketch** method is a probabilistic method for counting the number of times items of a certain type have been observed. When queried the structure returns an estimation which is considered an *upper bound* for the corresponding count.

 3. The **HyperLogLog** method counts the number of different items seen in a large set of individuals without keeping count of every single individual.
