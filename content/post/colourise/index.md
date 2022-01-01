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
- Photo

categories:
- AI
- Architecture
- Deep Learning


---

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
 - https://github.com/richzhang/colorization : This is quite well referenced and the results look quite promising.
 - https://github.com/junyanz/interactive-deep-colorization : This is an interactive tool that allow you to specify the colour of a specific region which can be useful for stopping colour bleeding or to force a specific colour in an area. This is now included in Adobe Photoshop Elements.
 - https://github.com/google-research/google-research/tree/master/coltran : The power of Google research. Should be good, right?
 - https://github.com/jantic/DeOldify : A pretty impressive tool that is now available within [MyHeritage](https://www.myheritage.com/incolor) website. This is the original tool minus any new updates in the MyHeritage version.

There's strengths and weaknesses for each of these options and there is also a dependence on the dataset used for training, both it's size and content. If you use a model trained on pictures containing people nd animals only, it will probably do a relatively poor job colouring landscape images.

There's a really nice [post](https://habr.com/en/company/ruvds/blog/568426/) that makes a comparison between the colour transformer and DeOldify approaches which shows that the transformer can give great results, but more often than not it will do something strange while DeOldify is much more consistent from years of training and tweaking. However, it does show that DeOldify can have a more limited and restrained colour palette because of how it works.

Anyway, after much reading and thinking about what I want to achieve (reliable colourisation of old photos), I've decided to start with DeOldify's notebooks and see how well it performs on my images.

 # Colourised Images

 I'm using  set of photos of from a previous post of a [lost local landmark](../shanbally/) to get an idea of what it might look like if I walked past it today.

## High Resolution Images

The first set of images I tested the AI tool on was the higher quality images of the exterior of the castle shot early in it's lifetime. These photos are relatively good resolution without many defects in the image.

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_3450.png" title="**View of Shanbally Castle from front elevation with porte-cochère**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_3450_Col.png" title="**View of Shanbally Castle from front elevation with porte-cochère - now in colour**" >}}
    </div>
</div>

**Verdict:** The first photo comparison is not to bad but the mono-tone sky really washes out the image. The grass and shrubbery in the foreground is quite well coloured, but there is some questionable *"moss"* on the walls as they look a little green in places.


<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/wl_3451.png" title="**View of Shanbally Castle across the southern gardens**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_3451_Col.png" title="**View of Shanbally Castle across the southern gardens - now in colour**" >}}
    </div>
</div>

**Verdict:** For this image the AI has done an *ok* job, but it has really struggled where the tree is cutting off a small bit of the south-west tower and there is an uncoloured patch on the building because of this. This could be manually touched up, but I've left it as how the AI completed the task to show some of the places it has struggled. 

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_3452.png" title="**End Elevation of Shanbally castle showing towers containing the oval drawing room (right) and dining room (left)**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_3452_Col.png" title="**End Elevation of Shanbally castle showing towers containing the oval drawing room (right) and dining room (left) - now in colour**" >}}
    </div>
</div>

**Verdict:** I think the AI has done an **amazing** job this photo, it looks completely natural in the coloured version - no strange bleeding of colours at boundaries or suspect colours, just an idea of how well the castle looked on a slightly cloudy day in south Tipperary!


<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_5167.png" title="**View of Shanbally Castle from front elevation with porte-cochère**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_5167_Col.png" title="**View of Shanbally Castle from front elevation with porte-cochère - now in colour**" >}}
    </div>
</div>

**Verdict:** This is a good good attempt here. 
It's practically the same photo as the first one, just a slightly shifted location and sky that is not washed out. 
The tree in the mid right foreground is causing lots of problems as it's not able to define clear edges. The wall behind it is uncoloured and there's a bit of a yellow *"halo"* around the path to the right. 
I think it may have painted the gravel green though, but I'm not sure!
The AI has really struggled dealing with trees that are partially obscuring the background building.


<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_5169.png" title="**View of Shanbally Castle across the southern gardens. Main Library is visible in centre of facade with single storey conservatory to the right**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_5169_Col.png" title="**View of Shanbally Castle across the southern gardens - now in colour**" >}}
    </div>
</div>

**Verdict:** This is another really good attempt, with only a small part of the central tower above the ivy not getting picked up fully. I think this is capturing the scene quite well, even with the mono-tone grey sky.

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_6909.png" title="**View of Shanbally Castle across the southern gardens**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_6909_Col.png" title="**View of Shanbally Castle across the southern gardens - now in colour**" >}}
    </div>
</div>

**Verdict:** Another really good attempt here, and not upset by the tree that is over the photographers positions. 
The top of the central tower still has the same slight colour variation as the previous photo - maybe it is real? Unfortunately no way to tell.
I think this may be my favourite.

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally/WL_6910.png" title="**Approach to Shanbally Castle with porte-cochère visible at left**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_colour/WL_6910_Col.png" title="**Approach to Shanbally Castle with porte-cochère visible at left - now in colour**" >}}
    </div>
</div>

**Verdict:** Again another image that has been very well done. 
Only one small washed out path in the front right corner between the two fence poles. 
My only question/doubt here relates to the colour of the material on the road - the AI has gone green as it seems to think it's chopped grass, but my suspicion is that it's actually a gravel road and that is should be a more natural stone colour.


The AI has done a pretty decent job of colourising these photos, with some obvious sections that would require a manual touch-up. 
The colour adds a new perspective to these images and I'm surprised by how much of a difference it makes.


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
        {{< figure src="albums/shanbally_demo_colour/Image_009_28122012.png" title="**Main library - now in colour**" >}}
    </div>
</div>

**Verdict:** This is probably a difficult one for the AI to deal with as there is nothing of obvious colour (grass, sky, etc.) for it to work from, so what you end up with something like a room being lit under a low evening sun with a sort of evening glow. 
I think this is probably related to the *DeOldify* algorithm and training set which tends to being average colours. 
The *Google Transformer* AI would probably give a more impressive result on these interior photos. 
Also, I have no idea on the actual interior decoration and what colours to expect here.

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally_demo/Image_010_28122012.jpg" title="**Inside of drawing room**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_demo_colour/Image_010_28122012.png" title="**Inside of drawing room - now in colour**" >}}
    </div>
</div>

**Verdict:** Same problem as previous - no distinct colours leading to an average orange/brown glow. There is a hint of the greenery coming through the windows though, so some credit due.

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally_demo/Image_007_28122012.jpg" title="**Main groundfloor gallery**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_demo_colour/Image_007_28122012.png" title="**Main groundfloor gallery - now in colour**" >}}
    </div>
</div>

**Verdict:** Same problem as again - no distinct colours leading to an average orange/brown glow.


<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally_demo/Image_005_28122012.jpg" title="**Main staircase from Gallery**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_demo_colour/Image_005_28122012.png" title="**Main staircase from Gallery - now in colour**" >}}
    </div>
</div>

**Verdict:** Same problem as again - no distinct colours leading. I think the natural wood staircase should pop out a bit more from the relatively light coloured wall. Also the exposed red-brick isn't really picked up.

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally_demo/Image_006_28122012.jpg" title="**Vaulted ceiling over main staircase**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_demo_colour/Image_006_28122012.png" title="**Vaulted ceiling over main staircase - now in colour**" >}}
    </div>
</div>

**Verdict:** This may be an unfair test - it's probably a white ceiling so this looks about right with some colour from the window light coming through.

<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally_demo/Image_003_28122012.jpg" title="**Octagonal tea room**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_demo_colour/Image_003_28122012.png" title="**Octagonal tea room - now in colour**" >}}
    </div>
</div>

**Verdict:** An outdoor shot with something contrast. This all looks pretty good, with maybe the exception of the sky in the upper left corner, which appears to be a bit dark given the level of sunshine evident elsewhere. I think the quality of the original photo may be the cause of the problem as there may not be enough information.


<div class="row">
    <div class="column_2">
        {{< figure src="albums/shanbally_demo/Image_002_28122012.jpg" title="**Castle from the distance**" >}} 
    </div>
    <div class="column_2">
        {{< figure src="albums/shanbally_demo_colour/Image_002_28122012.png" title="**Castle from the distance - now in colour**" >}}
    </div>
</div>

**Verdict:** This is by far the best of the this batch of low quality photos. The only blemish is the slightly green tint appearing in the sky. It does look like a glorious late summer's day in Tipperary though. Amazing what  little colour can do.


# Conclusion

Overall, the quality of the colourised images is pretty impressive for an automated process that only took 5-10s per image. 
Some more time was obviously spent finding the best input parameters as this can vary per image, depending on the image quality.

The AI and algorithm worked much better on the the first batch of higher quality images and there were a few really impressive conversions. It struggled a bit with the second set of images which were lower quality with a pixelated appearance due to being scans of printed images. I also think the image content didn't help, with it struggling to add colours to the interior and things all just ending up with an average *'brownish'* wash because it did quite well on the exterior images in this batch.

I've been impressed by what these new tools can do, but they will probably never quite have the accuracy of a lovingly created, historically accurate, manually colourised image. But if you just want a splash of color for a new perspective, then this is great.