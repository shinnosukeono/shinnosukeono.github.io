---
title: "Transporting, handling and storing behaviour of iron ore fines"

summary: This project attempts to deal with the challenges associated with handling and storage of cohesive solids in the mining industry.


tags:
- DEM
- Data Analytics
- Temperature dependent
- Time dependent
- Coupling
- MBD
- Adhesion
- Cohesion
- EEPA
- EBBM

date: "2013-07-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Fully coupled Jenike Shear Cell (left) and Simple Vertical Stress Only Control (right)
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
- album: post_doc
  image: jenike_cell.png
  caption: Comparison in simulations (force network, geometry positions and particle velocities) of fully coupled (with rotation) MBD simulation of Jenike cell against simplified vertical stress application only
- album: post_doc
  image: jenike_stresses.png
  caption: Comparison in stress fields for fully coupled (with rotation) MBD simulation of Jenike cell against simplified vertical stress application only
- album: post_doc
  image: temporally_scaled_uniaxial.jpg
  caption: Comparison of DEM Consolidation Time against experimental dataset

---

# Introduction
---

This project attempts to deal with the challenges associated with handling and storage of cohesive solids in the mining industry. An adhesive-frictional model has been recently developed for DEM simulation of cohesive particles at the University of Edinburgh. This project will exploit the new method for modelling cohesive particulates for specific problems, such as effect of fines in silo discharge and the effect of time consolidation. 


Fines are produced during transportation, handling and storing of iron pellets. 
The presence of fines can significantly affect the behaviour of iron ore pellets during these processes. In addition, increased volumes of sinter fines are being produced and handled and their behaviour can also be significantly affected.  
Silos and other equipment handling the fines can experience such phenomena as caking, arching and alteration of flow pattern, leading to operational difficulties. 


The behaviour of fines is extremely complex, affected by numerous factors such as particle size, size distribution, stress level (e.g. the maximum vertical stress in a silo), stress state (i.e. the stresses in different directions), stress history, temperature, moisture content, time and chemical bond/fusion. Different combinations of these factors can lead to different behaviours, such as caking with different strength and size, which in turn result in different effects on the solids flow in silos and other handling scenarios in the mining industry.

DEM simulations can also be affected by the prescribed boundary conditions and as such the effect of oversimplification of the degrees of freedom for a Jenike cell are explored in detail, through the use of fully coupled multi-body dynamics for all geometry movements.

# Image Gallery
---

{{< gallery album="post_doc" thumbnailResizeOptions="600x400 Lanczos q90" >}}



# Video Gallery
---

{{< youtube E9fa6P68QDs >}}


{{< youtube SvEnSW8LemE >}}


---