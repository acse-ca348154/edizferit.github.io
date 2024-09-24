---
title: "Parallelising and Optimising Circuits"
img: ms_kapak.webp
date: 2024-04-03
---

<div align="justify">
This project was a group project included in my master's program at Imperial College London. Here, I implemented a genetic algorithm to find the optimum circuit configuration to separate minerals with the maximum performance.
</div>

### Optimum Circuit Configuration

<center>
<img src="/images/ms_best.png" alt="Best Circuit" style="width: 90.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

<div align="justify">
The above circuit is the one giving the maximum performance in separating a valuable mineral called 'Gerardium' (not a real mineral). It will extract the maximum amount of Gerardium while maintaining high purity.
</div>

### Genetic Algorithm

<center>
<img src="/images/ms_diagram.png" alt="Genetic Algorithm Workflow" style="width: 50.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

<div align="justify">
I implemented a genetic algorithm to find the best circuit. It includes two main phases: exploration and exploitation. Random crossovers and mutations are used.
</div>

### Convergence

<center>
<img src="/images/ms_convergence.png" alt="Genetic Algorithm Convergence" style="width: 90.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

<div align="justify">
Genetic algorithm converges after 500 generations, as shown in the figure above. The larger jumps in the plot represent the mutations, while smaller but consistent improvements represent the exploitation.
</div>

### Parallelisation with MPI

<center>
<img src="/images/ms_speedup.png" alt="Speedup vs Clusters" style="width: 90.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

<div align="justify">
The genetic algorithms are easily parallelisable. Therefore, I used C++ libraries, such as MPI and OpenMP, to make the optimisation faster. With MPI, I tested the performance using several cores and plotted the speedup and efficiency results, as seen above. With 4 processors, we can gain 2.5 times speedup.
</div>

### Parallelisation with OpenMP

<center>
<img src="/images/ms_openmp.png" alt="Time vs Threads" style="width: 70.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

<div align="justify">
I also tested the algorithm by parallelising it using OpenMP, which is straightforward to implement but limited by the number of cores on a single computer. In contrast, MPI allows for scaling across multiple processors on different computers, offering virtually unlimited computational power. However, MPI is more complex to implement due to the need for managing communication between processors.
</div>

### How Does the Optimum Cirucit Change with the Varying Values of Geraridum

<center>
<img src="/images/ms_economy.png" alt="Economic Effect of Gerardium Price Change" style="width: 90.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

<div align="justify">
Lastly, in the above figure, we see that if Gerardium price increases, the purity of the concetenate decreases slightly as seen in the red line. This balance depend on the cost of waste in the concatenate and amount of Gerardium extracted.
</div>
