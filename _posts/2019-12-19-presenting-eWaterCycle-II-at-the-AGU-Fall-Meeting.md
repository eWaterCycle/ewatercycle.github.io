---
layout: post
title: "Hydrographs, and models, for hydrologists, policy and RSEs: presenting eWaterCycle II at the AGU Fall Meeting"
image: /assets/FMBanner.jpg
authors: "Rolf Hut"
---

A year ago we promised ‘[nice hydrographs for everyone](https://www.ewatercycle.org/2018/11/12/introducing-ewatercycleII.html)’. Back then we had a [Minimal Viable Product (MVP)](https://www.youtube.com/watch?v=uv_9zSGVFJs) of the system we want to build. In the year since we have opened the system to hydrologists, added a software stack for pre-processing climate forcing data and started communicating with policymakers on a fully ‘FAIR by Design’ decision making environment. Naturally we wanted to share these results with everyone at the biggest geoscientific conference of the year: the [AGU Fall Meeting](https://www.agu.org/fall-meeting). But what session do you pick to share this in? A hydrology session? Or a policy session? Since our teams [knows a thing or two about science communication](https://doi.org/10.5194/hess-20-2507-2016), we decided to follow the ‘audience, message, medium’ mantra and not present a single message to multiple audiences, but present a different message to our three main audiences.

## For hydrologists: a model comparison study using eWaterCycle leads to better pre-processing tools

In eWaterCycle II we are building a ‘community environment for hydrological computational science’. Community is there for a reason: we want to build a system that benefits the hydrological community by making it easier to do their work. After the MVP of 2018, we expanded the system to be able to work with multiple users. Subsequently, we invited community members for a week long workshop to add their models to eWaterCycle and do a large comparison study together.

![Participants of the comparison study](/assets/leidenTeamPhoto.jpg)

During the workshop-week, hydrologists and research software engineers (RSEs) worked together to add hydrological models with different concepts (conceptual, semi-distributed and distributed) and with different programming languages (Python, Fortran, Matlab) into our system. The scientific question we set out to answer during the workshop was: “what is the impact for the hydrological community of the new ERA5 forcing dataset from ECMWF?”. And here we hit a snag. At the end of the week we had added nearly all models to our system, yet we had not pre-processed ERA5 for any of these models. It turned out that pre-processing of forcing data currently is mostly done using model specific scripts that are certainly not FAIR (Findable, Accessible, Interoperable and Re-usable). Since eWaterCycle II is a ‘FAIR by Design’ system, we could not let this stand and used most of the remaining time of 2019 to build a generic toolkit that allows hydrologists to pre-process climate forcing data that is FAIR. Build upon the pre-exisiting ESMValTool, hydrologist now only need to provide a ‘recipe’ to be able to pre-processes ERA5 or ERA-Interim data into model specific inputs. For the models in our comparison study we already provide template recipes.

At the fall meeting we were able to present the results for the first two models of the comparison in an oral talk I gave.

<figure>
<div class="aspect-ratio">
<iframe src="https://www.youtube.com/embed/GOkDY7lfCxQ" frameborder="0" allowfullscreen></iframe>
</div>
<figcaption style="text-align:right">Presentation at AGU Fall Meeting</figcaption>
</figure>

Looking forward, in 2020 the eWaterCycle team will focus on finishing (and publishing) the comparison study. After that we intend to open the system to the hydrological community for them to to their research in. We also plan to develop specific tools for academics that have to teach hydrology to students to use eWaterCycle II in their courses.

## For policy: a FAIR by Design decision making environment

Whether it is for deciding where flood mitigation measures need to be implemented, or decide if that hydrodam is worth the societal investment, policymakers rely on advice from scientists to base their decisions on. As much as we demand that the policymaking (democratic) process has to be transparent, we should also demand the same from the scientific results that are used as input to this process. eWaterCycle II, being developed in a ‘FAIR by Design’ manner, will provide a transparent and open environment for model studies that policymakers can rely on. While still working on building eWaterCycle II, we wanted to alert policymakers on the need for FAIR by Design and on what we are intending to build with eWaterCycle II. The workshop participant with the most policy expertise of us all, [Caitlyn Hall](https://twitter.com/caitlynahall), presented our vision: “eWaterCycle: Putting the Public in Charge is Only FAIR” in the “Actionable Climate Tools and Data: Rigorous, Accessible Products Tailored to User Needs” session with both a talk and a poster.

![Poster presented at AGU Fall Meeting](/assets/eWaterCyclePublicFiarSMALL.png)

## For Research Software Engineers: a stack of re-usable technology

eWaterCycle II is a flagship project of the Netherlands eScience Center together with Delft University of Technology. The projects run by the eScience Center differ from those funded by traditional funders (like the Dutch NWO or the American NSF) in that the bulk of the budget is provided in ‘in kind’ hours of their research software engineers (RSEs). These RSEs are tasked to not only provide solutions for scientists within the projects that they work on, but also to build these solutions as generic as possible, to facilitate re-use in other projects and domains. This means that most of the specific technology developed within eWaterCycle should be useable within and outside of the project. Three prime examples of how such re-usable technology are ERA5CLI, GRPC4BMI and our contribution to ESMValTool. We presented these contributions as an eLightning poster in the ‘Applications of Free and Open-Source Technologies for Advancing Earth and Space Science’ session.

![eLightning presented at AGU Fall Meeting](/assets/eLightningPoster.png)

### [ERA5CLI](https://github.com/eWaterCycle/era5cli)

As part of the pre-processing workflow we build in 2019, we needed an automated method to download the ERA5 dataset from ECMWF. Currently, ERA5 can only be downloaded through the Climate Data Store (CDS), which requires manually entering information on what parts of the data a user wants to download. We build [ERA5CLI](https://github.com/eWaterCycle/era5cli), a command line interface to automatically download ERA5 data. This was received enthusiastically by the community and even ECMWF themselves advocate the use of ERA5CLI for advanced users of the CDS.

### [GRPC4BMI](https://github.com/eWaterCycle/grpc4bmi)

eWaterCycle aims to bring together a community of hydrological modellers who use different programming languages for their specific models. We needed a method allow scientists to interface with each others models without having to learn (another) programming language. The Basic Model Interface (BMI) developed at CSDMS already provides a generic way to interface with models that is defined in different programming languages. It does not, however, allow automatic translation of calls from one language into another. To this end we combined gRPC, container technology and BMI into [GRPC4BMI](https://github.com/eWaterCycle/grpc4bmi), an inter-language model coupler that allows a user in a jupyter notebook to treat a model in any programming language as a simple object it can call, without being confronted with the language that the model is written in. While GRPC4BMI is used in eWaterCycle to interface with different models, it can also be used to create one big (earth system) model build up from different sub models. Large modelling communities such as NOAA and NCAR expressed interest to use GRPC4BMI in their own workflows. We will follow up on these collaborations in 2020.

### [ESMValTool](https://github.com/ESMValGroup/ESMValTool)

Pre-processing of climate data to generate input for hydrological models usually includes operations such as parameter selection, region selection, re-gridding (interpolation / aggregation) and even some derivations. When we looked into building a pre-processor tool for hydrological models, we realized that such a tool already exist in the climate sciences: [ESMValTool](https://github.com/ESMValGroup/ESMValTool). We contributed to ESMValTool by adding hydrological concepts, such as the capability to select a catchment from a dataset using the shape of the catchment. This allows hydrologist to use this powerful toolset to pre-process their input data in a FAIR manner. In 2020 we will be providing tutorials for hydrologists to help them get started with ESMValTool within eWaterCycle II.
