---
layout: post
title: Batch Crop Images Using ImageMagick
---
ImageMagick comes with a tool to perform batch image transforms, it is called mogrify. To crop a specific rectangular area in all images in a directory the formula looks like this,

    mogrify -crop [rectWidth]x[rectHeight]+[rectTopX]+[rectTopY] -path pathToStoreCroppedFiles pathToImgDirectory/*.extension

A realization of this might look like this 
    
    mogrify -crop 300x300+290+170 -path ./myCroppedFilesDir *.png

This crops a 300x300 rectangle whos top is positioned at 290x170 from all the png images in the current directory and saves them to the directory myCroppedFilesDir(make sure the dir exists before you run). 