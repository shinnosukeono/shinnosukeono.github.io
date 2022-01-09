---
title: Are you using Data Classes?

subtitle: ''

# Summary for listings and search engines
summary: An quick look at why data classes are so useful.

# Link this post with a project
projects: []

# Date published
date: "2021-05-16T18:00:00Z"

# Date updated
# lastmod: "2021-12-01T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: true

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
- Data Analytics
- Data

categories:
- Numerical Methods
- Data Analytics

math: true
---


## Introduction
---

I don't know about you but I have a tendency to store results in a dictionary and pass that around through function when I need to. I usually avoid created classes for storing data as it always seemed a bit of overkill for the job at hand. Here's a rather simple example of what I mean, where i'm gathering all the results of interest into a single return item. I find this easier than having multiple returns from multiple functions.


```python

import numpy as np
from dataclasses import dataclass

def some_complex_function(forces, scale):

    mult = np.pi**scale
    complex_calculated_forces = forces * mult
    
    result = dict()
    result["val_x"] = complex_calculated_forces[:, 0]
    result["val_y"] = complex_calculated_forces[:, 1]
    result["val_z"] = complex_calculated_forces[:, 2]
    result["mult"] = mult
    
    return result


forces = np.random.random([1000,3])

calculated_forces = some_complex_function(forces, 4)

calculated_forces.keys()

```

 This isn't beautiful code, but it it returns a single `dict` with all the related properties together. 
 Much handier if toy need to pass this into several other functions later on in yor workflow.

However, it's not particularly re-usable and not great for modifying in future. Maybe a class would be a better option? But there's so much effort involved in created a class I hear you say. All those `__init__` and `__repr__` methods that need to be defined, you may end up with a many lines of code for defining a very basic class.

## Data Classes
---
And that's why data classes were introduced in **python 3.7**, to remove all that unnecessary boilerplate code required and just let you use the classes quickly.

So here's my rather silly contrived example again, but this ime using a fancy new data class.

```python
import numpy as np
from dataclasses import dataclass

@dataclass
class resultant_force:
    x: np.ndarray
    y: np.ndarray
    z: np.ndarray
    multiplier: np.float64
    
    
def some_complex_function_using_dataclass(forces, scale):
    mult = np.pi**scale
    complex_calculated_forces = forces * mult
    
    return resultant_force(*complex_calculated_forces.T, mult)
    
forces = np.random.random([1000,3])

force_dataclass = some_complex_function_using_dataclass(forces, 4)

```

I can now run `dir(force_dataclass) on my result and see that it's a fully fledged class :  

```python
['__annotations__',
 '__class__',
 '__dataclass_fields__',
 '__dataclass_params__',
 '__delattr__',
 '__dict__',
 '__dir__',
 '__doc__',
 '__eq__',
 '__format__',
 '__ge__',
 '__getattribute__',
 '__gt__',
 '__hash__',
 '__init__',
 '__init_subclass__',
 '__le__',
 '__lt__',
 '__module__',
 '__ne__',
 '__new__',
 '__reduce__',
 '__reduce_ex__',
 '__repr__',
 '__setattr__',
 '__sizeof__',
 '__slotnames__',
 '__str__',
 '__subclasshook__',
 '__weakref__',
 'multiplier',
 'x',
 'y',
 'z']

```

So I can quite easily query `force_dataclass.multiplier` and get `Out[4]: 97.40909103400242`. What's nice about this is now tht it's a data class instead of a dictionary most IDE's will autocomplete the `dataclass` fields for you, which is another bonus.

The other major benefit is now I have a nice reusable data container which I could make a little more generic and use in many places. I can do this because dataclasses also accept default values for fields. So I can change my previous class to something like this:

```python
@dataclass
class resultant_force:
    x: np.ndarray
    y: np.ndarray
    z: np.ndarray
    multiplier: np.float64 = None
    
    
def some_complex_function_using_dataclass(forces, scale):
    mult = np.pi**scale
    complex_calculated_forces = forces * mult
    
    return resultant_force(*complex_calculated_forces.T, mult)

def some_complex_function_using_generic_dataclass(forces):
    complex_calculated_forces = forces * 2
    
    return resultant_force(*complex_calculated_forces.T,)    

force_dataclass = some_complex_function_using_dataclass(forces, 4)

generic_force_dataclass = some_complex_function_using_generic_dataclass(forces)

```

And now from one simple change I have a generic data structure that can be used in multiple places.

And data classes have one more nice trick where you can *"embed"* some calculation into the `class`.

```python
@dataclass
class resultant_force:
    x: np.ndarray
    y: np.ndarray
    z: np.ndarray
    multiplier: np.float64 = None
    
    def __post_init__(self):
        self.custom_var = np.sum(self.x) / 3

def some_complex_function_using_generic_dataclass(forces):
    complex_calculated_forces = forces * 2
    
    return resultant_force(*complex_calculated_forces.T,)    

force_dataclass = some_complex_function_using_dataclass(forces)

```

This now calculates whatever is in the `__post_init__` method when the object is created. Very handy if you always do some calculation with the data in the `class`, just simply embed the calculation within the class and it will be there for you when you need it!

## Conclusion
---

These are just some very simple examples of how useful data classes can be for organising and improving your code. I love how the boilerplate of class creation is gone, and how they can make code more readable and easier to maintain.

There are many other features you would expect of a class and these are also included such as automatic `__repr__` and object comparison. There's also easy conversion to lists and dictionaries. 

I suggest reading this [post](https://realpython.com/python-data-classes/) for a more detailed introduction to dataclasses and to see how they may help you.
