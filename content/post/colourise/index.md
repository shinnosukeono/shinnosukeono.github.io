---
title: "Colourising Old Photos: Shanbally Castle Revisited"

subtitle: Adding a splash of colour to some old photos using AI and deep learning.

# Summary for listings and search engines
summary: Adding a splash of colour to some old photos using AI and deep learning.

# Link this post with a project
projects: []

# Date published
date: "2021-12-31T00:00:00Z"

# Date updated
# lastmod: "2021-12-01T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: true

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Shanbally Castle, circa 1865'
  focal_point: ""
  placement: 2
  preview_only: false

authors:
- admin

tags:
- Tipperary
- Burncourt
- Shanbally Castle
- AI
- Deep Learning

categories:
- AI
- Architecture
- Deep Learning

# gallery captions
gallery_item:
- album: shanbally_plans
  image: Basement_plan.jpg
  caption: Plan of basement floor
- album: shanbally_plans
  image: Groundfloor_plan.jpg
  caption: Plan of ground floor
- album: shanbally_plans
  image: ChamberStorey_plan.jpg
  caption: Plan of chamber floor
- album: shanbally_plans
  image: ChamberStorey_TimberPlan.jpg
  caption: Timber plan for chamber floor
- album: shanbally_plans
  image: Entrance_South_Elevations.jpg
  caption: Elevations of the Entrance front and south (garden) front 
- album: shanbally_plans
  image: PorchSection_WestFront.jpg
  caption: Section through entrance porch, hall and gallery and west elevation
- album: shanbally_plans
  image: Kitchen_NorthElevation.jpg
  caption: North elevation of the kitchen and offices
- album: shanbally
  image: WL_3450.png
  caption: View of Shanbally Castle from front elevation with porte-cochère 
- album: shanbally
  image: WL_3451.png
  caption: View of Shanbally Castle across the southern gardens 
- album: shanbally
  image: WL_3452.png
  caption: End Elevation of Shanbally castle showing towers containing the oval drawing room (right) and dining room (left)
- album: shanbally
  image: WL_5167.png
  caption: View of Shanbally Castle from front elevation with porte-cochère
- album: shanbally
  image: WL_5169.png
  caption: View of Shanbally Castle across the southern gardens. Main Library is visible in centre of facade with single storey conservatory to the right.
- album: shanbally
  image: WL_6909.png
  caption: View of Shanbally Castle across the southern gardens 
- album: shanbally
  image: WL_6910.png
  caption: Approach to Shanbally Castle with porte-cochère visible at left
 



---

{{% callout note %}}
This post was originally published on [Jp's Blog](blog.johnpmorrissey.com) in 2012.
{{% /callout %}}

{{< toc >}}

# Introduction
---

While recently organising some old black & white photos that I had digitised I began to think about whether it would be possible to colourise those photos using some modern deep learning techniques rather than manually colourising in either PhotoShop or GIMP. Manually colourising may be the best way to ensure accuracy (if you know a specific colour in the image) but it can be incredibly slow and tedious taking hours, days or even months, depending on the photo. This didn't sound appealing to me. The promise of automatically (automagically?) coloured in minutes by an AI sounded ...easier.

Here's a great video on the process of colourising images properly:
{{< youtube vubuBrcAwtY >}}

## The Contenders

As it turns out, there's quite a lot of work after getting done in the area in the past few years and a little bit of research threw up some of the main contenders - here's a well curated [list](https://reposhub.com/python/deep-learning/oskar-j-awesome-image-coloring.html) of some of the many options. After some further reading, I narrowed the list down to a few contenders:
 - https://github.com/richzhang/colorization  
 - https://github.com/junyanz/interactive-deep-colorization
 - https://github.com/google-research/google-research/tree/master/coltran
 - https://github.com/jantic/DeOldify


 # Colourised Images

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_3450.png" title="**View of Shanbally Castle from front elevation with porte-cochère**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_3450_Col.png" title="**View of Shanbally Castle from front elevation with porte-cochère - now in colour**" >}}
    </div>
</div>
 

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_3451.png" title="**View of Shanbally Castle across the southern gardens**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_3451_Col.png" title="**View of Shanbally Castle across the southern gardens - now in colour**" >}}
    </div>
</div>


<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_3452.png" title="**End Elevation of Shanbally castle showing towers containing the oval drawing room (right) and dining room (left)**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_3452_Col.png" title="**End Elevation of Shanbally castle showing towers containing the oval drawing room (right) and dining room (left) - now in colour**" >}}
    </div>
</div>


<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_5167.png" title="**View of Shanbally Castle from front elevation with porte-cochère**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_5167_Col.png" title="**View of Shanbally Castle from front elevation with porte-cochère - now in colour**" >}}
    </div>
</div>


<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_5169.png" title="**View of Shanbally Castle across the southern gardens. Main Library is visible in centre of facade with single storey conservatory to the right**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_5169_Col.png" title="**View of Shanbally Castle across the southern gardens - now in colour**" >}}
    </div>
</div>


<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_6909.png" title="**View of Shanbally Castle across the southern gardens**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_6909_Col.png" title="**View of Shanbally Castle across the southern gardens - now in colour**" >}}
    </div>
</div>

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_6910.png" title="**Approach to Shanbally Castle with porte-cochère visible at left**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_6910_Col.png" title="**Approach to Shanbally Castle with porte-cochère visible at left - now in colour**" >}}
    </div>
</div>