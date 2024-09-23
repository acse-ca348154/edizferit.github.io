---
title: "Parallelising and Optimising Mineral Separator Circuits"
img: ms_web.webp
date: 2024-04-03
---

<div align="justify">
This project was a group project included in my master's program at Imperial. Here, I implemented a genetic algorithm to find the optimum circuit configuration to separate minerals.
</div>

<div align="justify">
The optimum circuit configuration can be seen below.
</div>

<center>
<img src="/images/ms_best.png" alt="Best Circuit" style="width: 90.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

The workflow of the genetic algorithm is shown in the below diagram.

<center>
<img src="/images/ms_diagram.png" alt="Genetic Algorithm Workflow" style="width: 50.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

Genetic algorithm converge after 500 generations as seen below.

<center>
<img src="/images/ms_convergence.png" alt="Genetic Algorithm Convergence" style="width: 90.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

Speedup gained by using multiple nodes is provided below.

<center>
<img src="/images/ms_speedup.png" alt="Speedup vs Clusters" style="width: 90.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

The time it takes for using different thread numbers are shown in the below figure.

<center>
<img src="/images/ms_openmp.png" alt="Time vs Threads" style="width: 70.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

Lastly, if the price of the mineral changes, the change in the optimum circuit values can be seen below.

<center>
<img src="/images/ms_economy.png" alt="Economic Effect of Gerardium Price Change" style="width: 90.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

To be continued...
