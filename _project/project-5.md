---
title: "Automatic Guitar Tuning Machine"
img: gt_cover.webp
collection: project
date: 2021-04-03
---

<div align="justify">
Every guitar player dreams of a machine that will tune the guitar automatically. We designed and built that machine as a term project for our mechatronics class. LCD screen and push button enable users to choose the desired tuning type. It is entirely portable as the design includes everything needed, such as the microcontroller, amplifier circuit, DC motors, motor controllers, and user interface.
</div>

<center>
<img src="/images/gt_all.jpg" alt="Automatic Guitar Tuner Complete Setup" style="width: 90.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

### Amplifier Circuit

<div align="justify">
The sound waves coming from the guitar are amplified in the amplifier circuit that we constructed. Also the noise is filtered here providing a smooth sound. Amplifier circuit consists of LM386 and many other external circuit elements such as capacitors to reduce the noise and fluctuations.
</div>

<center>
<img src="/images/gt_ampCir.jpg" alt="Amplifier Circuit" style="height:200px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
<img src="/images/gt_ampCirSchematic.jpg" alt="Amplifier Circuit Schematic" style="height: 200px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
</center>

### Fast Fourier Transform

<div align="justify">
Fast Fourier Transform is applied to these sound waves in the microcontroller. This way, the signal is transformed from the time domain to the frequency domain where we can work more easily. Harmonics caused some trouble in determining the exact frequencies of the strings, but we handled them in the end. 
</div>

<center>
<img src="/images/gt_fft.jpg" alt="Automatic Guitar Tuner Complete Setup" style="width: 95.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

### Motor Control

<div align="justify">
Six DC motors are used, one for each string, which are controlled by three motor drivers. Because there is a limited number of pins available in the microcontroller, NOT gates are used to decrease the total pin usage by implementing the logic for each motor. A PID controller is programmed with Arduino, which makes motors rotate slower when they approach the desired frequency for fine-tuning.
</div>

<center>
<img src="/images/gt_tuner.jpg" alt="Guitar Tuner" style="height:200px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
<img src="/images/gt_motorControl.jpg" alt="Motor Drivers" style="height: 200px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
</center>
<br/>

### Main Components
* Microcontroller: 
    * Teensy 3.2
    * Arduino Uno
* Amplifier Circuit:
    * LM386
    * Capacitors and resistors
* User Interface:
    * LCD Screen
    * Push Button
* Motor Driver: L293D
* Hex Inverter NOT Gate IC: 74LS04
* DC motor: 12V 26 RPM Brushless DC Gearmotor
* Power Supply Module
* Mechanical Structure

### Board Schematic

<center>
<img src="/images/gt_schematic.jpg" alt="Board Schematic" style="width: 95.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>

