---
title: Have you met Julia Yet?
summary: An introduction to the *new kid on the block.

date: 2022-02-13T08:00:00.000Z

draft: true
featured: true

authors:
  - admin

image:
  filename: featured
  focal_point: Smart
  preview_only: false

---
There are many different programming languages out there such as `c`, `c++` and `Java`. These are probably considered more general computing languages.
Then there are some others that are higher level languages such as python. There are languages that have developed communities like `R` for data science. 
For years scientific computing was dominated by `Fortran` and `MATLAB`. There are many more examples but what they show is that there is rarely a language that does everything well.

For example, `python` is easy to learn and can do almost anything, but the trade of here is that it is an interpreted language and this makes it slow in comparison to `Java` and `C` which are compiled. 
However, it's ease of use has made it a star in recent years it the recent explosion in data science and AI has seen python's popularity soar.

If you have come from a scientific or academic background, then you will probably have spent many years using MATLAB as it was (and still is) a staple of many science and engineering undergraduate courses. 
And once you learn something you tend to keep using it because of familiarity: the devil you know is better than one don't!

I fall into this last category, I learned off MATLAB as an undergraduate but couldn't understand why we were being though something like this - who would ever need it. Roll on a few years into my Ph.D. and the first thing i did most days after switching on my computer was to open MATLAB in preparation for the days work. I enjoyed using MATLAB as it made my life easier for reading big data files and doing all my calculations. I couldn't have managed without it really. But I always had a desire to find something that didn't have a big price tag attached. 
Something similar and familiar feeling but free. 

I'd heard of this language called python that was like a cross between MATLAB and Perl and thought *"This sounds good"*, but I was nearing the end of my Ph.D. and the looming deadline meant I didn't have time to explore. 
Around the same time I also came across an [announcement](https://julialang.org/blog/2012/02/why-we-created-julia/) of a new language that sounded like my ideal language. Like MATLAB to use but as fast as `C`. Perfect. 
But it was new, and still under development. And my deadlines meant I soon forgot about it. Eventually I moved on to python and have been well served by it for many years now.

But I still long for more speed at times. Particularly as my data sets grow with passing time (much like my waistline really).



## Meet Julia

Julia is still young. It's only been about 10 years since that early announcement that sounded so intriguing to me. 
I must admit that I forgot about it for many years as python did such a good job of filling all the holes. 

Recently I picked up an old computer and logged in looking for some old files and same this icon on the desktop for `Julia`. It was time to look it up and see how it was doing. Had they fulfilled their initial greedy ambitions? Was it even still active.

As it turns out, `Julia` is alive and well, possibly even thriving as more and more people  become aware of it. I don't want to write a tutorial on the use of Julia as there are already plenty of those. 
What I would like to do is just show a simple use case that highlights the power of `Julia`.

##  Use Case: Vector Normalisation
Vector normalisation is possibly something that you would be doing frequently in scientific computing or some data processing. 
The most commonly encountered **vector norm** (often simply called *"the norm"* of a vector, or sometimes the magnitude of a vector)[1] is the **L2-norm**, given by 

$ \left | x \right |_{2} = \left | x \right | = \sqrt({x_{1}}^{2} + {x_{2}}^{2} + ... + {x_{n}}^{2}) $


This is a relatively simple calculation but can have a significant impact on performance if you happen to be calculating this for a large number of vectors, partly because of the repeated use of a square root.

### Python Implementation

It's quite trivial to implement such a function in Native `python` but the numerical computing library `NumPy` provides a ready made solution for this[2] in the *Linear Algebra* submodule and also provides the flexibility to calculate various other vector norms.

But if doing things in `python` quickly is something you want to do, you may also be interested in the `Numba` package and I'll give a quick example why.

Here's the implementation of both the native and `Numba` functions for calculating the L2-norm. The interesting thing here is probably how little needs to be done to *'jit'* a function with `Numba` and unlock huge performance gains. In this case, just once change is required - the addition of `@njit()` before the function. Super easy!!

````python
import numpy as np
import math

from numba import njit

#%% Test functions - L2 Norm
# Native Python Implementation  

def native_norm(vects):
    norms = []
    for vec in vects:
        norms.append(math.sqrt(vec[0]**2 + vec[1]**2 + vec[2]**2))
        
    return norms

# Numba Implementation
@njit()
def numba_norm(vects):
    norms = []
    for vec in vects:
        norms.append(math.sqrt(vec[0]**2 + vec[1]**2 + vec[2]**2))
        
    return norms

````

As many operations are size dependent, I'm going to use the `perfplots` package to helpfully run a benchmark suite os sizes, from a single element to a very large array of 3-component vectors. 


````python
out = perfplot.bench(
    setup=lambda n: np.random.random([n,3]),  # or setup random nx3 array
    kernels=[
        lambda a: native_norm(a),
        lambda a: np.linalg.norm(a, axis=1),
        lambda a: numba_norm(a),
    ],
    labels=["Native", "NumPy", "Numba"],
    n_range=[2**k for k in range(25)],
    xlabel="Number of vectors [Nr.]",
    title="L2-norm Performance"

)

out.show(
    time_unit="us",  # set to one of ("auto", "s", "ms", "us", or "ns") to force plot units
)
````
{{< figure src="perf.png" title="**Performance of various computation methods for L2-norm calculation**" >}}


This automates the whole process and creates a nice plot of the relative performance of the supplied function which you can see in the figure below. Some interesting takeaways from the te results are:
  1. The native python implementation is the slowest (Not Surprising)
  2. Numba is a powerful just-in-time compiler than can make your functions many times quicker. The *'jitted'* function is somewhere between 1 nd 2 orders of magnitude quicker than the native `python` code. 50-100x faster for one line of code more!
  3. As the array size increase, the `Numba` and `NumPy` solutions converge to the same results suggesting th code is being compiled to the same machine code. `NumPy` is slower for the smaller array sizes due to the overhead related to the `NumPy` function such as various implementation options and error checking. This overhead is large for the small array sizes but disappears for arrays above about several thousand rows in this. This is worth bearing in mind if you will only be working on small datasets.

Although, I'm using a specific package for my benchmarking, it's really just automating the process of using `timeit`. 
You will get very similar results running the following code for each size of array.

````python
vects = np.random.random([100,3])

%timeit native_norms = native_norm(vects)
183 µs ± 1.76 µs per loop (mean ± std. dev. of 7 runs, 10000 loops each)

%timeit numpy_norms = np.linalg.norm(vects, axis=1)
13.6 µs ± 110 ns per loop (mean ± std. dev. of 7 runs, 100000 loops each)

%timeit numba_norms = numba_norm(vects)
2.84 µs ± 53.1 ns per loop (mean ± std. dev. of 7 runs, 100000 loops each)
````

### Julia Implementation
Using `Julia` is a bit like writing code for `python` or `MATLAB` and and can be executed from the Julia REPL or using scripts. 
`Julia` is in some sense acting a bit like `Numba` in that is is compiling all the code before execution to benefit from the performance gained from compiled code.  

While I'm not yet aware of any `perfplot` equivalent for Julia just yet, it is relatively easy to measure the performance of any functions using the `BenchmarkTools` package. 
I'm also going to use the `LinearAlgebra` and `LoopVectorization` packages to explore other options.


I've written the equivalent Julia function to my native python function from earlier but I've written this in a vectorised manner as this is how I would write a similar function using `Numpy`. 
Years of python exposure has *"loops are bad"* seared in my brain. 

````julia
using BenchmarkTools
using LinearAlgebra
using LoopVectorization

vec_1 = rand(50000,3)

function normalize_by_row(arr)
   sqrt.(sum(arr.^2, dims=2))
end

@btime nrm = normalize_by_row($vec_1);

````

`@btime` provides a similar output to `timeit`, however, it also includes the amount of memory used and number of memory allocations in the function. Useful information for improving any function. 
A more 'full-fat' option of @benchmark can also be used to get some additional information.

````julia
julia> @btime nrm = normalize_by_row($vec_1);
582.561 μs (10 allocations: 1.91 MiB)


julia> @benchmark nrm = normalize_by_row($vec_1)
BenchmarkTools.Trial: 6431 samples with 1 evaluation.
 Range (min … max):  595.614 μs …   2.605 ms  ┊ GC (min … max): 0.00% … 40.86%
 Time  (median):     677.413 μs               ┊ GC (median):    0.00%
 Time  (mean ± σ):   762.290 μs ± 234.618 μs  ┊ GC (mean ± σ):  4.58% ±  9.81%

  ▃▅▆█▆▅▅▄▄▃▃▃▂▂▁▂▂▂▁▁▂▂                                        ▂
  ████████████████████████▇▇▇▆▅▆▆▆▅▃▄▅▅▃▃▁▃▃▃▄▆██▇▆▆▅▆▆▆▇██▇▆▆▅ █
  596 μs        Histogram: log(frequency) by time        1.8 ms <

 Memory estimate: 1.91 MiB, allocs estimate: 10.


````

From this output we can see that our `Julia` function competes this operation on 50,000 3-component vectors.
We can also see that our function is using about 2MB of memory to carry out this process.

So how did our python code perform for the same size array? Here's the comparison:

````python
%timeit native_norms = native_norm(vects)
85.6 ms ± 1.67 ms per loop (mean ± std. dev. of 7 runs, 10 loops each)

%timeit numpy_norms = np.linalg.norm(vects, axis=1)
1.2 ms ± 7.37 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)

%timeit numba_norms = numba_norm(vects)
1.48 ms ± 18.2 µs per loop (mean ± std. dev. of 7 runs, 1000 loops each)
````

Well that's interesting - the **quickest python** implementation (`Numpy`) is about **twice as slow** as this `Julia` implementation. 
I'm already beginning to see a case for switching to using `Julia`...

But what about my initial code? Can it be improved? What about all those memory allocations - do they make things slow? 
Let's have a look at a few more possible options and see if there is a bit more performance to be gained.

Here's the first attempt.
````julia
 function normalize_by_row_v2(arr)
    norms = Vector{Float64}(undef, size(arr)[1])
    temp = arr.^2
    for i in axes(arr,1)
       @views norms[i] = sqrt(sum(temp[i,:]))
    end
    
    return norms
 end

julia> @btime nrm = normalize_by_row_v2($vec_1);
  472.435 μs (4 allocations: 1.53 MiB)

````

This implementation looks quite different from the first attempt which was a simple broadcasted one-line solution. 
This one has a **loop**! 
It's also using a temporary array for storage and the views function to reduce copying to memory.
Interestingly, even though this is using a for loop, it's still quicker than the initial implementation and has reduced memory usage and the number of memory allocations. 

Here's another attempt at the one-liner and a subtle change does improve the performance but it's only similar to the extra loop example.

````julia

function normalize_by_row_v1(arr)
    sqrt.(sum(x->x^2,arr, dims=2))
end

julia> @btime nrm1 = normalize_by_row_v1($vec_1);
  447.826 μs (8 allocations: 781.42 KiB)

````

I've gone thorough the docs, watched a few youtube videos and scoured some of the popular user forums and come up with a few possible options. 
It seems it is possible to squeeze more performance but how much better can we do? 



## Are loops really that bad?
So I briefly mentioned this idea that loops are bad and you may be familiar with this concept if you are coming from python and MATLAB, where the for-loop option is often many times slower than the vectorised approach. 

But most software that is fast is written in a language that is built around loops such as `Fortran`, `C` or `Java`. 
However, the key difference in these cases is that they are statically typed and compiled languages and not interpreted like `MATLAB` or `python`. 
This static typing and compilation allows much more performance to be extracted as all the information is know beforehand whereas in interpreted languages there is a constant need to check everything. 
Packages like `NumPy` provide highly optimised functions that are actually compiled to `C` beforehand, hence their performance. 
I think that's partly where this *"loops are bad"* mentality comes from in an interpreted language - there are quick vectorised libraries that you can use and they are quicker than something that will be compiled into `bytecode` by the `python` compiler.

So to prove this I've take the extra information gathered though trawling the web and hope to show it's not all bad!

````julia
 function normalize_by_row_v7(arr)
    norms = Vector{Float64}(undef, size(arr)[1])
    @inbounds for i in axes(arr, 1)
        anorm2 = zero(eltype(arr))
        for j in axes(arr, 2)
            anorm2 += arr[i, j]^2
        end
        norms[i] = sqrt(anorm2)

    end
    return norms
end

julia>  @btime nrm7 = normalize_by_row_v7_turbo($vec_1);
    319.993 μs (2 allocations: 390.67 KiB)

````


It's possible to use the `LoopVectorization` package to enable some extra optimisations during the compilation process.  
Always verify that these optimisations don't affect the results from your calculations as they may be doing something like changing the order of calculations.

````julia
using LoopVectorization

function normalize_by_row_v7_turbo(arr)
    norms = Vector{Float64}(undef, size(arr)[1])
    @turbo for i in axes(arr, 1)
        anorm2 = zero(eltype(arr))
        for j in axes(arr, 2)
            anorm2 += arr[i, j]^2
        end
        norms[i] = sqrt(anorm2)

    end
    return norms
end

julia>  @btime nrm7 = normalize_by_row_v7_turbo($vec_1);
    161.017 μs (2 allocations: 390.67 KiB)

````

## Summary
So the one line summary? If you want to make your `python` code ***10x times quicker*** use `Julia`!!

# References


[^1]: Weisstein, Eric W. "Vector Norm." From MathWorld--A Wolfram Web Resource. https://mathworld.wolfram.com/VectorNorm.html. Accessed on 13/2/2022
[^2]: NumPy API Reference, . https://numpy.org/doc/stable/reference/generated/numpy.linalg.norm.html#rac1c834adb66-1. Accessed on 13/2/2022