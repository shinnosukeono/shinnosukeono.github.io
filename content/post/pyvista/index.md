---
title: Favourite Tool/Package of 2020

subtitle: ''

# Summary for listings and search engines
summary: An introduction to my favourite tool or package for 2020.

# Link this post with a project
projects: []

# Date published
date: "2020-12-19T00:00:00Z"

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
- python
- Visualisation
- Data Analytics
- Data

categories:
- Numerical Methods
- Data Analytics

math: true
---


## Introduction
---

Working with **Discrete Element Method (DEM)** usually means that you need to visualise your results somehow after the simulation is complete. This is usually the case with some of the open source codes. If you use a commercial code like [EDEM](https://www.altair.com/edem/) or [Rocky](https://rocky.esss.co/), the visualisation aspect is usually taken care for you by the software, but occasionally you may wish to do something that isn't supported. That's life in research...

Anyway, that's where [ParaView](https://www.paraview.org/) usually comes in. It's a hugely powerful open-source data analysis and visualization application. However, it's built on top of the **VTK** library and usually requires writing all your data out in a *ascii* VTK format, which is not always practical.

And that's where my new favourite Python Library comes in ... Hello **PyVista**.


## PyVista
---

[PyVista](https://docs.pyvista.org/) is a powerful and flexible library for plotting 3D figures using python. It's also based on **VTK**, but implements a higher level API that interfaces through [Numpy](https://numpy.org/). PyVista is:
> 3D plotting made simple and built for large/complex data geometries

I don't want to write a huge tutorial here because there are lots of great examples on the [PyVista website](https://docs.pyvista.org/examples/index.html) which should help you get started. I'm just going to include my favourite examples here and then let you go explore as you wish.

### Examples

This is an interactive example of slicing a 3D dataset (a brain!) using a plane widget, but this is super cool and super easy to use.

```python
# sphinx_gallery_thumbnail_number = 2
import pyvista as pv
from pyvista import examples

vol = examples.download_brain()

p = pv.Plotter()
p.add_mesh_clip_plane(vol)
p.show()

```

As a DEM user you might be interested in plotting some spheres (particles) and this is also very easy, see this example for 1M spheres which renders in about 10s on my laptop.

```python
import numpy as np
import pyvista as pv
pv.set_plot_theme('dark')

n = 1_000_000
mesh = pv.PolyData(np.random.random((n, 3))*1000)
mesh["radius"] = np.random.rand(n) * 2

# Low resolution geometry
geom = pv.Sphere(theta_resolution=8, phi_resolution=8)

# Progress bar is a new feature on master branch
glyphed = mesh.glyph(scale="radius", geom=geom, progress_bar=True)


p = pv.Plotter(notebook=False)
p.add_mesh(glyphed, smooth_shading=True) # if you want everything mono coloured then add the following argument: color='yellow'
# if you want it to look really nice, add the smooth shading option smooth_shading=True. 
# This will be slower rendering!

p.show()

```

{{% callout note %}}
Rendering 1M spheres is quite a task, you may wish to test with a smaller value of *n* initially. 

Performance will depend on your machine specification.
{{% /callout %}}