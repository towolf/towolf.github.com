---
layout: mfile
title: FindThreshWeibYN
categories:
  - Psychometric
encoding: UTF-8
---

threshold = FindThreshWeibYN(pcorrect, alpha, beta)

 Invert Weibull function to find threshold
 for given pcorrect, alpha, and beta.
 This function should invert ComputeWeibullYN().

 threshold = alpha \* pow( -1.0\*log(1.0-pyes) , 1.0/beta );


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./Psychometric/FindThreshWeibYN.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./Psychometric/FindThreshWeibYN.m">changelog</a></span>
</div>
<div class="code">
  <code>./Psychometric/FindThreshWeibYN.m</code>
</div>
