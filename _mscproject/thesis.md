---
title: "AI-Based Framework to Accelerate Flow Simulation"
img: slb_kapak.webp
date: 2024-08-03
---

<div align="justify">
This page contains a summary of my master's thesis, which was conducted in collaboration with Imperial College London and SLB. I created an artificial intelligence model that predicts subsurface CO2 flow with greater speed than traditional physics-based simulators. Unlike other studies, the aim here is not to reach a general reservoir model, but to train the models specifically for the reservoir and task at hand. To make this technology accessible, I also crafted a user-friendly web application that facilitates both the training and prediction processes.
</div>

### Web Application Video

<center>
  <img src="/videos/slb_web.gif" alt="Website Demo" style="width:90%; border-radius:5px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br>

<div align="justify">
The web application is designed in a modular fashion, making it easy to add new features. I utilized an open-source package called webviz-config, in addition to Python's Plotly and Dash libraries for development. The repository structure is as follows:
</div>

<center>
  <img src="/images/slb_repositories.jpg" alt="Website Repositories" style="width:90%; border-radius:5px; margin-top: 8px; margin-bottom: 8px;">
</center>

<div align="justify">
Data flow in the web application is shown in the below diagram:
</div>

<center>
  <img src="/images/slb_files.png" alt="Website File Flow" style="width:90%; border-radius:5px; margin-top: 8px; margin-bottom: 8px;">
</center>

### Inputs and Outputs

<center>
  <img src="/images/slb_inputs.jpg" alt="AI Input Output" style="width:90%; border-radius:5px; margin-top: 8px; margin-bottom: 8px;">
</center>

<div align="justify">
The user can select arbitrary number of inputs out of 35 static reservoir properties and arbitrary number of outputs out of 17 dynamic reservoir properties and they can decide on the time step resolution. The model is automatically generated on the fly according to the user's selections. This offers huge flexibility as not all reservoirs have uncertainty in the same attributes.
</div>

### Neural Network Architecture

<center>
  <img src="/images/slb_arch.jpg" alt="AI Architecture" style="width:90%; border-radius:5px; margin-top: 8px; margin-bottom: 8px;">
</center>

<div align="justify">
I designed an encoder-decoder architecture using convolutional layers to handle 4-dimensional inputs. I incorporated residual connections to increase the depth of the network. Additionally, batch normalization was implemented to regularize the model and facilitate the learning process. The ReLU activation function was utilized in all layers except the output layer.
</div>

### Comparison

<center>
  <img src="/images/slb_comparison.png" alt="AI Predictions vs Physics Simulation" style="width:90%; border-radius:5px; margin-top: 8px; margin-bottom: 8px;">
</center>

<div align="justify">
AI predictions closely resemble the physics simulation, as shown in the comparison figure. AI predictions are generated in less than a second, while the physics simulation takes 5 minutes.
</div>

### Code Avaliability

Some portion of the source code is available in [this](https://github.com/acse-efk23/WebAI) GitHub repository. The Python packages required to process the raw Intersect data are confidential and not shared. At the moment, the data is not publicly available. Because of these, reproducing the same functionality is not possible. Still, the pages other than data loading would work fine.

<div align="justify">
More information will be available once the paper is published. For further inquiries, please contact me via email.
</div>