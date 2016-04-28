---
layout: post
title: Iterating over Lists of Lists OR Creating Nested For loops in Python
---
Lets say you have a list of lists containing values that you want to iterate over. The problem is that the number of lists keeps on changing so you can't really make it into a hard coded set of nested for loops. What you really need is to dynamically create a set of nested for loops. In Python you can use the itertools for these kind of jobs. Extremly handy if you want to do grid search over a set of values for example. In code it might look like this,

    # Python3
    import numpy as np 
    from itertools import product

    # Create a list of np array values  
    rangeList = []
    rangeList.append(np.linspace(0.,10.,10))
    rangeList.append(np.linspace(40.,1000.,10))
    rangeList.append(np.linspace(10.,40.,10))

    # Iterate over all of the lists values 
    for vals in product(*rangeList):
        for val in vals:
            print(val,end=",")
        print(" ")

this will print the following, 

    >>  0.0,40.0,10.0,
        0.0,40.0,13.3333333333,
        0.0,40.0,16.6666666667,
        0.0,40.0,20.0,
        0.0,40.0,23.3333333333,
        0.0,40.0,26.6666666667,
        ....

