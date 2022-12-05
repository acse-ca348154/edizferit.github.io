---
title: "Design of a LiDAR"
img: ld_rendered.webp
collection: project
date: 2022-12-05
---

A novel mechanical Lidar design is created, which proposes two axes rotation with only one actuator. This enables the construction of a 3D map using only one motor and one rangefinder, reducing Lidar's cost. 

A combination of gear,  worm gear, and planetary gear is used to enable two axes rotation with only one axis torque input. 

### MSC Adams

<center>
<img src="/images/ld_adams.jpg" alt="Proposed design" style="height: 350px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
</center>
<br>
At first, the proposed gear combination is dynamically simulated in MSC ADAMS, which is a multibody dynamic simulation software. Results verified that the rangefinder (red) moved one degree upwards in each revolution of the motor, which is connected to the arm (yellow). The relative rotation speeds of the ring gear and the worm gear enable this motion of the laser sensor.

### Solidworks

<center>
<img src="/images/ld_solid.jpg" alt="Solidworks Drawing with Cap" style="height:450px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
<img src="/images/ld_solid_no_cap.jpg" alt="Solidworks Drawing without Cap" style="height: 450px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
</center>
<br>
The design is finalized in Solidworks by adding all other components like supports, slip ring, and cover, which holds the rangefinder. Static simulation is carried out to confirm the device's mechanical resistance against static failure.

### Data Transfer Calculations

The microcontroller is chosen according to the necessary data transfer speed and amount. Data sizes regarding the three defining coordinates are shown below:

<img align="right" src="/images/ld_point.jpg" alt="LiDAR Illustration" style="height:150px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px; margin-left: 3px;">

* **Vertical angle**: 7 bit. 
_Vertical field of view is 120° with 1° resolution, 7 bit = $2^7$ = 128_
* **Horizontal angle**: 9 bit.
_Horizontal field of view is 360° with 1° resolution, 9 bit = $2^9$ = 512_
* **Distance**: 11 bit.
_Range is 20 m with 1 cm resolution, 0.00 – 20.00, 11 bit = $2^{11}$ = 2048_

<center>
<img src="/images/ld_data_transfer.jpg" alt="Data Transfer Diagram" style="width: 60.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>

### Optimization of Gear Parameters

Specialties of the number of teeth, diameter, module, and face width of the gears are optimized in Matlab.

The following checks are done in Matlab:

1. There must be no **interference**. 
2. **Contact ratio** should be greater than 1.4.
3. **Pitch line velocity** should not be too large in case of high dynamic effects.

<img align="left" src="/images/ld_velocities.jpg" alt="LiDAR Illustration" style="height:200px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px; margin-left: 3px; margin-right: 30px">

Governing equations and constraints:
1.  $w_{ring} = (w_{ring} - w_{arm}) (360 / N_{gear})$

_Gear should rotate one degree in each revolution of the arm._
 
2.  $w_{arm} / w_{ring} = N_{ring} / (N_{sun} + N_{ring})$  

_Pitch line velocity must be the same at the contact point._
  
3.  $r_{worm} + r_{gear} = r_{sun} + d_{planet}$

_Rangefinder must be vertically aligned with the edge of the planet gear._

### Main Components

* Rangefinder:
  * Lite v3HP
* Microcontroller:
  * Arduino Uno
* Motor-Encoder:
  * Pololu brand DC motor with 1030 rpm, 9.7:1 reducer ratio, 48 ppr
* Slip Ring:
  * Hollow shaft slip ring
* Gears:
  * Module: 4 mm
  * Face width: 40 mm
  * Pressure angle: 20°

### Dynamic Simulation Recording

<center>
<video class="projectVideo" muted autoplay loop>
  <source src="/videos/ld.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>
</center>
<center>
<u><i><b>Dynamic Simulation Result by MSC Adams</b></i></u>
</center>
<br />
