---
layout: mfile
title: LjgToXYZ
categories:
  - PsychColorimetric
encoding: UTF-8
---

XYZ = LjgToXYZ(Ljg)

Convert OSA Ljg to XYZ (10 degree).  Works by using numerical
search to invert XYZToLjg.  See XYZToLjg for details on
formulae used.  See also TestOSAUCS.

This can return imaginary values if you pass XYZ values
that are outside reasonable physical gamut limits.

3/27/01  dhb      Wrote it.
3/4/05   dhb        Handle new version of optimization toolbox, too.
9/23/12  dhb, ms  Update options for current Matlab versions.