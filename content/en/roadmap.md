---
title: AMSIMP Roadmap
sidebar: false
---

## Overview
The main aim of AMSIMP is to develop an open-source solution that leverages machine learning to improve numerical weather prediction. Currently, as far as we are aware, there are no machine learning models in use for numerical weather prediction. We’re applying machine learning to weather prediction and making it available for everyone: citizens in particular. The goal of this page is to highlight the short and long term aims and goals of AMSIMP.

## Goals

### Model Architecture

The existing model’s performance is lacking. As described in the most recent paper, the spatial awareness of the model as measured by the anomaly correlation coefficient becomes useful after approximately 120 hours of forecast time. This can be regarded as quite poor. It appears that the spatial aspect of a weather forecast is not being captured by the current neural network architecture. A couple of new approaches currently under development, however, should solve this issue.

One of the most natural coordinate systems to use on Earth is a latitude‐longitude grid. This was the coordinate system of choice for this project due to its simplicity, but, this system has singularities at the North Pole and South Pole that makes it difficult to use translationally‐invariant convolution operations on this grid. 

To combat this particular problem in this project, the poles were excluded from the dataset, however, a more elegant solution to preserve spatial locality is to approximate data on the globe using the cubed sphere. This projection has been shown to give more uniformly sized grid cells than the alternative projections and to also produce better solutions to finite‐difference and discontinuous Galerkin approximations to partial differential equations on the sphere. 

The cubed sphere is used for state‐of‐the‐art NWP such as in the FV3 dynamical core of the National Oceanic and Atmospheric Administration's Global Forecast System model. This is an avenue that will be explored in the coming months.

### Ensemble Prediction System

### Verification Metrics

### Resolution

With the present model, it was decided to use a spatial resolution of approximately 100 kilometres (1 degree). With the model currently in development, the spatial resolution is approximately 25 kilometres (0.25 degrees). This is a standard resolution for global meteorological weather models, such as those used by the National Weather Service and the European Centre for Medium-Range Weather Forecasting. 

Through higher spatial resolutions, a forecast can show the effects of local air currents, topography and soil cover. These forecasts produced thereby show local weather differences in a more precise way. High resolution produces high precision, hence, while choosing a lower resolution may have lowered the computational burden during training, it may have had a significant effect on the performance of the model. How this is typically combatted is through regional models, which typically can have higher resolutions than their global counterparts. As such, once a satisfactory level of performance is achieved with the global model, the architecture will be generalised to function on a regional level. At present, American and European regional models are proposed for development. Further development of regional models for other regions may be considered at a later stage.

### Weather Forecast Website and Mobile Application

## Milestones

## Timeline
