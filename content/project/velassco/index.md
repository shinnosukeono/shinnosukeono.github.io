---
title: "VELaSSCo: Visualization for Extremely Large-scale Scientific Computing"
summary: The Vision of VELaSSCo is to provide new approaches for visual analysis of large-scale simulations for the Exabyte era. 

tags:
- DEM
- FEM
- CFD
- Data Visualisation
- Data Analytics
- Big Data

date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: VELaSSCo
  focal_point: Smart

links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/jp_morr

url_pdf: https://cordis.europa.eu/docs/projects/cnect/9/619439/080/reports/001-VELaSSCoFinalReport1summary.pdf
url_slides: ""
url_video: ""
url_poster: ''
url_project: http://www.cimne.com/projects/velassco/index.html
url_source: ''
url_code: https://github.com/velassco/VELASSCO

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""

# gallery captions
gallery_item:
- album: velassco
  image: embankment.png
  caption: Railway embankment test case
- album: velassco
  image: embankment_density.png
  caption: Coarse-grained bulk density in railway embankment
- album: velassco
  image: EmbankmentSzz.jpg
  caption: Coarse-grained vertical stress in railway embankment
- album: velassco
  image: EmbankmentVelocity_Cuts.jpg
  caption: Coarse-grained bulk density in railway embankment
- album: velassco
  image: fluidised_bed_temporal_spatial.png
  caption: Temporal and spatial averaging of fluidised bed


---

# Introduction
---

One of the major problems experienced by engineers and scientists running high-end real-scale simulation models is the management and exploitation (in terms of visualization) of the outputs of their models. 
Inspecting large dataset distributed over numerous clusters located remotely, is often a significant difficulty to be overcome to ensure that users (both in academia and industry) are able to take the best advantage of current (and future) HPC infrastructures.

The Vision of VELaSSCo is to provide new approaches for visual analysis of large-scale simulations for the Exabyte era. It does this by building on big data tools and architectures for the engineering and scientific community and by adopting new ways of in-situ processing for data analytics and hardware accelerated interactive visualization.

To better manipulate the data from simulations with billions of records it is crucial that the engineering and scientific community adopts big data tools. VELaSSCo will provide a simulation data analysis platform consisting of:

  - A database structure, based on widely used technologies such as Hadoop-HBase, that can organise and store a diverse range of large-scale simulation data sets for collaborative use.
  - An innovative approach, adopting big data best practices, to handle large scale simulation data sets that have to be stored on multiple servers.
  - A framework equipped with advanced in-situ processing tools to analyse the output of parallel simulation solvers.
  - An analysis platform to analyse and visualize large-scale data sets interactively. This builds on leading edge graphics hardware.


## Project Partners
The VELaSSCo consortium has a wide variety of expertise aligned with the objectives of the project. 
Expertise of the partners can be classified mainly in two principal categories: **Institutions specialized in the development and implementation of visualization software**, particularly addressed to facilitate analysis of HPC simulations in engineering and scientific first-class problems (CIMNE, UNEDIN and FRAUNHOFER); and **institutions with experience in Data Analytics**, Big Data, Big Data Handling and Cloud Computing (SINTEF, INRIA, JOTNE and ATOS).

The partnership also counts with a large group of potential end-users of the outcomes of the projects, ranging from large engineering companies, SME's on engineering modelling and software houses, to research organisations doing large scale engineering modelling, linked to the User Panel already described.

List of partners:

 - [Centre Internacional de Metodes Numerics en Enginyeria (CIMNE)](http://www.cimne.com/) 
 - [The University of Edinburgh](www.eng.ed.ac.uk)
 - [SINTEF Institute of Information and Communications Technology](https://www.sintef.no/en/digital/) 
 - [Institut National De Recherche En Informatique Et En Automatique (INRIA)](https://www.inria.fr/en)
 - [Fraunhofer Institute for Computer Graphics Research IGD](https://www.igd.fraunhofer.de/en )
 - [AtoS Spain](https://atos.net/en/about-us?utm_source=/en-us/home/we-are/insights-innovation/research-and-innovation.html&utm_medium=301)
 - [Jotne](https://jotneit.no/)


# Project Gallery
---

{{< gallery album="velassco" >}} 


{{< youtube kG3St1mDlLw >}}

{{< youtube U9LxMexQCBg >}}

{{< youtube sqvzmdp-k-U >}}

{{< youtube ZnUl35qK3No >}}
