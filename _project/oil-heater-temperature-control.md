---
title: "Temperature Control of an Oil Heater"
img: tc_kapak.png
collection: project
date: 2023-01-09
---

# Oil Heater Simulation

An oil heater cycle is modeled by MATLAB/Simulink as graduation project in the Boğaziçi University's **ME 492** class.

The oil cycle is a part of the Organic Rankine Cycle located at the [BURET Lab](http://buret.boun.edu.tr/facilities/organic-rankine-cycle/) of Boğaziçi University. The oil is used to heat up the working fluid R134A. The oil undergoes four different components, including a pump, heater, evaporator, and tank. The system, including the four components, is modeled in MATLAB/Simulink by using governing differential equations and experimental data.

The simulink models and the LaTeX code can be found [here](https://github.com/edizferit/Oil-Heater-Simulation).

---

The diagram that represents the oil cycle and the default control strategy applied at the heater to keep the oil at the desired temperature is given below:

<center>
<img src="/images/tc_def.png" alt="Experiment Setup" style="height:250px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
</center>
<br>

Curve fitting techniques are applied to the experimental data to obtain several variables. Below figue is an example showing the fitted functions which are used to find the heat transfer at the evaporator with respect to the temperature.

<center>
<img src="/images/tc_evaporator_curve_fit.png" alt="Experiment Setup" style="height:250px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
</center>
<br>

The experimental data is split to two parts as training and validation, which can be seen below:

<center>
<img src="/images/tc_experimental-data.png" alt="Experiment Setup" style="height:250px; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;"/>
</center>
<br>
