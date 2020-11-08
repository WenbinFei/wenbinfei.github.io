---
layout: page
title: Finite element simulation of heat transfer based on CT image
modified: 
excerpt: " "
comments: true
share: true
image:
  feature: 
  credit: 
  creditlink: 
---
There are numerous definition of particle shape descriptors, but it is necessary to select proper descriptors carefully. I compared several equations of 3D particle shape descriptors in paper:

**Fei W, Narsilio GA, Disfani MM. Impact of three-dimensional sphericity and roundness on heat transfer in granular materials. Powder Technology 2019, 355:770-781, [doi](https://doi.org/10.1016/j.powtec.2019.07.094)** 

Then I determined to use the following equation:

<body>
	<p align="left"> 
	    <img src="/images/sphericity-roundness-equation.png"  width='100%'/><br>	    
	</p>
</body>

*Fig.1 Equations of 3D particle shape descriptors*

A framework developed to calculate the above sphericity and roundness and their on effective thermal conductivity can be quantified..

<body>
	<p align="left"> 
	    <img src="/images/particle-shape-framework.png"  width='100%'/><br>	    
	</p>
</body>

*Fig.2 Framework to calculate 3D particle shape descriptors*

The framework works well on sands with distinct particle shape. 

<body>
	<p align="left"> 
	    <img src="/images/CT-images.png"  width='100%'/><br>	    
	</p>
</body>

*Fig.3 Photos and CT images of five sands*

<body>
	<p align="left"> 
	    <img src="/images/sphericity-roundness-sands.png"  width='100%'/><br>	    
	</p>
</body>

*Fig.4 Sphericity and roundness of individual grains in five sands*

**Please cite our relevant papers**  

- **Fei W**, Narsilio GA, Disfani MM. Impact of three-dimensional sphericity and roundness on heat transfer in granular materials. Powder Technology 2019, 355:770-781, [doi](https://doi.org/10.1016/j.powtec.2019.07.094).  
- **Fei W**, Narsilio GA. Network analysis of heat transfer in sands. Computers and Geotechnics 2020, 127:103773, [doi](:https://doi.org/10.1016/j.compgeo.2020.103773).











