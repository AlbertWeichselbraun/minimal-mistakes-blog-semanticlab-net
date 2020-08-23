---
status: publish
published: true
title: Suffix array
categories:
- Big data
tags:
- data structures
- text search
comments: []
math: true
---
The suffix array is a memory-efficient alternative to the suffix tree which provides a sorted list of string indices indicating the string's suffixes.

## Creation

Provided that the sentinel character `$` has the smallest value the suffix array for the string `barbapapa` is determined as follows:

 1. determine all possible suffixes and the corresponding start indices (the index one indicates the first position).

     | suffix | start position in string|
     | -------| --------------:|
     | barbapapa$ | 1          |
     |  arbapapa$ | 2          |
     |   rbapapa$ | 3          |
     |    bapapa$ | 4          |
     |     apapa$ | 5          |
     |      papa$ | 6          |
     |       apa$ | 7          |
     |        pa$ | 8          |
     |         a$ | 9          |
     |          $ | 10         |

 2. sort all suffixes

     | suffix | start position in string|
     | -------| --------------:|
     |          $ | 10         |
     |         a$ | 9          |
     |       apa$ | 7          |
     |     apapa$ | 5          |
     |  arbapapa$ | 2          |
     | barbapapa$ | 1          |
     |    bapapa$ | 4          |
     |        pa$ | 8          |
     |      papa$ | 6          |
     |   rbapapa$ | 3          |

 3. the suffix array only records the start positions, i.e. contains the values `[10, 9, 7, 5, 2, 1, 4, 8, 6, 3]` in the example above.

Suffix arrays can be derived from suffix trees in $$\mathcal{O}(n^2 log\quad n)$$ although more efficient algorithms that are able to build the array in $$\mathcal{O}(n)$$ exist.

## Applications:

 1. searching: *e.g. does the suffix `papa` occur in the string?* Do a binary search in the array and lookup the corresponding string value to determine whether a suffix is present.
 2. counting: *e.g. how often does the suffix `apa` occur?*. Do a binary search and count the neighboring suffixes starting with `apa`.
 3. K-mer counting: compute all substrings of up to size `k` and the number of times they occur in the string.

