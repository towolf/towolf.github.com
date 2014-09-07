---
layout: mfile
title: SplineSpd
categories:
  - PsychColorimetric
encoding: UTF-8
---

[spd\_out] = SplineSpd(wls\_in, spd\_in, wls\_out, [extend])

Convert the wavelength representation of a spectral power distribution.
Takes change of deltaLambda into account to keep matrix computations
consistent across wavelength samplings.


Handling of out of range values:
  extend == 0: Cubic spline, extends with zeros [default]
  extend == 1: Cubic spline, extends with last value in that direction
  extend == 2: Linear interpolation, linear extrapolation

spd\_in may have multiple columns, in which case spd\_out does as well.

wls\_in and wls\_out may be specified as a column vector of
wavelengths or as a [start delta n] description.

\5/6/98  dhb  Change normalization method so that sum is constant.
             This is a little closer to the desired result for
             functions with big derivatives.
\12/7/98 dhb  Remove 5/6/98 change, as it produces the wrong power
             when you spline across different wavelength regions.
\7/26/03 dhb  Add extend argument and pass to SplineRaw.
\8/13/11 dhb  Update comment to reflect changes in SplineRaw.
\5/10/12 dhb  Small comment fix


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychColorimetric/SplineSpd.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychColorimetric/SplineSpd.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychColorimetric/SplineSpd.m</code>
</div>
