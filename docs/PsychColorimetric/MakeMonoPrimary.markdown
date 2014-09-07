---
layout: mfile
title: MakeMonoPrimary
categories:
  - PsychColorimetric
encoding: UTF-8
---

primary = MakeMonoPrimary(wl,S)

Make a monochromatic primary SPD at the passed
wavelength sampling.

Note, this routine will do the wrong thing
if the passed wavelength is not represented
in the underlying wavelength sampling.

10/3/95     dhb     Wrote it.