---
title: "Ground Coverage using DTSM"
author: Bangyou Zheng
date: 2020-07-31
slug: ground-coverage
toc: true
weight: 2
authors:
- bangyou-zheng
menu:
  docs:
    parent: phenotypic-function
    weight: 2
---

Ground coverage is defined as the ratio of green pixel in the certain area and calculated using decision-tree-based segmentation model (DTSM) algorithm developed by Guo et al. 2013. The decision tree algorithm is used to cluster each pixel into two groups (i.e. vegetation and background). The algorithm is originally developed using MatLab by Guo et al. 2013, rewrote using R by Duan et al. 2017.

## Reference

* Guo W, Rage UK, Ninomiya S. 2013. Illumination invariant segmentation of vegetation for time series wheat images based on decision tree model. Computers and Electronics in Agriculture 96, 58–66.
* Duan T, Zheng B, Guo W, Ninomiya S, Guo Y, Chapman S. 2017. Comparison of ground cover estimates from experiment plots in cotton, sorghum and sugarcane based on images and ortho-mosaics captured by UAV. Functional Plant Biology 44, 169-183.
* Guo W, Zheng B, Duan T, Fukatsu T, Chapman S, Ninomiya S. 2017.  EasyPCC: Benchmark datasets and tools for high-throughput measurement of the plant canopy coverage ratio under field conditions. Sensors 17, 798.
