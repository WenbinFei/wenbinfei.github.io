---
layout: post
title: "Image processing in Python"
excerpt: "Brief several python libraries for image processing"
modified: 2020-11-15
tags: [blog]
comments: false
---
Many ways to process images in Python.
- Pillow
- Matplotlib
- Scipy
- skimage
- OpenCV
- Other libraries to open propriatery images like - czi, OME-TIFF

### Pillow
Pillow is an image manipulation and processing library. You can use pillow to crop, resize images and to do basic filtering. For advanced tasks that require computer vision or machine elarning we have other packages such as openCV, scikit image and scikit learn. 

### Matplotlib
Matplotlib is a plotting library for the Python programming language. Pyplot is a Matplotlib module which provides a MATLAB-like interface. Pyplot is commonly used not just to generate plots and graphs but also to visualize images because visualizing images is nothing but plotting data in 2D. 

### Scipy
Scipy is a python library that is part of numpy stack. It contains modules for linear algebra, FFT, signal processing and image processing. Not designed for image processing but has a few tools

### Scikit image
scikit image is an image processing library that includes algorithms for segmentation, geometric transformation, color space manipulation, analysis, filtering, feature detection, and more. A very good package for traditional machine learning, using Random forest or SVM.

### Opencv
openCV is a library of programming functions mainly aimed at computer vision. Very good for images and videos, especially real time videos. It is used extensively for facial recognition, object recognition, motion tracking, optical character recognition, segmentation, and even for artificial neural netwroks. 

You can import images in color, grey scale or unchanged usingindividual commands 
- cv2.IMREAD_COLOR : Loads a color image. Any transparency of image will be neglected. It is the default flag.
- cv2.IMREAD_GRAYSCALE : Loads image in grayscale mode
- cv2.IMREAD_UNCHANGED : Loads image as such including alpha channel  

Instead of these three flags, you can simply pass integers 1, 0 or -1 respectively.

**Note: OpenCV represents RGB images as multi-dimensional NumPy arrays, but as BGR.**

we can convert the images from BGR to RGB  
`plt.imshow(cv2.cvtColor(color_img, cv2.COLOR_BGR2RGB))`

We can also change color spaces from RGB to HSV..  
`plt.imshow(cv2.cvtColor(color_img, cv2.COLOR_BGR2HSV))`
