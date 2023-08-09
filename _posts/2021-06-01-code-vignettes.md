---
title: "Tutorials and Vignettes"
excerpt: "Self-guided resources for using NOAA FIT tools"
date: 2021-06-01
toc: true
categories:
  - NOAA FIT
tags:
  - fish and fisheries drawer
  - tutorials
  - software user resources
---
These code vignettes will walk you through how to set up and use some commonly used fish stock assessment models. All of these tools can be found in [NOAA Fisheries Integrated Toolbox](https://noaa-fisheries-integrated-toolbox.github.io/).

## [Stock Synthesis (SS3)](https://noaa-fisheries-integrated-toolbox.github.io/SS3)
Stock Synthesis (SS3) is an age-structured population dynamics model that is used to assess the impact of fisheries on fish and shellfish stocks while taking into account the influence of environmental factors.

- [Getting started with SS3](https://nmfs-stock-synthesis.github.io/doc/Getting_Started_SS.html)

- [Developing an SS3 model](https://nmfs-stock-synthesis.github.io/doc/ss_model_tips.html)

## [Woods Hole Assessment Model (WHAM)](https://timjmiller.github.io/wham/)
The Woods Hole Assessment Model (WHAM) is a general state-space age-structured stock assessment framework designed to include environmental effects on population processes. The state-space framework is attractive because it can estimate observation and process error, as well as naturally propagate random effect parameters in stock projections. WHAM can be configured to estimate a range of assessment models including statistical catch-at-age (SCAA) model with recruitments as fixed effects, SCAA with recruitments as random effects, and “full state-space model”, abundance at all ages are random effects.

- [WHAM Tutorial](https://noaa-fisheries-integrated-toolbox.github.io/WHAM)

## [Metapopulation Assessment System (MAS)](https://nmfs-fish-tools.github.io/MAS/)
The Metapopulation Assessment System (MAS) is a modular tool for creating and fitting fisheries stock assessment models. The R interface to MAS, [r4MAS](https://nmfs-fish-tools.github.io/r4MAS/index.html) allows users to build and run MAS models directly using the R language. It also includes functions to help translate between MAS and other stock assessment software and to plot outputs of MAS models, including estimates of key biological and observation parameters and derived quantities such as biological reference points, estimated biomass, and estimated numbers-at-age.

- [Getting started with r4MAS](https://nmfs-fish-tools.github.io/r4MAS/articles/001_Introduction.html)
