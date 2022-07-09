---
title: "Modelling Particle Breakage Using a Bonded Particle Model"

event: "10th International Conference on Conveying and Handling of Particulate Solids"
event_url: https://www.chops2022.it

location: Grand Hotel Salerno
address:
  street: "Lungomare Clemente Tafuri, 1"
  city: Salerno
  region: Campania
  postcode: "84127"
  country: Italy

summary: "**Oral Presentation** at 10th International Conference on Conveying and Handling of Particulate Solids"

abstract: |-
  Particle size reduction, either intended or through damage, is a process that is common across a wide range of industries. Whether intended or not, the effect of this breakage can be significant and predicting the breakage process in simulations can be a challenge.
  The Discrete Element Method (DEM) has seen a significant increase in usage in recent years due to advance in both the underlying hardware being more capable and through advances in the modelling techniques. However, despite these advances the inclusion of breakage in DEM is still in its infancy due to the significant computational cost and simplicity of proposed methods. Several techniques have been proposed such as the Bonded Particle Model (BPM), Particle Replacement Method (PRM) and Discrete Grain Method (DGM).

  The Particle Replacement Method (PRM) instantly replaces a particle with a predefined size distribution of child particles once the failure criteria are met for that particle. This is typically a single maximum compressive force, but more complex failure criteria can be implemented. This method suffers from and inability to incorporate natural breakage patterns (chipping, splitting, etc.) and does not account for weakening from repeated loading events. A BPM approximates the material as a bonded DEM particle fabric at a suitably chosen particle length scale which gives a greater degree of freedom in simulating smaller and irregular-shaped fragments. This method does not impose any predetermined limitations such as failure planes or crack initiation points and allows the model to be used to study the complex phenomena that arise in breakage. 

  This study investigates the effectiveness of the BPM at simulating particle breakage and predicting the breakage size distributions. A rigorous Beam Bond Model is utilised to form the bonded fabric. The study demonstrates that the BPM model is capable of capturing breakage phenomena under both static and dynamic loading conditions and can be used to study damage due to varying levels of impact velocity and cumulative damage from repeated loadings. By tracking the development of bond breakage, the evolution of crack propagation through the material can be visualized.
       


# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: "2022-07-09T12:00:00Z"
date_end: "2022-07-09T12:20:00Z"
all_day: false

# Schedule page publish date (NOT talk date).
publishDate: "2022-07-01T00:00:00Z"

authors:
 - admin
 - Xizhong Chen
 - Lige Wang
 - Jin Y. Ooi

tags: ["DEM", "breakage", "BPM", "Bond Model", "Timoshenko"]

# Is this a featured talk? (true/false)
featured: true

image:
  caption: 'Image credit: [**CHoPS**](https://www.chops2022.it/)'
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
slides: ""

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects:
- []

---

{{% callout note %}}
Click on the **Slides** button above to view the built-in slides feature.
{{% /callout %}}

Slides can be added in a few ways:

- **Create** slides using Wowchemy's [*Slides*](https://wowchemy.com/docs/managing-content/#create-slides) feature and link using `slides` parameter in the front matter of the talk file
- **Upload** an existing slide deck to `static/` and link using `url_slides` parameter in the front matter of the talk file
- **Embed** your slides (e.g. Google Slides) or presentation video on this page using [shortcodes](https://wowchemy.com/docs/writing-markdown-latex/).

Further event details, including [page elements](https://wowchemy.com/docs/writing-markdown-latex/) such as image galleries, can be added to the body of this page.
