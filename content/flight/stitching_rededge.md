---
title: "Stitching (RedEdge images)"
author: "Sophie Chen"
date: "15/07/2019"
slug: stitching_rededge
weight: 2
tags:
  - stitching
output:
  blogdown::html_page:
    toc: false
---

The final object is to creat an *ortho-mosaic* for **RedEdge images** by taking the following procedures.

This process consists of uploading images through this website and manually running Pix4D software.

## Upload images

This step is the same to [uploading RGB images](stitching.html#upload-images).

## Run Pix4D for performing other steps

A useful tutorial video: [How to Process MicaSense Sensor Data in Pix4D] (https://support.micasense.com/hc/en-us/articles/115000831714-How-to-Process-MicaSense-Sensor-Data-in-Pix4D)

### Create a new project

Open Pix4D sofeware, and click **New Project ...** to open the interface for creating a new project. To complete the creation of a new project, several steps need to be finished one by one:

- set path and name of the project

<img src="stitching_rededge/1-new project.png" width="30%"/>

- select images for processing

Add directories              |  Import images            |  Read images
:-------------------------:|:-------------------------:|:-------------------------:
![](stitching_rededge/2-import images.png)   | ![](stitching_rededge/3-import images.png)  | ![](stitching_rededge/4-read images.png)

- set image properties, output coordinate system, process template

Image properties           | Output coordinate system  | Process option template
:-------------------------:|:-------------------------:|:-------------------------:
![](stitching_rededge/6-image properties.png)   | ![](stitching_rededge/7-coordinate system.png)  | ![](stitching_rededge/8-select a template.png)

### Adjust processing options

- Select *Processing optioms* -> *1.Initial Processing* -> *Calibration*, choose **All Prior** on the drop-down list of *Internal Parameters Optimization*.

<img src="stitching_rededge/9-change processing options-Internal Parameters Optimization.png" width="30%"/>

- Calibrate reflectance: Select *Processing optioms* -> *3.DSM,Orthomosaic and Index* -> **Index Calculation**, choose **Camera Only** as *Correction Type*, Click *Calibrate...* to open the pop-up window, then import the corresponding band image using the *Brown* button, complete the reflectance calibration by drawing a rectangle on the calibration panel and inputting the reflectance factor of this band.

<img src="stitching_rededge/10-calibration one by one.png" width="30%"/>

- Set raster output option

<img src="stitching_rededge/11-set raster ouput.png" width="30%"/>


### Add GCPs

