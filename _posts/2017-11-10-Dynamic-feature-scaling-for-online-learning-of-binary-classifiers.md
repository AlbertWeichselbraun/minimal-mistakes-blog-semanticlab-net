---
status: publish
published: true
title: Dynamic feature scaling for online learning of binary classifiers
citation: Bollegala, Danushka (2017). Dynamic feature scaling for online learning of binary classifiers. Knowledge-Based Systems, 129, 97–105. https://doi.org/10.1016/j.knosys.2017.05.010
categories:
- Big data
tags:
- artificial intelligence
- machine learning
- feature scaling
- classification
comments: []
math: true
---
This article describes and evaluates different online feature scaling approaches and their impact on the performance of binary classifiers.
 1. online feature scaling requires features to be adapted on the fly, i.e. *before* all properties of the underlying distribution are known.
 2. the evaluations in the article suggest, that the rather simple **unsupervised dynamic scaling** approach performs exceptionally well when used with the average weight vector for training and testing, to reduce the impact of the last features encountered in the learning step.


## Method 

 1. The feature value $$x_j$$ for feature $$j$$ is transformed using the medium $$\mu_j$$ and standard deviation $$\sigma_j$$ to the scaled value $$x_j'$$:

    $$x_j' = \frac{x_j - \mu_j}{\sigma_j}$$

 2. estimations of the *k*th update of the mean and standard deviation for the *j*th feature are obtained from:

      $$\begin{align}
            \mu^k_j &= \mu^{k-1}_j + \frac{x_j^k - \mu_j^{k-1}}{k} \\
              s^k_j &= s^{k-1}_j + (x^k_j - \mu_j^{k-1}) (x_j^k - \mu_j^k) \text{ with}\\
         \sigma^k_j &= \sqrt{s^k_j/(k-1)}
      \end{align}$$
