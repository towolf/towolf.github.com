---
layout: mfile
title: FindModelWeights
categories:
  - PsychColorimetric
encoding: UTF-8
---

output = FindModelWeights(input,B)

Find the linear model weights for a spectral
power distribution.

# INPUT
  input - source spectral power distribution
          (number-of-wavelengths by number-of-lights)
  B - linear model for spectral power distributions
          (number-of-wavelengths by n-dimension)
OUTPUT
  output - linear model weights
           (n-dimension by number-of-lights)


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychColorimetric/FindModelWeights.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychColorimetric/FindModelWeights.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychColorimetric/FindModelWeights.m</code>
</div>
