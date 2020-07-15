---
title: Workflow with your control
date: 2020-07-15
toc: true
type: docs
weight: 25
slug: workflow
menu:
  docs:
    parent: introduction
    weight: 1
---

<style>
.timeline {
    list-style: none;
    padding: 20px 0 20px;
    position: relative;
}

    .timeline:before {
        top: 0;
        bottom: 0;
        position: absolute;
        content: " ";
        width: 3px;
        background-color: #eeeeee;
        left: 50%;
        margin-left: -1.5px;
    }

    .timeline > li {
        margin-bottom: 20px;
        position: relative;
    }

	.timeline > li:before,
	.timeline > li:after {
		content: " ";
		display: table;
	}

	.timeline > li:after {
		clear: both;
	}

	.timeline > li:before,
	.timeline > li:after {
		content: " ";
		display: table;
	}

	.timeline > li:after {
		clear: both;
	}

	.timeline > li > .timeline-panel {
		width: 46%;
		float: left;
		border: 1px solid #d4d4d4;
		border-radius: 2px;
		padding: 20px;
		position: relative;
		-webkit-box-shadow: 0 1px 6px rgba(0, 0, 0, 0.175);
		box-shadow: 0 1px 6px rgba(0, 0, 0, 0.175);
	}

		.timeline > li > .timeline-panel:before {
			position: absolute;
			top: 26px;
			right: -15px;
			display: inline-block;
			border-top: 15px solid transparent;
			border-left: 15px solid #ccc;
			border-right: 0 solid #ccc;
			border-bottom: 15px solid transparent;
			content: " ";
		}

		.timeline > li > .timeline-panel:after {
			position: absolute;
			top: 27px;
			right: -14px;
			display: inline-block;
			border-top: 14px solid transparent;
			border-left: 14px solid #fff;
			border-right: 0 solid #fff;
			border-bottom: 14px solid transparent;
			content: " ";
		}

	.timeline > li > .timeline-badge {
		color: #fff;
		width: 50px;
		height: 50px;
		line-height: 50px;
		font-size: 1.4em;
		text-align: center;
		position: absolute;
		top: 16px;
		left: 50%;
		margin-left: -25px;
		background-color: #999999;
		z-index: 100;
		border-top-right-radius: 50%;
		border-top-left-radius: 50%;
		border-bottom-right-radius: 50%;
		border-bottom-left-radius: 50%;
	}

	.timeline > li.timeline-inverted > .timeline-panel {
		float: right;
	}

	.timeline > li.timeline-inverted > .timeline-panel:before {
		border-left-width: 0;
		border-right-width: 15px;
		left: -15px;
		right: auto;
	}

	.timeline > li.timeline-inverted > .timeline-panel:after {
		border-left-width: 0;
		border-right-width: 14px;
		left: -14px;
		right: auto;
	}

.timeline-badge.primary {
    background-color: #2e6da4 !important;
}

.timeline-badge.success {
    background-color: #3f903f !important;
}

.timeline-badge.warning {
    background-color: #f0ad4e !important;
}

.timeline-badge.danger {
    background-color: #d9534f !important;
}

.timeline-badge.info {
    background-color: #5bc0de !important;
}

.timeline-title {
    margin-top: 0;
    color: inherit;
}

.timeline-body > p,
.timeline-body > ul {
    margin-bottom: 0;
}

    .timeline-body > p + p {
        margin-top: 5px;
    }

@media (max-width: 767px) {
    ul.timeline:before {
        left: 40px;
    }

    ul.timeline > li > .timeline-panel {
        width: calc(100% - 90px);
        width: -moz-calc(100% - 90px);
        width: -webkit-calc(100% - 90px);
    }

    ul.timeline > li > .timeline-badge {
        left: 15px;
        margin-left: 0;
        top: 16px;
    }

    ul.timeline > li > .timeline-panel {
        float: right;
    }

	ul.timeline > li > .timeline-panel:before {
		border-left-width: 0;
		border-right-width: 15px;
		left: -15px;
		right: auto;
	}

	ul.timeline > li > .timeline-panel:after {
		border-left-width: 0;
		border-right-width: 14px;
		left: -14px;
		right: auto;
	}
}
</style>
<section class="bgfbox">
    <div class="container">
        <ul class="timeline">
            <li>
                <div class="timeline-badge"><i class="glyphicon glyphicon-info-sign"></i></div>
                <div class="timeline-panel">
                    <div class="timeline-heading">
                        <h4 class="timeline-title">Create meta data</h4>
                    </div>
                    <div class="timeline-body">
                        <p>Create farm, field and flight to manage meta information.</p>
                    </div>
                </div>
            </li>
            <li class="timeline-inverted">
                <div class="timeline-badge"><i class="glyphicon glyphicon-picture"></i></div>
                <div class="timeline-panel">
                    <div class="timeline-heading">
                        <h4 class="timeline-title">Upload images</h4>
                    </div>
                    <div class="timeline-body">
                        Upload all images in a flight through web or transfer to storage.
                    </div>
                </div>
            </li>
            <li>
                <div class="timeline-badge"><i class="fas fa-wave-square"></i></div>
                <div class="timeline-panel">
                    <div class="timeline-heading">
                        <h4 class="timeline-title">Extract image information</h4>
                    </div>
                    <div class="timeline-body">
                        <p>The image information is extracted by cluster and visualized to show flight path and raw images.</p>
                    </div>
                </div>
            </li>
            <li class="timeline-inverted">
                <div class="timeline-badge"><i class="fas fa-map-marker-alt"></i></div>
                <div class="timeline-panel">
                    <div class="timeline-heading">
                        <h4 class="timeline-title">Add ground control point</h4>
                    </div>
                    <div class="timeline-body">
                        <p>Ground control points are manually added into raw images.</p>
                    </div>
                </div>
            </li>
            <li>
                <div class="timeline-badge"><i class="fas fa-object-group"></i></div>
                <div class="timeline-panel">
                    <div class="timeline-heading">
                        <h4 class="timeline-title">Stitch ortho-mosaic</h4>
                    </div>
                    <div class="timeline-body">
                        <p>All raw images are stitched together using all information above and specified parameters.</p>
                    </div>
                </div>
            </li>
            <li class="timeline-inverted">
                <div class="timeline-badge"><i class="fas fa-map"></i></div>
                <div class="timeline-panel">
                    <div class="timeline-heading">
                        <h4 class="timeline-title">Generate pyramid retile</h4>
                    </div>
                    <div class="timeline-body">
                        <p>All ortho-mosaic and vegetative index are retiled for online visualization.</p>
                    </div>
                </div>
            </li>
            <li>
                <div class="timeline-badge"><i class="fas fa-th"></i></div>
                <div class="timeline-panel">
                    <div class="timeline-heading">
                        <h4 class="timeline-title">Segment plots</h4>
                    </div>
                    <div class="timeline-body">
                        <p>Plots are created using drawing tools and copied from flights in the same field. The reverse calculation is used to segment undistorted images.</p>
                    </div>
                </div>
            </li>
            <li class="timeline-inverted">
                <div class="timeline-badge"><i class="fas fa-map"></i></div>
                <div class="timeline-panel">
                    <div class="timeline-heading">
                        <h4 class="timeline-title">Label for machine learning</h4>
                    </div>
                    <div class="timeline-body">
                        <p>Labeling ortho-mosaic and raw images in arbitrary groups which can be used in machine learning using online drawing tools.</p>
                    </div>
                </div>
            </li>
            <li>
                <div class="timeline-badge"><i class="fas fa-seedling"></i></div>
                <div class="timeline-panel">
                    <div class="timeline-heading">
                        <h4 class="timeline-title">Extract phenotypic values</h4>
                    </div>
                    <div class="timeline-body">
                        <p>Phenotypic values are extracted using pre-defined functions and applied for each vegetative index.</p>
                    </div>
                </div>
            </li>
        </ul>
    </div>
</section>

