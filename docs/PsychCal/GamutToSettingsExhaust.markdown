---
layout: mfile
title: GamutToSettingsExhaust
categories:
  - PsychCal
encoding: UTF-8
---

settings = GamutToSettingsExhaust(gammaInput, gammaTable, gamut)

Find the best device settings to produce
the passed linear device coordinates.

This version works by exhaustive search of the fit gamma table,
and returns the value in that table that produces output closest
to desired.

The passed coordinates should be in the range [0,1].
The returned settings also run from [0,1], but after
inversion of the device's gamma measurements.

5/26/12  dhb  Wrote it.