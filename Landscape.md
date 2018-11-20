---
layout: page
title: Landscape
---

# eWaterCycle Landscape Overview

*The eWatercycle II project aims to overcome the challenge of locality in hydrological models using a Community Multi-Model environment. In eWatercycle II we will build an e-Infrastructure that will allow quick and safe inclusion of sub-models and model concepts into global hydrological models, leading to better understanding of the global hydrological cycle.
In this document we review the landscape of state-of-the-art hydrological research. 
We examine overall related projects and platforms that we are inspired by and that we would potentially collaborate with, as well as software, models and databases that we would like to use, or reference in our project (or at least be aware of).*

## Overall related projects

**[CSDMS](https://csdms.colorado.edu/wiki/Main_Page):** The Community Surface Dynamics Modeling System is a group of experts dealing with research about the Earth’s surface. The group support the development, sharing of models to explain Earth’s surface processes by disseminating integrated software. They mainly deals with movements of fluids and the flux of sediments and their basins.

**[CUASHI HIS](http://his.cuahsi.org):**  The Consortium of Universities for the Advancement of Hydrological Science developed a suite of applications to enable hydrological researchers to share their data. The suite is made of three components: the HydroServer, the HydroCatalog and the HydroDesktop. The HydroServer provides access to the data, the HydroCatalog provides search functions for data discovery and the HyroDesktop app allows modeling and analysis of the data locally.

**[Hydroshare](https://www.hydroshare.org):** Community platform to share data, models and code. Operated by CUASHI HIS. Can be used to share, access, visualize and manipulate a broad set of hydrologic data types and models. Roughly consists of file storage to share resources (data/publications/code/executables/ etc), and added functionalities like metadata descriptions, data access API, DOI data publication and an apps library (e.g., jupyterhub notebook, online SWAT, HydroshareGIS and others). 

**[The Earth System Grid Federation (ESGF)](https://esgf.llnl.gov/):** Peer-to-Peer (P2P) enterprise system is a interagency and international collaboration that provides software infrastructure for the management, dissemination, and analysis of model output and observational data. ESGF's primary goal is to facilitate advancements in Earth System Science. Users can apply for access to the data, i.e., they are provided a username and password.
Users can request a persistent identifier to be assigned to the dataset that they upload.
ESGF "core" metadata includes mandatory and optional fields that are needed to search and download data throughout the ESGF system. These fields are not specific to any scientific discipline, rather they are common to any discipline that intends to leverage the ESGF infrastructure. Core metadata fields are defined in the ESGF meta-schema file esgf.xml, which is always used for validation whenever metadata records are published.

**[Aqueduct Global Flood Analyzer](http://floods.wri.org/#/):** The Aqueduct Global Flood Analyzer is a web-based interactive platform which measures river flood impacts by urban damage, affected GDP, and affected population at the country, state, and river basin scale across the globe, as well as 120 cities.

**[OpenStreams](https://publicwiki.deltares.nl/display/OpenS):** A collection of building blocks for integrated Hydrological models. Integrated modeling means to connect multiple models for different domains (e.g., surface water domein and groundwater domain) so the interaction processes between the domains will be taken into account. The aim is to allow integrated modelling, promote usage of model tools in different frameworks and settings,and  provide applications for model coupling.

**[ESMF](https://www.earthsystemcog.org/projects/esmf/):** Consortium of US institutes (NASA, National Weather Center, etc.). Hosted by the university of Colorado. They deal with Earth Sciences, predominantly oceanography and atmospheric physics. Mostly focussed on HPC (native interfaces). 


**[GEOGLOWS](https://www.arcgis.com/apps/Cascade/index.html?appid=414730116a3c4c119b80ec9d1727ab74):** A framework that uses RAPID (Routing Application for Parallel computatIon of Discharge), and the ECMWF (European Centre for Medium-Range Weather Forecasts) forecasts to map streams. The system currently contains more than 200,000 streams throughout North and South America, Africa, and South Asia. It produces a new 15-day ensemble streamflow forecast for each stream every day. The framework also computed a 35-year streamflow history for each stream. It uses a web server application for visualization, and working towards an improved streamflow visualization which will allow users to quickly identify areas of concern in a watershed at each time step in the forecast. Also contains a validation toolbox.


**[GloFAS](http://www.globalfloods.eu/):** The Global Flood Awareness System (GloFAS), jointly developed by the European Commission and the European Centre for Medium-Range Weather Forecasts (ECMWF), is independent of administrative and political boundaries. It couples state-of-the art weather forecasts with a hydrological model and with its continental scale set-up it provides downstream countries with information on upstream river conditions as well as continental and global overviews. GloFAS produces daily flood forecasts in a pre-operational manner since June 2011.

**[GLOFRIM](https://github.com/openearth/glofrim):** Globally Applicable Framework for Integrated Hydrological-Hydrodynamic Modelling. Developed by Jannis M. Hoch (Utrecht University). A platform to couple (chain) models. Currently couples PCR-GLOBWB with Delft3D Flexible Mesh (Deltares) or LISFLOOD-FP (University of Bristol). Uses BMI to facilitate the coupling, thus models have to be BMI-compatible.

**[Catch X](https://earthwatch.org.uk/get-involved/projects-activities/catchexp):** - The Catch X open data platform will improve access, or provide access for the first time, to standard water balance information at a local catchment level around the world. Catch X is a partnership between the University of Leeds, Earthwatch, WWF UK, WWF South Africa, Marks & Spencer, SSBN Ltd. and Richard Carter and Associates.

## Related efforts in other domains

**[Evidencio](http://www.evidencio.com):** Project to share medical decision support models with researchers and (especially) clinical practitioners.

**[Codeocean](https://codeocean.com/):** A cloud-based computational reproducibility platform that provides researchers and developers an easy way to share, discover and run code. The platform provides open access to the code and the data. Users can execute all published code without installing anything on their personal computer. Everything runs in the cloud on CPUs or GPUs. It is possible to change parameters, modify the code, upload data, etc. It is free of charge for an individual researcher, but does have a cost for teams or institutions, as it has a business approach.

**[E3SM](https://e3sm.org/):** - Energy Exascale Earth System Model. Earth system modeling, simulation, and prediction project that optimizes the use of DOE laboratory resources. The platform aims to integrate model development with leading-edge computational advances to lead ultra-high-resolution modeling with throughput for coupled Earth system simulations. They aim to bridge the gap in scales and processes and use ensemble modeling to quantify uncertainty. They focus on 3 scientific “drivers”- Water cycle (hydrological cycle and its sensitivity to model resolution and forcing), Biogeochemistry and energy (biogeochemical cycles interaction with Earth system components and their influence on energy-sector decisions) and Cryosphere-Ocean (rapid changes in cryospheric systems and their contribution to sea level rise and coastal vulnerability). Effort is also invested in computational research so to make effective use of upcoming DOE exascale computing platforms. Data is open and available through the ESGF archives ([data description](https://e3sm.org/data/get-e3sm-data/data-description/)).

**[MINT](http://mint-project.info/):** The MINT (Model INTegration) project aims to integrate models from separate disciplines, including geosciences, agriculture, economics, and social sciences. It uses 
artificial intelligence technologies to assist modelers by automating and improving important aspects of model integration. It incorporates three key innovations: 1) Semantic technologies to address model and data discovery and to bridge the heterogeneity of model requirements and assumptions; 2) Automated planning to resolve data mismatches by including data transformations; and 3) Machine learning to improve model parameterization through the extraction of more accurate data from remote sensing and other sources and search optimization.

**[Wekeo](https://www.wekeo.eu/):** The European Organisation for the Exploitation of Meteorological Satellites (EUMETSAT), the European Centre for Medium Range Weather Forecasts (ECMWF) and Mercator Ocean have launched the WEkEO Copernicus Data and Information Access Service. Wekeo offers Copernicus Data, i.e., EU environmental monitoring data,  for free download and features cloud–based hosted processing and tools allowing users to transform the data and services.

**[Google Earth Engine](https://earthengine.google.com/):** Earth Engine is a platform for scientific analysis and visualization of geospatial datasets. It hosts satellite imagery and stores it in a public data archive that includes historical earth images going back more than forty years. It also provides APIs and other tools to enable the analysis of large datasets.

## Metadata schemes

**[Dublin Core Metadata Initiative (DCMI)](http://www.dublincore.org/groups/sam/):** Organization supporting innovation in metadata design and best practices across the metadata ecology. The [element set](http://dublincore.org/documents/1998/09/dces/) for metadata curation includes 15 elements that covers the basic characteristics of any data set.


**[Datacite](https://www.datacite.org/):** DataCite is a non-profit organisation that provides DOIs for research data. The goal is to help the research community locate, identify, and cite research data. They support the creation and allocation of DOIs and accompanying metadata. Datacite also provides services that support the enhanced search and discovery of research content. Their metadata scheme covers different types of data and software. 


**[CodeMeta](https://github.com/codemeta/codemeta):** - CodeMeta contributors are creating a minimal metadata schema for science software and code, in JSON and XML. The goal of CodeMeta is to create a concept vocabulary that can be used to standardize the exchange of software metadata across repositories and organizations. CodeMeta started by comparing the software metadata used across multiple repositories, which resulted in the CodeMeta Metadata Crosswalk. That crosswalk was then used to generate a set of software metadata concepts, which were arranged into a JSON-LD context for serialization.


## Related software

*Instead of reinventing the wheel, we would like to use and adapt as much software and toolkits as possible, assuming it is open-source, updated and maintained.*

**[OpenDA](https://www.openda.org/):** Software that allows a fast and effective integration of observations and models through data assimilation. OpenDA is a generic environment for data assimilation tasks like parameter calibration and measurement filtering. It provides a platform that allows an easy interchange of algorithms and models. 

**[AMUSE](http://www.amusecode.org/)/[OMUSE](https://bitbucket.org/omuse/omuse):** Software framework for multi-physics/multi-scale simulations. AMUSE/OMUSE provides an homogeneous environment to interface with existing numerical simulation codes. AMUSE was developed for astrophysical applications, while its offshoot OMUSE was developed for the oceanographic domain. They share a common framework code base.

**[OpenMI](https://sites.google.com/a/openmi.org/home/):** An open modeling interface, originally developed to facilitate the simulation of interacting environmental processes. Now used to exchange between models and software components. Can be applied to linking any combination of models, databases and analytical and visualisation tools. The interface is not maintained anymore/expired.

**[Renku](https://renku.readthedocs.io/en/latest/index.html):** A scalable & secure open software platform designed to foster multidisciplinary data (science) collaboration. The platform uses Python-based command-line interface (CLI) and Python API. Renku records the commands into a CWL to allow for reproducible analysis. Still in very early beta version.

**[SILK](http://silkframework.org/):** The Linked Data Integration Framework - open source framework for integrating heterogeneous data sources. Use cases include generating links between datasets, linking data sources, and applying simple data transformations to structured data sources. It can be used to create linked water-related datasets, to enrich datasets with additional information and/or descriptions of terms. Basically can be used as a source for metadata about water-related data sets.

**[Cylc](https://cylc.github.io/cylc/):** A workflow engine for cycling systems - it orchestrates distributed suites of interdependent cycling tasks that may continue on indefinitely.

**[DART](http://www.image.ucar.edu/DAReS/DART/):** Data assimilation toolkit

**[DAPPER](https://github.com/nansencenter/DAPPER):** Data assimilation toolkit in python

**[EMPIRE](http://www.met.reading.ac.uk/%7Edarc/empire/index.php):** Data assimilation toolkit

**[WHIST](http://hype.sourceforge.net/WHIST/):** WHIST is a tool from SMHI to extract and repurpose information to create input files for hydrological models, including the Hype Model, from different types of databases. WHIST is the core tool when setting up a hydrological model for new geographical domains or changing model resolution. From the information of topographic databases, for example, WHIST can delineate the sub-basins, and the linking (routing) between them.

**[Delft Flood Early Warning System (Delft-FEWS)](https://www.deltares.nl/en/software/flood-forecasting-system-delft-fews-2/):** Expert software to build hydrological forecasting systems. Originally, it was developed as a flood forecasting and warning system, recently it resulted into an open data handling platform. Delft-FEWS is composed by several modules, which allows to build a hydrological forecasting system customizable to the requirements of specific organizations.

**[ENKI](https://www.sintef.no/en/software/enki-hydrological-modelling-framework/):** Hydrological modelling framework - The main focus of the framework is on precipitation models and hydropower. Focussed on improving hydrological forecasting for hydropower scheduling. Currently, no further development is in place.

**[FUSE](https://github.com/ICHydro/r_fuse):** Framework for Understanding Structural Errors (R package), dedicated for hydrological modelling.

**[HydroMAD](http://hydromad.catchment.org/):** Hydrological Model Assessment and Development (R package). A modelling framework for environmental hydrology: water balance accounting and flow routing in spatially aggregated catchments. It supports simulation, estimation, assessment and visualisation of flow response to time series of rainfall and other drivers. [Github link](https://github.com/josephguillaume/hydromad).

**[HydroStats](https://pypi.org/project/hydrostats/):** Tools for use in comparison studies, specifically in hydrology. The library contains preprocessing tools, visualization, a package dependency ([HydroErr](https://github.com/waderoberts123/HydroErr)) with more than 60 error metrics. Also provides a library of metrics to measure forecast, i.e., to compare ensembles with observations. The library is written in Python, well-documented and available via github. It is still in its prerelease version.

**[Emma](https://github.com/nlesc-sherlock/emma/):** Ansible playbook to create a cluster with GlusterFS, Docker, Spark and JupyterHub services.

## Related ontologies/controlled vocabularies

**HyFO:** Models “containers” of water, identifying the common concepts of container and water body. The ontology has been recently extended to characterize also hydrological flow processes [Stephen, 2017](http://drops.dagstuhl.de/opus/volltexte/2017/7763/pdf/LIPIcs-COSIT-2017-7.pdf). No available working link to ontology.

**Surface Water Ontology:** Ontology composed by two modules: the dry module and the wet module. The dry module expresses the semantics of ground features, which exist regardless of the presence of water. The wet module reuses some dry module features to express the semantics of hydro features. [Sinha, 2014](http://www.semantic-web-journal.net/system/files/swj675.pdf). No available working link to ontology.

**[CUAHSI Ontology](http://edscvs.ccny.cuny.edu/cuahsi/):** - supports the discovery of time series hydrologic observations including physical, chemical, and biological measurements. 

**[Water ML](http://www.opengeospatial.org/standards/waterml):** A common conceptual feature model for describing typical features of the hydrology domain using established models and patterns endorsed by WMO and UNESCO.

**[CSDMS standard names](https://github.com/csdms/standard_names_registry):** -  set of cross-domain naming conventions for describing process models, data sets and their associated variables. CSDMS Standard Names were developed to facilitate semantic mediation, i.e., name matching, between models and/of data sets within the CSDMS modeling framework. The  CSDMS Standard Names is further developed in the context of the MINT project and is now called the [GeoScience Ontology](http://www.geoscienceontology.org/news.html). 

**[SWEET](https://bioportal.bioontology.org/ontologies/SWEET/?p=summary):** The Semantic Web for Earth and Environmental Terminology is a mature foundational ontology that contains over 6000 concepts organized in 200 ontologies represented in OWL. Top level concepts include Representation (math, space, science, time, data), Realm (Ocean, Land Surface, Terrestrial Hydroshere, Atmosphere, etc.), Phenomena (macro-scale ecological and physical), Processes (micro-scale physical, biological, chemical, and mathematical), Human Activities (Decision, Commerce, Jurisdiction, Environmental, Research). Originally developed by NASA.

**[QUDT](https://bioportal.bioontology.org/ontologies/QUDT):** The Quantity, Unit, Dimension and Type collection of ontologies define the base classes properties, and restrictions used for modeling physical quantities, units of measure, and their dimensions in various measurement systems.

**[OM](http://www.foodvoc.org/page/om-1.8):** The ontology of measurements (OM) contains thousands of terms on quantities and units pertaining to things like length, weight and energy value – from metres and inches to spoons and millilitres per liter.

**[OntoSoft](http://www.ontosoft.org/ontology.html):** Ontology for scientific software metadata. It is part of the OntoSoft project, which aims to promote knowledge sharing about the software developed for geosciences. The ontology is the basis for the design of the user interface in the OntoSoft portal, the organization of the underlying knowledge base, and the integration with other software repositories.


## Notebook platforms

**[Pangeo](http://pangeo.pydata.org/hub/login):** Big data geoscience Jupyter server.

**[SciServer Compute](http://www.sciserver.org/tools/compute/):** big data access for SkyServer.

**[SWAN](https://swan.web.cern.ch/):** Service for Web based ANalysis by CERN.

## Geospatial visualizations

**[Regis](https://github.com/ReGIS-org/regis):** Re-GIS (Research Environment for GIS) is an environment for visualizing data on maps. It was developed by the Netherlands eScience Center and TNO.

**[Cesiumjs](https://cesiumjs.org/):** An open-source JavaScript library for world-class 3D mapping of geospatial data.

**[TerriaJS](http://terria.io/):** GIS data catalogue from Australia

**[GeoWeb](https://geoweb.knmi.nl/#/):** Web-based visualization for NetCDF Data. In turn based on [ADAGUC](http://adaguc.knmi.nl/) - OpenDAP/WMS server and client.




## Opendap/WMS/WCS servers

**[THREDDS](https://www.unidata.ucar.edu/software/thredds/current/tds/):** The THREDDS Data Server (TDS) is a web server that provides metadata and data access for scientific datasets, using a variety of remote data access protocols. 

**[ESGF](https://esgf.llnl.gov/):** the Earth System Grid Federation Peer-to-Peer (P2P) enterprise system is a collaboration that develops, deploys and maintains software infrastructure for the management, dissemination, and analysis of model output and observational data.


## Friendly Neighbourhood Hydrological Models

*Hydrological models that we would like to include in eWatercycle II (but see cartoon for unwanted outcome, **credit:** [xkcd](https://xkcd.com/927/)).*

![center-aligned-image](/assets/standards.png){: .align-center}

**[PCR-GLOBWB](http://www.globalhydrology.nl/models/pcr-globwb-2-0/):** PCRaster Global Water Balance is a large-scale, grid-based hydrological model intended for global to regional studies. Resolution of 0.5deg and 5 arcmin in space and days in time. [Github link.](https://github.com/UU-Hydro/PCR-GLOBWB_model)

**[WFLOW](https://wflow.readthedocs.io/en/2017.01/):** Hydrological simulations platform that includes various hydrological models (also allows to introduce new models using the framework). The different models share the same structure but are fairly different with respect to the conceptualisation. The shared software framework includes the basic maps (dem, land-use, soil, etc) and the hydrological routing via the kinematic wave. The Python class framework also exposes the models as an API and is based on the PCRaster. WFLOW includes links to BMI, OpenMI and OpenDAP. [Github link.](https://github.com/openstreams/wflow)

**[HYPE](http://hypecode.smhi.se/):** HYdrological Predictions for the Environment. Hydrological model for simulation of water and water quality over time. [Code link.](https://sourceforge.net/projects/hype/)

**[WALRUS](https://www.wur.nl/en/Research-Results/Chair-groups/Environmental-Sciences/Hydrology-and-Quantitative-Water-Management-Group/Research/WALRUS-1.htm):** Wageningen Lowland Runoff Simulator. [Github link (R).](https://github.com/ClaudiaBrauer/WALRUS)

**[SUMMA](https://ral.ucar.edu/projects/summa):** Structure for Unifying Multiple Modeling Alternatives. An hydrologic modeling framework that can be used for the systematic analysis of alternative model conceptualizations with respect to flux parameterizations, spatial configurations, and numerical solution techniques. Different modeling approaches can then be implemented within the structural core, enabling a controlled and systematic analysis of alternative modeling options. [Github link.](https://github.com/NCAR/summa)


## Related datasets

*Datasets used in hydrological modeling. These datasets are specific and curated and include metadata. Some of the datasets comply with the [FAIR](https://github.com/FAIRMetrics/Metrics/blob/master/ALL.pdf) principles*

**[GEFS](https://www.ncdc.noaa.gov/data-access/model-data/model-datasets/global-ensemble-forecast-system-gefs):** The Global Ensemble Forecast System is a weather forecast model made up of 21 separate forecasts, or ensemble members. 

**[GFS](https://www.ncdc.noaa.gov/data-access/model-data/model-datasets/global-forcast-system-gfs):** The Global Forecast System is a weather forecast model produced by the National Centers for Environmental Prediction (NCEP). 

**[GLCC](https://landcover.usgs.gov/landcoverdata.php):** Land cover data.

**[GLiM](https://www.clisap.de/research/b:-climate-manifestations-and-impacts/crg-chemistry-of-natural-aqueous-solutions/global-lithological-map/):** Global surface lithology at 1 km

**[GLHYMPS](http://www.uni-frankfurt.de/45218039/Global_Irrigation_Map):** Global map of irrigated areas 

**[SoilGrids1km](https://soilgrids.org/#!/?layer=TAXNWRB_250m&vector=1):** Global soils and soil properties at 1 km

**[GRanD](http://sedac.ciesin.columbia.edu/data/set/grand-v1-dams-rev01):** The Global Reservoir and Dam Database

**[HYDRO1k](https://lta.cr.usgs.gov/HYDRO1K):** 1km hydrological DEM and drainage network

**[HydroSHEDS](http://www.hydrosheds.org/):** Hydrological data and maps based on SHuttle Elevation Derivatives at multiple Scales

**[MIRCA2000](http://www.uni-frankfurt.de/45218023/MIRCA):** Global dataset of monthly irrigated and rainfed crop areas around the year 2000 

**[CRU](https://crudata.uea.ac.uk/cru/data/hrg/):** Monthly meteorological forcing from observations 1901-current

**[ERA-40 1.25deg](http://apps.ecmwf.int/datasets/data/era40-daily/levtype=sfc/):** Daily meteorological forcing from ECMRWF reanalysis 1958-2001

**[ERA-Interim 0.8deg](http://data-portal.ecmwf.int/data/d/interim_daily/):** Daily meteorological forcing from ECMRWF reanalysis 1979-current

**[GPCP](https://www.esrl.noaa.gov/psd/data/gridded/data.gpcp.html):** Global precipitation climatology project: daily, monthly, and climatology data sets at 18 composed from combinations of multi-satellite data (microwave, infrared), 6000 gauges and sounding observations

**[MERRA](https://gmao.gsfc.nasa.gov/reanalysis/MERRA/):** Daily meteorological forcing from the NASA Goddard Earth Observing System Data Assimilation System. 

**[NOMANDS](https://www.ncdc.noaa.gov/nomads):** NOAA National Operational Model Archive and Distribution System.  NOMADS is a network of data servers using technologies to access and integrate model and other data stored in geographically distributed repositories in heterogeneous formats. Enables sharing and comparing of model results and is a major collaborative effort, spanning multiple government agencies and academic institutions. The data available include model input and numerical weather prediction gridded output from NCEP, and global climate models (GCMs) and simulations from GFDL and other international institutions

**[WFD](http://www.waterandclimatechange.eu/about/watch-forcing-data-20th-century):** Watch Forcing Dataset: 0.5deg -  3/6 hourly meteorological forcing from ECMRWF reanalysis (ERA40) bias-corrected and extrapolated by CRU TS and GPCP (rainfall) and corrections for under catch

**[EWA](http://www.bafg.de/GRDC/EN/04_spcldtbss/42_EWA/ewa_node.html):** European Water Archive (catchment data)

**[FLUXNET](https://daac.ornl.gov/cgi-bin/dataset_lister.pl?p=9):** Water vapor, energy, and CO2land-atmosphere ﬂuxes from towers

**[GRACE](https://grace.jpl.nasa.gov/):** Gravity recovery and climate experiment

**[GRDC](http://www.bafg.de/GRDC/EN/Home/homepage_node.html):** Global Runoff Data Center

**[ISMN](https://ismn.geo.tuwien.ac.at/):** Global network of soil moisture data

**[MOPEX](http://www.nws.noaa.gov/ohd/mopex/mo_datasets.htm):** US catchment data

**[RIVDIS](https://daac.ornl.gov/RIVDIS/guides/rivdis_guide.html):** Global River Discharge 1807-1991

**[NASA Global Change Master Directory (GCMD)](https://gcmd.nasa.gov/index.html):** Earth science dataset and service descriptions, which cover subject areas within the Earth and environmental sciences. Users may perform searches through the Directory’s website using controlled keywords, free-text searches, map/date searches or any combination of these 

**[NASA Global Hydrology Resource Center (GHRC) DAAC](https://ghrc.nsstc.nasa.gov/home/):** A comprehensive active archive of both data and knowledge augmentation services, with a focus on hazardous weather, its governing dynamical and physical processes, and associated applications. Focuses on lightning, tropical cyclones and storm-induced hazards through integrated collections of satellite, airborne, and in-situ data sets.

**[USGS (US Geological Survey) Science Data Catalog](https://data.usgs.gov/datacatalog/#fq=dataType%3A(collection%20OR%20non-collection)&q=*%3A*):** (near) Real-time data and information on current conditions and earth observations

**[Australian Geoscience Data Cube (AGDC)](https://github.com/GeoscienceAustralia/agdc)**











