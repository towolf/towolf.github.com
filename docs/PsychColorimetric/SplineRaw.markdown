---
layout: mfile
title: SplineRaw
categories:
  - PsychColorimetric
encoding: UTF-8
---

[spec\_out] = SplineRaw(wls\_in, spec\_in, wls\_out, [extend])

Convert the wavelength representation of a spectrum.

Handling of out of range values:
  extend == 0: Cubic spline, extends with zeros [default]
  extend == 1: Cubic spline, extends with last value in that direction
  extend == 2: Linear interpolation, linear extrapolation

spec\_in may have multiple columns, in which case spec\_out does as well.

wls\_in and wls\_out may be specified as a column vector of
wavelengths or as a [start delta num] description.

7/26/03  dhb  Add extend argument
8/13/11  dhb  Added linear extrapolation option for extend