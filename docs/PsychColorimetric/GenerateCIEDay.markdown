---
layout: mfile
title: GenerateCIEDay
categories:
  - PsychColorimetric
encoding: UTF-8
---

[spd,xd,yd] = GenerateCIEDay(Temp,[B])

Generate CIE daylights of the desired correlated color
temperature.  Formulae are from W+S, pp. 145-146.

The required basis vectors may be obtained by loading
the file B\_cieday.

# INPUT
  Temp - row vector of color temperatures.  These should be
      in the range 4000 - 25000.
  B - CIE daylight basis vectors.

# OUTPUT
  spd - desired spectral power distributions
  xd  - row vector of x chromaticities
  yd  - row vector of y chromaticities

9/28/93   dhb, jms  Changed argument name to Temp
                    If B not passed, return spd = [] and other data