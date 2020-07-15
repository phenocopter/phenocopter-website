+++
widget = "featurette"  # See https://sourcethemes.com/academic/docs/page-builder/
headless = true  # This file represents a page section.
active = true  # Activate this widget? true/false
weight = 20  # Order that this section will appear.

[[feature]]
  icon = "info"
  icon_pack = "fas"
  name = "Manage flights"
  description = """[Meta data](/docs/introduction/meta/) of UAV (Unmanned Aerial Vehicle) flights organize using farm and field, store related drone and camera information, and share with other users with read only or write permissions."""
  
[[feature]]
  icon = "sort-amount-down-alt"
  icon_pack = "fas"
  name = "Process images in a workflow"
  description = "Data processing is split into 9 steps with a sequential workflow. The workflows are manually or automatically, could be restarted at the any points and processed in the high performance cluster. An email notification is sent to all users with write permission when a workflow is finished and failed."
  
[[feature]]
  icon = "camera"
  icon_pack = "fas"
  name = "Support multiple types of cameras"
  description = "Different types of cameras are supported to process including visual cameras, multi-spectral cameras (e.g. [RedEdge](https://www.micasense.com/rededge-mx), [Altum](https://www.micasense.com/altum) and [AirPhen](https://www.hiphen-plant.com/our-solutions/airphen/)), thermal cameras (e.g. [Tau2](https://www.flir.com.au/products/tau-2/), [TEAX ThermalCapture Fusion](https://thermalcapture.com/thermalcapture-fusion-beyond-drone-thermal-imaging/) and [ZENMUSE XT](https://www.dji.com/au/zenmuse-xt)). New camera types could be easily added."    

[[feature]]
  icon = "images"
  icon_pack = "fas"
  name = "View and work on raw images"
  description = "High quality raw images are displayed along the flight path in the map and are viewable and zoomable for high performance. More components are added to image viewer including ground control points, plot segmentation and labeling."    

  
[[feature]]
  icon = "leaf"
  icon_pack = "fas"
  name = "Calculate vegetative indexes"
  description = "Lots of vegetative indexes (VIs) are calculated for each type of camera (i.e. visual, multispectral and thermal). All VIs are viewable and zoomable in a map for high performance."    


[[feature]]
  icon = "th"
  icon_pack = "fas"
  name = "Segment field into plots"
  description = "The whole field can be split into individual plot for breeding and agronomy trials through multiple methods, e.g. defining the boundary of blocks, copying from other flights in the same field, importing from external files. The plots are stored as GEOJSON format for post-processing."    
  
[[feature]]
  icon = "map"
  icon_pack = "fas"
  name = "Label images and ortho-mosaics"
  description = "Raw images and ortho-mosaics can be labeled with any number of groups for machine learning using easy-to-use tools including point, box, line and polygon."    
  
[[feature]]
  icon = "seedling"
  icon_pack = "fas"
  name = "Extract phenotypic values"
  description = "Phenotypic values are extracted for each plot in all vegetative indexes using predefined functions in the system (e.g. basic statistics of each plot, ground coverage). More traits will be added soon."    
  
[[feature]]
  icon = "eye"
  icon_pack = "fas"
  name = "View and process images at any places"
  description = "Images captured by UAV process on the cloud with a few clicks and are visualized on the web browser. All intermediate and final outputs can be accessed from any devices at any places (e.g. computers, tablets or mobiles)."    
  
+++