---
title: "Discrete Element Modelling of Iron Ore Fines to Include the Effects of Moisture and Fines"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- admin

# Author notes (optional)
author_notes:

date: "2013-07-01T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-08-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["7"]

# Publication name and optional abbreviated publication name.
publication: In *Wowchemy Conference*
publication_short: In *ICW*

abstract: Across industry the majority of raw materials handled are particulate in nature, ranging
in size and properties from aggregates to powders. The stress regimes experienced
by the granular solids vary and the exhibited bulk behaviours can be complex and
unexpected. The prevalence of granular solids makes them an area of interest for
industry and researchers alike as many challenges still remain, such as dealing with
complex cohesive behaviour in materials, which often gives rise to handling difﬁculties.

Storage and transportation are an important part of the process chain for industries
where particulate solids are commonplace. Failure to properly account for the cohesive
nature of a particulate solid can be costly as it can easily lead to blockages in a silo
such as ratholing or arching near the outlet during discharge. The cohesive strength of
a bulk material depends on the consolidation stress it has experienced. As a result, the
stress history in the material leading up to a handling scenario needs to be considered
when evaluating its handling behaviour.

The Discrete Element Method (DEM) has been extensively used to simulate the be-
haviour of granular materials, however the majority of the focus has been on non-
cohesive systems. For cohesive solids, it is crucial that the stress history dependent
behaviour is adequately captured. Many of the contact models commonly used in DEM
simulations to simulate cohesive granular materials such as the JKR model or liquid
bridge models are elastic in nature and may not capture the stress history dependent
behaviour observed in cohesive particulate solids.

A comprehensive study on the effect of cohesion arising from the addition of moisture
on the behaviour of two types of LKAB iron ore ﬁnes (KPBO and KPRS) has been car-
ried out. The addition of moisture to the sample has been found to have a signiﬁcant
effect on both kinds of ﬁnes. KPRS ﬁnes were found to have a much higher uncon-
ﬁned strength and ﬂow function at higher moisture contents, and also show a greater
increase in cohesion with the addition of moisture, while at moisture contents of less
than 2% the KPBO ﬁnes demonstrate higher unconﬁned yield strength. The KPBO ﬁnes
were also found to achieve a signiﬁcantly looser initial packing at much lower moisture
content when compared to the KPRS ﬁnes. The lateral pressure ratio has also been
evaluated.

In this study a mesoscopic adhesive contact model that accounts for contact plasticity
and stress history dependency in the bulk solid, the Edinburgh Elasto-Plastic Adhesion
(EEPA) mode, has been presented and mathematically veriﬁed. A parametric study of
the DEM contact model parameters was conducted to gain a deeper understating of the
effect of input parameters on the simulated cohesive bulk behaviour.

The EEPA contact model has been used to predict an experimental ﬂow function of
KPRS iron ore ﬁnes. The contact model has demonstrated the ability to capture the
stress history dependent behaviour that exists in cohesive granular solids. The DEM
simulations provide a very close match to the experimental ﬂow functions, with the
predicted unconﬁned strengths found to be within the standard deviations of the exper-
imental results. Investigations into the failure mode predicted by the DEM simulations
show that the samples are failing from the development of shear planes similar to those
observed experimentally.

The effect of increasing levels of adhesion has been explored for a ﬂat bottomed silo
where the level of adhesion has been varied. The DEM simulations were found to
capture the major phenomena occurring in silo discharge including the various ﬂow
zones associated with a ﬂat bottomed silo. Funnel ﬂow, the effective transition and
mass ﬂow which are associated with a mixed ﬂow pattern were observed in the model
silo. The location of the effective transition height was identiﬁed:: above this was mass
ﬂow. The velocity determined from the discharge rate was found to be in excellent
agreement with the velocity proﬁles found in the zones of mass ﬂow. A high velocity
core ﬂow zone was observed above the outlet where velocities were greater than 1.25
times the mass ﬂow velocity, VMF.

The level of adhesion in the silo was found to affect the discharge rate - a reduced
ﬂow rate was found until the eventual blockage of the silo at a high level of adhesion
was found. As the level of adhesion increased the probability of arching also increased,
and the formation of intermittent arching behaviour was noted in the cases with higher
levels of adhesion in the system. The development of both temporary and permanent
cohesive arches over the silo outlet were also observed with stopped ﬂow from the silo.

# Summary. An optional shortened abstract.
summary: ""

tags: ["DEM", "Cohesion", "Silo", "Contact model", "Iron ore", "Granular solid", "fines"]

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: https://era.ed.ac.uk/handle/1842/8270?show=full
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- example

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
