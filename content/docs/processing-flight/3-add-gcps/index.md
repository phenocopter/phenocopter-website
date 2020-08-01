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


## Add/Change EPSG

EPSG Geodetic Parameter Dataset (also EPSG registry) is a public registry of spatial reference systems, Earth ellipsoids, coordinate transformations and related units of measurement. EPSG reference list can be found from [spatialreference](https://spatialreference.org/ref/epsg/).

* If your GCPs are latitude and longitude, The EPSG might be `4326` with WGS84. Check with your GCPs providers.
* If you use [AeroPoints](https://www.propelleraero.com/aeropoints/) as GCPs, you can download `CSV (Simple)` format from propeller website and find the EPSG in the section `Coordinate Systems`. 

{{< figure src="epsg-aeropoints.png" title="Find EPSG from aeropoint website" width="100%" lightbox="true" numbered="true" >}}


* If you use [Trimble RTK](https://geospatial.trimble.com/products-and-solutions/gnss-systems), you can check the output coordinates system in the Trimble.


**Steps to add/change EPSG in PhenoCopter**
* Click on the `Select an EPSG` to show the dropdown menu and search input.
* Start to type the EPSG in the search input. The available EPSGs are listed if the input chapracters are not less than 4.
* Select your EPSG in the list to confirm.

{{< figure src="update-epsg.png" title="Selection of EPSG" width="50%" lightbox="true" numbered="true" >}}

## Import CSV file

GCPs can be upload into PhenoCopter from a `csv` file. Currently we only support csv file with three/four columns. 

* For csv file with three columns: X, Y, Z or longitude, latitude, elevation
* For csv file with four columns: id, X, Y, Z or id, longitude, latitude, elevation


{{< figure src="gcp-example-csv.png" title="An example CSV file downloaded from AeroPoint" width="50%" lightbox="true" numbered="true" >}}

{{% alert warning %}}
The header is ignored at importing so it does not matter about the column name. Keep the correct column order. 
{{% /alert %}}

After CSV file imported, the GCP markers are listed in the **Add GCP** panel and shown on the map. The GCPs are named from A to Z with the order in the csv file. The color of GCP can be adjusted and stored into PhenoCopter through the color box at the bottom of GCP list. 

{{< figure src="uploading-csv.png" title="Uploaded GCPs from CSV file" width="90%" lightbox="true" numbered="true" >}}


## Add or delete GCPs on the raw image

### Add new GCP on the raw image

1. Select a GCP in the GCP list. The corresponding marker on the map will be highlighted with larger size.

{{< figure src="gcp-select-point.png" title="Select a GCP from list" width="90%" lightbox="true" numbered="true" >}}

2. Click the point on the flight path which is close to the selected GCP to open the [image viewer]({{<ref "../2-extract-flight-path/">}}). Make sure `Raw image` is selected in the layer selector of top-right corner as there are multiple types of images are generated during data processing. 

{{< figure src="raw-image.png" title="Raw image viewer" width="50%" lightbox="true" numbered="true" >}}

3. Using the zoom feature (middle mouse button, toolbar at the bottom, or double click of left button of mouse) to zoom into your GCP. 


{{< figure src="raw-image-zoom.png" title="Zoom into GCP on raw image" width="50%" lightbox="true" numbered="true" >}}

4. Click the tool `Add a point as GCP` at the top of map (the last item at the toolbar, red circle at the figure above), then mouse will transfer into a blue point.

5. Click the center of GCP (or the measured point at GCP) to add a new GCP. A new marker is created at GCP using the same symbol with selected GCP. 

{{< figure src="adding-new-point.png" title="Add a new GCP point on the raw image" width="50%" lightbox="true" numbered="true" >}}

6. Switch another images to add the same GCP through 1) closing the current image and open another one, or 2) clicking the previous and next buttons at the bottom of map.

7. Repeat the above steps for other GCPs and add GCP on a minimum of 2-3 images

### Modify or delete GCP on the raw image

In Step 4 above, click the tool `Modify or delete GCP` at the top of map. 

1. Click on marker to select GCP.
2. Hold down the mouse left button and drag marker to move GCP.
3. Click the delete button at the toolbar to delete GCP. 

{{< figure src="modify-delete-gcp.png" title="Modify or delete a GCP on raw image" width="50%" lightbox="true" numbered="true" >}}

## Workflow

This workflow **Add GCPs** is a manual step and can be skip if the flight don't have any GCPs. This step has to be `Mark as Finish` when all GCPs are added.

