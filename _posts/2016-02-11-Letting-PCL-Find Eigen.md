---
layout: post
title: Helping PCL find Eigen when using Homebrew
---
Most of the time when compiling a Point Cloud Library application one sometimes gets compile errors like 

    fatal error: 'Eigen/Core' file not found

For Mac owners using Homebrew this due to there being no Eigen directory in /usr/local/include. Instead one has to some CMake magic to find the directories. It is a bit easier to create a symbolic link in the include directory, like this, for Eigen version 3.2.7,

    ln -s /usr/local/Cellar/eigen/3.2.7/include/eigen3/Eigen /usr/local/include/Eigen