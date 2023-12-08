---
layout: post
title:  "Global Heatwave Visualisation"
date: 2023-08-29
description: "Animation of daily heatwaves during July 2023 in the ERA5 dataset."
tags: visualisations code
thumbnail: assets/img/era5-heatwaves.png
---

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/C3S_july-2023.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
  Figure 1: Globally averaged surface air temperature for all months of July from 1940 to 2023. Shades of blue indicate cooler-than-average years, while shades of red show years that were warmer than average. Data: ERA5. Credit: C3S/ECMWF (https://climate.copernicus.eu/july-2023-sees-multiple-global-temperature-records-broken).
</div>

July 2023 was the warmest month on record (Fig. 1) with concurrent heatwaves around the globe (see the [Copernicus Climate Change Service report](https://climate.copernicus.eu/july-2023-sees-multiple-global-temperature-records-broken) for more detail). I wanted to use my Climate Archive engine to visualise the global pattern of the heat waves raging around the globe and link them to mainstream weather and climate news of this truly extreme month. 

For this, I used daily near-surface air temperatures (2m) from the [ERA5 reanalysis](https://www.ecmwf.int/en/forecasts/dataset/ecmwf-reanalysis-v5) produced by ECMWF. I calculated anomalies compared to the long-term mean (1991-2020) and only focused on significantly warmer than normal temperatures. I followed the UK MetOffice [heatwave definition](https://rmets.onlinelibrary.wiley.com/doi/pdf/10.1002/wea.3629) to track the occurence of heatwaves. Wherever a heatwave occured over the course of July 2023, the background color of the map switches from gray to black. This gives the effect of a scratch map that gets slowly revealed over the whole month and illustrates that more than 50% of the global population experienced at least one heatwave during July 2023! 

Links to the source data and all analysis code (Python) is available on [GitHub](https://github.com/sebsteinig/era5-heatwaves). The final visualisation is shown below and is also accessible in an interactive version at [era5.climatearchive.org](https://era5.climatearchive.org).

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/ERA5_july-2023_heatwaves.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>
<div class="caption">
    Final animation of daily near-surface air temperature anomalies for July 2023 in the ERA5 reanalysis.
</div>