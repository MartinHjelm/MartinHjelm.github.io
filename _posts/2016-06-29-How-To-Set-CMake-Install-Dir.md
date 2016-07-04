---
layout: post
title: Setting Install Directory When Using CMake 
---
Sometimes we want to install a build to a different directory. In CMake this can be done by setting the CMAKE_INSTALL_PREFIX variable. When we are building OpenCV3 for examle we would do,

    cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local ../opencv-3
