---
layout: post
title:  "Exhibition: Understanding Climate"
date: 2022-10-21
description: My first interactive exhibit for a museum
tags: visualisations museum outreach
thumbnail: assets/img/frankfurt-1.png
---

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/frankfurt-0.jpg" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Exhibition poster. Credits: https://museumfrankfurt.senckenberg.de
</div>

My very first collaboration to visualise climate data for a museum is now on display!

It is part of a special exhibition about paleoclimate research that is opening today in the Senckenberg Natural History 
Museum in Frankfurt, Germany, which is the second-largest natural history museum in Germany with around 400,000 visitors 
each year. The [exhibition](https://museumfrankfurt.senckenberg.de/de/ausstellung/sonderausstellungen/klimawissen-schaffen/) explains how we can learn about past climate changes and what this might tell us for 
our own future. 

Visitors will be able to explore the climate change of the last 500 million years in our Bristol model simulations. Playing with the visualisation at the end of the exhibit is somewhat the reward for learning a lot about paleoclimate research before :). I am using my climatearchive.org engine for visualisation, but I had to overcome some interesting challenges.

This is the first time I tried a dual-screen setup. The museum wanted to have one touchscreen for a single user to interact with the data and control the visualisation. In addition, the actual 3D world should be mirrored to a large projection area with only limited additional information. This should make it possible to effectively use the exhibit even in a larger group (e.g. school classes) and put the actual Earth front and center. A screenshot of the two different displays is shown below.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/frankfurt-4.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Screenshot of dusal-screen setup with interactive touchscreen (left) and room projection (right).
</div>

Another challenge was to make the visualisation "museum-proof". This included removing some more complex user interfaces, disabling zoom, adding easy-to-understand information and help buttons and translations into German and English. During my conversations with the curators I learned a lot about the unique requirements of museum interactives and differences to the academic world. Thank you to Lisa Voigt and Andrea Weidt for inviting me to this super exciting collaboration and I am looking forward to visiting the exhibition later this year in person!

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/frankfurt-1.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/frankfurt-2.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/frankfurt-3.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

<div class="caption">
    Impressions from my interactive contribution to the exhibition. Credits: Senckenberg Naturmuseum Frankfurt/Main, Foto: Sven Tränkner.
</div>

