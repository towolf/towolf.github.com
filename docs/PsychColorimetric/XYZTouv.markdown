---
layout: mfile
title: XYZTouv
categories:
  - PsychColorimetric
encoding: UTF-8
---

uv = [XYZTouv](/docs/XYZTouv)(XYZ,[compute1960])

Compute uv from XYZ.

These are u',v' chromaticity coordinates in notation
used by CIE.  See CIE Colorimetry 2004 publication, or Wyszecki
and Stiles, 2cd, page 165.

Note that there is an obsolete u,v chromaticity diagram that is similar
but uses 6 in the numerator for v rather than the 9 that is used for v'.
See CIE Colorimetry 2004, Appendix A, or Judd and Wyszecki, p. 296. If
you want this (maybe to compute correlated color temperatures), you can
pass this as 1.  It is 0 by default.

10/10/93  dhb   Created by converting CAP C code.
5/06/11   dhb   More extensive comment.  Optional 1960 version.