---
layout: mfile
title: ComputeDKL_M
categories:
  - PsychColorimetric
encoding: UTF-8
---

M = ComputeDKL\_M(bg,T\_cones,T\_Y)  

Compute the matrix that converts between incremental cone  
coordinates and DKL space.  The order of  
the coordinates in the DKL column vectors is (Lum, RG, S)  

The code follows that published by Brainard  
as an appendix to Human Color Vision by Kaiser  
and Boynton, but has been generalized to work  
for passed cone fundamentals and luminosity  
function.  

These should be passed in standard Psychtoolbox  
form (LMS in rows of T\_cones; luminosity function  
as single row vector T\_Y).  

The argument bg is the LMS cone coordinates of the  
background that defines the space.  

See [DKLDemo](/docs/DKLDemo) for proper use of this function.  Also  
DKLToConeInc and ConeIncToDKL.  

8/30/96   dhb  Pulled it out.  
4/9/05    dhb  Allow passing of cones and luminance to be used.  
11/17/05  dhb  Require passing of cones and luminance.  
          dhb  Fixed definition of M\_raw to handle arbitrary L,M scaling.  
10/5/12   dhb  Comment specifying coordinate system convention.  Supress extraneous printout.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychColorimetric/ComputeDKL_M.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychColorimetric/ComputeDKL_M.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychColorimetric/ComputeDKL_M.m</code>
</div>
