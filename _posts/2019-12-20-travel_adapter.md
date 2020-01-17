---
layout: post
title: "A universal travel adapter: using a climate model validation tool for FAIR hydrology"
image: /assets/blogpost_travel_adapter1.png
authors: "Peter Kalverla"
---

# Introduction

A few weeks ago I represented the eWaterCycle II project at a workshop in Reading, UK. The workshop, co-organized by the [H-SAF](http://hsaf.meteoam.it) and [HEPEX](https://hepex.irstea.fr) communities, was hosted by the European weather agency ECMWF.

Upon arrival at the conference centre (having drained most of my laptop’s battery on the train) I triumphantly produced my travel adapter… only to find out that the 3-prong plug on my charging cable did not fit the ungrounded travel socket. Outside it was raining.

As the last participants burnt their tongues to the damping tea and hurried towards the lecture theatre, a distressed phone call took place in the weather room next door. A hydrologist was trying to use the weather centre’s precipitation forecasts for a flood risk assessment but struggled to decode the ingenious grib format of the data.

# (Ab)using a climate tool for the benefit of hydrology

If you’re a hydrologist yourself, you’ve probably developed your own workflow to obtain and transform (meteorological) input data for your go-to model. And if I tell you that we’re working on a tool that’ll do this for you, it’s probably too little, too late. After all, you already have your ‘adapter’.

I could tell you instead that we’re working on a tool to do this for others. Potential new users of your model. Reviewers that want to check your work. Colleagues, who want to compare your results to theirs. And for other models, so that you don’t have to reinvent the adapter to use said new model. But still, it'd be just another tool.

So let me tell you that we're gathering existing code and integrating it with an existing tool. A tool that understands many different sources of meteorological data. A tool that comes with efficient and reliable functions for common tasks, such as regridding, interpolation, etc. And moreover, a tool that tracks provenance to facilitate transparancy and reproducibility.

That tool is called [ESMValTool](https://www.esmvaltool.org/about.html). It's an open source software project with roots in the climate sciences. It's designed for consistent and reproducible analysis of climate model output data. But instead of analysing these data, we're using the tool to convert them to a format that hydrological models can understand.

# Why?
Because we want to compare hydrological models, but each model expects different types of input. Because we want the results to be reproducible, but preparation of the forcing data is often a tedious process, which is far from transparent. And because we want to automate this process, to make it easier, more consistent, and less error-prone.

# Harmonization of climate model output data

A typical use case of ESMValTool would be visualize global temperature trends according to 30 or so different climate models, for example. Once upon a time, all these models came with different variable names, units, grids, etc. But it was recognized that some standardization was useful to make it easier to combine data from different models. Long story short, climate scientists now exchange their data according to the CF-conventions.

An invaluable tool in this endeavour was the climate model output rewriter (CMOR). As the name suggests, this tool is used to convert climate data to the new standardized format. And this is an ongoing effort, especially for new observational datasets that can be used for model validation.

![Conceptual illustration of ESMValTool functionality]({{ site.url }}/assets/blogpost_travel_adapter2.png)
*ESMValTool functionality illustrated using a cartoon by [XKCD](https://xkcd.com/1406/).*

In ESMValTool, the process of making a dataset CF-compliant (the red square in the image above) is called ‘cmorisation’. The work we’ve been doing includes, for example, adding support for ERA-Interim and ERA5. These datasets (among others) are commonly used in hydrological applications.

# Passing climate data on to hydrological models

By exploiting the CF-conventions, we immediately have access to a large and growing pool of meteorological datasets. The remaining challenge is thus in passing that data on to hydrological models (the blue square).

An example meteo2hydro workflow is illustrated below. It typically involves extracting a specific area or time interval, regridding, selecting and renaming the right variables, perhaps deriving some additional variables, unit conversions and writing the output to a specific format.

![Illustration of a typical workflow to prepare forcing data for hydrological models]({{ site.url }}/assets/blogpost_travel_adapter3.png)
*A typical workflow to prepare forcing data for hydrological models.*

Many of these functions exist in ESMValTool. Thus, our work consists of making [ESMValTool ‘recipes’](https://esmvaltool.readthedocs.io/en/latest/recipes/recipe_hydrology.html) that specify the variables, period(s), area(s), frequency, grid, and so on that are needed for each of the models participating in eWaterCycle II.

We’ve also added some functions specific to hydrology. For example, De Bruin’s formula to derive potential evapotranspiration, a lapse-rate correction for temperature regridding, and an ‘extract-shape’ function to work with shapefiles describing certain (sub-)catchments.

# Towards a universal standard?

A nice aspect of ESMValTool is that it is supported by a large and growing user base. Integrating hydrological applications is thus also a way to provide feedback. The CF conventions still evolve. Our recipes and cmorisers are effectively mapping how they can evolve to better facilitate hydrologists.

Of course, it also works the other way around. Perhaps, hydrological models will evolve to work out of the box with CF-compliant data files. Or maybe new conventions will emerge. After all, coupling earth system models is an active area of research.

You could say that our work on ESMValTool for eWaterCycle II is complete once the tool becomes obsolete. But until that time, it’s a very useful piece of software to bridge the remaining gaps. For all I know, travel adapters are still around as well. Let's try to make them even easier to use :-).