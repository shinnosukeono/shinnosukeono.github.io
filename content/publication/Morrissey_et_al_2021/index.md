---
title: "Conceptualisation of an Efficient Particle-Based Simulation of a Twin-Screw Granulator"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- admin
- Kevin J. Hanley
- Jin Y. Ooi

# Author notes (optional)
# author_notes:

date: "2021-12-12T00:00:00Z"
doi: "10.3390/pharmaceutics13122136"

# Schedule page publish date (NOT publication's date).
publishDate: "2021-12-13T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: In *Pharmaceutics , Vol. 13*
publication_short: In *Pharmaceutics*

abstract: |-
  Discrete Element Method (DEM) simulations have the potential to provide particle-scale understanding of twin-screw granulators. This is difficult to obtain experimentally because of the closed, tightly confined geometry. An essential prerequisite for successful DEM modelling of a twin-screw granulator is making the simulations tractable, i.e., reducing the significant computational cost while retaining the key physics. 
  
  Four methods are evaluated in this paper to achieve this goal: (i) develop reduced-scale periodic simulations to reduce the number of particles; (ii) further reduce this number by scaling particle sizes appropriately; (iii) adopt an adhesive, elasto-plastic contact model to capture the effect of the liquid binder rather than fluid coupling; (iv) identify the subset of model parameters that are influential for calibration. 
  
  All DEM simulations considered a GEA ConsiGma&trade; 1 twin-screw granulator with a 60&deg; rearward configuration for kneading elements. Periodic simulations yielded similar results to a full-scale simulation at significantly reduced computational cost. If the level of cohesion in the contact model is calibrated using laboratory testing, valid results can be obtained without fluid coupling. Friction between granules and the internal surfaces of the granulator is a very influential parameter because the response of this system is dominated by interactions with the geometry.

# Summary. An optional shortened abstract.
summary: ""

tags: ["powder agglomeration", "Discrete Element Method", "DEM", "cohesion", "wet granulation", "twin-screw granulation"]

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: https://www.mdpi.com/1999-4923/13/12/2136
url_code: ''
url_dataset: https://datashare.ed.ac.uk/handle/10283/4179
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# add Altmetric and dimensions badges
add_badge: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Agglomerate formation in TSG'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- mmpp

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

{{% callout note %}}
Click the *Cite* button above to demo the feature to enable visitors to import publication metadata into their reference management software.
{{% /callout %}}

{{% callout note %}}
Create your slides in Markdown - click the *Slides* button to check out the example.
{{% /callout %}}

Supplementary notes can be added here, including [code, math, and images](https://wowchemy.com/docs/writing-markdown-latex/).

