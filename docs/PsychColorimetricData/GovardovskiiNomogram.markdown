---
layout: mfile
title: GovardovskiiNomogram
categories:
  - PsychColorimetricData
encoding: UTF-8
---

T\_absorbance = GovardovskiiNomogram(S,lambdaMax)

Compute normalized absorbance according to the
nomogram provided in Victor I. Govardovskii et al., 2000,
Visual Neuroscience, Vol. 17, pp. 509-528.

The polynomial approximation has two bands.
Alpha-band, the major band of A1 pigments is taken from
Equation (1) and equation (2) in wavelength range [350,700] nm
(see page 515 in paper)

Beta-band, the minor band of A1 pigments is taken from
Equation (3) and equation (5a, 5b) in wavelgnth range [350,700] nm
(see page 516 in paper)

T\_absorbance contains the absorbance.
This is specified according to the CVRL web page
definition absorbance = log(I\_incident/I\_transmitted),
so the numbers are all positive.  The peak is normalized
to one.

For low density, the absorbance has the same shape as
the spectral senstivity.

The result is in quantal units, in the sense that to compute
absorptions you want to incident spectra in quanta.
To get sensitivity in energy units, apply EnergyToQuanta().

Argument lambdaMax may be a column vector of wavelengths.

03/08/2002 ly  Wrote it starting from DawisNomogram.