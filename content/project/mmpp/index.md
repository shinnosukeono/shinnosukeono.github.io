---
title: Models for the Manufacturing of Particulate Process (Models MPP)
summary: A project focused on establishing a generic framework and core capability to improve industrial productivity.
tags:
- Model Driven Design (MDD) Framework
- DEM
- PBM
- DEM-PBM
- Coupled Models
- Granulation
- Cohesion
- EEPA

date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: DEM simulation of granule formation in a TSG
  focal_point: Smart

links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/jp_morr
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""

# gallery captions
gallery_item:
- album: mmpp
  image: Example_screw_configuration.png
  caption: Examlpe Screw Configuration for periodic simulations
- album: mmpp
  image: TSG_streamlines.png
  caption: Particle streamlines in full-scale TSG
- album: mmpp
  image: CG_solidfraction.png
  caption: Solid fraction distribution on typical elements in a TSG
- album: mmpp
  image: reduced_domain_overview.png
  caption: Reduced-domain TSG model in EDEM
- album: mmpp
  image: particle_sizes.png
  caption: Reduced-domain model - effect of particle size
- album: mmpp
  image: no_periodic_reduced_domain.png
  caption: Agglomeration in cohesive, non-periodic reduced domain model
  
---


# Introduction
---

Particle processes in industry are both common and challenging. The complexity of particulate systems means that it is prohibitively difficult to gain a comprehensive understanding of the particulate mechanics which control a process using solely laboratory experiments. Even though some numerical models are available in the literature which describe particle processes, these tend to be inadequate to meet the requirements of industry. 
Industry requires robust models which contain the key relevant physics, which are user-friendly and which are focused on delivering the output product specifications given a limited number of measured input parameters.

Despite the significant academic activity in the development of multi-scale, multi-phase modelling approaches, few of the models originating in academia are fully implemented in industrial practice. 
As a result, the full benefits of model-based development have not been derived. The creation and implementation of a better approach to implementing useful models from academia into industrial practice could therefore lead to significant economic benefits relating to enhanced speed of development, reduced development costs and improved product quality.

This project aims to create a generally applicable framework for transferring academic innovations in the modelling of particulate materials into industrial practice in the UK. The process of twin-screw granulation has been selected as an exemplar industrial process which is simulated across multiple scales using the coupled methods of population balance modelling and the discrete element method.

## Project Members
The project involved **two academic partners**, the [University of Edinburgh](https://www.ed.ac.uk/) and the [University of Sheffield](https://www.sheffield.ac.uk/), and **six industrial partners**: [Pfizer](https://www.pfizer.co.uk/), [AstraZeneca](https://www.astrazeneca.co.uk/), [Procter and Gamble](https://www.pg.co.uk/), [Johnson Matthey](https://matthey.com/en), [Process Systems Enterprise](https://www.psenterprise.com/) and [DEM Solutions](https://www.altair.com/edem/) (*Now Altair EDEM*). The project was led by the [Centre for Process Innovation](https://www.uk-cpi.com/) with funding coming from Innovate UK.


## Project Summary
The two-year Models for the **Manufacturing of Particulate Process (Models MPP)** project focused on establishing a generic framework and core capability to improve industrial productivity.

As part of the drive to provide more leverage and integration of the wealth of formulations expertise in the UK, the £700,000 project, funded by **Innovate UK** as part of CPI’s National Formulation Centre Strategic Projects Programme, has facilitated the translation of the UK’s world-leading expertise in computational modelling and simulation for the manufacturing of particulate processes. 

Connecting industry and university research groups with state-of-the-art technology has resulted in the development of a generic framework for translating particle models of industrial relevance into industrial practice. The developed framework incorporates a decision support methodology/​tool for models development that will allow easier access and adoption by leading UK-based industrial organisations. 
These models are expected to be deployed within industry to accelerate the development of innovative products and improve productivity and cost-effectiveness of product manufacturing processes.

This framework will provide guidance for the coupling of well-established computer modelling techniques at different size scales, to enable development scientists and engineers to develop models that simulate different parts of manufacturing processes from the dispensing of input materials through mixing, agglomeration and other subsequent processing steps.

**Twin-screw wet granulation**, a method used in a number of industry sectors, was used as an exemplar. Wet granulation is a process in which small primary particles are joined together using agitation and a liquid binder. The purpose is to improve the properties of very fine cohesive powders used in formulated products such as pharmaceuticals, ceramics, detergents and fertilizers.
Granulation is commonly used in the pharmaceutical industry during tablet manufacturing. Fine powders are granulated to improve flow prior to tableting and reduce the potential for dusting and other production issues. The formation of granules also helps to reduce segregation and improve the content uniformity of the final product which is critical for consistent product performance.

The academic partners at the Universities of Edinburgh and Sheffield conducted a review of the current state of the art and used this insight to develop coupled models using EDEM and PSE software platforms and the technology vendor’s expertise in developing industrially robust models. These models were validated using real life trials at the industrial partner’s production facilities. 

While granulation is an important process in many industries, including pharmaceuticals, foods and agrochemicals, the framework provided by Models MPP means it can be broadly re-applied to other manufacturing operations and industries.

The legacy capability established from this project will be applied to other CPI strategic projects, e.g. in the **development of a digital twin** with a sister National Formulation Centre strategic project focused on a fully PAT enabled twin screw extruder (***‘PROSPECT CP’***).




# Project Gallery
---

{{< gallery album="mmpp" resize_options="x150">}} 

{{< youtube NkXqJJG5tWg >}}

---