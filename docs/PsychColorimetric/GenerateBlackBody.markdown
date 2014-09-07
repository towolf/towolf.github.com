---
layout: mfile
title: GenerateBlackBody
categories:
  - PsychColorimetric
---

\[spd\] = GenerateBlackBody\(T,wls\_in\)

Generate spectral power distributions for black body radiators.
Generated according to formula in W\+S, pp. 11\-12.
We compute output as radiant exitance in units of W m\-2 nm\-1.

# INPUT
  T \- row vector of desired temperaturs in Kelvin.
  wls\_in \- column vector of wavelengths.

# OUTPUT
  spd \- the spectral power distributions are in the columns.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychColorimetric/GenerateBlackBody.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychColorimetric/GenerateBlackBody.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychColorimetric/GenerateBlackBody.m</code>
</div>
