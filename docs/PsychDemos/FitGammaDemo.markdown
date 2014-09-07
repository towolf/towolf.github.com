---
layout: mfile
title: FitGammaDemo
categories:
  - PsychDemos
encoding: UTF-8
---

FitGammaDemo.

Shows how function FitGamma may be used to fit various functions through measured gamma data.
We typically call FitGamma in scripts that perform calibrations to generate a full gamma table.

NOTE: FitGamma uses the MATLAB optimization toolbox.

NOTE: FitGamma is now a little obsolete, as we typically call it through
the function CalibrateFitGamma. That function has more fit options, but
is also more tied to our calibration structure.

Also see RefitCalGamma, CalibrateFitGamma, FitGamma.

8/7/00  dhb  Wrote it.
3/5/05  dhb  A few more tests.
6/5/10  dhb  Made sure this still runs OK.  A few small tweaks.