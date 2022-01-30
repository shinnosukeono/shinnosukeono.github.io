---
title: New Year, New Site

subtitle: ''

# Summary for listings and search engines
summary: A quick intorduction to my new website layout.

# Link this post with a project
projects: []

# Date published
date: "2022-01-03T18:00:00Z"

# Date updated
# lastmod: "2021-12-01T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: ''
  focal_point: ""
  placement: 2
  preview_only: false

authors:
- admin

tags:
- web
- blog
- wowchemy

categories:


math: true
---


## Introduction
---

After many years of neglect and sitting on a default `404 error` page for several years after transferring domain hosts, I've finally gotten around to fixing my website. 
When I originally created the site many years ago, the purpose was to learn something about `html` and `css` by taking on a project. 
It took me a while, and I was quite proud of the final output. It wasn't perfect, but it had a fancy *'slider carousel'* and some nice css filters in the gallery.
However, after creating it, I quickly realised that I didn't have a whole lot to add to add and i found creating new posts for the blog a struggle. 
I wrote a few good posts that got some traction, but much of it was more personal in nature and possibly not of much interest to other people.
The personal domain for email became the main draw and when I swapped providers a few years ago, the website didn't get transferred.

{{ < figure src="old_site.png" title="**Homepage of Original Site**" > }}

This was probably a mistake - some of the posts were actually of interest and had lots of comments. 
I had been using wordpress to handle the blog but I never transferred out all the comments before just putting thins on ice. So to anyone reading who may be about to do something similar - remember to back up or export things like comments as well as the raw data of the site.
There is one saving grace [The Wayback Machine](https://web.archive.org/) which does a great job of keeping an archive of the web. 
Due to this fantastic resource I can still see snapshots of my website and the useful comments that were left. 
Maybe there's a way to recover comments from this archive and re-import them to the current site? 
If you know how to do this, let me know in the comments below!

## Version 2.0

So after years of manual `html` and `css` tinkering, I wanted something that was just as flexible but allowed easy content creation and the option to tinker and customise as required. I didn't want to be tied to some CMS backend that limits what you can do. So I started doing some research!

So it turns out what I was looking for is a **Static Site Generator**, which basically takes some type of template file or files in one format and converts into lots of html and css files that can be deployed on your server. This has an advantage over dynamics sites as they should be faster to load and more secure.

And there are lots of these SSG's out there and in various languages. `Jekyll`, `Gatsby` and `Hugo` are just a few of the most common.
I was drawn to `Hugo` by the fact that all the templating is written in markdown format, but also the claims of speed. Apparently, it's very fast!



