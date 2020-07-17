---
title: "Plot segmentation"
author: Bangyou Zheng
date: 2020-07-17
slug: plot-segmentation
toc: true
menu:
  docs:
    parent: processing-flight
    weight: 6
---


Segmentation of the ortho-mosaics into individual plots are key step to calculate phenotypic values for experiments in breeding and agriculture. The manual step requires users interactively create plots on the web interface or inject plots from RESTAPI. 





## Terminology

---

**Source** is the method to create plots. PhenoCopter implements two methods (i.e. boundary of experiment and flight from in the same field).

**Trial** is a group of plots which refers to whole experiment, a block of experiment or any part of experiments. Trial name have to unique in each flight.

**Boundary** is the outline of an experiment layout and can further segment into individual plots. A boundary is quadrilateral and defined by ***four*** corners. 

**Plot** refers as the individual plot in a trial and is identified by **Row** and **Column** in the experiment layout.  

**Row** and **Column** refer as the experiment layout and have the alternative names in some of experiment design tools (e.g. **Range** and **Plot**). 

---


In each flight, multiple trials can be defined using methods below. The trial names have to be unique and only contain alphabet, number and underscore. The unique name is automatically generated when a trial is created. The name can be changed through clicking the title of each trial. There are no links between trials and methods to generate these trials.
A trial is defined as a group of plots. Here two methods are provided to generate a trial.


## Manually create boundary 

### Create a new boundary

The boundary method can be used if the experiment layout is a regular rectangle (i.e. quadrilateral in general). The boundary can be defined for whole block through drawing a polygon in the four corners.



{{< figure src="new-boundary.png" title="Create a new boundary" width="50%" lightbox="true" numbered="true" >}}

### Edit a boundary

Methods to generate trials

### Create new plot

## Copy from other flights

## Inject plots using RESTAPI


## Edit plots


{{% alert warning %}}
There are no link between boundary and trials after new plots are created. Any editing of plots will be lost if new plots are created from boundary.
{{% /alert %}}




