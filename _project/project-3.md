---
title: "Electric Motor Thermal Management for EVs and PHEVs"
img: tm_cover.webp
collection: project
date: 2021-01-03
---

An alternative thermal management system is proposed to cool down an electric motor of an EV. The design uses a ninety percent ethylene glycol-water mixture as the coolant, and it utilizes a combined cooling system that comprises of a cylindrical housing that covers the motor and absorbs the heat, and an aluminum heat sink on the base of the car to dissipate that heat.

<center>
<img src="/images/tm_motor.jpg" alt="Motor Cover" style="height:200px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
<img src="/images/tm_solid.jpg" alt="Heat Dissipation System" style="height: 200px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
</center>
<br>

After the concept design phase, free variables are optimized in a way that maximize the heat dissipation and minimize the pressure losses. Appropriate governing and boundary equations are derived and formulated in accordance with the literature. Then, these equations are fed to an algorithm to iteratively find the optimum design parameters using MATLAB.

<center>
<img src="/images/tm_matlab1.jpg" alt="3D Plot" style="height:250px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
<img src="/images/tm_matlab2.jpg" alt="2D Contour Plot" style="height: 250px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
</center>
<br>

Validation of the model is done via Ansys Fluent tool, a finite element computer software. All the parameters, equations, and constraints are entered to the software along with the optimum geometry of the components. Solidworks is used to create three main components:
1. Heat Tubes
1. Heat Sink
1. Cooling Cylinder

<center>
<img src="/images/tm_tube.jpg" alt="Heat Tube" style="height:230px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
<img src="/images/tm_heatsink.jpg" alt="Heat Sink" style="height: 230px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
</center>
<br>

The solution is obtained by making iterations until the residuals converge to a small, predetermined limiting value.

<center>
<img src="/images/tm_res.jpg" alt="Solution Residuals" style="height:220px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
<img src="/images/tm_cool.jpg" alt="Cooling Cylinder" style="height: 220px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
</center>
<br>

Grid independence test is carried out for each element by trying different mesh sizes and observing the differences in the
output pressures. When variations in the resulting parameter are not significant after a certain mesh element size, that size is selected as an ideal mesh element size, since increasing it after that point would only increase the necessary computational work.

<center>
<img src="/images/tm_grid.jpg" alt="Grid Independence Test" style="height:250px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
<img src="/images/tm_mesh.jpg" alt="Mesh Element Table" style="height: 200px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
</center>

