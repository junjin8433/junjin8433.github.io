---
layout: post
section-type: post
title: install opencv on ubuntu
category: tech
tags: [ 'tutorial'  ]
---


## requirements
Ubuntu  Opencv Cmake gcc
before install opencv, libgtk2.0-dev and pkg-config are the pre-required packages that should be setted first. If you install opencv without these two packages, it might cause some errors like:

```
 OpenCV Error: Unspecified error (The function is not implemented. Rebuild the library with Windows, GTK+ 2.x or Carbon support. If you are on Ubuntu or Debian, install libgtk2.0-dev and pkg-config, then re-run cmake or configure script) in cvNamedWindow, file /usr/local/opencv/OpenCV-2.0.0/src/highgui/window.cpp, line 100
 terminate called after throwing an instance of 'cv::Exception'
```
to fix it, you should remove opencv and reset it.

```
$ apt-get install libgtk2.0-dev
$ apt-get install pkg-config
```

## Getting the Latest Stable OpenCV Version
 Go to the opencv Sourceforge page
 Grab the latest snapshot from Git repository

## Building OpenCV from Source Using CMake, Using the Command Line

```
 cd ~/opencv
 mkdir release
 cd release
 cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local ..
 make
 sudo make install
```

## Uninstall Oencv
 go to the build directory and run ```sudo make uninstall```
 remove the opencv directory

