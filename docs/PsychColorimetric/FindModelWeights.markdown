---
layout: mfile
title: FindModelWeights
categories:
  - PsychColorimetric
encoding: UTF-8
---

output = FindModelWeights(input,B)

Find the linear model weights for a spectral
power distribution.

# INPUT
  input - source spectral power distribution
          (number-of-wavelengths by number-of-lights)
  B - linear model for spectral power distributions
          (number-of-wavelengths by n-dimension)
OUTPUT
  output - linear model weights
           (n-dimension by number-of-lights)