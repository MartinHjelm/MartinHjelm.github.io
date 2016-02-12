---
layout: post
title: Converting a Numpy One-Dimensional Array to Two Dimensions
---
Lets say we have created a 1-dimensional array in Python using numpy, that is,

    import numpy as np
    x = np.array([1,2,3])
    print x.shape
    >> (3,)

This array is one-dimensional and wow we want to convert that array into a two-dimensional object. To do it we can do either 

    x.shape = (1,-1)

or

    x = x.reshape(1,-1)

If we want to transpose it at the same time we just flip -1 and 1,

    x = x.reshape(-1,1)