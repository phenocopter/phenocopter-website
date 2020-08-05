---
title: "Workflow"
author: Bangyou Zheng
date: 2020-07-31
slug: workflow
toc: true
authors:
- bangyou-zheng
menu:
  docs:
    parent: restapi
    weight: 2
---


The status of workflow can be changed by RESTAPI. The R pcakge [PhenoCopterAPI](https://github.com/phenocopter/PhenoCopterAPI) is a wrapper of PhenoCopter API. 


## Update the status for a field

In the example below, we trigger the workflow to `archive` all flights in a field. See [workflow status]({{<ref "../../processing-flight">}}) for all status can be set, 


```r

# Load package
library(tidyverse)
library(PhenoCopter)

# Login PhenoCopter
pc_options(host = Sys.getenv('PC_HOST'),
           email = Sys.getenv("PC_EMAIL"),
           password = Sys.getenv("PC_PASSWORD"))
pc_login()

# List of flights
flights <- get_flights()

# Filter field by ID
field_flights <- keep(flights, function(x) {
    x$fieldId == 999999
})

# Update status for each flight
for (i in seq(along = field_flights)) {
	# Get the workflow
    workflow <- get_flight_workflow(flight = field_flights[[i]]$id)
	# Filter workflow "archive"
    workflow_archive <- keep(workflow, function(x) {
        x$workflow$name == 'archive'
    }) %>%
        magrittr::extract2(1)
	
	# Check the status is "wait"
    if (workflow_archive$status$name == "Wait") {
		# Set the status as processing (3)
        workflow <- list(id = workflow_archive$id,
                         flightId = field_flights[[i]]$id,
                         workflowId = workflow_archive$workflowId,
                         statusId = 3)
        a <- put_flight_workflow(flight = field_flights[[i]]$id,
                                 id = workflow_archive$id,
                                 workflow = workflow)
    }
}

```
