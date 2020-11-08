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

\\( a^2 = b^2 \\)

A framework has been developed used to calculate three-dimensional sphericity and roundness.

After that, the impact of particle shape on effective thermal conductivity can be quantified.

<figure align="center"> 
<img src="/images/particle-shape-framework.png" width='100%'/><br>
<b>Fig.1 Framework of quantifying the impact of particle shape on effective thermal conductivity</b>
</figure> 

The geometry of a sand sample can be reconstructed from scanned CT images and used to simulate heat transfer in a similar fashion as in  by numerically solving an elliptic partial differential equation (Equation 1), Fourier’s law (Equation 2) and a continuity equation (Equation 3), using COMSOL Multiphysics . The thermal conductivity of the packing are obtained by integrating the heat flux at the top and bottom boundaries using Equation 444,  and their average is taken as the effective thermal conductivity of the entire sample.

$ρC ∂T/∂t+ρCu⋅∇T=∇⋅(λ∇T)		(1)

where, for each phase involved in the simulation, ρ is the density (kg/m), C is the heat capacity (J/(kg K)), T is the temperature (K), t is the time (s), u is the velocity vector (m/s), λ is the thermal conductivity (W/(m K)).
	q=λ∇T	(2)


	-n(q_s-q_p )= 0		(3)

where n is the unit normal vector of the solid-pore interface, qs and qp are the heat fluxes in the particle and pore, respectively. 
The effective thermal conductivity λ_eff  (W m^(-1) K^(-1) ) of a sample of horizontal cross-section area A (m2) is found as:
	λ_eff=(1/A ∫_A▒〖Q_z  dA 〗)/((T_a-T_b)/L)	(4)

where T_a and T_b are the prescribed temperatures at the inlet and outlet boundaries, L (m) is the height of the sample and Q_z   (W/m2) is the vertical heat flux of nodes at the inlet or outlet.
The mesh of the Ottawa sand is shown in Figure 1 and it was generated in Simpleware  ScanIP  by setting coarseness as -40 after a mesh size sensitivity analysis showed convergence to an asymptotic value of computed thermal conductivity (analysis not included here). The thermal conductivity of minerals has been suggested to be set between 1 and 8 W/(m K) in the literature . Since the aim of this study is on the effect of particle shape on effective thermal conductivity, 3 W/(m K)  is assigned to solid particles in all samples to mitigate the potential effects of different mineralogy on the effective thermal conductivity. Thermal conductivity of 0.025 W/(m K)  and 0.591 W/(m K)  is assigned to the void space within the packings for simulating heat transfer in dry and water-saturated granular materials, respectively . The boundary temperature on the top surface is prescribed at 293 K, while at 292 K on the bottom surface to generate a small thermal gradient, other boundaries are considered as insulation as shown in  Figure 1. With this material and boundary conditions, the system is numerically solved for temperature distribution and heat fluxes are estimated to then derive an effective thermal conductivity.

