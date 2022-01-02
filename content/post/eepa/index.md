---
title: The Edinburgh Elasto-Plastic Adhesion (EEPA) Model... in EDEM 2018!

subtitle: 'Now included as inbuilt model in EDEM'

# Summary for listings and search engines
summary: The EEPA model is now included as a default model in EDEM offering all the benefits with reduced computational overheads.

# Link this post with a project
projects: 
 - phd
 - gran_ed

# Date published
date: "2017-10-10T00:00:00Z"

# Date updated
# lastmod: "2021-12-01T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Edinburgh Elasto-Plastic Adhesion (EEPA) Model'
  focal_point: ""
  placement: 2
  preview_only: false

authors:
- admin

tags:
- DEM
- EEPA
- EDEM

categories:
- Numerical Methods
- DEM

math: true
---

{{% callout note %}}
This post was originally published on [www.edemsimulation.com](https://www.edemsimulation.com/news/more-particles-faster-edem-2018/).

Since Altair's aquistion of EDEM in 2020 the original post has been taken down. A cached copy of that post can be found [here](https://shackletonventures.com/more-particlesfaster-with-edem-2018/).
{{% /callout %}}

## Introduction
---

EDEM has just announced the new 2018 version of the software that includes many new features with a focus on performance on productivity. I don't normally show much interest in the release of new version of software but this is a bit different. 
I'm excited to announce that the **Edinburgh Elasto-Plastic Adhesion (EEPA) Model**[^1]<sup>,</sup>[^2] which started it's life in my Ph.D. 

This is a significant milestone and highlights how popular the model has become since it's release as an API model to EDEM users just over 3 years ago. EDEM is considered the leading Discrete Element Method software application for bulk material simulation in the market and is used my many companies across fields as varied as mining, food manufacturing and pharmaceuticals. 
EDEM is also used by thousands of researchers in more then 200 universities around the world.

> In parallel, a new contact model for modeling complex cohesive materials such as fine dry powders, organic materials, soil and ore fines is now available as a standard built-in contact model in EDEM. This model, called Edinburgh Elasto-Plastic Adhesion (EEPA), offers a solution for cohesive granular solids whose behavior changes depending on the stresses experienced by the material beforehand. It can help realistically simulate applications such as material adhesion to earthmoving equipment, soil-tyre interaction or for instance a cohesive powder compaction process such as tabletting.

This will allow users to take advantage of the EEPA model without the computational cost of running the API. 
This could be as much as 30% reduction in runtime for your simulations - effectively for free!! All of the features of the API model [^3]<sup>,</sup>[^4] exist and are nicely integrated into the GUI. 
There should also be a GPU implementation of the modelling making bigger simulations more tractable.


<div class="row">
  <div class="column_2">
    {{< figure src="contact_model_physics.png" title="**EEPA now available in Contact Model Physics**" height="50%" >}} 
  </div>
  <div class="column_2">
    {{< figure src="eepa_prefs.png" title="**Inputting EEPA Parameters**" >}}
  </div>
</div>


I hope this helps making simulation of cohesive granular materials more accessible to more user and that the models popularity continues to grow.


## Citations
---
{{< cite page="/publication/morrissey_2013" view="4" >}}

{{< cite page="/publication/thakur_et_al_2014" view="4" >}}

## References
--- 


[^1]:	Morrissey, J.P.,  *Discrete Element Modelling of Iron Ore Fines to Include the Effects of Moisture and Fines*, University of Edinburgh, 2013. https://www.era.lib.ed.ac.uk/handle/1842/8270.

[^2]:	Thakur, S.C., Morrissey, J.P., Sun, J., Chen, J.F., & Ooi, J.Y. (2014). *Micromechanical analysis of
cohesive granular materials using discrete element method with an adhesive elasto-plastic contact
model.* Granular Matter, 16(3), 383–400. doi:10.1007/s10035-014-0506-4

[^3]:	Morrissey, J.P., Thakur, S., & Ooi, J.Y. (2014a). *EDEM Contact Model: Adhesive Elasto-Plastic Model.
University of Edinburgh.* doi:10.13140/RG.2.2.10139.18724

[^4]:	Morrissey, J.P., Thakur, S., & Ooi, J.Y. (2014b). *Using the Elasto-plastic Adhesion Model: Example
Problem. University of Edinburgh.* doi:10.13140/RG.2.2.10978.04809

