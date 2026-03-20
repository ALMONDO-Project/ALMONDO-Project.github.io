---
layout: post
title: Data-Model Integration and Software Implementation Report
tags: [Page]
categories: Publications
subcategory: "Project Reports"
date: 2026-03-20
excerpt: "This report presents the integration between empirical data and the ALMONDO opinion-dynamics model, along with the development of the simulation platform and its user-friendly web interface."
---

**Project Milestone 3 & 4 📊💻** - The Data-Model Integration and Software Implementation Report is now available to be downloaded.



# 📊 Report Description 

This report documents the integration of empirical data with the ALMONDO opinion-dynamics model and the development of the associated simulation software and web interface.

The work builds on the ALMONDO project, funded by the European Union – NextGenerationEU (NRRP), and focuses on bridging experimental evidence with computational modeling. In particular, the model is calibrated using data from a nationally representative Italian survey experiment (N=1,633), capturing how individuals update beliefs about climate change under advocacy and skepticism treatments. The calibration procedure translates observed belief dynamics into behavioral parameters, such as underreaction and motivated reasoning, enabling realistic simulation scenarios.

The report details the full calibration pipeline, including dataset preparation, parameter estimation through cross-entropy minimization, and robustness checks. Results indicate substantial baseline underreaction in belief updating, while motivated reasoning plays a comparatively smaller role. The calibration output serves as a key input for the simulation environment.

On the software side, the report describes the architecture of the ALMONDO platform, which combines:
- a backend modeling layer based on NDlib and NetworkX,
- a simulation engine supporting single runs and Monte Carlo experiments,
- and a React-based web interface for scenario configuration and interactive visualization.

The platform enables users to define scenarios, configure behavioral and network parameters, simulate lobbying strategies, and analyze opinion dynamics through advanced metrics such as polarization, clustering, and influence performance.

The final system represents a fully integrated research pipeline, linking empirical data, simulation modeling, and user-oriented tools. This enhances reproducibility, accessibility, and the practical usability of the ALMONDO framework for both researchers and policymakers.

<a href="/assets/documents/ALMONDO_Data_Model_Software_Report.pdf" download style="display: inline-block; padding: 10px 20px; background-color: #98cbcf; color: black; text-decoration: none; border-radius: 5px; font-size: 16px; text-align: center;">Download Report 📊</a>