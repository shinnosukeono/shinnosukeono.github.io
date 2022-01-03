---
title: Favourite Tool/Package of 2019

subtitle: ''

# Summary for listings and search engines
summary: An introduction to my favourite tool or package for 2019.

# Link this post with a project
projects: []

# Date published
date: "2019-12-28T00:00:00Z"

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
- Performance

categories:
- Numerical Methods
- Data Analytics

math: true
---


## Introduction
---

When you are dealing with relatively large datasets on a regular basis, the computation time required to process your data becomes an issue. We always want more speed. If you can cut run time from 30 minutes to 10 minutes, then that is a huge gain. 

In python there's the usual performance gain coming from removing native loops and vectorising with `NumPy`, using `pandas` and then there's even the new kid on the block, `Numba` (not actually that new now, but still newer!) which requires a bit more effort rewriting some code into functions that can be Just-In-Time (JIT) compiled. However, not everything can be compiled.

But there are also some other very simple performance tweaks that can be made and that can have a significant effect on runtime. That's where **Bottleneck** comes in.


## Bottleneck
---

[Bottleneck](https://bottleneck.readthedocs.io/en/latest/index.html) is a:
>  collection of fast, NaN-aware NumPy array functions written in C.

Bottleneck is basically a drop-in replacement for some popular NumPy functions such as sum, mean, min, max, etc. Please refer to the [documentation](https://bottleneck.readthedocs.io/en/latest/reference.html) for the full list.

Here's a very simple example of bottleneck at work:
```python
import numpy as np
import bottleneck as bn

a = np.array([1, 2, np.nan, 4, 5])

np.nanmean(a)
bn.nanmean(a)

```

Bottleneck also provides some really useful rolling window functions that work along a single axis. Super easy and useful for calculating moving averages. The output will be the same shape as the input, but with the first few values smaller than the windo size returned as `nan`.

```python
b = np.random.random(100)

rolling_avg_3 = bn.move_mean(b, window=3)
rolling_avg_10 = bn.move_mean(b, window=10)

```

### Performance

Bottleneck comes with a built in benchmarking suite that you can run on your machine to see what your performance will be like. Simply run `bn.bench()`

Here's the results output from my machine:

```python
Bottleneck performance benchmark
    Bottleneck 1.3.2; Numpy 1.20.3
    Speed is NumPy time divided by Bottleneck time
    NaN means approx one-fifth NaNs; float64 used

              no NaN     no NaN      NaN       no NaN      NaN    
               (100,)  (1000,1000)(1000,1000)(1000,1000)(1000,1000)
               axis=0     axis=0     axis=0     axis=1     axis=1  
nansum         37.4        1.8        2.3        3.3        3.4
nanmean        99.5        2.2        3.0        4.3        4.2
nanstd        167.6        2.3        3.4        5.1        3.4
nanvar        165.2        2.2        2.5        4.1        2.9
nanmin         25.5        0.6        1.8        1.0        3.3
nanmax         24.2        0.8        1.9        0.8        3.1
median        113.3        1.3        3.8        1.1        3.8
nanmedian     113.3        6.5        7.1        5.5        5.9
ss             13.0        1.9        2.2        3.6        3.5
nanargmin      58.4        3.4        4.6        2.5        5.6
nanargmax      59.8        3.4        5.3        2.4        5.7
anynan          7.8        0.5       37.5        0.3       26.0
allnan         10.2      158.2      118.7       82.9       89.2
rankdata       23.5        1.3        1.3        2.6        2.6
nanrankdata    23.6        1.5        1.4        2.8        2.8
partition       4.6        1.0        1.3        0.9        1.3
argpartition    9.1        1.2        1.4        1.1        1.5
replace         7.6        0.9        1.0        0.9        0.9
push         1091.2        4.5        5.5        9.4        8.9
move_sum     2973.9       52.0      104.7      201.4      253.1
move_mean    7566.5       60.3      112.3      286.9      286.2
move_std     8564.2       73.8      146.0      190.7      302.7
move_var    11758.3       81.3      172.4      253.6      392.3
move_min     1361.0       15.6       31.8       22.8       53.8
move_max     1463.0       15.7       33.1       26.9       52.0
move_argmin  3319.4       67.4      102.3       77.0      128.4
move_argmax  3476.7       61.9       75.8       71.2      119.1
move_median  1704.8      137.2      160.7      171.2      185.9
move_rank     911.9        1.5        1.9        1.9        2.4

```

In the vast majority of cases bottleneck provides close to a 2x increase in performance of some of the most frequently used `NumPy` functions which can really help reduce that runtime and increase productivity. It's definitely noticeable for me in my work.

{{% callout note %}}
Only arrays with data type (`dtype`) `int32`, `int64`, `float32`, and `float64` are accelerated. All other `dtypes` result in calls to slower, unaccelerated functions. 
{{% /callout %}}