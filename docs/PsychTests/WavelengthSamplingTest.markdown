---
layout: mfile
title: WavelengthSamplingTest
categories:
  - PsychTests
encoding: UTF-8
---

WavelengthSamplingTest

There are three formats used to represent wavelength
sampling in the Psychtoolbox.
  S-format      - a 3 by 1 row vector [start step numberSamples].
  wls-format    - a list of evenly spaced wavelengths.
  struct-format - a structure with fields start, step, and numberSamples.

The S-format predates the availability of structures in MATLAB, but
is used widely in extant code.  Low level conversion routines transform
between these representations, and in particular routines MakeItS,
MakeItWls, and MakeItStruct take any of the three formats and return
one.  By calling one of these before using wavelength format information,
it is possible to write code that is compatible with all three.

7/11/03  dhb  Wrote this test program.