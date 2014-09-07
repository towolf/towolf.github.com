---
layout: mfile
title: LambNomogram
categories:
  - PsychColorimetricData
encoding: UTF-8
---

T = LambNomogram(S,lambdaMax)

Compute spectral sensitivities according to the
nomogram provided in Lamb, 1995, Vision Research,
Vol. 35, pp. 3083-3091, equation 2'.

The result is in quantal units, in the sense that to compute
absorptions you want to incident spectra in quanta.
To get sensitivity in energy units, apply EnergyToQuanta().

Argument lambdaMax may be a column vector of wavelengths.

8/20/98 dhb  Wrote it.