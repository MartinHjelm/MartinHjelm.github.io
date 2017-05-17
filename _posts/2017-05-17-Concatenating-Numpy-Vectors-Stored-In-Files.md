---
layout: post
title: Concatenating Numpy Vectors Stored In Files
---
Sometimes you have vectors or matrices stored in files, and you need to read them and concatenate them. One way of doing this is reading them into a list and then using Numpy's hstack or vstack to create the vector or matrix. Like this for concatenating rows

    result = np.hstack([np.genfromtxt(fName,delimiter=";") for fName in fList])

where the read matrix or vector all are of size ```MxNf```, that is the rows, ```M```, are the same across all read matrices while ```Nf``` can vary. The same goes for vertical stacking but then the sizes are reversed, that is, ```NfxM```, and we have,

    result = np.vstack([np.genfromtxt(fName,delimiter=";") for fName in fList])
