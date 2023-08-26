---
layout: page
title: Cloth Simulation
permalink: /ClothSimulation/
description: "Cloth simulation project in C++ with OpenGL and various optimizations Cross platform"
---

# Cloth Simulation Sample Code/Tutorial

This cloth simulation project was part of the Advanced Animation for Computer Games (COMP 477) class I took in Winter 2011 with [Dr. P. Grogono](http://users.encs.concordia.ca/~grogono/){:target="_blank"} at [Concordia University](http://www.concordia.ca/){:target="_blank"}.

This project provides a simplistic approach for simulating cloths. I based my implementation on Dr. Mosengaard's implementation available [here](http://cg.alexandra.dk/2009/06/02/mosegaards-cloth-simulation-coding-tutorial/){:target="_blank"}. To avoid repetition on how a cloth is constructed and simulated consult Dr. Mosegaard's article on cloth simulation.

The source code provided is a cross-platform implementation for simulating cloths written in C++ using OpenGL as main graphics toolkit. For optimized mathematical operations I chose the Eigen library which supports vectorization (SSE instruction set) and has most of the basic mathematical operations required in CG.

From this page you can download the source code of the project, which can be used as sample code/tutorial for your own cloth simulation application or game smiley.

## Cloth Simulation Screenshots
![alt text](/assets/data/ClothSimulation/ClothSimScreen1.jpg)
![alt text](/assets/data/ClothSimulation/ClothSimScreen2.jpg)


## Cloth Simulation Binaries
[Windows x64](/assets/data/ClothSimulation/ClothSimulation_x64.zip) [Windows 32](/assets/data/ClothSimulation/ClothSimulation_Win32.zip)

To execute the x64 version of cloth simulation you need the VS2010 runtime environment that can be downloaded from here

## Cloth Simulation Source Code
[Windows VS2010](/assets/data/ClothSimulation/ClothSimulation.zip)

Even through I am a linux guy I did this project on Windows. I will be though pretty easy to write some makefiles and port the code. The only windows dependent code I am using is :

* The old C code for loading a windows open file dialog
* Of course the #include <windows.h>
* AND THAT'S IT...
