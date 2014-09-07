---
layout: mfile
title: ISO2007MPEComputeType1ContinuousRetIrradianceTHWeightedValue
categories:
  - PsychISO2007MPE
encoding: UTF-8
---

function [val\_UWattsPerCm2,limit\_UWattsPerCm2] = ISO2007MPEComputeType1ContinuousRetIrradianceTHWeightedValue(...
  S,radiance\_WattsPerSrM2,weightingR,stimulusDurationSecs,[eyeLengthMm])

Compute the weighted thermal retinal irradiance for Type 1 instruments as given on page 98, Table 2,
5\.4.1.6.a

Input spectrum is radiance in units of Watts/[sr-m2-wlinterval].

Also return the exposure limit for this quantity.

See page 6 for a definition of a Type 1 instrument.  As far as I can tell, the key
criterion is that it doesn't put out more light that exceeds the Type 1 limits.

If the exposure time is longer than 2 hours the specified limits should be reduced by
1/exposureDuration in hours.  This routine implements that adjustment for its returned
limit value.  It does not implement a further reduction of of the limit (by a factor of 2)
specifed for microscopes and endoilluminators.

The standard specifies that the passed radiance should be the highest averaged over
an aperture of a specified size, where the size depends on the instrument.  This
routine does not worry about that aspect.  The most conservative thing to do is
to pass the highest localized power that will be presented.

The standard does not a pupil diameter to use for the conversion from radiance
to retinal irradiance, nor an eye length.  We use a 7 mm diameter pupil, to match
what is specified for the photochemical limit.  We use 17 mm eye length by default.  You
can override the eye length by passing a different length in mm.

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
IMPORTANT: Before using the ISO2007MPE routines, please see the notes on usage
and responsibility in PsychISO2007MPE/Contents.m (type "help PsychISO2007MPE"
at the Matlab prompt.
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

6/26/13  dhb  Wrote it.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychRadiometric/PsychISO2007MPE/ISO2007MPEComputeType1ContinuousRetIrradianceTHWeightedValue.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychRadiometric/PsychISO2007MPE/ISO2007MPEComputeType1ContinuousRetIrradianceTHWeightedValue.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychRadiometric/PsychISO2007MPE/ISO2007MPEComputeType1ContinuousRetIrradianceTHWeightedValue.m</code>
</div>
