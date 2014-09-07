---
layout: mfile
title: NearestResolution
categories:
  - PsychOneliners
---

res=NearestResolution\(screenNumber,\[width,height,hz,pixelSize\]\)
res=NearestResolution\(screenNumber \[,width\]\[,height\]\[,hz\]\[,pixelSize\]\)
res=NearestResolution\(screenNumber,desiredRes\)

Finds the available screen resolution most similar \(in log cartesian space\) to that
requested. Any argument that is \[\] or NaN will be ignored in assessing similarity.
If you specify pixelSize then the returned res will specify pixelSize. Typically
you'll use the returned "res" to set your screen's resolution:

SetResolution\('Resolution', screenNumber, res\)

Also see SetResolution, ResolutionTest, and [Screen](/docs/Screen) Resolution and Resolutions.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychOneliners/NearestResolution.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychOneliners/NearestResolution.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychOneliners/NearestResolution.m</code>
</div>
