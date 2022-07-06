---
layout: post
title: "So you want to eWaterCycle?"
image: /assets/eWaterCycleHydrologists.jpeg
authors: "Rolf Hut"
---

eWaterCycle is a platform for Open and FAIR Hydrological research collaboration. We’ve built eWaterCycle to allow hydrologists to work with each other's models and data and to do so in a way that is FAIR by design. On top of that, eWaterCycle is easy to use and available now. If that gets you excited to work with eWaterCycle, we totally understand. But where to start? This short blog will guide you on how to get started working with eWaterCycle.

## So what is eWaterCycle?

At its core, eWaterCycle is a software stack, a collection of programs and libraries, that allow users (hydrologists) to do numerical experiments using hydrological models. eWaterCycle takes away much of the pain involved in 

* Getting someone elses model to run.
* Getting input (forcing) files in the correct format for your chosen model.
* Coupling models together, especially when they are written in different languages. 

eWaterCycle is a platform that gives users access to hydrological models and (input) datasets through a Jupyter Notebook environment. Since all models in eWaterCycle run inside (Docker or Singularity) containers, the user does not interact directly with the code of the model. A Hydrologist could be doing a model comparison of a Matlab based model (like MARRMoT) and a Fortran based model (like HYPE) all from a Python based notebook. 

Detailed information on eWaterCycle can be found in our paper in Geoscientific Model Development, which is also the paper to cite if you use eWaterCycle to conduct your research. You can find that paper here: [https://doi.org/10.5194/gmd-2021-344](https://doi.org/10.5194/gmd-2021-344). A brief introduction into eWaterCycle is given in the video below.

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/eE75dtIJ1lk/1.jpg)](https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)

## Where is eWaterCycle currently running / hosted

This platform needs to run somewhere. In theory you can install eWaterCycle on a laptop[^1]. However the datasets required to run hydrological models are usually quite large. Therefore you don’t typically run eWaterCycle on a laptop, but on dedicated high performance computer infrastructure. We have a few options to help get you started with eWaterCycle. The options are described below and summarized in this flow diagram.

![alt_text](/assets/So_You_Want_To_eWaterCycle_diagram.png "Flowchart")

### A quick look at eWaterCycle on our demonstration machine

If you want to get a feel for the eWaterCycle platform we have a small demonstration machine available. You will need a login for this machine which we will email you if you fill in this form. This machine is completely wiped and restarted regularly, including all login information. So don’t get excited and start doing research as this machine is only intended to take a quick look around, generate a hydrograph and play around with the options, not to do research. To get to know the platform we recommend looking at the use cases from the GMD paper which live in their own repository and can be accessed through the “Tech Paper Notebooks” button at the top of the screen in the explorer. Or you can use the explorer to browse the available models and datasets and let the system generate a notebook for you.

### Run eWaterCycle on your own SURF Research Cloud account

Researchers with an account[^2] on the [SURF researchCloud](https://www.surf.nl/en/surf-research-cloud-collaboration-portal-for-research) can start up their own machine. This machine will out of the box be able to run a few example models and datasets, such as PCRGlobWB and WFLOW for the Rhine Area. Users can add their own models and datasets following the steps explained in the [documentation](https://ewatercycle.readthedocs.io/en/latest/adding_models.html).

Note that multiple users can work on one machine. This is handled by the SURF Research Access Management ([SRAM](https://wiki.surfnet.nl/display/SRAM/)) system.  

### Run eWaterCycle on your own machine

For researchers with access to their own machine there is the option of installing eWaterCycle on it and providing access to users of that machine. This machine should run Linux and have plenty of storage. While in theory this machine could be a laptop, usually this will be a server where users login. Following the steps at [the system setup page of the documentation](https://ewatercycle.readthedocs.io/en/latest/system_setup.html) provides you with all the needed info.To save many headaches we recommend that Installing eWaterCycle on your own hpc or cloud infra is done by system administrators or research software engineers who are comfortable doing so.

### Models and datasets

All of the above ways of working with eWaterCycle will give you access to the models and example datasets that are supported by the package. More datasets can be added in the process of setting up the platform. On our demonstration machine we have several additional datasets, see [https://www.ewatercycle.org/demo](https://www.ewatercycle.org/demo) for details. eWaterCycle is a work in progress and we keep adding models and datasets as we move forward. 

Currently adding one's own model requires quite a few steps as described [in the documentation](https://ewatercycle.readthedocs.io/en/latest/adding_models.html). Simplifying this process is one of the things we will be working on in the future (see below). 

### Future options: what are we working on?

Our goal is to provide easy access to eWaterCycle to as many researchers and students as possible. To achieve this we are working on the following options:

#### eWaterCycle for education: Open Educational Resources

Through a grant of the Dutch ministry of Education and Science we will be importing all educational material on computational hydrological modeling being taught at Dutch universities into eWaterCycle and make those available as ‘Open Educational Resources’ for anyone to use. We in this case is a collaboration between Delft University of Technology, Wageningen University and Research, University Twente and the Netherlands eScience center. 

#### eWaterCycle at Delft University of Technology

Of course we are using eWaterCycle for our own hydrology research. Recent examples (using older versions of the platform than currently available!) include 

* Coupling a global glacier model to a global hydrological model prevents underestimation of glacier runoff  ([Wiersma 2022, in Review in HESS](https://doi.org/10.5194/egusphere-2022-106))
* Large-sample assessment of spatial scaling effects of the distributed wflow_sbm hydrological model shows that finer spatial resolution does not necessarily lead to better streamflow estimates ([Aerts 2021, in Review in HESS](https://doi.org/10.5194/hess-2021-605))  

#### eWaterCycle far future
We are currently looking for funds and partnerships to keep on expanding both access to eWaterCycle as well as expanding the features of, and models and data available through, eWaterCycle. For example, adding support for more easily adding your own datasets and models to eWaterCycle is high on our wishlist. If you want to collaborate, or host eWaterCycle for your community or for the entire world, please contact us at [questions@ewatercycle.org](mailto:questions@ewatercycle.org). 

<!-- Footnotes themselves at the bottom. -->
## Notes

[^1]:
     and some do

[^2]:
     and associated budget 
