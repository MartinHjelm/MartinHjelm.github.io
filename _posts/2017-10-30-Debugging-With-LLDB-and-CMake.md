---
layout: post
title: When Debugging With LLDB and CMake Make Sure to Turn of Optimization
---
When debugging C++ using LLDB from the command line. It seems you have to put 
    
    make DCMAKE_BUILD_TYPE=debug

Just removing optimization flags and writing 

    set(CMAKE_BUILD_TYPE Debug)

in the CMakeLists.txt does not seem to do the trick when there are underlying CMakeLists.txt hierarchies or some other parameters. Nevertheless, by using the DCMAKE_BUILD_TYPE parameter you get access to the otherwise, by optimization, hidden variables.    
