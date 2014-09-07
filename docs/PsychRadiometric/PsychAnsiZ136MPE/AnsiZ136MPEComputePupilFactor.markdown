---
layout: mfile
title: AnsiZ136MPEComputePupilFactor
categories:
  - PsychAnsiZ136MPE
encoding: UTF-8
---

P = AnsiZ136MPEComputePupilFactor(stimulusDurationSeconds,stimulusWavelengthNm)

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
IMPORTANT: Before using the AnsiZ136 routines, please see the notes on usage
and responsibility in PsychAnsiZ136MPE/Contents.m (type "help PsychAnsiZ136MPE"
at the Matlab prompt.
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Delori et al. (2007) JOSA A, pp. 1250-1265 define a pupil
factor (their Table 2) that they use to modify the ANSI
standard as a function of stimulus duration and wavelength.
This is applied when converting between the corneal irradiance
of a a beam overfilling the pupil and the allowable power
in the pupil.

This routine computes that factor P.

3/2/13  dhb  Wrote it.