---
layout: mfile
title: RetIrradiancePerAreaAndEyeLengthToRetIrradiancePerDegrees2
categories:
  - PsychRadiometric
encoding: UTF-8
---

retIrradiance\_PerDegrees2 = RetIrradiancePerAreaAndEyeLengthToRetIrradiancePerDegrees2(retIrradiance\_PerArea,eyeLength)  

Convert retinal irradiance measured in units of Y/x^2 to units of  
Y/deg^2, where x is a unit of distance (m, cm, mm, um, etc.) and  
Y is a measure of light amount (Watts, Joules, quanta/sec, quanta, etc.)  

Eye length should be passed in units of x.  

The conversion assumes that we are in the small angle regime, where  
degrees are essentially linear with retinal extent.  

See also: PsychRadiometric, RetIrradiancePerDegrees2AndEyeLengthToRetIrradiancePerArea.  

6/23/13  dhb  Wrote it.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychRadiometric/RetIrradiancePerAreaAndEyeLengthToRetIrradiancePerDegrees2.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychRadiometric/RetIrradiancePerAreaAndEyeLengthToRetIrradiancePerDegrees2.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychRadiometric/RetIrradiancePerAreaAndEyeLengthToRetIrradiancePerDegrees2.m</code>
</div>
