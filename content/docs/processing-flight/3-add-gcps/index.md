---
title: "Add GCPs"
author: Bangyou Zheng
date: 2020-07-17
slug: add-gcps
toc: true
menu:
  docs:
    parent: processing-flight
    weight: 3
---
# Adding GCPs
Once the flight path has been extracted the next step is to mark the location of the GCPs in the images. 
- Make sure the "View Flight Path" is enabled  under the Stitching menu. Click on the "Add GCPs" option to expand the menu.
![](resources/M.JPG)

- Click on the "Select an EPSG" dropdown list to select and specify the EPSG Coordinate system to use. 
-   Upload a CSV containing the Coordinates of the GCPs with the following order of values
    - GCP ID
    - Longitude
    - Latitude
    - Height
- After uploading the CSV file containing the GCP locations they should appear on the flight path. Select the GCP from the list to be marked in images, this will highlight the selected GCP in the Flight path.
![](resources/GCPH.JPG)
- Click on a image around the GCP to open the image, click on the "ADD a new point as GCP" button from the options list on top.
-![](resources/AGCP.JPG)
- Click on the location of GCP inside the image to finishing marking the GCP
-![](resources/AP.png)
- Repeat the above steps for each GCP, and add a minimum of 2-3 images per GCP
- When finished adding images for all GCPs, click on the Add GCP option and then click on marked as finish
![](resources/MAF.JPG)

