---
title: Deployment
date: 2020-07-16
toc: true
type: book
authors:
- bangyou-zheng
slug: deployment
---

## Infrastructure 

The specification of all components below depending on the number of flight you would like to process everyday. 

The specification below is the infrastructure we use in the demo website
* **MySQL database server** requires enough disk space to store data all phenotypic data.
* **Data store** to store all all images and outputs. We used 40TB about 1000 flights. 
* **Web server** for front end (PhenoCopter website) and geoserver for sering ortho-mosaics. We use 2 cpus with 20GB memory.  
* Windows software to run stitching software which requires a good GPU with enough memory.
* Linux cluster to run workflow except stitching process



