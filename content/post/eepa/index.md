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
I'm excited to announce that the **Edinburgh Elasto-Plastic Adhesion (EEPA) Model** which started it's life in my Ph.D. 

This is a significant milestone and highlights how popular the model has become since it's release as an API model to EDEM users just over 3 years ago. EDEM is considered the leading Discrete Element Method software application for bulk material simulation in the market and is used my many companies across fields as varied as mining, food manufacturing and pharmaceuticals. 
EDEM is also used by thousands of researchers in more then 200 universities around the world.

> In parallel, a new contact model for modeling complex cohesive materials such as fine dry powders, organic materials, soil and ore fines is now available as a standard built-in contact model in EDEM. This model, called Edinburgh Elasto-Plastic Adhesion (EEPA), offers a solution for cohesive granular solids whose behavior changes depending on the stresses experienced by the material beforehand. It can help realistically simulate applications such as material adhesion to earthmoving equipment, soil-tyre interaction or for instance a cohesive powder compaction process such as tabletting.

This will allow users to take advantage of the EEPA model without the computational cost of running the API. 
This could be as much as 30% reduction in runtime for your simulations - effectively for free!! All of the features of the API model exist and are nicely integrated into the GUI. 
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

{{< cite page="/publication/morrissey_2013" view="4" >}}

{{< cite page="/publication/thakur_et_al_2014" view="4" >}}

# References
[^1]:	American Society of Mechanical Engineers., *Guide for verification and validation in computational solid mechanics*, American Society of Mechanical Engineers, 2006. https://www.asme.org/products/codes-standards/v-v-10-2006-guide-verification-validation (accessed July 13, 2017).

[^2]:	T.A. Bell, E.J. Catalano, Z. Zhong, J.Y. Ooi, J.M. Rotter, *Evaluation of the Edinburgh powder tester*, in: PARTEC 2007 - Congr. Part. Technol., Nürnberg, 2007: pp. 1–6. http://scholar.google.com/scholar?hl=en&btnG=Search&q=intitle:Evaluation+of+the+Edinburgh+Powder+Tester#0 (accessed October 5, 2013).

[^3]:	L.P. Maltby, G.G. Enstad, *Uniaxial Tester for Quality Control and Flow Property Characterization of Powders*, Powder Handl. Process. 13 (1993) 135–139.

[^4]:	M. Röck, M. Ostendorf, J. Schwedes, *Development of an Uniaxial Caking Tester*, Chem. Eng. Technol. 29 (2006) 679–685. doi:10.1002/ceat.200600068.

[^5]:	R.E. Freeman, X. Fu, *The Development of a Compact Uniaxial Tester*, in: Part. Syst. Anal. 2011, Edinburgh, UK, 2011: pp. 1–6.

[^6]:	Z. Zhong, J.Y. Ooi, J.M. Rotter, *Predicting the handlability of a coal blend from measurements on the source coals*, Fuel. 84 (2005) 2267–2274. doi:10.1016/j.fuel.2005.05.023.

[^7]:	S.C. Thakur, H. Ahmadian, J. Sun, J.Y. Ooi, *An experimental and numerical study of packing, compression, and caking behaviour of detergent powders*, Particuology. 12 (2014) 2–12. doi:10.1016/j.partic.2013.06.009.

[^8]:	J.P. Morrissey, *Discrete Element Modelling of Iron Ore Fines to Include the Effects of Moisture and Fines*, University of Edinburgh, 2013. https://www.era.lib.ed.ac.uk/handle/1842/8270.

[^9]:	S.C. Thakur, J.P. Morrissey, J. Sun, J.F. Chen, J.Y. Ooi, *Micromechanical analysis of cohesive granular materials using discrete element method with an adhesive elasto-plastic contact model*, Granul. Matter. 16 (2014) 383–400. doi:10.1007/s10035-014-0506-4.

[^10]:	S.C. Thakur, J.Y. Ooi, H. Ahmadian, *Scaling of discrete element model parameters for cohesionless and cohesive solid*, Powder Technol. (2015). doi:10.1016/j.powtec.2015.05.051.

[^11]:	A. Janda, J.Y. Ooi, *DEM modeling of cone penetration and unconfined compression in cohesive solids*, Powder Technol. 293 (2016) 60–68. doi:10.1016/j.powtec.2015.05.034.

[^12]:	J.P. Morrissey, J.Y. Ooi, J.F. Chen, K.T. Tano, G. Horrigmoe, *Measurement and prediction of compression and shear behavior of wet iron ore fines*, in: 7th World Congr. Part. Technol., Beijing, China, 2014: p. 8.

