---
layout: mfile
title: BaylorNomogram
categories:
  - PsychColorimetricData
encoding: UTF-8
---

T = BaylorNomogram(S,lambdaMax)

Compute spectral sensitivities according to the
nomogram provided in Baylor, Nunn, and Schnapf, 1987.

The result is in quantal units, in the sense that to compute
absorptions you want to incident spectra in quanta.
To get sensitivity in energy units, apply EnergyToQuanta().

Argument lambdaMax may be a column vector of wavelengths.

6/22/96  dhb  Wrote it.
10/16/97 dhb  Add comment about energy units.