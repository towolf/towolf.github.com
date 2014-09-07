---
layout: mfile
title: M_PToP
categories:
  - PsychColorimetric
encoding: UTF-8
---

[M] = M\_PToP(Psource,Pdest,T)
[M,dest] = M\_PToP(Psource,Pdest,T,source)

Compute the conversion matrix between two color
spaces with known primaries.
The transformation requires a set of color matching
functions to describe the observer.

M - the conversion matrix
 (n\_chromacy by n\_chromacy)

Psource - source color primary spectral power distributions
  (n\_wavelengths by n\_chromacy)
Pdest - destination primary spectral power distributions
  (n\_wavelengths by n\_chromacy)
T - a set of color matching functions
  (n\_chromacy by n\_wavelengths)

# OPTIONAL
source - source tristimulus vectors
 (n\_chromacy by n\_lights)
dest - destination tristimulus vectors
 (n\_chromacy by n\_lights)

8/2/94      dhb     Fixed bug in optional arg handling.