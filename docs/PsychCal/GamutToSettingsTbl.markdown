---
layout: mfile
title: GamutToSettingsTbl
categories:
  - PsychCal
encoding: UTF-8
---

[settings] = GamutToSettingsTbl(iGammaTable,gamut)

Find the best integer device settings to produce
the passed linear device coordinates. Use a precomputed
inverse gamma table.

The passed coordinates should be in the range [0,1].
The returned values run from [0,nlevels-1], where nlevels
is the number of quantized levels available on the device.

1/21/95     dhb     Wrote it.
5/26/12       dhb     Remove reference in comments to a return value that does not exist.