---
title: "Image and Volume Processing Library"
img: vp_kapak.webp
date: 2024-04-03
---

In my Advanced Programming class at Imperial, I worked on a group project with 4 other students. Our goal was to develop a C++ library that could process images and volumes with a user-friendly Python-based GUI.

My contribution was to create and optimise Image and Volume classes and implement volume processing functions, such as three-dimensional blurs and projections. Throughout the week, I guided the team in effectively using GitHub: managing the repository, creating issues and branches, committing, pushing, creating pull requests, resolving merge conflicts, and conducting code reviews.

### Image Processing Video

<center>
<img src="/videos/vp_2d.gif" alt="GIF 2D" style="width: 90.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

### Volume Processing Video

<center>
<img src="/videos/vp_3d.gif" alt="GIF 3D" style="width: 90.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>
<br />

### UML Diagram

<center>
<img src="/images/vp_uml.png" alt="UML Diagram" style="width: 95.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>

An abstract `Dataset` is created as a base class. `Volume` and `Image` classes inherit the same data members; copy, move constructors; copy, move assignment operators while overwriting Read.
- Copy and move operators are defined to prevent memory leaks and optimise speed and memory usage.
- All pixel data is stored in a one-dimensional array (`unsigned char*`) for both volumes and images.
- Get and Set functions are defined to enable easy access to any pixel from its location x,y,z.

### Data Storing Mechanism

<center>
<img src="/images/vp_data.png" alt="UML Diagram" style="width: 90.0%; border-radius: 3px; margin-top: 8px; margin-bottom: 8px;">
</center>

Three methods are tried to decide on how to store data of volumes.
1. My first idea was to store the pointers to image objects in a `std::vector` container. But this method is slow because when we try to access a pixel value, we need to go through one more step.
2. Storing all values in a simple one dimensional array gave the best results. It provided 20% increase in speed of all functions due its better memory access times.
3. I also considered storing all of the data in a `std:vector` container thinking that a special container might give better access times. But it was slower than a simple one dimensional array. I believe the reason is that `std::vector` has so many features we don’t use which provide overhead. For instance, we don’t need to resize the data once we read it. So, we don’t need operators such as `.push_back()` which vector container provides. Thus, `unsigned char*` is the best way of storing data.
