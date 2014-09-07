---
layout: mfile
title: MexTimingLoopTest
categories:
  - PsychTests
encoding: UTF-8
---

MexTimingLoopTest

Run a timing loop within a mex file, as part of the MATLAB process but without returing control to the
 MATLAB engine.

SEE ALSO: TestMATLABTimingOSX.m

# AUTHORS:
Allen Ingling     awi     Allen.Ingling@nyu.edu

# HISTORY:
9/22/03   awi     Adapted from previous versions and other stuff.
11/04/03  awi     Added axis labels.
4/6/05    awi     Replaced "GetBusFrequencymex" calls with "MachTimebase"
4/8/05    awi     Updated "MachTimebase" to new name "MachAbsoluteTimeClockFrequency"