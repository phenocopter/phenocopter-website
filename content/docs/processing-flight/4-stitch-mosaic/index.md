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


After finishing uploading the GCPs and marking them in images the next step is to is to start the stitching process for genrating the othomosaic. (make sure the GCP step is finished before proceeding)

{{< figure src="finished-gcp.png" title="finished adding GCPs" width="50%" lightbox="true" numbered="true" >}}

- Click on the "Stitching for Ortho-mosaic" option to expand it, followed by clicking on the "Stitching Mosaic" option to exapnd and the set the configuration parameters for stitching the orthomosaic. 
-   Click on the drop down list for every stitching option and set the following configuration parameters 
    - image_scale: Rapid
    - calibration_method: Alternative
    - internal_param_optimization: AllPrior

{{< figure src="stitching-options.png" title="Configuring stitching parameters" width="50%" lightbox="true" numbered="true" >}}
- After configuring the stitching options select "start" to begin the stitching process for the ortho mosaic

{{< figure src="start-stitching.png" title="Start Stitching" width="50%" lightbox="true" numbered="true" >}}
