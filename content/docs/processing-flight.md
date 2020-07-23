---
title: Processing flight in a workflow
date: 2020-07-16
toc: true
type: docs
authors:
- bangyou-zheng
slug: processing-flight
---


After a new flight is created, there are seven steps to process a flight from raw images to phenotypic values. Some steps require user interaction through web interface, and other can be automatically processed in the server side. 

## Workflow overview

1. **[Upload images]({{<ref "processing-flight/1-upload-images">}})**: Upload all images in a flight through web or transfer to storage.
2. **[Extract image information]({{<ref "processing-flight/2-extract-flight-path">}})**: The image information is extracted by cluster and visualized to show flight path and raw images.
3. **[Add ground control point]({{<ref "processing-flight/3-add-gcps">}})**: Ground control points are manually added into raw images.
4. **[Stitch ortho-mosaic]({{<ref "processing-flight/4-stitch-mosaic">}})**: All raw images are stitched together using all information above and specified parameters.
5. **[Generate pyramid retile]({{<ref "processing-flight/5-pyramid-retile">}})**: All ortho-mosaic and vegetative index are retiled for online visualization.
6. **[Segment plots]({{<ref "processing-flight/6-plot-segmentation">}})**: Plots are created using drawing tools and copied from flights in the same field. The reverse calculation is used to segment undistorted images.
7. **[Extract phenotypic values]({{<ref "processing-flight/7-extract-phenotype">}})**: Phenotypic values are extracted using pre-defined functions and applied for each vegetative index.


## Workflow status

* Wait
* Ready
* Schedule
* Processing
* Finish

{{< figure src="workflow.png" title="Workflow for a flight" numbered="true" lightbox="true" >}}

## Workflow notification and logs



