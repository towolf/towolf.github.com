---
layout: mfile
title: FindSpectralPeaks
categories:
  - PsychCal
encoding: UTF-8
---

peaks = FindSpectralPeaks(spectrum,[S],[noiseLevel])

Find the local peaks in a spectrum.
Uses the heuristic of requiring increasing
and decreasing in neighborhood of peak to
get rid of noise.

Parameter noiseLevel (default 0) causes
the routine to ignore peaks lower than
noiseLevel\*maxValue where maxValue is the
largest measurement in the spectrum.

1/6/96      dhb     Wrote it.
5/17/99   dhb   Added  noiseLevel parameter.