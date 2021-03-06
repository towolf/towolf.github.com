---
layout: mfile
title: uvYToXYZ
categories:
  - PsychColorimetric
encoding: UTF-8
---

XYZ = [uvYToXYZ](/docs/uvYToXYZ)(uvY,[compute1960])

Compute tristimulus coordinates from chromaticity and luminance.

These are u',v' chromaticity coordinates in notation
used by CIE.  See CIE Colorimetry 2004 publication, or Wyszecki
and Stiles, 2cd, page 165.

Note that there is an obsolete u,v chromaticity diagram that is similar
but uses 6 in the numerator for u rather than the 9 that is used for u'.
See CIE Coloimetry 2004, Appendix A, or Judd and Wyszecki, p. 296. If
you want this (maybe to compute correlated color temperatures), you can
pass this as 1.  It is 0 by default.

See also XYZTouvY, [xyTouv](/docs/xyTouv), XYZToxyY, [xyYToXYZ](/docs/xyYToXYZ)

10/31/94    dhb  Wrote it.
5/06/11   dhb  Improve comment.