---
layout: post
title:  "DeepMIP database overview paper"
date: 2023-12-05
description: "Paper describing the database and web application submitted to Scientific Data"
tags: visualisations code
thumbnail: assets/img/database-scores.png
---

<div class="row justify-content-sm-center">
    <div class="col">
        {% include figure.html path="assets/img/scientific-data.jpeg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>


I am happy to announce the submission of our new overview paper "The DeepMIP-Eocene model database and interactive web application versions 1.0".

## Motivation
The model results of the coordinated Deep-Time Model Intercomparison Project (DeepMIP; [https://www.deepmip.org](https://www.deepmip.org)) have been used in many studies so far. Until now, the data were hosted at the University Bristol and users had to register in order to access it. We want to make access to and use of the data as easy as possible for anyone who is interested. We therefore revisited the data, applied a new, consistent naming convention across all models and wrote an overview paper as a technical documentation of the dataset. We also introduced a new metric to check the internal consistency of the dataset to flag any potential post-processing issues and inconsistencies between individual models (Fig. 1). The abstract gives a good overview of the
aim of the paper:

>Paleoclimate model simulations provide reference data to help interpret the geological record and offer a unique opportunity to evaluate the performance of current models under diverse boundary conditions. Here, we present a database of 35 climate model simulations of the warm early Eocene Climatic Optimum (EECO; ∼ 50 million years ago) and corresponding preindustrial reference experiments. To streamline the use of the data, we apply standardised naming conventions and quality checks across eight modelling groups that have carried out coordinated simulations as part of the Deep-Time Model Intercomparison Project (DeepMIP). Gridded model fields can be downloaded from an online repository or accessed through a new web application that provides interactive data exploration. Local model data can be extracted in CSV format or visualised online for streamlined model-data comparisons. Additionally, processing and visualisation code templates may serve as a starting point for advanced analysis. The database and online platform aim to simplify accessing and handling complex data, prevent common processing issues, and facilitate the sharing of climate model data across disciplines.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/database-scores.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
   Figure 1: Technical validation of atmospheric global model fields of the x3 experiment across the ensemble. Variables with multiple vertical levels are shown for the respective model pressure level closest to 500 hPa.
</div>

## Web application
A very common use case of the data will be be the comparison with existing and new geochemical reconstructions of the early Ecoene climate (e.g. surface temperature, precipitation). This will be helpful to both validate the model simulations and to test the global relevance of any local reconstruction data. This model data-data comparison normally involves downloading the global model data, interpolating the data to a common horizontal grid, reconstructing the paleoposition of the site of interest and finally extracting the model data at the closest grid point to this paleoposition. All these steps can now now be performed interactivaley on our new web application at [https://data.deepmip.org](https://data.deepmip.org). We think this will greatly streamline this common analysis task and enable a quantitative comparison without writing any code. The web app was built with Streamlit, which is an open-source Python library that makes it easy to create custom web apps based on your Python code. See the related [blog post](/blog/2023/DeepMIP-app/) for more info. All code is open access and available on [GitHub](https://github.com/sebsteinig/deepmip-eocene-app).

## Get the data and paper
The submitted (non-peer reviewed) paper can be viewed [here](/assets/pdf/DeepMIP-Eocene_model_database_descriptor.pdf). All model data are freely avaialble via [Google Drive](https://drive.google.com/drive/folders/1dH-OxAQi4eI0US6LlPrN8pfAYxNAEv0M). Once the manuscripted and database are accepted, this data will be deposited on the UK [CEDA Archive](https://archive.ceda.ac.uk) for long-term storage and scriptable access.