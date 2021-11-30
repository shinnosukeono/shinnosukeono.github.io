---
title: A new uniaxial tester for measuring flowability and calibrating DEM models for cohesive particulates
subtitle: ''

# Summary for listings and search engines
summary: 
  Handling of particulate products is a task that is at the core of many industries, from pharmaceuticals to foods to mining. Measuring the flowability of such materials or characterising the properties for a DEM cohesive material model in a simulation is not necessarily a trivial task.

# Link this post with a project
projects: []

# Date published
date: "2019-12-13T00:00:00Z"

# Date updated
lastmod: "2021-12-01T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ""
  placement: 2
  preview_only: false

authors:
- admin

tags:
- DEM
- Calibration
- Uniaxial

categories:
- Numerical Methods
- Calibration
---

## Overview

Handling of particulate products is a task that is at the core of many industries, from pharmaceuticals to foods to mining. However, all share a very similar challenge of keeping their processes flowing reliably, since cohesive particulates (either naturally cohesive or those affected by external factors such as moisture) can trigger difficult material handling situations. Measuring the flowability of such materials or characterising the properties for a DEM cohesive material model in a simulation is not necessarily a trivial task.

The flow function of a cohesive particulates is a material property that is typically measured to indicate the flowability and handleability of a material. In industry this is typically measured with some direct shear device such as a Jenike tester or a dynamic flow tester such as a FT4 Powder Rheometer. Ring shear testers and rotational testers are also frequently used. While each one has its advantages, many are compromised by the high cost, amount of time required for carrying out testing or lack of relevance to specific industrial situations.

Uniaxial testers offer an attractive alternative method for characterising the flowability of powders and sticky granular materials in industrial situations. Uniaxial testers apply a consolidation stress followed by a failure load vertically to a sample. This is appealing for being a mechanically simple device that’s easy to operate and also its physical similarity to the stress path associated with feeding industrial equipment and the unconfined yield strength [^1]. One of the challenges with uniaxial testers is achieving a uniform level of consolidation throughout the height of the sample, as wall friction can mean that the vertical stress in the sample at the bottom is significantly lower than the vertical stress applied at the top surface. To combat this there have been many designs considered over the years to deal this, each with their own strengths [^2] [^3] [^4]. 

The *University of Edinburgh* had previous experience of developing successful uniaxial testers for sticky solids with larger particles [^5]. From this experience the **Edinburgh Powder Tester (EPT)** was developed for measuring the flowability of compressible cohesive powders with a focus on speed, robustness and high repeatability for industrial use [^1]. The key differences between the **Edinburgh Powder Tester** and some previous devices lie in the attention to mechanical details for both the consolidation and failure load application and the strategic intent [^1], which means the EPT offers repeatable results in the range of 5-10% relative standard deviation (RSD) for a vast range of materials [^6] [^7].

Recently, Freeman Technology; which has many years of experience of both powder testing and development of testing apparatus, including extensive knowledge of shear cells; entered into a highly productive collaboration with the *University of Edinburgh*, *DuPont* and *The Chemours Company* to develop a uniaxial powder tester for the commercial market that incorporates the key design elements of the EPT. The result of this collaboration is **‘The Uniaxial Powder Tester from Freeman Technology’** which is a standalone uniaxial shear tester for powders, capable of testing a stress range of up to 100 kPa. 

The simplicity and flexibility of uniaxial testers, coupled with a high level of repeatability, make uniaxial testers ideal tools for calibrating a DEM model for cohesive solids. The **Freeman UPT**, which is a semi-automated uniaxial tester, provides rapid measurements of key bulk mechanical properties of powders, including the stress–strain and the stress–density response during confined compression, the stress–strain response during unconfined compression including the peak unconfined strength and the increased cohesive (caking) strength developed over time in consolidation, all of which can be utilised for calibrating your DEM simulation of a cohesive solid to provide a realistic prediction. 

{{< figure src="upt.jpg" title="**Freeman Advanced UPT**" >}}

{{< figure src="upt_consolidation_station.jpg" title="**Offline consolidation station for time consolidation and temperature & humidity testing**" >}}

## References
[^1]:	T.A. Bell, E.J. Catalano, Z. Zhong, J.Y. Ooi, J.M. Rotter, *Evaluation of the Edinburgh powder tester*, in: PARTEC 2007 - Congr. Part. Technol., Nürnberg, 2007: pp. 1–6. http://scholar.google.com/scholar?hl=en&btnG=Search&q=intitle:Evaluation+of+the+Edinburgh+Powder+Tester#0 (accessed October 5, 2019).

[^2]:	L.P. Maltby, G.G. Enstad, *Uniaxial Tester for Quality Control and Flow Property Characterization of Powders.*, Powder Handl. Process. 13 (1993) 135–139.

[^3]:	M. Röck, M. Ostendorf, J. Schwedes, *Development of an Uniaxial Caking Tester*, Chem. Eng. Technol. 29 (2006) 679–685. doi:10.1002/ceat.200600068.

[^4]:	R.E. Freeman, X. Fu, *The Development of a Compact Uniaxial Tester*, in: Part. Syst. Anal. 2011, Edinburgh, UK, 2011: pp. 1–6.

[^5]:	Z. Zhong, J.Y. Ooi, J.M. Rotter, *Predicting the handlability of a coal blend from measurements on the source coals*, Fuel. 84 (2005) 2267–2274. doi:10.1016/j.fuel.2005.05.023.

[^6]:	S.C. Thakur, H. Ahmadian, J. Sun, J.Y. Ooi, *An experimental and numerical study of packing, compression, and caking behaviour of detergent powders*, Particuology. 12 (2014) 2–12. doi:10.1016/j.partic.2013.06.009.

[^7]:	J.P. Morrissey, *Discrete Element Modelling of Iron Ore Fines to Include the Effects of Moisture and Fines*, University of Edinburgh, 2013. https://www.era.lib.ed.ac.uk/handle/1842/8270.




## License

Copyright 2019-present [J.P. Morrissey](https://johnpmorrissey.com).
Released under the [MIT](https://github.com/wowchemy/wowchemy-hugo-modules/blob/master/LICENSE.md) license.
