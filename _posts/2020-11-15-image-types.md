---
layout: post
title: "Image data types"
excerpt: "What do unit8, unit16... mean?"
modified: 2020-11-15
tags: [blog]
comments: false
---
Some image types are shown as below:
 
- uint8 = 0 to 255  
- uint16 = 0 to 65535  
- unit32 = 0 to ((2<sup>32</sup>) - 1)  
- float = -1 to 1 or 0 to 1  
- int8 = -128 to 127  
- int16 = -32768 to 32767  
- int32 =-2<sup>31</sup> to 2<sup>21</sup> - 1  

*It is better to use float when do image processing. If using uint8, some pixel value will be larger than 255 during processing by some algorithm and these pixel will be given 255*

Functions that convert images to desired type and properly rescale their values in **scikit-image**

- img_as_float - convert to 64-bit floating point 
- img_as_ubyte - convert to 8-bit unit  
- img_as_uint - convert to 16-bit unit
- img_as_int - convert to 16-bit unit  