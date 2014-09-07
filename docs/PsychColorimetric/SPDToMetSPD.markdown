---
layout: mfile
title: SPDToMetSPD
categories:
  - PsychColorimetric
encoding: UTF-8
---

output = SPDToMetSPD(input,T,B)

Convert spectral power distribution
to another metameric spectral power distribution.

output - metameric spectral power distribution
 (number-of-wavelengths by number-of-lights)
input - source spectral power distribution
 (number-of-wavelengths by number-of-lights)
T - source color matching functions
 (n-chromacy by number-of-wavelengths)
B - linear model for spectral power distributions
 (number-of-wavelengths by at least n-chromacy)