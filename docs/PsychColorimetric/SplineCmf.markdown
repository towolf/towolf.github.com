---
layout: mfile
title: SplineCmf
categories:
  - PsychColorimetric
encoding: UTF-8
---

[T\_out] = SplineCmf(wls\_in, T\_in, wls\_out, [extend])

Convert the wavelength representation of a color matching functions/
spectral sensitivities.

Handling of out of range values:
  extend == 0: Cubic spline, extends with zeros [default]
  extend == 1: Cubic spline, extends with last value in that direction
  extend == 2: Linear interpolation, linear extrapolation

T\_in may have multiple rows, in which case T\_out does as well.

wls\_in and wls\_out may be specified as a column vector of
wavelengths or as a [start delta num] description.

7/26/03 dhb  Add extend argument and pass to SplineRaw.
8/22/05 pbg  Changed T\_out to include the extend variable (previously was
             hardwired to "1".
8/13/11 dhb  Update comment to reflect changes in SplineRaw.