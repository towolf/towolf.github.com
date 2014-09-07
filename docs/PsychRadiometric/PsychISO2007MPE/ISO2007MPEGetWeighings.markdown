---
layout: mfile
title: ISO2007MPEGetWeighings
categories:
  - PsychISO2007MPE
encoding: UTF-8
---

[wls,weightingR,weightingA,weightingS,wls\_R,rawWeigtingR,wls\_A,rawWeightingA,wls\_S,rawWeightingS] = ISO2007MPEGetWeighings(S)

Read the text files and get the three weighting functions needed for the
standard's calculations.

These are splined to the evenly spaced wavelengths specified by S, and
padded with 0 outside the wavelength range over which each function is
specified in the standard.  This simplifies calculations.

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
IMPORTANT: Before using the ISO2007MPE routines, please see the notes on usage
and responsibility in PsychISO2007MPE/Contents.m (type "help PsychISO2007MPE"
at the Matlab prompt.
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

6/25/13  dhb  Wrote it.