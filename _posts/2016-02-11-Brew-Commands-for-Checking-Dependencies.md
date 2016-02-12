---
layout: post
title: Brew Commands for Checking Dependencies
---
To check which dependencies a particular formula has write 
     brew deps opencv
     ant atk autoconf automake bison boost...
Here it will show all dependencies recursively.

To check which formulas is dependent on a particular formula
    brew uses --installed boost
    boost-python homebrew/science/pcl homebrew/science/vtk...
