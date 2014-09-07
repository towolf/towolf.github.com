---
layout: mfile
title: TriToMetSPD
categories:
  - PsychColorimetric
encoding: UTF-8
---

output = TriToMetSPD(input,T,B)

Convert tristimulus coordinates in a color space
specified by a set of known color matching
functions to an estimate of the original spectral
power distribtuion.

output - estimated spectral power distribution
 (number-of-wavelengths by number-of-lights)
input - source tristimulus vectors
 (n-chromacy by number-of-lights)
T - source color matching functions
 (n-chromacy by number-of-wavelengths)
B - linear model for spectral power distributions
 (number-of-wavelengths by at least n-chromacy)