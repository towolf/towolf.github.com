---
layout: mfile
title: ISO2007MPECheckType1ContinuousRadiance
categories:
  - PsychISO2007MPE
encoding: UTF-8
---

[IsOverLimit,ISO2007MPEStruct] = ISO2007MPECheckType1ContinuousRadiance(S\_in,radiancein\_WattsPerSrM2,stimulusDurationSecs,stimulusAreaDegrees2,eyeLengthMm)

Run all the checks that apply to a radiance measurement for the ISO 2007 MPE standard, for a Type 1 instrument and continuous exposure.
Does not do the convergent beam check -- see comment in Contents.m about when we think this applies.

Returns a flag set to 1 if the input exceeds any of the limits, and a structure with the computed ISO2007MPE
values and corresponding limits.

We use 17 mm eye length by default.  You can override the eye length by passing a different length in mm.
This value is used in the conversion from radiance to retinal irradiance.

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
IMPORTANT: Before using the ISO2007MPE routines, please see the notes on usage
and responsibility in PsychISO2007MPE/Contents.m (type "help PsychISO2007MPE"
at the Matlab prompt.
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

6/28/13  dhb  Wrote it.