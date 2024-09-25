---
title: "AI Model to Accelerate Flow Simulation"
img: slb_kapak.webp
date: 2024-08-03
---

<div align="justify">
This project forms the core of my master's thesis, undertaken in collaboration with Imperial College London and SLB. I developed an artificial intelligence model that predicts subsurface CO2 flow with greater speed than traditional physics-based simulators. To make this technology accessible, I also crafted a user-friendly web application that facilitates both the training and prediction processes.
</div>

### Web Application Video

<center>
  <img src="/videos/slb_web.gif" alt="Website Demo" style="width:90%; border-radius:5px; margin-top: 8px; margin-bottom: 8px;">
</center>

<div align="justify">
The web application is built with a modular fashion and it is easy to add on new features. I used an open source package called webviz-config, along with Python's Plotly and Dash libraries for development.
</div>

### Neural Network Architecture

<center>
  <img src="/images/slb_arch.jpg" alt="AI Architecture" style="width:90%; border-radius:5px; margin-top: 8px; margin-bottom: 8px;">
</center>

<div align="justify">
I designed an encoder-decoder architecture with convolutional layers to process 4-dimensional inputs and added residual connections to make the network deeper.
</div>

### Comparison

<center>
  <img src="/images/slb_comparison.png" alt="AI Predictions vs Physics Simulation" style="width:90%; border-radius:5px; margin-top: 8px; margin-bottom: 8px;">
</center>

<div align="justify">
AI predictions closely resemble the physics simulation, as shown in the comparison figure. AI predictions are generated in less than a second, while the physics simulation takes 5 minutes.
</div>
<br />

<div align="justify">
More information will be available once the paper is published. For further inquiries, please contact me via email.
</div>
