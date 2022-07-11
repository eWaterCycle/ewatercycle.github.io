---
layout: page
title: Demo
---

If you would like to use the eWaterCycle platform, we have a machine available for demo purposes.

You can find the machine at https://demo1.ewatercycle-nle.src.surf-hosted.nl/

Note that you need an account to start an experiment on our Jupyterhub. Please contact us at questions@ewatercycle.org to get one. Without an account, you can still browse the explorer. 


## Models available on the demo machine in the explorer

The eWaterCycle explorer can generate a notebook for you that runs a simple experiment using the selected model, forcing, and parameter set.

| Model |
| ----- |
| Marrmot M01 |
| PCRGlobWB |
| Wflow |

## Parameter Sets available on the demo machine

The demo machines contains a selection of parameter sets we use to develop and test the eWaterCyce platform. This makes it possible to quickly try out the eWaterCycle platform. As the demo machine is used for various developments, the data available on this machine may change without notice.

Which parameter sets are available on any machine running the eWaterCycle platform can be viewed with ewatercycle.parameter_sets.available_parameter_sets()

| Target Model  | Description                                | Identifier                                  | Note |
| ------------- | ------------------------------------------ | ------------------------------------------- | ---- |
| Hype          | Rhine basin                                | hype_Rhine                                  |
| Hype          | Great kei basin                            | hype_Great_Kei                              |
| Hype          | Doring basin                               | hype_Doring                                 |
| Hype          | Merrimack basin                            | hype_Merrimack                              |
| Hype          | Meuse basin                                | hype_Meuse                                  |
| Hype          | Savannah basin                             | hype_Savannah                               |
| Lisflood      | Fraser basin                               | lisflood_fraser                             |
| Lisflood      | 6 regions, calibrated for ERA5)            | lisflood_global-masked_01degree_ERA5        |
| Lisflood      | 6 regions, calibrated for ERA-Interim)     | lisflood_global-masked_01degree_ERA-Interim |
| Marrmot M01   | Buffalo River                              |                                             | includes forcing |
| Marrmot M01   | Savannah basin                             |                                             | includes forcing |
| PCRGlobWB     | Rhine-Meuse 30min resolution               | pcrglobwb_rhinemeuse_30min                  |
| PCRGlobWB     | Rhine 05min resolution                     | pcrglobwb_rhine_05min                       |
| PCRGlobWB     | Great Kei 05min resolution                 | pcrglobwb_great_kei_05min                   |
| PCRGlobWB     | Doring 05min resolution                    | pcrglobwb_doring_05min                      |
| PCRGlobWB     | Merrimack 05min resolution                 | pcrglobwb_merrimack_05min                   |
| PCRGlobWB     | Meuse 05min resolution                     | pcrglobwb_meuse_05min                       |
| PCRGlobWB     | Savannah 05min resolution                  | pcrglobwb_savannah_05min                    |
| Wflow         | Rhine SBM                                  | wflow_rhine_sbm_nc                          |
| Wflow         | Merrimack basin                            | wflow_merrimack_techpaper                   |
| Wflow         | Rhine basin calibrated for ERA-Interim     | wflow_Rhine_ERA-Interim-calibrated          |
| Wflow         | Great Kei basin calibrated for ERA-Interim | wflow_Great_Kei_ERA-Interim-calibrated      |
| Wflow         | Doring basin calibrated for ERA-Interim    | wflow_Doring_ERA-Interim-calibrated         |
| Wflow         | Merrimack basin calibrated for ERA-Interim | wflow_Merrimack_ERA-Interim-calibrated      |
| Wflow         | Meuse basin calibrated for ERA-Interim     | wflow_Meuse_ERA-Interim-calibrated          |
| Wflow         | Savannah basin calibrated for ERA-Interim  | wflow_Savannah_ERA-Interim-calibrated       |
| Wflow         | Rhine basin calibrated for ERA5            | wflow_Rhine_ERA5-calibrated                 |
| Wflow         | Great Kei basin calibrated for ERA5.       | wflow_Great_Kei_ERA5-calibrated             |
| Wflow         | Doring basin calibrated for ERA5           | wflow_Doring_ERA5-calibrated                |
| Wflow         | Merrimack basin calibrated for ERA5        | wflow_Merrimack_ERA5-calibrated             |
| Wflow         | Meuse basin calibrated for ERA5            | wflow_Meuse_ERA5-calibrated                 |
| Wflow         | Savannah basin calibrated for ERA5         | wflow_Savannah_ERA5-calibrated              |







## Frequently asked questions

**Q: Why do I get an error if I change the start and end date of my simulation?**

A: Due to storage constraints, the demo machine has a limited set of forcing data. Not all of ERA-5 and ERA-Interim is available.

