---
layout: mfile
title: FindLinMod
categories:
  - PsychColorimetric
encoding: UTF-8
---

\[B,A\] = FindLinMod\(X,n\_dimension\)

Find an n\_dimension linear model for the
data in the columns of X.

B - basis matrix for the linear model
 \(n\_wavelengths by n\_dimension\)
A - coefficients to approximate data within model
 \(n\_dimension by n\_data\)
X - matrix whose columns contain the data
 \(n\_wavelengths by n\_data\)
 \(n\_data \>= n\_dimension\)
n\_dimension - dimension of the linear model to find


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychColorimetric/FindLinMod.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychColorimetric/FindLinMod.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychColorimetric/FindLinMod.m</code>
</div>
