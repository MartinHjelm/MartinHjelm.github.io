---
layout: post
title: Fisher Vector & Caffe C++ Implementation 
---
I implemented a C++ pipeline for learning Fisher feature vectors using <a href="http://www.vlfeat.org">VLFeat</a> since Matlab should be avoided whenever possible. I managed to find Python bindings later. 

The code does the following from a a set of labeled images it extracts dense SIFT features. It finds the PCA representation of the SIFT reducing the dimension from 128 to 80 (or whatever dimension you want). It then computes the GMM clustering using the EM algorithm. From the learned the GMM it computes the Fisher vector representation. We can also add additional features from a text file, such as a sub layer from a CNN like Caffe. After computing the feature vectors  the code trains a linear SVM one for each class label. The code saves all representations so that the inference can be run on new images. 

The code use CMake for compilation and requires the Boost, <a href="http://opencv.org/">OpenCV</a> and <a hreF="http://eigen.tuxfamily.org">Eigen</a> libraries in addtion to <a href="http://www.vlfeat.org">VLFeat</a>. To train on some subset of images we can run from the terminal  

    ./fisher train 

and to test new images 

     ./fisher test

Just make sure you set the data paths correctly. <a href="https://github.com/MartinHjelm/fishercaffe">You can find the code here.</a>