---
layout: page
title: THMC coupling analysis at field scale
modified: 
excerpt: "AEEA Coupler"
comments: true
share: true
image:
  feature: 
  credit: 
  creditlink: 
---

As shown in Fig. 1, first, a thermo-hydro-chemical (THC) coupling process for multiphase flow in porous media is considered in ECLIPSE (Kuang et al., 2014). The linker program “AEEA Coupler” then reads the information of locations and variables, such as temperature, pore pressure and saturation, from the center point of the simulation grid that is used in ECLIPSE. Based on these data, the AEEA Coupler calculates the values of temperature and pore pressure and populates them for the finite element (FE) meshes that are used in ABAQUS (Li et al., 2002). Then, ABAQUS is run for a thermo-hydro-mechanical (THM) coupling analysis using the updated information, and new porosity, permeability and capillary pressure are obtained and used to update the values in the ECLIPSE simulation grid through the AEEA Coupler. The simulation then moves on to the next step (Fei, 2014).

<body>
<p align="center"> 
	<img src="https://github.com/WenbinFei/wenbinfei.github.io/blob/master/images/AEEA-coupler-scheme.jpg" width='70%'/><br>
	<b>Fig.1. Schematic diagram of the AEEA Coupler.</b>
</p>
</body>

The entire thermo-hydro-mechanic-chemical (THMC) coupled processes for multiphase flow is sequentially and explicitly considered between ABAQUS and ECLIPSE through the developed AEEA Coupler (Fei, 2014). The steps of the coupling analysis are illustrated in Fig. 2. First, a THC coupling analysis is conducted between t<sub>k</sub> and t<sub>k + 1</sub> in ECLIPSE, and its results are passed to ABAQUS in t<sub>k</sub>. Next, a THM coupling analysis is carried out between t<sub>k</sub> and t<sub>k + 1</sub> in ABAQUS, and the results of ABAQUS are passed back to ECLIPSE in t<sub>k + 1</sub> to perform the simulation for the next time step.


<p align="center"> 
	<img src="https://github.com/WenbinFei/wenbinfei.github.io/blob/master/images/AEEA-coupler-steps.jpg" width='70%'/><br>
	<b>Fig. 2. Time steps and variables update in coupling analyses.</b>
</p>

_Please find more details from https://doi.org/10.1016/j.enggeo.2015.07.017_