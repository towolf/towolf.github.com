---
layout: mfile
title: NearestResolution
categories:
  - PsychOneliners
encoding: UTF-8
---

res=NearestResolution(screenNumber,[width,height,hz,pixelSize])  
res=NearestResolution(screenNumber [,width][,height][,hz][,pixelSize][,outputId])  
res=NearestResolution(screenNumber,desiredRes)  

Finds the available screen resolution most similar (in log cartesian space) to that  
requested. Any argument that is [] or NaN will be ignored in assessing similarity.  
If you specify pixelSize then the returned res will specify pixelSize. Typically  
you'll use the returned "res" to set your screen's resolution:  

SetResolution(screenNumber, res)  

Note: On Linux, if more than one video display output is connected to  
a given screenNumber, you must specify the optional 'outputId' parameter  
to select the output for which you want a match.  

Also see SetResolution, ResolutionTest, and [Screen](/docs/Screen) Resolution and Resolutions.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/NearestResolution.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/NearestResolution.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/NearestResolution.m</code>
</div>
