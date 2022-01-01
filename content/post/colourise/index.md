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

While recently organising some old black & white photos that I had digitised I began to think about whether it would be possible to colourise those photos using some modern deep learning techniques rather than manually colourising in either PhotoShop or GIMP. 
Manually colourising may be the best way to ensure accuracy (if you know a specific colour in the image) but it can be incredibly slow and tedious taking hours, days or even months, depending on the photo. 
This didn't sound appealing to me. The promise of automatically (automagically?) coloured in minutes by an AI sounded ...easier.

Here's a great video on the process of colourising images properly:
{{< youtube vubuBrcAwtY >}}

## The Contenders

As it turns out, there's quite a lot of work after getting done in the area in the past few years and a little bit of research threw up some of the main contenders - here's a well curated [list](https://reposhub.com/python/deep-learning/oskar-j-awesome-image-coloring.html) of some of the many options. After some further reading, I narrowed the list down to a few contenders:
 - https://github.com/richzhang/colorization  
 - https://github.com/junyanz/interactive-deep-colorization
 - https://github.com/google-research/google-research/tree/master/coltran
 - https://github.com/jantic/DeOldify


 # Colourised Images

 I'm using  set of photos of from a previous post of [lost local landmark](./post/shanbally/) to get an idea of what it might look like if I walked past it today.

## High Resolution Images

The first set of images I tested the AI tool on was the higher quality images of the exterior of the castle shot early in it's lifetime. These photos are relatively good resolution without many defects in the image.

The first photo is not to bad but the mono-tone sky really washes out the image. The grass and shrubbery in the foreground is quite well coloured, but there is some questionable *"moss"* on the walls as they look a little green in places.
<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_3450.png" title="**View of Shanbally Castle from front elevation with porte-cochère**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_3450_Col.png" title="**View of Shanbally Castle from front elevation with porte-cochère - now in colour**" >}}
    </div>
</div>

The AI has done an ok job here, but it has really struggled where the tree is cutting of a small bit of the south-west tower and there is an uncoloured patch. This could be manually touched up, but I've left it as how the AI completed the task to show some of the places it has struggled. 
<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/wl_3451.png" title="**View of Shanbally Castle across the southern gardens**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_3451_Col.png" title="**View of Shanbally Castle across the southern gardens - now in colour**" >}}
    </div>
</div>

I think the AI has done an amazing job this photo, it looks completely natural in the coloured version - no strange bleeding of colours at boundaries or suspect colours, just an idea of how well the castle looked on a slightly cloudy day in south Tipperary!
<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_3452.png" title="**End Elevation of Shanbally castle showing towers containing the oval drawing room (right) and dining room (left)**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_3452_Col.png" title="**End Elevation of Shanbally castle showing towers containing the oval drawing room (right) and dining room (left) - now in colour**" >}}
    </div>
</div>


This is a really good attempt here. It's basically the same photo as the first one, just a slightly shifted location and sky that is not washed out. The tree in the mid right foreground is causing lots of problems as it's not able to define clear edges. The wall behind it is uncoloured and there's a bit of a yellow *"halo"* around the path to the right.
<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_5167.png" title="**View of Shanbally Castle from front elevation with porte-cochère**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_5167_Col.png" title="**View of Shanbally Castle from front elevation with porte-cochère - now in colour**" >}}
    </div>
</div>

This is another really good attempt, with only a small part of the central tower above the ivy not getting picked up fully. I think this is capturing the scene quite well, even with the mono-tone grey sky.
<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_5169.png" title="**View of Shanbally Castle across the southern gardens. Main Library is visible in centre of facade with single storey conservatory to the right**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_5169_Col.png" title="**View of Shanbally Castle across the southern gardens - now in colour**" >}}
    </div>
</div>

Another really good attempt here, and not upset by the tree that is over the photographers positions. The top of the central tower still has the same slight colour variation as the previous photo - maybe it is real? Unfortunately no way to tell.
<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_6909.png" title="**View of Shanbally Castle across the southern gardens**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_6909_Col.png" title="**View of Shanbally Castle across the southern gardens - now in colour**" >}}
    </div>
</div>

Again another image that has been very well done. Only one small washed out path in the front right corner between the two fence poles. My only question/doubt here relates to the colour of the material on the road - the AI has gone green as it seems to think it's chopped grass, but my suspicion is that it's actually a gravel road and that is should be a more natural stone colour.
<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_6910.png" title="**Approach to Shanbally Castle with porte-cochère visible at left**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_6910_Col.png" title="**Approach to Shanbally Castle with porte-cochère visible at left - now in colour**" >}}
    </div>
</div>

## Low Resolution Images
The second batch of photos I'm going to attempt colourising are the internal photos. 
These images are quite poor quality as they are scans of printed photos and not ones longingly created from negatives or originals. 
This means that although the resolution is relatively high, there is a lot of noise in the image, which may affect the colourising process. 
Ideally, these photos should probably be enhanced or restored before colourising but I'm going to skip that step. 
Maybe I'll come back to do it some other time.

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally_demo/Image_009_28122012.jpg" title="**Main library**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_demo_colour/Image_009_28122012_col.png" title="**Main library - now in colour**" >}}
    </div>
</div>

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally_demo/Image_010_28122012.jpg" title="**Inside of drawing room**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_demo_colour/Image_010_28122012_col.png" title="**Inside of drawing room - now in colour**" >}}
    </div>
</div>

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally_demo/Image_007_28122012.jpg" title="**Main groundfloor gallery**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_demo_colour/Image_007_28122012_col.png" title="**Main groundfloor gallery - now in colour**" >}}
    </div>
</div>

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally_demo/Image_005_28122012.jpg" title="**Main staircase from Gallery**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_demo_colour/Image_005_28122012_col.png" title="**Main staircase from Gallery - now in colour**" >}}
    </div>
</div>

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally_demo/Image_006_28122012.jpg" title="**Vaulted ceiling over main staircase**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_demo_colour/Image_006_28122012_col.png" title="**Vaulted ceiling over main staircase - now in colour**" >}}
    </div>
</div>

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally_demo/Image_003_28122012.jpg" title="**Octagonal tea room**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_demo_colour/Image_003_28122012_col.png" title="**Octagonal tea room - now in colour**" >}}
    </div>
</div>