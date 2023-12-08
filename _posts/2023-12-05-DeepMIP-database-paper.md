---
layout: post
title:  "DeepMIP database overview paper"
date: 2023-12-05
description: "Paper describing the database and web application submitted to Scientific Data"
tags: visualisations code
thumbnail: assets/img/database-scores.png
---

I am happy to announce the submission of our overview paper of "The DeepMIP-Eocene model database and interactive web application versions 1.0".


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/database-scores.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
   Figure 1: Technical validation of atmospheric global model fields of the x3 experiment across the ensemble. Variables with multiple vertical levels are shown for the respective model pressure level closest to 500 hPa.
</div>

## Technical Details
The web app was built with Streamlit, which is an open-source Python library that makes it easy to create custom web apps for machine learning and data science. All processing and plotting is implemented in pure Python with all underlying functions available to start/modify your own analysis. All code is open access and available on [GitHub](https://github.com/sebsteinig/deepmip-eocene-app).

## Get the data and paper
The submitted (non-peer reviewed) paper can be viewed [here](/assets/pdf/DeepMIP-Eocene_model_database_descriptor.pdf). All model data are freely avaialble via [Google Drive](https://drive.google.com/drive/folders/1dH-OxAQi4eI0US6LlPrN8pfAYxNAEv0M). Once the manuscripted and database are accepted, this data will be deposited on the UK [CEDA Archive](https://archive.ceda.ac.uk) for long-term storage and scriptable access.