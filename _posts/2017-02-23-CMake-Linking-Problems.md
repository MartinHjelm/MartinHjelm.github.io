---
layout: post
title: Batch Resize Images With Padding
---
ImageMagick comes with a tool to perform batch image transforms, it is called mogrify. To perform a resize of a set of images keeping the aspect ratio and padding with a white background we can use the following command, 

    mogrify -resize 100x100 -background white -gravity center -extent 100x100 -path ./resize_directory *.png

This command resizes all png images in the directory to a 100x100 and pads with white to keep the aspect ratio.  