---
layout: mfile
title: ISO2007MPEComputeType1ContinuousRadiancePCWeightedValue
categories:
  - PsychISO2007MPE
encoding: UTF-8
---

\[val\_UWattsPerSrCm2,limit\_UWattsPerSrCm2\] = ISO2007MPEComputeType1ContinuousRadiancePCWeightedValue\(...
    S,radiance\_WattsPerSrM2,weightingA,stimulusDurationSecs\)

 Compute the weighted aphakic \(photochemical\) radiance for Type 1 instruments as given on page 8, Table 2,
 5.4.1.3.b.

 Input spectrum is radiance in units of Watts/\[sr-m2-wlinterval\].

 Also return the exposure limit for this quantity.

 See page 6 for a definition of a Type 1 instrument.  As far as I can tell, the key
 criterion is that it doesn't put out more light that exceeds the Type 1 limits.

 If the exposure time is longer than 2 hours the specified limits should be reduced by
 1/exposureDuration in hours.  This routine implements that adjustment for its returned
 limit value.  It does not implement a further reduction of of the limit \(by a factor of 2\)
 specifed for microscopes and endoilluminators.

 The standard specifies that the passed radiance should be the highest averaged over
 an aperture of a specified size, where the size depends on the instrument.  This
 routine does not worry about that aspect.  The most conservative thing to do is
 to pass the highest localized power that will be presented.

 The indicates that radiance should be measured through a 7 mm aperture at the cornea.
 I believe this refers to the case where you are measuring radiance by measuring radiant
 flux through two apertures at a known distance apart.  It would then make sense that you'd
 want to know the radiance defined by the direction subtended by a 7 mm aperture at the
 cornea, e.g. right where a large pupil would be.  If you measure using some other device
 \(e.g. a PhotoResearch PR-XXX that directly obtains radiance and do so from the eye position,
 that also seems reasonable.

 \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
 IMPORTANT: Before using the ISO2007MPE routines, please see the notes on usage
 and responsibility in PsychISO2007MPE/Contents.m \(type "help PsychISO2007MPE"
 at the Matlab prompt.
 \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

 6/26/13  dhb  Wrote it.


<div class="code_header" style="text-align:right;">
  <span style="float:left;">Path&nbsp;&nbsp;</span> <span class="counter">Retrieve <a href=
  "https://raw.github.com/Psychtoolbox-3/Psychtoolbox-3/beta/./PsychRadiometric/PsychISO2007MPE/ISO2007MPEComputeType1ContinuousRadiancePCWeightedValue.m">current version from GitHub</a> | View <a href=
  "https://github.com/Psychtoolbox-3/Psychtoolbox-3/commits/beta/./PsychRadiometric/PsychISO2007MPE/ISO2007MPEComputeType1ContinuousRadiancePCWeightedValue.m">changelog</a></span>
</div>
<div class="code">
  <code>./PsychRadiometric/PsychISO2007MPE/ISO2007MPEComputeType1ContinuousRadiancePCWeightedValue.m</code>
</div>
