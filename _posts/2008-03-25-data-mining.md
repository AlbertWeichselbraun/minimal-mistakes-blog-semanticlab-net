---
status: publish
published: true
title: Data Mining...
wordpress_id: 15
wordpress_url: https://blog.semanticlab.net/2008/03/25/data-mining/
date: '2008-03-25 10:57:38 +0100'
date_gmt: '2008-03-25 09:57:38 +0100'
categories:
- Uncategorized
tags: []
comments: []
---
###  Google Tech Talk; Data1
Some interesting stuff we learned in the course

### Using R

```R
# ploting:
x<-seq(1,7,by=0.1)
plot(x,sin(x))
#
# help:
?seq
###
# read data
###
# read data from input files
setwd('/tmp') # set working directory
#
# header ... defines whether the first line contains a header
data<-read.csv("apache.log", sep=" ", header=F)
#
###
# view specific parts of the data
###
#
# view the first 5 rows
data[1:5,]    # data[rows,colums]
#
# vector:
v<-c(1,3)
#
# retrieve specific rows/columns:
data[c(1,7,21),1] # retrieves data from row nr 1,7, 21
```

### Type of attributes (data types):

* categorical vs. numeric
  - categorical (qualitative) - ip, eye color;
* nominal (no order)
* ordinal (meaningful order; rankings, grades)
* quantitative (numeric) - weight, price
  - interval (there is no "true" zero; no division; calendar dates, temperature in celsius)
  - ratio (there is a true zero; there is division; temperature in kelvin, length time)
* discrete vs. continuous

### Attribute type and mathematical operations:

* distinctness: =, != 
* order: > < 
* addition: + -
* multiplication: * /

* nominal : distinctness
* ordinal : distinctness, order
* interval: distinctness, order, addition
* ratio   : all 4
