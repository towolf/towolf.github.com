---
layout: mfile
title: FitLogistic
categories:
  - Psychometric
encoding: UTF-8
---

\[a,b\] = FitLogistic\(x,y\)

Fit a logistic function to the data pairs x,y.

The form of the logistic equation is y = 1/\(1+10^-\(ax+b\)\).
The method used here is to regres on transformed coordinates.
One could use search to do a maximum likelihood function for
psychometric data, but if you are going to do that, you
should probably fit a cumulative normal or Weibull function.

See also: ComputeLogistic, InvertLogistic, FitLogitYN, FitWeibTAFC,
  FitWeibYN, FitAlphaWeibTAFC.

2/15/95     dhb     Wrote it.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./Psychometric/FitLogistic.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./Psychometric/FitLogistic.m">changelog</a></span>
</div>
<div class="code">
  <code>./Psychometric/FitLogistic.m</code>
</div>
