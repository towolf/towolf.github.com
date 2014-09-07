---
layout: mfile
title: RadianceAndDistanceAreaToCornIrradiance
categories:
  - PsychRadiometric
encoding: UTF-8
---

cornealIrradiance\_PowerPerArea = RadianceAndDistanceAreaToCornIrradiance(radiance\_PowerPerSrArea,stimulusDistance,stimulusArea)  

Convert the radiance of a stimulus to corneal irradiance, given that we know the distance to the stimulus and the area  
of the stimulus.  Light power can be in your favorite units (Watts, quanta/sec) as can distance (m, cm, mm).  Area  
needs to be in units that are the square of your distance units, both for the radiance passed and the stimulus area  
passed. So, if radiance is in Watts/[cm2-sr] then distance needs to be in cm and irradiance will be in Watts/cm2.  

See also: RadianceAndDegrees2ToCornIrradiance, CornIrradianceAndDegrees2ToRadiance  

2/20/13  dhb  Wrote it.  


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychRadiometric/RadianceAndDistanceAreaToCornIrradiance.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychRadiometric/RadianceAndDistanceAreaToCornIrradiance.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychRadiometric/RadianceAndDistanceAreaToCornIrradiance.m</code>
</div>
