---
title: "Statistics Summary"
author: Bangyou Zheng
date: 2020-07-31
slug: summary
toc: true
authors:
- bangyou-zheng
menu:
  docs:
    parent: phenotypic-function
    weight: 1
---


This function only applies for layers with a single band (e.g. temperature, vegetative index or DSM).

The predefined functions include

* count: Number of pixels
* mean: Mean values of all pixels
* median: Median (50th percentile) values of all pixels
* q1: 1th percentile of all pixels
* q5: 5th percentile of all pixels
* q10: 10th percentile of all pixels
* q25: 25th percentile of all pixels
* q75: 75th percentile of all pixels
* q90: 90th percentile of all pixels
* q95: 95th percentile of all pixels
* q99: 99th percentile of all pixels

A plot is summarised in the whole plot level, and then split along the long and short sides which is defined by parameters `slice_long` and `slice_short`, respectively (1 in default without slicing). All pixels are further split by a single break which is defined by parameter `break` (empty for no breaks). All predefined functions are applied for slices and breaks.

In the outputs, 1) the function names are used as the trait; 2) the prefix of `1` and `2` in the trait names are used to represent the results of less and more than the break, respectively 3)two extra columns (`SampleLong` and `SampleShort`) are used to represent the sampling along the long and short sides, respectively (`0` for whole plot).

