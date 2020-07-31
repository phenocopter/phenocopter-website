---
title: "Extract flight path"
author: Bangyou Zheng
date: 2020-07-17
slug: extract-flight-path
toc: true
authors:
- bangyou-zheng
menu:
  docs:
    parent: processing-flight
    weight: 2
---

## Workflow

This workflow **Extract image information** does not require user inputs. This step will be automatically triggered when images are uploaded from web interface, but manually triggered if images directly copied into data storage. In the server side, image information are extracted from all uploaded images including 

* Latitude
* Longitude 
* Elevation
* Width
* Height
* Capture time

Images without location information are ignored. The images in a single shutter (i.e.  the same location) are grouped together (e.g. multiply spectral camera). 


{{% alert warning %}}
The thermal camera (e.g. Flir Tau2) might capture multiple images in a second which have the same GPS location. These images are grouped to view them on the flight path.
{{% /alert %}}


## View flight path

The flight path is rendered on the map using [openlayers](https://openlayers.org/) with points for the image locations and line string which is colored by the flight elevation. The flight elevation also is available in the panel at the top right corner. Hovering mouse over the elevation figure shows a star on the map and value of flight height.

{{< figure src="flight-path.png" title="Example of flight path" width=80%" lightbox="true" numbered="true" >}}

## View raw images

The raw image is rendered on the map using [openlayers](https://openlayers.org/)  through clicking each point on the flight path. Images can be switched if there are multiple image in the same locations. The images are tiled using [vips](https://iipimage.sourceforge.io/documentation/images/) and served with [IIPImage](https://iipimage.sourceforge.io/documentation/server/) for high performance rendering on the web browser.

{{< figure src="view-raw-image.png" title="View raw image" width=80%" lightbox="true" numbered="true" >}}

## Disable and enable images

Images with bad quality can be disabled for the further analysis at viewing raw images. There are 6 buttons at the top of images to disable/enable images.

* Disable all images before
* Disable this image
* Disable all images after
* Enable all images before
* Enable this image
* Enable all images after

{{< figure src="disable-img.png" title="Images disabled for further analysis" width=50%" lightbox="true" numbered="true" >}}
