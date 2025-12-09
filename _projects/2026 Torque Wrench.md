---
layout: project
title: MAE 3270 Strain gague torque wrench
description: Designed a Torque wrench for class given certain paramaters 
technologies: [Matlab, Solidworks, Ansys]
image: /assets/images/spaceship-design.jpg
---
![Strain Gague Wrench](/assets/images/Torque-Wrench-Drawing.jpg)
For MAE 3270 We were instructed to design a strain gague torque wrench This is my design, Its slightly slimmer then the baseline case, has a large filet around the driver and also is made out of a qunched and tempered 4340 steel for its greater ductitility over M42 Tool steel.

Here is a snippet from the matlab code of the material properties
E = 30.5e6;           % psi @73.4 degrees farenheight
poissons = 0.32;          %unitless
su = 217e3;         % psi
KIC = 82.8e3;         % psi*(in)^1/2
sfatigue = 78.1e3;   % psi
name = "4340 quenched and tempered";

