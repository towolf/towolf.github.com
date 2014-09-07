---
layout: mfile
title: RadianceAndDegrees2ToCornIrradiance
categories:
  - PsychRadiometric
encoding: UTF-8
---

cornealIrradiance\_PowerPerArea = RadianceAndDegrees2ToCornIrradiance(radiance\_PowerPerSrArea,stimulusAreaDegrees2)  

Convert the radiance of a stimulus to corneal irradiance, given that we know the area of the stimulus in degrees2.  
The routine assumes that the stimulus is rectangular with linear subtense sqrt(stimulusAreaDegrees2).  

Light power can be in your favorite units (Watts, quanta/sec) as can distance (m, cm, mm).  The units for  
area in the returned irradiance match those used for area in the passed radiance.  

So, if radiance is in Watts/[cm2-sr] then distance needs to be in cm and irradiance will be in Watts/cm2.  

The derivation also assumes the small angle approximation simulusSizeUnits = stimulusSizeRadians\*stimulusDistanceUnits,  
where units are the relavant units of length.  Although we don't have stimulusSizeUnits and stimulusDistanceUnits,  
these turn out to cancel out under the small angle approximation.  

See also: RadianceAndDistanceAreaToCornIrradiance  

2/20/13  dhb  Wrote it.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychRadiometric/RadianceAndDegrees2ToCornIrradiance.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychRadiometric/RadianceAndDegrees2ToCornIrradiance.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychRadiometric/RadianceAndDegrees2ToCornIrradiance.m</code>
</div>
