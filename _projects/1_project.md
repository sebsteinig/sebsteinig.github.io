---
layout: page
title: climatearchive.org
description: the Google Earth for climate data
img: assets/img/climatearchive_present_day_2.png
importance: 1
category: visualisation
---

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/climatearchive-overview-web-720p.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>
<div class="caption">
    Overview of some projects using the new Cliamte Archive engine.
</div>

## Motivation
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/PD_dragging.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>
<div class="caption">
    Demo of simple, Google-Earth-like user interface.
</div>

Climate change is the biggest threat modern humans have ever faced. But it is also a problem we can solve because we understand the science behind it. We are certain that human activities caused the warming over the last 150 years, we understand the relation between greenhouse gas emissions and temperature increase, and we therefore know exactly how we can stop any future warming. A lot of this knowledge comes from climate model simulations that produce huge amounts of data to understand past, present, and future climate change. As climate scientists, it is our responsibility to share this data to explain the urgent need for climate action to society and to provide a point of reference to make data-informed decisions.

Although extremely important, only few people have ever interacted with this raw climate data underpinning our future warming projections and resulting climate change policies. This is partly because scientists are used to provide their climate data in rather complex, static maps with different layers of geographical information which are not intuitively accessible for most people. But I would argue that actually nearly all of us know how to interact with maps and complex geographical information, because we do it nearly every day, whether it's checking the weather forecast, using navigation apps, or exploring our next holiday destination on Google Earth. The difference is that we are used to these super intuitive user interfaces like flicking the globe in Google Earth, instead of looking at a pile of static maps. 

And this is the whole idea of the Climate Archive project: we take our super important data and add a user interface that we are all familiar with to produce a Google Earth for climate data. We are all born with this intrinsic curiosity to explore, and by making this complex data more accessible and approaching it in a rather playful way, we can use this curiosity to extract the essential information and learn about the science behind climate change in a more engaging and rewarding way. This ultimately helps to make better use of the data across all user groups. 

## Technical details

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/wireframe_elevation.mp4" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/projection-change.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
<div class="caption">
    3D space is used for raised-relief maps and to seamlessly switch between planar and sphere projection.
</div>

I developed a completely new application to visualise climate model data in any modern web browser. It is built with the JavaScript library “Three.js” to allow the rendering of a 3D environment without the need to install any plug-ins. The real-time rendering gives instantaneous feedback to any user input and greatly promotes data exploration. Linear interpolation within a series of climate model simulations provides a continuous timeline. Model data is encoded in RGBA colour space for fast and efficient file handling in mobile and desktop browsers. The app allows the visualisation of simulated scalar (e.g., temperature and precipitation) and vector fields (winds and ocean currents) for different atmosphere and ocean levels. The user can seamlessly switch between a traditional 2D map and a more realistic 3D globe view and zoom in and out to focus on regional features. The model geographies are used to vertically displace the surface and to visualise tectonic changes through geologic time. Winds and ocean currents are animated by the time-dependent advection of thousands of small particles based on the climate model velocities. This technique – inspired by the “earth” project by Cameron Beccario – greatly helps to communicate complex flow fields to non-experts. Individual layers representing the ocean, the land, the atmosphere, and the circulation can be placed on top of each other to either focus on single components or their interactions. 

I received initial [seed corn funding from the Jean Golding Institute](https://jeangoldinginstitute.blogs.bristol.ac.uk/2021/01/07/seed-corn-funding-winner-announcement/) which enabled the collaboration with Tessa Alexander, a professional software engineer from the University of Bristol Research IT. This did not only help with transferring my ideas into a website but also ensured a solid technical foundation of the app which is crucial for future development and maintainability. In particular, a development workflow using a Docker container has been implemented to simplify sharing and expanding the app within the community.

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="https://www.youtube.com/embed/Ot3yYMwJRqY?start=1007" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="https://www.youtube.com/embed/-ADNyRWzYtE" class="img-fluid rounded z-depth-1" controls=true autoplay=true %}
    </div>
</div>
<div class="caption">
    I discuss some of the motivation and technical details in these YouTube videos.
</div>

#### 2023 update:
After the successful launch of the first version of climatearchive.org, I am super excited to announce some big plans for this year: Akina Renard and Willem Nicolas are MSc Computer Science and Software Engineering students from Toulouse, France and will spend five months this summer in Bristol to work with me on the next Climate Archive version. The goal is transform the current prototype into a modern, open-access data visualisation and sharing tool. We are currently rewriting all parts of the workflow (i.e. converting netCDF data, storing data sets in a database and rewriting the engine+website from scratch with React+Next.js). The first two parts of this workflow are already open-access and available as a new [netCDF converter](https://github.com/WillemNicolas/nimbus) and [model database+API](https://github.com/WillemNicolas/archive-db). We are currently working on the new engine and frontend with an open release scheduled for later this year.

## Example applications
#### Climate change across the last 540 million years
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/ca-intro-past.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>

The user can easily navigate on a geologic timescale to investigate climate variability due to changes in atmospheric CO2 and paleogeography throughout the last 540 million years. Based on our Bristol couple climate model simulations. Available at [https://climatearchive.org](https://climatearchive.org).

#### Climate change projections for the 21st century
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/cop26_climatearchive-app_overview.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>

Comparison of the consequences of a +1.5 °C or +3 °C world at the end of this century. Based on CMIP6 ensemble mean scenario projections. More info in the [COP26 blog post](/blog/2021/COP26/). Available at [https://climatearchive.org/cop26](https://climatearchive.org/cop26.html).

#### Climate change projections for the next one million years.
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/climatearchive-next-million.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
Return of the natural glacial-interglacial cycles after a sudden, strong anthropogenic warming. Based on emulator work to find safe nuclear waste storage locations. Available at [https://climatearchive.org/nextMillion](https://climatearchive.org/nextMillion.html).

#### Climate science meets sci-fi
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/Dune.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include video.html path="assets/video/wheel-of-time.mp4" class="img-fluid rounded z-depth-1" controls=true %}
    </div>
</div>
We have a history in Bristol of using pop culture examples to explain climate science to new audiences and I provided new visualisations to support this. For more info, see the respective blog posts about [Dune](/blog/2021/Dune/) and [Wheel of Time](/blog/2021/Wheel-of-Time-Weather/).

#### Climate Archive in museums
I used the engine to create custom, interactive climate change visualisations for natural and cultural history museums. For more info, see the respective blog posts on [Understanding Climate](/blog/2022/exhibition-frankfurt/) and [Horizons: Histories and Futures of Migration](/blog/2023/exhibition-nuremberg/).

## Feedback
I received a lot of positive and encouring feedback since the launch of the first version of climatearchive.org in [October 2021](/blog/2021/public-launch/). I wanted to collect some Twitter feedback here for documentation.

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% twitter https://twitter.com/ClimateOfGavin/status/1436159886073769987 %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% twitter https://twitter.com/leafwax/status/1436449888741429248 %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% twitter https://twitter.com/metbeni/status/1453021034383384584 %}
    </div>

</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% twitter https://twitter.com/FestOfTomorrow/status/1509815452188430337 %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% twitter https://twitter.com/qikipedia/status/1578399765859110912 %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% twitter https://twitter.com/microsiervos/status/1453270957150384137 %}
    </div>

</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% twitter https://twitter.com/ClimateDann/status/1452972586573475841 %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% twitter https://twitter.com/PaleoForams/status/1453078514945642498 %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% twitter https://twitter.com/Andrew_Mc30/status/1452988400479477770 %}
    </div>

</div>

