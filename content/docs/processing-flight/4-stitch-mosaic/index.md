---
title: "Stitch mosaic"
author: Bangyou Zheng
date: 2020-07-17
slug: stitch-mosaic
toc: true
authors:
- bangyou-zheng
- chrisbin-james
menu:
  docs:
    parent: processing-flight
    weight: 4
---


Raw images can be stitched into ortho-mosaics using commercial or open source software (e.g. [Pix4D](https://www.pix4d.com/), [PhotoScan](https://www.agisoft.com/) and [OpenDroneMap](https://www.opendronemap.org/)).  

We current only implemented Pix4D into the workflow. You have to purchase your own license from Pix4D to use this step.

{{% alert note %}}
Alternatively, you can skip all previous steps and the stitch mosaic in the workflow through uploading your ortho-mosaic into PhenoCopter. No web interface is implemented as the constrain of internet bandwidth. You can contact system manager to upload your own ortho-mosaic. The same folder structure has to be kept to use further workflows.  
{{% /alert %}}


This workflow only depends on the uploading of raw images. [Extract flight path]({{<ref "../2-extract-flight-path/">}}) and [Add GCPs]({{<ref "../3-add-gcps/">}}) can be skip if you don't need to check quality of raw images and have any GCPs. 


## Stitch othor-mosaic using Pix4D

The new project is generated for Pix4D using information in the workflow [Extract flight path]({{<ref "../2-extract-flight-path/">}}) (disabled images) and [Add GCPs]({{<ref "../3-add-gcps/">}}) (GCPs). 

Three options in Pix4D professional version can be adjusted through web interface.

{{< figure src="options.png" title="Configuring stitching parameters for Pix4D" width="100%" lightbox="true" numbered="true" >}}

* image_scale: full, rapid
* calibration_method: Standard, Alternative, GeolocationAndOrientation
* internal_param_optimization: None, Leading, All, AllPrior

The default parameters should be enough to stitch images in most of cases. Parameters can be adjusted if you notice any problems in the ortho-mosaic. 


## Workflow

Click the `Start` button in the workflow to trigger server to run stitching software. The next workflow [Pyramid retile]({{<ref "../5-pyramid-retile/">}}) will be automatically triggered when this step is finished. The quality report from stitching software is also available.

