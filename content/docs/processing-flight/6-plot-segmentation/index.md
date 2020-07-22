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

**Row** and **Column** refer as the experiment layout and have the alternative names in some of experiment design tools (e.g. **Range** and **Plot**). 

**Gap** in Row and Column is used if the layout has a big gap in the row and column. The unit of Gap is the ratio along the Row and Column. However, it will be better to keep the gaps to calculate the height with DSM. The **Trim** can be used the same purpose, but keep the gaps in the further analysis.

**Plot** refers as the individual plot in a trial and is identified by **Row** and **Column** in the experiment layout.  

**Trim** is used to remove parts of plot in the further calculation depending on the functions. See workflow [extract phenotypic values]({{<ref "../7-extract-phenotype">}}) for more details. 

---

In each flight, multiple trials can be defined using methods below. The trial names have to be unique and only contain alphabet, number and underscore. The unique name is automatically generated when a trial is created. The name can be changed through clicking the title of each trial. There are no links between trials and methods to generate these trials.
A trial is defined as a group of plots. Here two methods are provided to generate a trial.


## Create new plots from boundary

### Create a new boundary

The boundary method can be used if the experiment layout is a regular rectangle (i.e. quadrilateral in general). The boundary can be defined for whole block through drawing a polygon in the four corners.

Before drawing a boundary, you will need to determine

* The starting corner of your experiment layout (**Row 1 and Column 1** in general)
* The direction of Row and Column
* The number of Rows and Columns

Steps to create a new boundary

1. Edit the information in the new boundary area and click **New Boundary** button. 
{{< figure src="new-boundary.png" title="Create a new boundary" width="50%" lightbox="true" numbered="true" >}}

2. A **blue cursor** is showing if mouse overs the map.
3. Click the first point at the starting corner (**Row 1 and Column 1** in general)

{{< figure src="boundary-1.png" title="Click the first/starting corner" width="50%" lightbox="true" numbered="true" >}}

4. Click the second point along the **Column** side. 

{{< figure src="boundary-2.png" title="Click the second corner" width="50%" lightbox="true" numbered="true" >}}

5. Click the third point at the diagonal direction of the first point.

{{< figure src="boundary-3.png" title="Click the third corner" width="50%" lightbox="true" numbered="true" >}}

6. Click the forth/final point at the diagonal direction of the second point. The polygon will automatically close and segment the whole polygon according to parameters.

{{< figure src="boundary-4.png" title="Click the forth/final corner" width="50%" lightbox="true" numbered="true" >}}

7. Click **Save** button to save the polygon. 

### Edit a boundary

After a new boundary is created, a boundary panel is added into Boundary tab. The boundary polygon is separated into the number or row and columns (Row + 1 and Column + 1 lines in two directions of polygon). No plot polygons are created in this step.

Now you can 

1. Edit the boundary name by clicking the title of panel. The boundary name has to be unique in each flight and only contain alphabet, number and underscore. 
2. Edit the parameters in the input boxes. The layout will be automatically updated. 
3. Adjust colors for the boundary and gaps. The new colors are saved into system and are retrieved when page reloads.
4. Delete boundary from system. The created new plots are kept.
5. Edit boundary. A **Blue cursor** is showing when mouse moves over corners. You can drag the corner and drop into a new place to update the boundary. Zoom into your ortho-mosaic provide more accurate position of corners. 

{{< figure src="edit-boundary-1.png" title="Editing boundary" width="50%" lightbox="true" numbered="true" >}}

6. Edit gaps. A **blue cursor** is showing when mouse moves over to intersection of lines. You can drag the intersection and drop to edit gaps. Be carefully to use this feature as you might get strange polygons for plots.

{{< figure src="edit-gaps-1.png" title="Editing gaps" width="50%" lightbox="true" numbered="true" >}}

7. Create new plots from boundary by clicking **New Plot** button. 


{{% alert note %}}
The **Undo** and **Redo** at the top of map can be used during editing boundary and gaps.
{{< figure src="map-buttons.png" title="Redo and unto buttons" width=30%" lightbox="true" numbered="true" >}}

{{% /alert %}}


{{% alert warning %}}
**Edit boundary** will overwrite any changes of **edit gaps**. 

There are no link between boundary and trials after new plots are created. Any editing of plots will be lost if new plots are created from same boundary.
{{% /alert %}}


## Copy plots from other flights

If the [ground control points ]({{<ref "../../getting-started/gcp/">}}) are used in the same field (i.e. experiment in a season) and added into each flight, the plot segmentations can be copied from other flights.

After switching to the **Flight** tab in the **Source** panel, the dropdown menu shows a list of flights which have the plot segmentation in the same field. 

{{< figure src="copy-flight-list.png" title="List of flights with plot segmentation" width=50%" lightbox="true" numbered="true" >}}

You can switch the flight to show the list of plot segmentation and update the map to show all plots. The check boxes at the left can be used to select the trials. Finally, the **Copy plots** button is used to copy the plots into this flight.

{{< figure src="copy-flight-map.png" title="List of flights with plot segmentation" width=80%" lightbox="true" numbered="true" >}}



## Inject plots using RESTAPI

If you have the plot segmentation in the geojson format, you can use the **RESTAPI** to POST your data into flight. See the API documentation for details.

## Edit plots

In the trial panel, you can setup the trim in the row and column directions, change the color of plots and plots with trims, delete trial, and edit plots. 

{{< figure src="trials-list.png" title="Trial panel in the list" width=50%" lightbox="true" numbered="true" >}}

Plots can be edited in the **Trials** panel. The edit feature is implemented using [transform feature](https://viglino.github.io/ol-ext/examples/interaction/map.interaction.transform.html) in the [ol-ext](https://viglino.github.io/ol-ext/index.html) library to scale, translate, rotate and stretch the selected plots. See [ol-ext documentation](https://viglino.github.io/ol-ext/examples/interaction/map.interaction.transform.html) for details.

After clicking the **Edit** button under each trial panel, you can select a single plot by mouse click on the map, then single row, single column and all plots through button at the top of map. The edit can be undo and redo using the buttons at the top of map.  

{{< figure src="trials-edit-selection.png" title="Selection of plots to edit" width=100%" lightbox="true" numbered="true" >}}


After editing, you can **Save** or **Cancel** all changes.
