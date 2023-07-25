---
layout: post
title:  "Launch of DeepMIP-Eocene app"
date: 2023-04-05
description: "New interactive web app for streamlined data access"
tags: visualisations code
thumbnail: assets/img/deepmip-0.png
---

I built a new interactive, open-access web application to simplify access to the [DeepMIP-Eocene model databse](https://www.deepmip.org/data-eocene/) for non-programmers. The current version is available at [data.deepmip.org](https://data.deepmip.org/) and will be part of the upcoming of the Database description publication.

## Motivation
The DeepMIP-Eocene model database includes coordinated climate model output from eight modelling centres around the world, providing essential reference data for the paleoclimate community. Still, downloading and analysing large, global netCDF datasets presents a challenge for many potential users in our community. In addition, common tasks like model-data comparisons actually only need access to a very small subset of the global database and programming routuines that can be easily automated. For these reasons, the DeepMIP-Eocene app provides intuitive, browser-based access the model database to perform model-data comparisons of common variables (temperature, precipitation) and plotting of interactive charts and maps.

## Usage 
The app enables users without programming experience to extract common variables such as temperature, precipitation, etc., from all DeepMIP models at any specified location. Batch processing of sites is possible and example sets of locations from the DeepMIP-Eocene proxie database [(Hollis et al., 2019)](https://gmd.copernicus.org/articles/12/3149/2019/) are available to get started. The extracted data can be visualized and downloaded in CSV/Excel format for offline model-data comparison. The individual Python processing and analysis functions are saved in deepmip_modules.py and may also serve as a launchpad for more advanced offline analyses. Example screenshots of the possibilities are shown below. 

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/deepmip-2.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
   Overview of available model simulations.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/deepmip-3.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
   Table view of extracted model temperatures at the specified site. Data can be exported (CSV/XLSX/JSON) for further processing.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/deepmip-4.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
   Interactive visualisation of extracted model data at a single location. Charts can be interrogated online or downloaded.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/deepmip-5.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
   Eocene paleogeography with paleolocations of example sites.
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/deepmip-6.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
   Paleolocation of single site and comparison of regional paleogeographies in individual models.
</div>

## Technical Details
The web app was built with Streamlit, which is an open-source Python library that makes it easy to create custom web apps for machine learning and data science. All processing and plotting is implemented in pure Python with all underlying functions available to start/modify your own analysis. All code is open access and available on [GitHub](https://github.com/sebsteinig/deepmip-eocene-app).