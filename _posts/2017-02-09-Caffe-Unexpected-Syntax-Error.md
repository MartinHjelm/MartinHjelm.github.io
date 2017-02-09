---
layout: post
title: Caffe import - TypeError got an unexpected keyword argument 'syntax' error
---
Got the following error when importing the caffe package for python on Mac and OSX 10.12.

    from caffe.proto import caffe_pb2
    File "caffe/proto/caffe_pb2.py", line 23, in <module>
    x01(\x0b\x32\x1a.caffe.HDF5OutputParameter\".\n\nPoolMethod\x12\x07\n\x03MAX\x10\x00\x12\x07\n\x03\x41VE\x10\x01\x12\x0e\n\nSTOCHASTIC\x10\x02\"W\n\x0ePReLUParameter\x12&\n\x06\x66iller\x18\x01 \x01(\x0b\x32\x16.caffe.FillerParameter\x12\x1d\n\x0e\x63hannel_shared\x18\x02 \x01(\x08:\x05\x66\x61lse*\x1c\n\x05Phase\x12\t\n\x05TRAIN\x10\x00\x12\x08\n\x04TEST\x10\x01')
    TypeError: __init__() got an unexpected keyword argument 'syntax'

This was resolved by editing the ```caffe_pb2.py``` file and commenting out all lines which said ```syntax='proto2'```


