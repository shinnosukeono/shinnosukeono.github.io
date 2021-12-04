---
title: "Investigating the effects of Cohesion and Screw Configuration in a Twin-Screw Granulator using the Discrete Element Method"

event: "8th International Conference on Discrete Element Methods: DEM8"
event_url: https://mercurylab.co.uk/dem8/

location: Waaier building, University of Twente
address:
  street: Drienerlolaan 5
  city: Enschede
  region: County Durham
  postcode: '7522 NB'
  country: The Netherlands

summary: "**Oral Presentation** at 8th International Conference on Discrete Element Methods: DEM8"

abstract: |-
  Wet granulation is a process used to create larger stable agglomerates (granules) from fine powders. This has many desirable outcomes such as improving flowability, compactibility, and homogeneity. Granulation is commonly employed in the food, pharmaceutical, detergent, and fertilizer industries, but despite its wide adoption it is often problematic in operation, with high recycle ratios in continuous processes and high rejection rates in batch processes.
  
  Although tremendous efforts have been made to gain scientific insight into the granulating process, a fundamental understanding of wet granulation is still lacking due to the complexity of the mechanisms involved. With twin screw granulation becoming a popularly employed method of wet granulation, an in-depth understanding of particle enlargement in the granulating process is necessary in order to improve the quality of the final product without the need for large-scale Design-of-Experiment studies.

  Despite the extensive experimental research carried out for twin screw granulators in recent years, there has been little computational work carried out. This paper employs the Discrete Element Method (DEM) to study a 25 mm diameter, GEA ConsiGma™ 1 twin screw granulator with a series of typical configurations for the kneading elements considered. The DEM simulations were conducted using the commercial code EDEM with a DEM contact model developed for cohesive solids. The contact model is based on an elasto-plastic contact with adhesion and uses hysteretic loading and unloading paths to model the elastic-plastic contact deformation. In these simulations, the adhesion is used to capture the effect of the binder liquid without the complication of modelling the liquid directly. The adhesion parameter is a function of the plastic contact overlap. The model has previously been shown to be able to predict the stress-history-dependent behaviour depicted by a flow function of the cohesive bulk material.
  
  In this study, two important factors are investigated. Firstly simulations were performed to compare the behaviour of a cohesion-less material with a cohesive material to understand the effect of cohesion on the key results such as the residence time distribution, mass hold-up and the stress regimes on the kneading and conveying elements of a ConsiGma granulator. Secondly the effect of the changing screw configuration on the residence time distribution, local solid fraction and stresses experienced at different elements in the twin-screw granulator is assessed. The results shows the influence of these key factors which helps to determine an optimal configuration for the operation.

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: "2019-07-25T09:50:00Z"
date_end: "2019-07-25T10:10:00Z"
all_day: false

# Schedule page publish date (NOT talk date).
publishDate: "2019-07-15T00:00:00Z"

authors:
 - admin
 - Kevin J. Hanley
 - Jin Y. Ooi

tags: ["MMPP", "DEM", "Powder", "Cohesion", "Wet Granulation", "Twin screw", "Granulation"]

# Is this a featured talk? (true/false)
featured: true

image:
  caption: 'Image credit: [**MercuryLab**](https://www.mercurylab.org)'
  focal_point: Right

links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/jp_morr
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Markdown Slides (optional).
#   Associate this talk with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects:
- mmpp

---

{{% callout note %}}
Click on the **Slides** button above to view the built-in slides feature.
{{% /callout %}}

Slides can be added in a few ways:

- **Create** slides using Wowchemy's [*Slides*](https://wowchemy.com/docs/managing-content/#create-slides) feature and link using `slides` parameter in the front matter of the talk file
- **Upload** an existing slide deck to `static/` and link using `url_slides` parameter in the front matter of the talk file
- **Embed** your slides (e.g. Google Slides) or presentation video on this page using [shortcodes](https://wowchemy.com/docs/writing-markdown-latex/).

Further event details, including [page elements](https://wowchemy.com/docs/writing-markdown-latex/) such as image galleries, can be added to the body of this page.
