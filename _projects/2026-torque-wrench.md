---
layout: project
title: MAE 3270 Strain gague torque wrench
description: Designed a Torque wrench for class given certain paramaters 
technologies: [Matlab, Solidworks, Ansys]
image: /assets/images/wrenchcad.png
---

<img 
  src="{{ '/assets/images/Torque-wrench-drawing.jpg)' | relative_url }}"
  alt="Wrench drawing"
  style="max-width: 40%; height: auto;"
>

For MAE 3270 We were instructed to design a strain gague torque wrench This is my design, Its slightly slimmer then the baseline case, has a large filet around the driver and also is made out of a qunched and tempered 4340 steel for its greater ductitility over M42 Tool steel.

Here is a snippet from the matlab code of the material properties
E = 30.5e6;        % psi @73.4 degrees farenheight
poissons = 0.32;          %unitless
su = 217e3;         % psi
KIC = 82.8e3;         % psi*(in)^1/2
sfatigue = 78.1e3;   % psi
name = "4340 quenched and tempered";

The one con of 4340 is it is harder to machine then for example 4130

To accurately model the force through the torque wrench we use a zero displacement condition on the driver and we then apply a load to the end of the handle to mimmic 60 in-lbs on the 
<p>
<img 
  src="{{ '/assets/images/wrenchsetup.png' | relative_url }}"
  alt="Wrench setup"
  style="max-width: 40%; height: auto;"
>
After that I was able to mesh and solve the model. 
Looking at the stresses we get a very similar computed stress to the 


<img 
  src="{{ '/assets/images/wrenchstress.png' | relative_url }}"
  alt="Wrench stress"
  style="max-width: 40%; height: auto;"
>
Zooming in we see our peak stress to be at the 
<img 
  src="{{ '/assets/images/zoomedwrenchstress.png' | relative_url }}"
  alt="Wrench stress"
  style="max-width: 40%; height: auto;"
>
We can also look at the strain at our strain gague point which nearly exactly matches our calculated stress
<img 
  src="{{ '/assets/images/wrenchstrain.png' | relative_url }}"
  alt="Wrench strain"
  style="max-width: 40%; height: auto;"
>
<p>

And also we can look at our total deformation
<p>
<img 
  src="{{ '/assets/images/wrenchdeformation.png' | relative_url }}"
  alt="Wrench deformation"
  style="max-width: 40%; height: auto;"
><p>
Similar to the base case the total deformation is higher because we didn't take into account the collapse in beam theory at the very tip of the drive
