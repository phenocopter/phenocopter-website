---
title: "Add GCPs"
author: Bangyou Zheng
date: 2020-07-17
slug: add-gcps
toc: true
authors:
- bangyou-zheng
- chrisbin-james
menu:
  docs:
    parent: processing-flight
    weight: 3
---

The [ground control points ]({{<ref "../../getting-started/gcp/">}}) provide accurate survey of an field during growth season, and can be added into system through the web interface and used in the [stitching software]({{<ref "../4-stitch-mosaic">}}) after [flight path]({{<ref "../2-extract-flight-path">}}) is extracted. 


The **Flight path** and **Add GCPs** panels should be open in the left toolbar with the viewable flight path on the map. 

{{< figure src="view-flight-path.png" title="View flight path" width="50%" lightbox="true" numbered="true" >}}



## Find EPSG

EPSG Geodetic Parameter Dataset (also EPSG registry) is a public registry of spatial reference systems, Earth ellipsoids, coordinate transformations and related units of measurement. EPSG reference list can be found from [spatialreference](https://spatialreference.org/ref/epsg/).

* If your GCPs are latitude and longitude, The EPSG might be `4326` for WGS84
* If you use [AeroPoints](https://www.propelleraero.com/aeropoints/) as GCPs, you can download `CSV (Simple)` format from propeller website and find the EPSG in the section `Coordinate Systems`. 

{{< figure src="epsg-aeropoints.png" title="Find EPSG from aeropoint website" width="100%" lightbox="true" numbered="true" >}}


- Click on the "Select an EPSG" dropdown list to select and specify the EPSG Coordinate system to use.
{{< figure src="update-epsg.png" title="Selection of EPSG" width="50%" lightbox="true" numbered="true" >}}

## Import CSV file

-   Upload a CSV containing the Coordinates of the GCPs with the following order of values
    - GCP ID
    - Longitude
    - Latitude
    - Height
- After uploading the CSV file containing the GCP locations they should appear on the flight path. Select the GCP from the list to be marked in images, this will highlight the selected GCP in the Flight path.


{{< figure src="uploading-csv.png" title="Uploading CSV file" width="50%" lightbox="true" numbered="true" >}}

## Add and delete GCPs on the raw image

- Click on a image around the GCP to open the image, click on the "ADD a new point as GCP" button from the options list on top.


{{< figure src="raw-image.png" title="Add a new point as GCP" width="50%" lightbox="true" numbered="true" >}}


- Click on the location of GCP inside the image to finishing marking the GCP


{{< figure src="adding-new-point.png" title="Add a new point" width="50%" lightbox="true" numbered="true" >}}

- Repeat the above steps for each GCP, and add a minimum of 2-3 images per GCP
- When finished adding images for all GCPs, click on the Add GCP option and then click on marked as finish

{{< figure src="workflow.png" title="Mark workflow as finish" width="50%" lightbox="true" numbered="true" >}}


## Workflow

This workflow **Add GCPs** is a manual step and can be skip if the flight don't have any GCPs. This step has to be `Mark as Finish` when all GCPs are added.

