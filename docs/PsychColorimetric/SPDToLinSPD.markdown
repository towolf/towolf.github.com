---
layout: mfile
title: SPDToLinSPD
categories:
  - PsychColorimetric
encoding: UTF-8
---

output = SPDToLinSPD(input,B)

Find the best fitting spectrum within a linear model.

output - spectrum within the linear model
 (n-wavelengths by number-of-lights)
input - source spectral power distribution
 (n-wavelengths by number-of-lights)
B - linear model for spectral power distributions
 (number-of-wavelengths by n-dimension)

History:
30/11/07  Change call to non-existent SPDToLinWgts.m into call to
          FindModelWeights.m, as suggested by Mickey Rowe.         (MK)


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychColorimetric/SPDToLinSPD.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychColorimetric/SPDToLinSPD.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychColorimetric/SPDToLinSPD.m</code>
</div>
