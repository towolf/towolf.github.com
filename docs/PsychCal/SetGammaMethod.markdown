---
layout: mfile
title: SetGammaMethod
categories:
  - PsychCal
encoding: UTF-8
---

cal = SetGammaMethod(cal,gammaMode,[precision])

Set up the gamma correction mode to be used.  Options
are:
  gammaMode == 0 - search table using linear interpolation via interp1.
  gammaMode == 1 - inverse table lookup.  Fast but less accurate.
  gammaMode == 2 - exhaustive search

If gammaMode == 1, then you may specify the precision of the
inverse table.  The default is 1000 levels.

See also RefitCalGamma, CalibrateFitGamma, GamutToSettings

8/4/96  dhb  Wrote it.
8/21/97 dhb  Update for structure.
3/12/98 dhb  Change name to SetGammaCorrectMode
5/26/12 dhb  Add real exhaustive search mode (2).