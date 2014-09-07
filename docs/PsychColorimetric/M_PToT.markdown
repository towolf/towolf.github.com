---
layout: mfile
title: M_PToT
categories:
  - PsychColorimetric
encoding: UTF-8
---

[M] = M\_PToT(Psource,Tdest)
[M,dest] = M\_PToT(Psource,Tdest,source)

Compute the conversion matrix between a color
space with known primaries and one with known
color matching functions.

M - the conversion matrix
 (n\_chromacy by n\_chromacy)

Psource - source primaries spectral power distributions
 (n\_chromacy by n\_wavelengths)
Tdest - destination color matching functions
 (n\_chromacy by n\_wavelengths)

# OPTIONAL
source - source tristimulus vectors
 (n\_chromacy by n\_lights)
dest - destination tristimulus vectors
 (n\_chromacy by n\_lights)

8/2/94      dhb     Fixed variable name bug.