---
layout: mfile
title: GenerateBlackBody
categories:
  - PsychColorimetric
encoding: UTF-8
---

[spd] = GenerateBlackBody(T,wls\_in)

Generate spectral power distributions for black body radiators.
Generated according to formula in W+S, pp. 11-12.
We compute output as radiant exitance in units of W m-2 nm-1.

# INPUT
  T - row vector of desired temperaturs in Kelvin.
  wls\_in - column vector of wavelengths.

# OUTPUT
  spd - the spectral power distributions are in the columns.