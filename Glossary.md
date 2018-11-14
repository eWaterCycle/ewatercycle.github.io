---
layout: home
title: Glossary
---
# eWaterCycle Glossary

This glossary is a list of terms commonly used in eWaterCycle II project. 

***Disclaimer:** The definitions and descriptions may not be agreed upon by every individual in the hydrological community, but will serves to provide a common ground for anyone working in the eWaterCycle II project.*

**Model:** A model is the (software) implementation of an algorithm. It computes state vectors using previous state vectors, parameters and/or observations. 
Note that in this definition model does not include the parameters and/or observations (see Input set below).

**Hydrological model:** A simplification of a real-world system (e.g., surface water, soil water, wetland, groundwater, estuary) that aids in understanding, predicting, and managing water resources [Wikipedia]. Typical models are partially based on physics and partially on concepts to simplify reality. A model will receive an Input set, to compute flux/storage of water. The Output will be the derived variables or state variables that are exported or stored for (future) use. In the case of hydrological models, typical outputs are discharge to river network or discharge+river flow.

**Input set:** everything a model needs to run: e.g., Forcings (precipitation, driver for evaporation - sun or sun+wind), Model parameters, background parameters. 

**Types of Hydrological models:**
 * **Grid-based / distributed model:** make predictions that are distributed in space by dividing the entire catchment in to small units, usually square cells or triangulated irregular network, so that the parameters, inputs and outputs can vary spatially. 
 * **Lumped models:** the entire river basin is taken as a single unit and spatial variability is disregarded.
 
**Types of models to simulate global hydrology (Wada et al., 2017):**
  * **Large-scale Hydrological Models (LHMs):** hydrological process at long temporal (decades) but fine spatial resolution (10-50 km). Model include human-induced change. Typically simulate the dynamics of soil moisture due to precipitation and evapotranspiration, the generation of runoff, and the discharge  through the river network on a coarse grid. Most LHMs are based on water balance concept and track the flow of water. (Example: PCR-GLOBWB)
  * **Land-Surface Models (LSMs):** Simplified simulation of the surface hydrology associated with human-induced change with focus of the interaction of the land-atmosphere for climate models.
  * **Dynamic Vegetation Models (DVMs):** simplified treatment of the surface hydrology and human and use change with a focus on the biosphere.

**Forcing (function of time):** model input that is not impacted by the model. Forcing data is used to define the necessary boundary conditions to the model throughout its time evolution, such as air temperature and precipitation.

**Observations:** measurements of physical phenomena (can relate to forcings states, derived states and output): e.g., discharge gauge, soil moisture.

**Model parameters:** fixed parameters (depth of river, land use, irrigation channels, dams). Considered constant during a model run.

**States:** Set of independent time-dependent variables within the model. Time-stepping the model is equivalent to progressing the state variables with time. 

**Derived states:** variables (often observed) not included in the state that are calculated diagnostically from states (e.g., brightness temp).

**Initial state and spin-up:** The initial state of an hydrological model is a complete model state that allows the model to evolve from. It can have a strong effect on the model evolution path. Usually one needs a spin-up to arrive at a physically consistent state that is close to a given set of observations. Good spin-up will guarantee that the physical conditions are updated. The duration and behaviour of the spin-up is input set dependent.

**Schematization:** all the time-independent data and information that is required to start a model (e.g., configuration file). Together with forcing and initial state, this defines the input of a model.

**Data assimilation:** continuous updating of the initial state for forecast, based on observations. 

**Assimilation time step:** we will have a method to represent a model state including its uncertainty, such as for example an ensemble. At t1=t0+t we introduce observations (with uncertainty) and assimilate these into the state using a Data Assimilation (DA) method, such as Ensemble Kalman Filtering (EnKF). Then we run the model on the state until the next observation time step. This is referred to as a single assimilation time step, and will repeat for another time step (t2=t0+2t).

**Time step (of a model):** the time difference (in model time, not wallclock) between outputs of the model. For a large number of hydrological models, the timestep is “daily”.

**Ensemble Kalman Filter (EnKF):** Filter that does a Monte Carlo implementation of the Bayesian update problem (Bayes theorem used to obtain pdf from the data likelihood- the posterior distribution). It allows to advance the model in time, using new observations, to correct our knowledge of the system. For high-dimensional problems we must have an ensemble of Kalman filters to replace the COV matrix by the sample COV (computed from the ensemble). The EKF is used for data assimilation and gives a statistical approximation of the state of the modeled system by sampling the errors of the forecast and analysis 

**Hydrograph:** graph showing the rate of flow (discharge) vs. time (passing a specific location in a river or other channel). [m3/sec]

**Standard FAIR data repository:** contains model output, forcings and observations. 

**BMI:** Basic Model Interface (BMI) - specifies a library interface for computer programs that use a time-stepping procedure to calculate physical processes, discretized on a spatial grid. The interface is predominantly used in the hydrological community for coupling various models.

**gRPC:** Remote procedure call framework by Google. This package allows communication between running processes using protocol buffers. gRPC allows communication between applications written in different languages, running on different processors.

**Forecast (general):** output of a model run (or ensemble of model runs) for a feature time. If the model needs forcing, than a forecast of forcing is also needed. In hydrology forecasts usually require atmospheric forecasts as inputs.

**Forecast (data assimilation):** the state of the model, just prior to updating / assimilating new observations into the model. The Forecast is based on the analysis state of the previous timestep, and forcings if applicable.

**Analysis (data assimilation):** the state of the model after updating / assimilating new observations into the model. Sometimes explained as “the best estimate of the current state based on observations and historical model runs”. Note that the observation itself has some pdf, that the new forecast has to take into account. 

**Reanalysis:** model state and output generated using forcing that has become available (long) after real time. Usually considered “the best estimate of how things were”.

--------------------------------

