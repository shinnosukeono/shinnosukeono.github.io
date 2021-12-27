---
title: "Discrete Element Modelling of Iron Ore Pellets to Include the Effects of Moisture and Fines"
summary: "Characterisation and calibration of iron ore fines for DEM simulations" 
tags:
- DEM
- Data Analytics
- Calibration
- Characterisation

date: "2009-09-27T00:00:00Z"
date_end: "2013-06-30T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: ""
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
- album: phd
  image: EEPA.png
  caption: Edinburgh Elasto-Plastic Adhesion contact model force-overlap relationship
- album: phd
  image: bulkdensity_vs_moisture.png
  caption: Bulk density comparison from uniaxial tests for different types of iron ore fines at varying moisture contents
- album: phd
  image: EPT.jpg
  caption: "The Edinburgh Powder Tester **(EPT)**: a) the EPT b) Confined consolidation of sample in EPT c) Unconfined compression to failure in EPT d) Typical Failed sample"
- album: phd
  image: EPT_Sim.png
  caption: DEM simulation of EPT consisting of confined consolidation and unconfined compression
- album: phd
  image: EPT_DEM_comp.png
  caption: Comparison of DEM flow function with experimentally measured flow function at various moisture contents
- album: phd
  image: exp_ff_kprs.png
  caption: Uniaxial flow function from multiple uniaxial tests for iron ore fines at various mositure contents
- album: phd
  image: exp_uc_stress_strain.png
  caption: Stress-strain curves for iron or fines at various consolidation stresses
- album: phd
  image: ff_comp.png
  caption: Flow function comparison from uniaxial tests for different types of iron ore fines at varying moisture contents
- album: phd
  image: planar_shearband.png
  caption: Shear band development in unconfined compression of numerical sample
- album: phd
  image: uuys_vs_moisture.png
  caption: Unconfined yield strength comparison from uniaxial tests for different types of iron ore fines at varying moisture contents

---

# Introduction
---

Across industry the majority of raw materials handled are particulate in nature, ranging in size and properties from aggregates to powders. 
The stress regimes experienced by the granular solids vary and the exhibited bulk behaviours can be complex and unexpected. 
The prevalence of granular solids makes them an area of interest for industry and researchers alike as many challenges still remain, such as dealing with complex cohesive behaviour in materials, which often gives rise to handling difficulties.
The cohesive strength of a bulk material depends on the consolidation stress it has experienced. As a result, the stress history in the material leading up to a handling scenario needs to be considered when evaluating its handling behaviour.


Storage and transportation are an important part of the process chain for industries where particulate solids are commonplace. 
Failure to properly account for the cohesive nature of a particulate solid can be costly as it can easily lead to blockages in a silo such as ratholing or arching near the outlet during discharge. 


# Research Goals
Cohesive granular solids such as powders can have a very loose, highly porous structure under very low stresses. 
While it is possible to generate similar initial packing structures in a DEM simulation, it is not feasible to attempt to match all stress states. 
In this study, stress states larger than 5-10 kPa are of interest and as such all packing structures will aim to match the experimental results from this stress level. 

## Numerical
The main aim of the research is to develop an improved contact model to better capture the behaviour of cohesive granular solids, particularly iron ore fines, which are significantly affected by the presence of moisture. In order for numerical simulations to be successfully used for more efficient design and management of industrial equipment and structures, the transition from qualitative to quantitative prediction needs to be made. 

In this study a mesoscopic adhesive contact model that accounts for contact plasticity and stress history dependency in the bulk solid, the **Edinburgh Elasto-Plastic Adhesion (EEPA)** mode, has been presented and mathematically verified. A parametric study of the DEM contact model parameters was conducted to gain a deeper understating of the effect of input parameters on the simulated cohesive bulk behaviour.

{{< figure src="albums/phd/EEPA.png" title="**Edinburgh Elasto-Plastic Adhesion (EEPA) Model**"  >}}


The **EEPA** contact model has been used to predict an experimental flow function of KPRS iron ore fines. 
The contact model has demonstrated the ability to capture the stress history dependent behaviour that exists in cohesive granular solids. 
The DEM simulations provide a very close match to the experimental flow functions, with the predicted unconfined strengths found to be within the standard deviations of the experimental results. 

{{< figure src="albums/phd/EPT_DEM_comp.png" title="**Comparison between Experimental and DEM Flow Functions for Iron ore fines**"  >}}


Investigations into the failure mode predicted by the DEM simulations show that the samples are failing from the development of shear planes similar to those observed experimentally.

{{< figure src="albums/phd/planar_shearband.png" title="**Shear Failure mode in DEM Simulations**"  >}}


## Experimental
To help achieve this a secondary aim is to rigorously characterise the properties of the material that are required for calibration of a numerical model. 
A study of the effect of the parameters of the adhesive contact model is also carried out. 
In this study a particular focus is paid to the two types of iron ore fines: **KPBO** and **KPRS**, with the purpose of characterising the different materials types and assessing the distinct behaviour exhibited by the different fines.

A comprehensive study on the effect of cohesion arising from the addition of moisture on the behaviour of two types of LKAB iron ore fines (KPBO and KPRS) has been carried out using a uniaxial tester, the **Edinburgh Powder Tester (EPT)**. 
The addition of moisture to the sample has been found to have a significant effect on both kinds of fines. 
KPRS fines were found to have a much higher unconfined strength and flow function at higher moisture contents, and also show a greater
increase in cohesion with the addition of moisture, while at moisture contents of less than 2% the KPBO fines demonstrate higher unconfined yield strength. 
The KPBO fines were also found to achieve a significantly looser initial packing at much lower moisture content when compared to the KPRS fines. 
The lateral pressure ratio has also been evaluated.


# Image Gallery
---

{{< gallery album="phd" resize_options="x150" >}}



# Video Gallery
---

{{< youtube 1ImEki7yguQ >}}


{{< youtube Big3upY2fJw >}}


{{< youtube dRgQn6ZiQK0 >}}


{{< youtube -q4zcXTXgM4 >}}


{{< youtube YArm17GYORE >}}



{{< youtube flw11XeAU5M >}}



---


