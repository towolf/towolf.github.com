---
layout: mfile
title: AnsiZ136MPEComputeExtendedSourcePhotochemicalLimit
categories:
  - PsychAnsiZ136MPE
encoding: UTF-8
---

[MPEPhotochemicalIntegratedRadiance\_JoulesPerCm2Sr, ...
 MPEPhotochemicalRadiance\_WattsPerCm2S, ...
 MPEPhotochemicalCornealIrradiance\_WattsPerCm2, ...
 MPEPhotochemicalCornealRadiantExposure\_JoulesPerCm2] = ...
 AnsiZ136MPEComputeExtendedSourcePhotochemicalLimit(stimulusDurationSec,stimulusSizeDeg,stimulusWavelengthNm,[CONELIMITFLAG])

\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*
IMPORTANT: Before using the AnsiZ136 routines, please see the notes on usage
and responsibility in PsychAnsiZ136MPE/Contents.m (type "help PsychAnsiZ136MPE"
at the Matlab prompt.
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

Compute time photochemical MPE for an extended source
ANSI Z136.1-2007, Table 5b, p. 75.

Set CONELIMITFLAG to false (default true) to skip the asterisked
alternative computation desribed in Table 5 (see comments in code).

2/20/13  dhb  Wrote it.
3/2/13   dhb  Make limiting cone angle computation controllable.