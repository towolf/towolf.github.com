---
layout: mfile
title: WlsToS
categories:
  - PsychColorimetric
encoding: UTF-8
---

S = WlsToS(wls)

Converts a list of wavelengths to a [start delta num]
description.  Wavelengths must be evenly spaced.

4/17/02  dhb  Handle special case of one wavelength passed.
              Delta argument is arbitrarily set to 0 for this case.
7/11/03  dhb  Handle case the wls is passed in struct format.
1/3/12   dhb  Fix check for evenly spaced wavelengths.