---
layout: mfile
title: M_TToT
categories:
  - PsychColorimetric
encoding: UTF-8
---

[M] = M\_TToT(Tsource,Tdest)
[M,dest] = M\_TToT(Tsource,Tdest,source)

Compute the conversion matrix between two color
spaces with known color matching functions.

M - the conversion matrix
 (n\_chromacy by n\_chromacy)

Tsource - source color matching functions
  (n\_wavelengths by n\_chromacy)
Tdest - destination color matching functions
  (n\_wavelengths by n\_chromacy)

# OPTIONAL
source - source tristimulus vectors
 (n\_chromacy by n\_lights)
dest - destination tristimulus vectors
 (n\_chromacy by n\_lights)